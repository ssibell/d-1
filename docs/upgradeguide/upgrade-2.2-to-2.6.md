---
layout: page
title: upgrade-2.2-to-2.6
permalink: /docs/upgrade-2.2-to-2.6/
top_graphic: 1
date: 2017-2-22T00:00
---

# The ultimate golden release upgrade guide
## How to get from dCache 2.2 to dCache 2.6

Author
Gerd Behrmann <behrmann@nordu.net>

#General changes

License change

dCache has moved from a proprietary shared source license to the AGPL 3 free and open source license. The xrootd, NFS and RPC code has been moved out of dCache and into self-contained projects released under the LGPL 3.

Source code repository

The main source code repository has been migrated from a private SVN server to GitHub. The source can be found at https://github.com/dCache/dcache. Third parties are welcome to fork the repository and submit pull requests with contributions. Note that the copyright of all contributions must be transferred to DESY.

Transfer protocols

NFS

The NFS 4.1 service now supports sending all pool interfaces to the NFS client. This allows the NFS client to choose the most appropriate interface, including whether to use IPv4 or IPv6.

The location and name of the NFS exports file is now configurable using the nfs.export.file configuration property.

Several performance related improvements have been made.

A new dot command for querying the locality of a file, ie whether the file is currently online, nearline, or unavailable. The command follows the format .(get)(filepath)(locality). This information has previously been available through SRM.

The NFS 4.1 door's exports ls command now accepts an argument that allows the list of exports to be limited to those of a particular host.

Since NFS doors are unable to map available pools to how much logical space is available to the end user, the total size of the file system exported by the NFS door is hardcoded to a large fixed value. This value has been increased from 10 petabyte to 1 exabyte. This is to ensure that the reported size is bigger than the reported used space.

NFS 4.1 doors cache gPlazma lookups for improved performance. Admin shell commands for inspecting and clearing the cache have been added. Use login clear cache to clear the cache and login dump cache to inspect the content of the cache.

Commits: 53a08ce, e59531a, 4602f17, c59e7b7, 82d3bc5, 9007c10, f1d2e5c, c957736.

DCAP

DCAP per session cells are no longer exported as well-known cells. This means that to talk to the cell through the admin shell, one has to cd to the fully qualified cell name including the @domain suffix. Only the cells created for each client connection are affected by this change. By not exporting the cell name of these relatively short lived cells, the routing overhead in the cells messaging system is reduced.

The DCAP no longer disables a pool when a client tries to write to a file opened for reading.

DCAP doors now detect if its thread for accepting client connection has died, and will stop publishing to the login broker.

DCAP doors now only log protocol violations and unclean client disconnects at debug level. This is to prevent that automated port scans fill up the log files.

Minor performance improvements for gsidcap have been implemented.

Commits: bb098d6, eb03cef, f6df217, de2ee90, 09cbbd7, d0bb771.

WebDAV

Pools now include the Content-Location header it replies to GET requests. This header allows dCache to associate the resource with the URI pointing to the WebDAV door.

The WebDAV door is now able to redirect PUT requests to a pool, thus avoiding proxying the data through the WebDAV door. This functionality has previously been available for GET requests. Note that many clients do not support redirects on PUT. The functionality can be disabled by setting webdav.redirect.on-write to false, analogous to disabling redirect on GET by setting webdav.redirect.on-read to false.

chroot

Resource handling of the HTTP mover running on pools has been changed. The mover no longer allocates a thread per connection, and the thread pools used for network and disk I/O are now allocated per pool rather than per domain. Ie several pools running in the same domain now each allocate their own thread pools for HTTP transfers. This affects the interpretation of the httpMoverXXX family of configuration properties.

Commits: 8ba35d9, b7bc58d, b460302, dd1031b.

Xrootd

A notable change, albeit invisible to users and end users, is that the majority of the xrootd code has moved to its own project, called xrootd4j. We hope the code will be useful to other projects.

The xrootd stack in both the xrootd doors and the xrootd mover running on pools has been extended with a new plugin type. These plugin have full access to introspect, intercept and alter the communiation between the xrootd client and dCache. Previous versions of dCache supported authentication and authorization plugins for doors. These are still supported, although they have been refactored as special cases of the newer and more powerful plugin system. The properties xrootdAuthNPlugin and xrootdAuthzPlugin have been deprecated in favor of the xrootdPlugins property. Note that the new property must be defined separately for doors and pools.

Resource handling of the xrootd mover running on pools has been changed. The mover no longer allocates a thread per connection, and the thread pools used for network and disk I/O are now allocated per pool rather than per domain. Ie several pools running in the same domain now each allocate their own thread pools for xrootd transfers. This affects the interpretation of the xrootdMoverXXX family of configuration properties.

Commits: 97b0ecb, c2cc075, 5a4c6a9, e66a2e4, 4acadb6, dd1031b.

FTP

The clear text FTP service now works with space manager, although it is limited to the use of default space tokens bound to a directory through directory tags.

FTP per session cells are no longer exported as well-known cells. This means that to talk to the cell through the admin shell, one has to cd to the fully qualified cell name including the @domain suffix. Only the cells created for each client connection are affected by this change. By not exporting the cell name of these relatively short lived cells, the routing overhead in the cells messaging system is reduced.

FTP doors now detect if the thread for accepting client connection has died, and will stop publishing to the login broker.

Commits: 0c0bdbf, 09cbbd7, d0bb771.

Name space

PNFS

PNFS is no longer supported by dCache. The use of Chimera is mandatory in dCache 2.6.

Commits: 41ca6c2.

Chimera

The Chimera database schema is now managed automatically by dCache. This means that on first installation, only an empty database needs to be created and the pnfsmanager service will automatically populate the database with tables, indexes, triggers, etc. On upgrade, the schema will be automatically updated with the latest changes. The automatic update can be disabled by setting the db.schema.auto to false. In that case the schema update has to be applied manually by using the dcache database update command. The SQL script for creating the Chimera schema shipped with previous versions of dCache are no longer included.

Warning

On first startup after upgrade to dCache 2.6 from dCache 2.2, the schema update may take quite a while (hours) on large instances. In some cases upgrading to PostgreSQL 9.2 prior to the dCache upgrade will speed up the schema update.

There has been work on supporting embedded databases with Chimera. At the moment H2 and HSQLDB are supported, although the cleaner currently works with neither of them. At the time of writing, use cases are limited to test and demo deployments.

Added support for converting Enstore data stored in level 4 during migration from PNFS to Chimera.

Performance of file deletion has been improved by using cascading deletes in the database schema.

Chimera is now able to track the last access time of a file. The access time is updated whenever a pool reads a file. To reduce the performance overhead for files accessed frequently, the precision of the access time can be reduced in pnfsmanager by setting the atime.gap property.

Connection pooling parameters for pnfsmanager are now exposed through the new db.connections.* family of configuration properties. Consult the pnfsmanager.properties file for further details.

Commits: b3b5138, 2becbe3, 05231fb, 3b04b88, e02ea48, 3dc7628, 8b1fb2d, 81a0504, d07e01c, a6c8c97, 7af4309.

Chimera command line tool

The chimera-cli has been improved with several new features.

The new rmtag can be used to delete directory tags using.

$ chimera-cli writetag / test foo
$ chimera-cli lstag / 
Total: 1
test
$ chimera-cli readtag / test
foo
$ chimera-cli rmtag / test
The chown command can now change the group of filesa and directories.

$ chimera-cli ls /
total 2
drwxr-xr-x 3 0 0 512 Oct 21  2011 pnfs
drwxr-xr-x 2 0 0 512 May 10  2012 test
$ chimera-cli chown /test 1000:1000
$ chimera-cli ls /
total 2
drwxr-xr-x 3    0    0 512 Oct 21  2011 pnfs
drwxr-xr-x 2 1000 1000 512 May 10  2012 test
The checksum has been extended with features to query, set and remove specific checksums of a file.

$ chimera-cli checksum /pnfs/dcache-vm/data/test-1344174183-2 list
ADLER32:5ce8e869
$ chimera-cli checksum /pnfs/dcache-vm/data/test-1344174183-2 get ADLER32
5ce8e869
$ chimera-cli checksum /pnfs/dcache-vm/data/test-1344174183-2 delete ADLER32
$ chimera-cli checksum /pnfs/dcache-vm/data/test-1344174183-2 add ADLER32 5ce8e869
$ chimera-cli checksum /pnfs/dcache-vm/data/test-1344174183-2 list
ADLER32:5ce8e869
Commits: 9962dcd, f4ef444, 047126f.

Services

pnfsmanager

Even though support for PNFS has been removed, the name space service of dCache is still called pnfsmanager. The unique IDs of files stored in dCache is called a PNFS ID like it has always been.

The previously deprecated the set storageinfo command has been removed. The implementation was incomplete.

Commits: e769d4c, 88b5041.

poolmanager

Added option to enable logging of pool selection and cost information to billing. The feature can be enabled by setting poolmanager.cache-hit-messages.enabled=true.

Fixed a bug in the interpretation of the onerror setting that could cause requests to suspend rather than to fail.

The rc ls admin shell command has been extended with an option to list the clients that issued the request.

The online help of the psu create unit command has been improved.

[dcache-vm] (PoolManager) admin > help psu create unit
NAME
    psu create unit

SYNOPSIS
    psu create unit UNITTYPE NAME

DESCRIPTION
    Creates a new unit of the specified type.  A unit is a predicate
    that is used to select which pools are eligable for a specific user
    request (to read data from dCache or write data).  Units are
    combined in unit-groups; see psu create unitgroup for more details.

    The UNITTYPE is one of '-net', '-store', '-dcache' or '-protocol'
    to create a network, store, dCache or protocol unit, respectively.

    The NAME of the unit describes which particular subset of user
    requests will be selected; for example, a network unit with the
    name '10.1.0.0/24' will select only those requests from a computer
    with an IP address matching that subnet.

    The NAME for network units is either an IPv4 address, IPv6 address,
    an IPv4 subnet or an IPv6 subnet.  Subnets may be written either
    using CIDR notation or as an IP address and netmask, joined by a
    '/'.

    The NAME for store units has the form @.
    Both  and  may be replaced with a '*' to
    match any value.  If the HSM-type is 'osm' then  is
    constructed by joining the store-name and store-group with a colon:
    :@osm.

    The NAME for a dcache unit is an arbitrary string.  This matches
    against the optional cache-class that may be set within the
    namespace in a similar fashion to the storage-class.

    The NAME for a protocol unit has the form /. If
     is '*' then all versions of that protocol match.

OPTIONS
    none
Lowers the default limit of allowed replicas of a file from 500 to 3. This affects classic and wass partitions. The limit can be controlled by setting the max-copies parameter through the pm commands in PoolManager.

Commits: 646bb5d, 81c8948, c949a47, 1d56502, 1c75200.
gplazma

The gplazma1 plugin that previously provided support for legacy gPlazma configuration has been removed. On upgrade to dCache 2.6 the equivalent gPlazma plugins have to be configured. Note that although the authorization files used by those plugins are syntactically identical to those used by the gplazma1 plugin, there may be subtle semantic differences. Refer to the 2.2 upgrade guide for further details.

A new ldap plugin for the map and identity phases has been added. Consult the gplazma.ldap.* family of properties documented in gplazma.properties for further details.

The kpwd plugin now accepts 0 as a valid value for the UID and GID fields.

Commits: 34be5d7, 3358c57, 4537675, bb14ddd.

srm

The srmLsRequestLifetime property has been removed. Support for this property was never implemented.

The srm now respects the gplazma property, which allows the gPlazma instance used by srm to be configured.

Logging of unexpected problems has been improved.

Fixed a bug that would cause srm startup to fail with an IllegalStateException if SRM requests have expired while dCache was shut down.

Persistence of authorization information was ported from the Eclipse TopLink library to DataNucleus. Although this is mostly an internal change, the table names for this information have changed from authrecord, authgroup and authgrouplist to AUTHRECORD, AUTHGROUP and AUTHGROUPLIST. The old tables can be dropped after upgrade, although they will not be dropped automatically. These tables do not contain any data that needs to be preserved for longer periods of time.

Commits: 466f9a6, 38e4e04, 4fc6e2b, f4ed5c5, f113467.

spacemanager

Log output has been cleaned up.

Commits: 0e10456, 980e834.

admin

We consider support for the SSH 1 protocol deprecated. Expect this to be removed in a future update.

Host and server keys for SSH 2 are not generated automatically during installation of the RPM and DEB packages.

For those cells that support the bean ls command, components internal to the Spring library are no longer listed. This also avoids the error messages that would otherwise be logged whenever the bean ls command is used.

Remaining bits of the obsolete legacy logging system have been removed. In particular the deprecated set printout command has been removed.

Commits: 63e75f5, c0a7264, 5120744, b1764a1.

pool

The library used for the Berkeley DB metadata backend has been updated. The new version uses a new on-disk format. Pools using the Berkeley DB backend will be upgraded to the new format during the first startup.

It may be necessary to run a small script to prepare for the upgrade. If the pool fails to start with an EnvironmentFailureException failure after upgrading, then the script /usr/sbin/dcache-pool-meta-preupgrade needs to be executed.
Warning

Automatic downgrade is not possible. To downgrade, first convert the meta data to the file backend, downgrade and then convert back to the Berkeley DB backend. The dcache pool convert command can be used to convert the metadata.

Lock contention for meta data access using the Berkeley DB backend has been reduced.

The migration module commands have been extened with -force-source-mode option to override the pool mode of the source pool. This allows files to be transferrred from a disabled pool.

Pools cells are no longer required to be well-known cells, nor are pool cells required to have the same name as the pool they expose. Although mostly a curiousity at the moment, this feature may eventually allow the same pool to be exposed by multiple cells.

Pool shutdown has been cleaned up considerably. Thread pools are now shut down prior to pool shutdown. Ongoing transfers are explicitly killed, allowing them to notify the door, billing and pnfsmanager.

The mover set max active command now accepts 0 as a valid limit. This allows queues to be suspended.

Several minor performance enhancements have been made in interacting with billing and pnfsmanager.

Commits: 84fb7b0, ade5ee9, 5245c98, bf10dfc, 62e8541, 797efe5, bef8f45, f370ba9, e875c96, 806aa55, 3c255f3, e3358e1, b059363.

8290f2f pool: Let file backend cache StorageInfo
billing

Logging of a particular billing message to billing files can now be disabled by setting the billing format of that message to the empty string.

The MoverInfoMessage now contains a p2p field which captures whether the transfer is a pool to pool transfer or a regular transfer. billing can be configured to log this field to the billing files. See billing.properties for details. The initiator field has been updated to prefix the initiator with either pool: or door:, depending on whether the request is a pool to pool transfer or a regular transfer.

The billing DB schema has been extended with additional indexes. These indexes are of particular use when combined with the Gratia tool from Open Science Grid. The schema is automatically updated on first start and for large billing databases it is expected that the schema update will take some time.

If these indexes were already created by hand prior to the upgrade, then these should either be deleted or renamed as follows. This has to be done prior to updating dCache.

Column	Index name
billinginfo.client	billinginfo_client_idx
billinginfo.initiator	billinginfo_initiator_idx
billinginfo.pnfsid	billinginfo_pnfsid_idx
billinginfo.storageclass	billinginfo_storageclass_idx
billinginfo.transaction	billinginfo_transaction_idx
doorinfo.owner	doorinfo_owner_idx
doorinfo.pnfsid	doorinfo_pnfsid_idx
doorinfo.transaction	doorinfo_transaction_idx
storageinfo.pnfsid	storageinfo_pnfsid_idx
storageinfo.transaction	storageinfo_transaction_idx
storageinfo.storageclass	storageinfo_storageclass_idx
hitinfo.pnfsid	hitinfo_pnfsid_idx
hitinfo.transaction	hitinfo_transaction_idx
Connection pooling parameters for billing are now exposed through the new db.connections.* family of configuration properties. Consult the billing.properties file for further details.

Commits: 438d84f, be864e8, 208c3a3, c6c422f.

missingfiles

Currently, when a user requests to read a file that doesn't exist, the door will respond to the user with the appropriate error message.

There are two use-cases where something more sophisticated is desirable. The first is that dCache should notify one or more external services that it was requested to read a file that doesn't exist. The second is that dCache will populate the missing file from some external source, allowing the read request to succeed. There may be other examples where it is desirable for dCache to react to failed read attempts.

The missingfiles service is a new dCache component. It exists to allow dCache to react in a coordinated fashion to a user's request to read a file that doesn't exist. This central service instructs the door to either fail the request or retry (which makes sense only if the file has been fetched from some external source).

The missingfiles service is pluggable. It takes a list of plugins and instantiates them. These plugins are used to determine how dCache should react when a user attempts to read a missing file. Each plugin is asked in turn what to do until a plugin replies with a terminating answer or the list of plugins is exhausted. A plugin replies saying to fail the request, to retry the request or to ask the next plugin in the chain. If the last plugin defers the request then then the missingfiles service will instruct the door to fail the request.

Currently only the WebDAV door has been updated to support the new service. With the default configuration, the WebDAV door does not send messages to the missingfiles service; therefore, sites should be unaffected unless they enable support by setting missing-files.enabled=true.

Only the semsg demo plugin is shipped with dCache.

Commits: c19deca.

httpd

The webadmin service has been integrated into the httpd service. Webadmin is no longer available as a separate service. The default index page of httpd has been replaced by webadmin. The old pages are available under the /old path.

Authentication for httpd must can be enabled by setting authenticated=true. Pages in webadmin that require authentication will be inoperative if authentication is not enabled.

httpd can now host any webapp. A webapp can be added using the set alias name webapp path-to-the-war-directory app-specific options ... admin shell command. Add the command to a custom httpd.conf configuration to make the configuration persistent.

Webadmin has been extended with plots produced from billing data stored in the billing DB. Support for these plots has to be explicitly enabled by setting generatePlots to true. In previous version such plots could be produced by the billing, which meant that billing and httpd had to share a common file system. This is no longer required.

Commits: 8157ab8, 361382d, 8a0e75c, c14d931, 327b428, 439c54b, 72142e2, 42388b0, feb987c.

alarms

The new alarms service is a centrallized log classifier and log collector. dCache domains can be configured to send all log output above a certain threshold to a central instance of the alarms service, which in turn classifies the messages into alarms. These alarms can be stored in a database and visualized through webadmin.

The intention is that this system is used for events that are known to require administrative action, such as checksum errors on pools, pools that become disabled due to I/O errors, files that fail to stage from tape, etc. Over time the dCache developers will classify certain events as alarms, but the alarms service allows the admin to classify additional log messages as alarms.

One percularity of the alarms service is that it must run in a domain on its own. This is because it uses a customized logback configuration that would interfere with any other service running in the same domain.

Consult the alarms.properties file for available configuration properties.

Commits: 1ab7e19, ff90d0b, 285f4b8.

Miscellaneous

Java 7

Java 7 is now a required dependency for dCache. As always, we recommend installing the JDK over the JRE, because the JDK contains additional debugging tools.

Commits: 5c18a89.

Third party libraries

A large number of third party libraries have been upgraded. We list the biggest upgrades here as they may impact customized installations.

DataNucleus 3.1
DataNucleus is a database persistence library used by srm and pinmanager.
Jetty 7.5
Jetty is an embedded HTTP server used by webdav, srm, and httpd service.
Berkeley DB Java Edition 5.0.58
Berkeley DB is an embedded non-relational database used by pool for meta data. The upgrade changes the on-disk format and pools cannot be automatically downgraded.
JGlobus 2.0
JGlobus is an implementation of GSI and GridFTP used by srm, webdav, gsidcap, and gridftp. The main improvements in JGlobus 2 are support for the SHA-2 cryptographic hash function, and that it no longer relies on the obsolete PureTLS library.
Milton 2.3
Milton is an implementation of the WebDAV protocol used by webdav.
ActiveMQ 5.7
ActiveMQ is a messaging broker that can be used as an alternative to native cells messaging.
OpenMQ 4.5
OpenMQ is a message broker that can be used as an alternative to native cells messaging.
Netty 3.6
Netty is an I/O framework used by xrootd and the xrootd and HTTP movers in pool.
Commits: 8834e4e, 290f97e, 30557fd, 31c6ee7, 3a29584, 4ae97a4, 11e9a8d, 8cc5e7a, 21fd8dd, e2cbf55, 49394ac, 6febf98, 605f7f7, 8ce45fe.

dcache command line utility

The dcache status command was extended to show the uptime of dCache:

$ dcache status
DOMAIN          STATUS                   PID  USER     
dCacheDomain    running (for 23 seconds) 4520 dcache   
adminDomain     running (for 23 seconds) 4581 dcache   
namespaceDomain running (for 23 seconds) 4620 root     
pool            running (for 2 seconds)  5518 behrmann 
gridftp-Domain  running (for 23 seconds) 4738 dcache
The dcache database ls command was extended to show information about connection limits:

$ dcache database ls
DOMAIN          CELL                  DATABASE HOST      USER      MIN  MAX MANAGEABLE AUTO 
dCacheDomain    SrmSpaceManager       dcache   localhost srmdcache          No         Yes  
dCacheDomain    cleaner               chimera  localhost chimera            No         No   
dCacheDomain    PinManager            dcache   localhost srmdcache          Yes        Yes  
dCacheDomain    billing               billing  localhost srmdcache 3    30  Yes        Yes  
dCacheDomain    RemoteTransferManager dcache   localhost srmdcache          No         Yes  
dCacheDomain    SRM-dcache-vm         dcache   localhost srmdcache          No         Yes  
namespaceDomain PnfsManager           chimera  localhost chimera   30   90  Yes        Yes  
namespaceDomain NFSv3-dcache-vm       chimera  localhost chimera            No         No   
TOTAL                                                              33   120    
Commits: 8dd8d94, 3c37b0f.

Version numbers

Since dCache has moved to Git as its primary source code management system, SVN revision numbers are no longer used when reporting dCache component versions. Instead a build identifier consisting of a timestamp and the user who build dCache is used. This information is visisble in the webadmin interface and through the info service.

$ curl http://localhost:2288/info/domains/dCacheDomain/cells/PoolManager/version
<?xml version="1.0"?>
<dCache xmlns="http://www.dcache.org/2008/01/Info">
  <domains>
    <domain name="dCacheDomain">
      <cells>
        <cell name="PoolManager">
          <version>
            <metric name="revision" type="string">2013-05-01_09-47_behrmann</metric>
            <metric name="release" type="string">2.6.0-SNAPSHOT</metric>
          </version>
        </cell>
      </cells>
    </domain>
  </domains>
</dCache>
Commits: 4ab9351.

Storage accounting

dCache supports publishing accounting information in the SSM2 format using the skel/bin/dcache-star script.

Commits: 60f8aa7, 8c4cd3c.

JMX

JMX is a facility for monitoring Java virtual machines. JMX information can be accessed with jconsole and other tools. Several changes to expose more information through JMX have been made, including request counters in pnfsmanager and srm.

Commits: d288241, 20b5997, a70ead6.

Configuration

Most invocations of the dcache and other command line utilities require that the configuration files are parsed. This involves a slow JVM startup, which is responsible for the somewhat sluggish performance observed from this utility in earlier versions. A configuration cache has now been added that will cache the parsed configuration and reuse it when none of the input files have been changed. The cached information is stored in /var/lib/dcache/config/cache. If sensistive information is stored in any configuration file, access to the cache directory should be protected.

Trailing white space is now stripped from the layout file.

The example layout file single.conf has been altered to no longer disable the interdomain message broker. This is intended to make it easier for new users to configure a multidomain dCache. However be aware that access to port 11111 has to be firewalled for a secure setup.

Commits: 538bc1a, 2efced3, bff3740.

Reference material

Upgrade checklist

Known issues when upgrading

too many threads/processes
When upgrading to RHEL 6 the number of processes (and therefore, the number of threads) is limited to 1024 for non-root users. For a dCache domain (in particular SRM, dcap and FTP doors, and FTP and dcap transfers on pools) 1024 threads is too few for a busy site. As dCache does not run as root but as the user 'dcache' this limit needs to be extended.

One symptom of this problem is the message:

java.lang.OutOfMemoryError: unable to create new native thread
Another symptom is, on pool nodes, the message:
ClosedByInterruptException [..] DiskErrorCacheException: Disk I/O Error
The problem may be solved by granting 'dcache' user a specific profile; for example, by creating the file /etc/security/limits.d/dCache with the following contents:


	dcache  soft  nofile  unlimited
      
too many database connections
dCache requires rather a large number of database connections, but it doesn't make active use of these connections. Therefore, future versions of dCache will likely reduce the number of database connections.

When upgrading dCache from v2.2 to v2.6, the policy of when database connections are established has changed. Some components in v2.2 established connections only when needed; in dCache v2.6 these components establish database connections on startup.

Since dCache prior to v2.6 will typically not make use of all database connections, a dCache instance may be configured to use a far greater number of database connections that the PostgreSQL instance allows without any problem. When such a site upgrades to v2.6, their dCache instance will fail since dCache will attempt to establish all connections on start up.

The symptom is that a dCache core component that uses a database (chimera, pin-manager, SRM, space-manager, transfer-manager, billing) fails to start and the PostgreSQL log files describe how there are too many connections.

The problem may be solved by simply increasing the number of concurrent connections that PostgreSQL allows.

Terminology

cell
A component of dCache. dCache consists of many cells. A cell must have a name which is unique within the domain hosting the cell.
domain
A container hosting one or more dCache cells. A domain runs within its own process. A domain must have a name which is unique throughout the dCache instance.
service
An abstraction used in dCache configuration files to describe atomic units to add to a domain. A service is typically implemented through one or more cells.
layout
Definition of domains and services on a given host. The layout is specified in the layout file. The layout file may contain both domain- and service- specific configuration values.
pool
A service providing physical data storage.
Services

This section lists all supported services. Those marked with a * are services that dCache requires to function correctly. Dotted dependencies are optional.

Core services
Name	Decscription
broadcast∗	Internal message broadcast service.
cleaner∗	Service to remove files from pools and tapes when the name space entry is deleted.
cns	Cell naming service used in conjuction with JMS for well known name lookup.
dir	Directory listing support for DCAP.
gplazma	Authorization cell
hopping	Internal file transfer orchestration.
loginbroker	Central registry of all doors. Provides data to SRM for load balancing.
pinmanager	Pinning and staging support for SRM and DCAP.
pnfsmanager∗	Gateway to name space (either PNFS or Chimera).
pool∗	Provides physical data storage.
poolmanager∗	Central registry of all pools. Routes transfers to pools, triggers staging from tape, performs hot spot detection.
replica	Manages file replication for Resilient dCache.
spacemanager	Space reservation support for SRM.
srm-loginbroker	Central registry of all SRM doors.
Admin and monitoring services
Name	Decscription	Dependencies
admin	SSH based admin shell.	
alarms	Centrallized log collector for alarms.	
billing∗	Service for logging to billing files or the billing database.	
httpd	Monitoring portal. Includes webadmin.	loginbroker topo
info	Info service that collects information about the dCache instance.	httpd
statistics	Collects usage statistics from all pools and generates reports in HTML.	
topo	Builds a topology map of all domains and cells in the dCache instance.	
Doors
Name	Decscription	Dependencies
authdcap	Authenticated DCAP door.	dir pinmanager
dcap	dCap door.	dir pinmanager
gsidcap	GSI dCap door.	dir pinmanager
kerberosdcap	Kerberized dCap door.	dir pinmanager
ftp	Regular FTP door without strong authentication.	
gridftp	GridFTP door.	
kerberosftp	Kerberized FTP door.	
nfsv3	NFS 3 name space export (only works with Chimera).	
nfsv41	NFS 4.1 door (only works with Chimera).	
srm	SRM door.	pinmanager loginbroker srm-loginbroker transfermanagers spacemanager
transfermanagers	Server side srmCopy support for SRM.	
webdav	HTTP and WebDAV door.	
xrootd	XROOT door.	
Obsolete services
Name	Reason
acl	Integrated into pnfsmanager.
dummy-prestager	dcap now uses pinmanager for staging.
webadmin	Integrated into httpd.
gPlazma plugins

The following gplazma plugins ship with dCache and can be used in gplazma.conf. Note that several plugins implement more than one type. Usually such plugins should be added to all phases supported by the plugin.

gPlazma plugins
Name	Type	Description
jaas	auth	Implements password authentication through the Java Authentcation and Authorization Services (JAAS). A valid JAAS setup for password verification has to be defined in etc/jgss.conf. Fails if no password credential is provided or if JAAS denies the login. A username principal is generated upon success.
kpwd	auth	Implements password authentication using the kpwd file. Fails if no password credential is provided, if the username is not defined in the kpwd file, if the password is invalid, or if the entry has been disabled in the kpwd file.
voms	auth	Validates any VOMS attributes in an X.509 certificate and extracts all valid FQANs. Requires that a vomsdir is configured. Fails if no valid FQAN is found.
x509	auth	Extracts the DN from an X.509 certificate. The certificate chain is not validated (it is assumed that the door already validated the chain). The plugin fails if no certificate chain is provided.
xacml	auth	
authzdb	map	Maps user and group name principals to UID and GID principals according to a storage authzdb file. The file format does not distinguish between user names and group names and hence each entry in the file maps to both a UID and one or more GIDs. Therefore the UID and the primary GID are determined by the mapping for the primary group name or user name. The name of that mapping is kept as the user name of the login and may be used for a session plugin or for authorization in space manager. Remaining GIDs are collected from other mappings of available group names.
gridmap	map	Maps DN principals to user name principals according to a grid-mapfile. Fails if no DN was provided or no mapping is found.
kpwd	map	Maps user names, DNs and Kerberos principals according to the kpwd file. Only user names verified by the kpwd auth plugin are mapped. Fails if nothing was mapped or if the kpwd entry has been disabled. Maps to user name, UID and GID principals.
krb5	map	Maps Kerberos principals to username principals by stripping the domain suffix.
nis	map	Maps user name principals to UID and GID through lookup in NIS.
nsswitch	map	Maps user name to UID and GID according to the system native Name Service Switch.
vorolemap	map	Maps FQAN principals to group name principals according to a grid-vorolemap file. Each FQAN is mapped to the first entry that is a prefix of the FQAN. The primary FQAN (the first in the certificate) is mapped to the primary group name. Fails if no FQAN was provided or no mapping was found.
ldap	map	
mutator	map	
argus	account	
kpwd	account	Fails if the kpwd entry used during the map has been disabled.
authzdb	session	Associates a user name with root and home directory and read-only status according to a storage authzdb file.
kpwd	session	Adds home and root directories and read-only status to the session. Only applies to mappings generated by the kpwd map plugin.
nis	session	Associates a user name with a home directory through NIS lookup. The sessions root directory is always set to root and the session is newer read-only.
nsswitch	session	Sets the session home directory and root directory to the file system root, and sets the session's read-only status to false.
ldap	session	
nis	identity	Maps user name principals to UID and group name principals to GID.
nsswitch	identity	Maps user name principals to UID and group name principals to GID.
ldap	identity	
Please consult gplazma.properties for details about available configuration properties.

Changed properties
