---
layout: page
title: 2.10 Upgrade
permalink: /docs/upgrade-2.6-to-2.10/
top_graphic: 1
date: 2017-2-22T00:00
---

# The ultimate golden release upgrade guide

## How to get from dCache 2.6 to dCache 2.10

<address>

<strong>Author</strong><br/>

Gerd Behrmann &lt;behrmann@ndgf.org&gt;

</address>



## About this document


<p>The dCache golden release upgrade guides aim to make migrating

between golden releases easier by compiling all important information

into a single document. The document is based on the release notes of

versions 2.7, 2.8, 2.9 and 2.10. In contrast to the release notes, the

guide ignores minor changes and is structured more along the lines of

functionality groups rather than individual services.</p>


<p>Although the guide aims to collect all information required to

upgrade from dCache 2.6 to 2.10, there is information in the release

notes not found in this guide. The reader is advised to at least have

a brief look at the release notes found

at <a href="http://www.dcache.org/">dCache.org</a>.</p>


<p>There are plenty of changes to configuration properties, default

values, log output, admin shell commands, admin shell output,

etc. If you have scripts that generate dCache configuration, issue

shell commands, or parse the output of shell commands or log files,

then you should expect that these scripts need to be adjusted. This

document does not list all those changes.</p>



## About this release


<p>dCache 2.10 is the fifth golden (long term support) release of

dCache. The release will be supported at least until summer 2016. This

is the recommended release for the second LHC run.</p>


<p>As always, the amount of changes between this and the previous

golden release is staggering. We have tried to make the upgrade

process as smooth as possible, while at the same time moving the

product forward. This means that we try to make dCache backwards

compatible with the previous golden release, but not at the expense of

changes that we believe improve dCache in the long run.</p>


<p>The most visible change when upgrading is that most configuration

properties have been renamed, and some have changed default

values. Many services have been renamed, split, or merged. These

changes require work when upgrading, even though most of them are

cosmetic - they improve the consistency of dCache and thus ease the

configuration, but those changes do not fundamentally affect how

dCache works.</p>


<p>dCache pools from version 2.6 to 2.9 can be mixed with services

from dCache 2.10. This enables a staged roll-out in which non-pool

nodes are upgraded to 2.10 first, followed by pools later. It is

however recommended to upgrade to the latest version of 2.6 before

performing a staged roll-out.</p>


<p>Upgrading directly from versions prior to 2.6 is not officially

supported. If you run versions before 2.6, we recommend upgrading to

2.6 first. That is not to say that upgrading directly to 2.10 is not

possible, but we have not explicitly tested nor documented such an

upgrade path.</p>



<p>Downgrading after upgrade is not possible without manual

intervention: In particular database schemas have to be rolled back

<em>before</em> downgrade. If pools use the Berkeley DB meta data

back-end, these need to be converted to the file back-end

<em>before</em> downgrading and then back to the Berkeley DB back-end

after downgrade.</p>





<h2>Incompatibilities</h2>



<p>Upgrading from 2.6 to 2.10 will require adjustments to the dCache

configuration. Most changes are described in detail in the following

sections, but for the impatient, the incompatible changes include:</p>



<ul>

<li>Most configuration properties have been renamed. Although most old

property names can still be used, some are no longer supported. Upon

upgrade these have to be changed in the dCache configuration.</li>

<li>Several service definitions have changed. In particular,

flavors of DCAP, FTP and NFS doors have been collapsed, and several

redundant services have been removed. The layout files instantiating

such services have to be updated.</li>

<li>The <code>classic</code> pool manager partition type has been

removed. <code>wass</code> or another pool selection algorithm must

be used instead. If you relied on the <code>classic</code> partition

type, you have to manually adjust

<code>poolmanager.conf</code> during upgrade.</li>

<li>The <code>wrandom</code> partition type has been removed. The same

behavior may be achieved with the <code>wass</code> partition

type.</li>

<li>Several default values for configuration properties have

changed. Although we believe the new defaults are better, you should

review the changes while upgrading.</li>

<li>The space manager database schema has changed. It will be updated

on upgrade, which may take some time on large databases. Previous

versions of dCache are not forward compatible with the new schema and

the schema has to be explicitly rolled back before downgrading

dCache.</li>

<li>The Chimera database schema has changed. It will be updated on

upgrade, which may take some time on large databases. Downgrade is

not possible without rolling back the schema changes.</li>

<li>The <code>chimera-cli</code> utility has been replaced

by <code>chimera</code>.</li>

<li>In DCAP, <code>ctime</code> is now <em>last attribute change

time</em> (like in POSIX) rather than <em>creation time</em>.</li>

<li>The space manager admin command line interface has been rewritten,

with several commands being removed, replaced, or modified.</li>

<li>The semantics of implicit space reservations and space

reservations for non-SRM transfers has changed.</li>

<li>If the NFS door and PnfsManager are hosted in the same domain then

the layouts file must have the <code>pnfsmanager</code> service

before the <code>nfs</code> service.</li>



<!-- 2.9 -->



<li>The new property <code>dcache.upload-directory</code> may have to

be defined on upgrade. Read the section on the <code>srm</code>

service for further details.</li>

<li>An internal change to how we implement dCache services in the

Spring framework breaks compatibility with third party plugins

providing custom services implemented with Spring. Plugin providers

should update their plugin to match the changes in

<a href="https://github.com/dcache/dcache/commit/b7234eeeb827edd86a9a520af9c4f4bdc7ed8e69">b7234ee</a>.</li>

<li>SRM uploads that are not finalized by submitting

an <code>srmPutDone</code> will be

deleted. The <code>srmPutDone</code> message is required by the SRM

standard and standard compliant clients will not have a problem with

this. The file is not available for reading

until <code>srmPutDone</code> has been issued.</li>

<li>IPv6 support is enabled by default.</li>

<li>Tape integration was rewritten. Classic HSM scripts continue to be

supported, however the pool setup file should be regenerated after

upgrade.</li>

<li>The HSM cleaner is enabled by default.</li>



<!-- 2.10 -->



<li>Kerberos uses values in <code>/etc/krb5.conf</code> by default. If

both <code>kerberos.realm</code> and

<code>kerberos.key-distribution-center-list</code> are set then

custom values are used.</li>

<li>In billing log files, transfer-specific information is written as

a colon-separated list of items. For HTTP and xrootd, the format has

changed, with a colon now separating the protocol version information

and the client IP address. The output for HTTP and xrootd is now

consistent with information recorded for other protocol

transfers.</li>

</ul>



<p><span class="label label-warning">WARNING</span> By default dCache

used to not allow overwriting of files using ftp or srm. In order to

be standards compliant this has been changed. The default value

for <code>srm.enable.overwrite</code> and

<code>ftp.enable.overwrite</code> is <code>true</code>. For srm, files

are not overwritten unless explicitly requested by the client.</p>



<h2>Services</h2>



<p>This section describes renamed, collapsed, split, and removed

services. A summary of the changes is contained in the following

table.</p>



<table id="tab:services" class="table table-condensed">

<thead>

<tr>

<th>Service</th>

<th>Alternative</th>

<th>Configuration / Remark</th>

</tr>

</thead>

<tbody>

<tr>

<td>gridftp</td>

<td>ftp</td>

<td>ftp.authn.protocol = gsi</td>

</tr>

<tr>

<td>kerberosftp</td>

<td>ftp</td>

<td>ftp.authn.protocol = kerberos</td>

</tr>

<tr>

<td>dcap</td>

<td>dcap</td>

<td>dcap.authn.protocol = plain<br/>

dcap.authz.anonymous-operations = READONLY</td>

</tr>

<tr>

<td>gsidcap</td>

<td>dcap</td>

<td>dcap.authn.protocol = gsi</td>

</tr>

<tr>

<td>kerberosdcap</td>

<td>dcap</td>

<td>dcap.authn.protocol = kerberos</td>

</tr>

<tr>

<td>authdcap</td>

<td>dcap</td>

<td>dcap.authn.protocol = auth</td>

</tr>

<tr>

<td>nfsv3</td>

<td>nfs</td>

<td>nfs.version = 3</td>

</tr>

<tr>

<td>nfsv41</td>

<td>nfs</td>

<td>nfs.version = 4.1</td>

</tr>

<tr>

<td>acl</td>

<td>pnfsmanager</td>

<td>pnfsmanager.enable.acl = true</td>

</tr>

<tr>

<td>dummy-prestager</td>

<td>pinmanager</td>

<td></td>

</tr>

<tr>

<td>webadmin</td>

<td>httpd</td>

<td></td>

</tr>

<tr>

<td>hopping</td>

<td>hoppingmanager</td>

<td></td>

</tr>

<tr>

<td>srm-loginbroker</td>

<td>loginbroker</td>

<td>srm-loginbroker

can be removed from the layout</td>

</tr>

<tr>

<td>gsi-pam</td>

<td>gplazma</td>

<td>most likely you can drop this service from the layout</td>

</tr>

</tbody>

</table>



<h3 id="mergedandsplitservices">Merged and split services</h3>



<p>In previous releases some protocols were implemented as several

doors, eg DCAP existed as both a plain, Kerberos and GSI doors, same

for FTP, and NFS existed as both an NFS 3 and an NFS 4 door (and the

NFS 4 version confusingly was able to serve NFS 3 too). Most

properties used by these doors were used by all variants. Other

protocols, such as HTTP and xrootd, only had a single door with the

authentication scheme being selectable through a configuration

property. </p>



<p>To improve consistency, variants of a door have now been collapsed

into a single service. A configuration option allows the

authentication type or NFS version to be configured.</p>



<p>Specifically, the services <code>ftp</code>, <code>gridftp</code>,

and <code>kerberosftp</code> have been collapsed into the service

<code>ftp</code> with the configuration option

<code>ftp.authn.protocol</code> setting the authentication

protocol. The services <code>dcap</code>, <code>gsidcap</code>,

<code>kerberosdcap</code>, and <code>authdcap</code> have been

collapsed into the service <code>dcap</code> with the configuration

option <code>dcap.authn.protocol</code> setting the authentication

protocol. The services <code>nfsv3</code> and <code>nfsv41</code> have

been collapsed into the service <code>nfs</code> with the

configuration option <code>nfs.version</code> defining the NFS

version.</p>



<h3 id="removedservices">Removed services</h3>



<p>The services <code>acl</code>, <code>dummy-prestager</code>, and

<code>webadmin</code> have been removed entirely. For several releases

these services did nothing more than print a warning that the

functionality has been embedded in other services.</p>



<p>The service <code>gsi-pam</code> has been removed. It was a legacy service that

did not serve any purpose.</p>



<p>The <code>srm-loginbroker</code> service has been removed. SRM now

registers directly with the regular <code>loginbroker</code>

service. Doors can be configured to register with specific

<code>loginbroker</code> instances if more flexibility is needed.</p>



<h3 id="renamedservices">Renamed services</h3>



<p>The <code>hopping</code> service has been renamed to

<code>hoppingmanager</code>.</p>



<h3 id="embedding-gplazma">Embedding gplazma</h3>



<p>gPlazma has always had two modes of operation: As a standalone service

or as a module in which it would be used directly by a door. In 1.9.12

the module-mode was replaced by an automatically created non-exported

gPlazma instance running in the same domain as the door. Due to the

way cell routing works, this meant that doors in that domain would use

the local gPlazma instance.</p>



<p>The explicit module-mode has now been removed completely. Instead

one can achieve the same effect by manually adding a gPlazma instance

to a domain with doors and set <code>gplazma.cell.export</code> to

false. Such a gPlazma instance is not published to the rest of dCache

and will thus only be used by doors in the same domain.</p>



<p>The benefits of this approach are that it is much more obvious how

things are put together, and such a local gPlazma instance can be

configured like any other gPlazma instance. It also makes it possible

to have other deployments, like two different local gPlazma instances

with non-default cell names, one which can be used by some doors, and

the other by other doors; or several exported gPlazma instances with

non-default cell names, and some doors configured to use one and other

doors to use the other instance. This could for instance be used to

distinguish between internal and external doors, or maybe have a

different gPlazma setup for admin and httpd login.</p>



<pre>[testDomain]

[testDomain/gplazma]

gplazma.cell.export = false

gplazma.cell.name = gPlazma-for-admin

gplazma.configuration.file = /etc/dcache/gplazma-for-admin.conf



[testDomain/admin]

admin.service.gplazma = gPlazma-for-admin

# The admin service now uses the gplazma service called 'gPlazma-for-admin',

# which uses the gplazma-for-admin.conf configuration file.



[testDomain/httpd]

# httpd uses the main 'gPlazma' service.

</pre>



<h2 id="configurationchanges">Configuration</h2>



<p>In dCache 1.9.12 the entire configuration system was rewritten. The

new system introduced a layered approach, with default files shipped

with dCache, a system wide configuration file,

<code>dcache.conf</code>, and a host configuration file, the layout

file.</p>



<p>At the time, most configuration properties remained unchanged, to

ease transition to the new configuration system. Over time this has

lead to an inconsistent mess of mixed naming schemes, inconsistent

configuration property names, inconsistent units for expressing

durations and timeouts, and inconsistent values for boolean

properties.</p>



<p>The new configuration system introduced in dCache 1.9.12 also

introduced a scoping operator. This operator has led to a lot of

confusion, as even expert users didn’t understand its semantics. The

operator allowed the same property to have different default values

depending on the service that used it. The operator was most widely

used for defining a cell name using the common <code>cell.name</code>

property, as well as for TCP ports using the <code>port</code>

property.</p>



<p>Based on feedback at the 2013 dCache user workshop, we decided to

clean up the dCache configuration. The configuration system itself

stays mostly unchanged: There are still default files, a <code>dcache.conf</code>

file, and a layout file. Most properties have however been renamed.</p>



<p>To the extend possible, old property names still work, although

they have been marked deprecated and are obsolete or forbidden in

dCache 2.11. The scoping operator has been removed and replaced by a

strict naming convention.</p>



<p><span class="label label-warning">WARNING</span> Because the scoping

operator was removed, some properties that relied on the operator can

no longer be supported and these <em>must</em> be changed on

upgrade. Except for trivial deployments, upgrading from 2.6 to 2.10

cannot be done without changing at least a few properties.</p>



<h3>Naming conventions</h3>



<p>All properties now follow a strict and hierarchical naming

scheme. Property names are always lower case, a hyphen is used as a

word separator, and dot as a node separator in the naming hierarchy.

All properties used by a service are prefixed by the service type, eg,

all <em>srm</em> properties begin with <code>srm.</code> and all

<em>pnfsmanager</em> properties with <code>pnfsmanager.</code>.</p>



<p>Properties that begin with <code>dcache.</code> don’t belong to any particular

service: They are either not used by services (such as properties for

defining JVM options, or options for configuring an entire domain), or

they are used by multiple services. In the latter case, each service

will define a similarly named property prefixed with its own name;

e.g., <code>dcache.net.listen</code> defines the primary IP address services bind

to, however no service uses that property directly. Instead each

service defines a <code>*.net.listen</code> property that defaults to the value

of <code>dcache.net.listen</code>, such as

<code>srm.net.listen=${dcache.net.listen}</code>. This provides some of the same

flexibility as the scoping operator used to, as we can define per

service defaults.</p>



<p>No rule without an exception (except one): Chimera database

properties begin with <code>chimera.</code>. Since the Chimera

database are accessed by <code>pnfsmanager</code>, <code>nfs</code>,

and <code>cleaner</code>, we have chosen a common set of properties to

define the database connectivity. In a sense, Chimera is its own

service.</p>



<h3>Time units</h3>



<p>All properties that specify a time duration now have a sibling,

suffixed with <code>.unit</code>, that specifies the time unit; e.g.,

<code>ftp.performance-marker-period</code> specifies the time between two FTP

performance markers. <code>ftp.performance-marker-period.unit</code> specifies

the time unit of <code>ftp.performance-marker-period</code> (which happens to be

SECONDS). In a few cases the time unit is immutable, however in most

places it is configurable.</p>



<p>We recommend to explicitly define the unit if any property

specifying a time duration is changed: In future releases we may

decide to change the time unit. Making the unit explicit in your

dCache configuration guards against such changes.</p>



<h3>Booleans</h3>



<p>In the past, boolean properties used a mixture of values like

<em>true</em>, <em>false</em>, <em>enabled</em>, <em>disabled</em>,

<em>yes</em>, <em>no</em>, etc. In some cases the properties involved

double negations, like <code>billingDisableTxt</code> which had to be

set to <em>no</em> to enable billing logging to flat text files.</p>



<p>Boolean properties now always use the values <em>true</em> and

<em>false</em>, and are always phrased as enabling something.</p>



<h3>Common properties</h3>



<p>Some property naming patterns are reused in most services. This

section describes some of them. In the following an asterix is used

where the service type is to be inserted.</p>



<dl class="dl-horizontal">

<dt><code>*.cell.name</code></dt>

<dd><p>Defines the name of the primary cell of the service.</p></dd>



<dt><code>*.cell.export</code></dt>

<dd><p>Controls whether the cell name is exported as a well known

cell. Well known cells must have a unique name throughout dCache, but

have the benefit that they can be addressed using the cell name only

rather than the fully qualified cell address (that also contains the

domain name).</p>

<p>This can for instance be used to embed <code>gplazma</code> in the

same domain as a door without exporting the gPlazma name. Such

a <code>gplazma</code> instance is only used by doors in that

domain. This replaces the feature to use gPlazma as a module.</p></dd>



<dt><code>*.service.<em>S</em></code></dt>

<dd><p>The cell address of service <code><em>S</em></code>. Eg

<code>ftp.service.pnfsmanager</code> is the cell address of

pnfsmanager as used by ftp doors. If the service has a well known

name, only the well known name needs to be specified in the

address. Otherwise the fully qualified cell address must be used. We

tried to make all service names configurable through this

mechanism.</p>

<p>Combined with the ability to change cell names and not exporting

services as well known, these changes provide lots of flexibility for

advanced deployments. Any hard-coded service names left in dCache

should be considered a bug to be reported.</p></dd>



<dt><code>*.service.<em>S</em>.timeout</code></dt>

<dd><p>The communication timeout for requests to

service <code><em>S</em></code>.</p></dd>



<dt><code>*.db.</code></dt>

<dd><p>Database parameters; e.g., name, host, user, password, etc.</p></dd>



<dt><code>*.enable.</code></dt>

<dd><p>Feature switches;

e.g., <code>*.enable.space-reservation</code>.</p></dd>

</dl>



<h3 id="any-ofannotations">any-of annotations</h3>



<p>A new <em>any-of</em> annotation was added. It is used for

properties that accept a list of comma separated values. This is

reserved for use in default files shipped with dCache and plugins.</p>



<h3>Layout files</h3>



<p>The example layout files were updated and placed in the

directory <code>/usr/share/dcache/examples/layouts</code> instead

of <code>/etc/dcache/layouts</code>.</p>



<p><span class="label label-default">IMPORTANT</span> RPM users who

used to call their layout files single, head or pool should please

check that RPM did not rename their layout file.</p>



<h2>Databases</h2>



<h3>Schema management</h3>



<p>Except for the <code>srm</code> and <code>replica</code> services,

all databases in dCache are managed through the <em>liquibase</em>

schema management library. This now also includes

the <code>spacemanager</code> service. The SQL scripts for creating

the Chimera schema by hand are no longer shipped with dCache.</p>



<p>Schema changes are automatically applied the first time a service

using the schema is started. Such changes may also be applied manually

before starting dCache using the <code>dcache database update</code>

command. It will update the schemas of all databases used by services

configured on the current node.</p>



<p>For even more hands-on schema management, the <code>dcache database

showUpdateSQL</code> command was added. It outputs the SQL that would

be executed if <code>dcache database update</code> was executed. The

emitted SQL may be applied manually to the database, thereby updating

the schema.</p>



<p>Before downgrading dCache, it is essential that schema changes are

rolled back to the earlier version. This needs to be

done <strong>before</strong> installing the earlier version of dCache.

Schema changes can be rolled back using the <code>dcache database

rollbackToDate</code> command. It is important to remember the date

the schema changes where applied in the first place so that it can be

rolled back to the version prior to the upgrade.</p>



<p><span class="label label-default">NOTE</span> The <code>nfs</code>

service does not automatically apply schema changes to Chimera - only

the <code>pnfsmanager</code> service does that. <code>nfs</code> will

however check whether the Chimera schema is current and refuse to

start if not. One consequence of this is that if <code>nfs</code>

and <code>pnfsmanager</code> run in the same domain,

either <code>nfs</code> must be placed after <code>pnfsmanager</code>

in the layout file or the changes must be applied manually

using <code>dcache database update</code>.</p>





<h3>Schema changes</h3>



<h4>Chimera</h4>



<p>Several changes have been made to the Chimera schema. For large

databases applying these changes will be a lengthy operation. If this

is a concern, we recommend doing a test migration on a clone of the

database.</p>



<p>The <code>uri_encode</code> and <code>uri_decode</code> stored

procedures have been introduced. These are used

by <em>Enstore</em>.</p>



<h4>Space manager</h4>



<p>Several changes have been made to the space manager schema. For

large databases applying these changes will be a lengthy operation. If

this is a concern, we recommend doing a test migration on a clone of

the database.</p>



<p>Third party alterations to the schema should be carefully inspected

before upgrading, and possibly be rolled back if they conflict with

the schema changes. Workarounds for outdated statistics for

the <code>srmspacefile</code> table are no longer necessary.</p>



<p>The database schema contains several fields which are aggregates of

other fields. In earlier versions, these aggregated fields were

maintained by dCache, adding considerable overhead in the form of

database round trips and locks. This logic has now been embedded in

the database in the form of database triggers. Be aware that these

triggers are essential and must be restored if the database is

restored from backup.</p>



<p>Many other changes have been made to the schema. Any third party

queries against this database will most likely require updates.</p>



<h3>Connection pool</h3>



<p>The BoneCP database connection pool library has been replaced with

HikariCP. HikariCP is more maintained, smaller, faster and more

robust.</p>



<p>HikariCP has slightly different controls for adjusting the database

connection pool. While BoneCP partitioned connections, HikariCP has no

such concept. HikariCP also maintains a minimum number of idle

connections; this is in contrast to the minimum number of connections

that BoneCP maintains. Sites that have tuned their data connections

limits should take note of these differences and adjust their

configuration accordingly.</p>



<p>The <code>srm</code> service has been updated to use HikariCP in

favor of an ad-hoc connection pool.</p>



<h3>JDBC 4 drivers</h3>



<p>The <code>*.db.driver</code> configuration properties have been

marked obsolete. The proper driver is now automatically discovered

from the JDBC URI. Only JDBC 4 compliant database drivers are

supported (this is only relevant if you install a custom JDBC

driver).</p>







<h2>Name space</h2>



<h3>Set group ID</h3>



<p>The setgid bit on directories has been implemented in

Chimera. This bit is useful for shared directories in which files and

sub-directories have to inherit the group ownership of the parent

directory. Using the set-gid bit is more flexible than relying on the

<code>pnfsmanager.inherit-file-ownership</code> property.</p>



<h3>Creation time</h3>



<p>Chimera has been updated to track the creation time of files in

addition to the attribute change time. The creation time for existing

files is obviously unknown. When updating the database schema,

existing files will receive a creation time being the oldest of the

mtime, ctime, and atime fields.</p>



<p>DCAP was updated to report last attribute change time in the ctime

field of a stat request. This was the intended semantics from the

beginning and is what ctime means in the POSIX standard, but in dCache

ctime has in some places been confused with creation time.</p>



<h3>Command line interface</h3>



<p>The Chimera command-line tool <code>chimera-cli</code> has been

replaced with <code>chimera</code>. The new tool offers an interactive

shell when invoked without arguments and can execute scripts. It can

also be invoked with a command on the command-line like the

old <code>chimera-cli</code> tool. Note that some commands have a

different argument order compared to the old tool (they now use the

same order as used by similar tools defined in the POSIX

standard).</p>



<p>To learn about the supported commands, start the Chimera shell by running

<code>chimera</code> and then type <code>help</code>.</p>



<h3>Lookup permission check</h3>



<p>Validation of lookup permissions on the full path is enabled by

default. Full path permission check may result in access to files and

directories, that was allowed before, to be denied. Sites are

advised to check the permission settings on directories on upgrade, or

to disable the POSIX compliant full path permission check by flipping

the property

<code>pnfsmanager.enable.full-path-permission-check</code>.</p>





<h2>Authn &amp; Authz</h2>



<h3>Password authentication</h3>



<p>A gPlazma password authentication plugin

called <code>htpasswd</code> was added supporting the common htpasswd

file format used by many web servers. Only the MD5 hash format is

currently supported. Use the

<code>htpasswd</code> utility available on most operating systems to

create and manage htpasswd files.</p>



<h3 id="ldap">LDAP</h3>



<p>Modified the gPlazma <code>ldap</code> plugin to fail in the map-

or session-phases of a login if no user name is supplied or if there is

no mapping for this user. Please check your gPlazma configuration if

you use the ldap plugin.</p>



<p>Previous versions of the plugin hard coded values for the home and

root directory. The root directory was set to <code>/</code> and the

home directory was set to the home directory as stored in the LDAP

server. The behavior is now configurable through two new

properties, <code>gplazma.ldap.home-dir</code> and

<code>gplazma.ldap.root-dir</code>. For those two properties it is

possible to use keywords that will be substituted by the corresponding

attribute value in LDAP. For example <code>%homeDirectory%</code> will

be replaced by the value of attribute <em>homeDirectory</em> in the

<em>people</em> tree.</p>



<h3 id="kerberos">Kerberos</h3>



<p>dCache will use the kerberos configuration

in <code>/etc/krb5.conf</code> by default. The existing configuration

is still supported, but the system configuration file is now taken as

the default.</p>





<h3>GridSite delegation</h3>



<p>Support for GridSite delegation v2.0.0 was added. The endpoint is

run as part of the <code>srm</code> service and has the

path <code>/srm/delegation</code>. The GridSite delegation endpoint

allows a user to delegate a credential, discover the remaining

lifetime of any delegated credential and destroy delegated

credentials. Those credentials delegated via GSI (typically as part of

an SRM operation) will have the delegated ID of

<em>gsi</em>. Using this, a client may query the lifetime of any already

delegated credential and delete credentials delegated via SRM

operations.</p>



<p>A delegation client that allows scripted and console-based interaction

with GridSite endpoints has been implemented. The client is released

independently, as part of the dCache srm client package.</p>



<h2>Logging</h2>



<p>If you have customized your <code>logback.xml</code>, it is

important that you reset the file back to its default when upgrading

to dCache 2.10. You can reapply local modifications to the updates

default after upgrade.</p>



<p>The biggest change to logging is the addition of an access log. The

log is created for every dCache domain, although currently only

the <code>srm</code>, <code>ftp</code>, and <code>webdav</code>

services support it. These log files contain an entry for every

protocol level request being made and are thus analogous to the common

access logs generated by most web servers. The log contains a

timestamp, the client address, and various protocol specific fields

describing the request and response. For complex protocols like SRM,

the access log cannot possibly contain the entire request. The log

does contain the SRM request ID and the entire request can be

retrieved through the admin shell. The log is created

in <code>/var/log/dcache/</code> and is named after the domain

followed by the string <code>.access</code>. The log is rotated and

compressed daily and kept for thirty days (this is configurable

through logback).</p>



<p>Most services have had their log output improved. In particular

the <code>srm</code> and <code>spacemanager</code> services are a lot

less noisy. For <code>srm</code> the session identifier has been

shortened.</p>



<h2>Admin shell</h2>



<h3>SSH</h3>



<p>SSH 1 support has been removed from the <code>admin</code>

door. This protocol is known to be insecure. The <code>admin</code>

door now requires SSH 2 and defaults to port 22224.</p>



<p>For password based authentication, the door relies on gPlazma. Thus

a password authentication plugin (eg <code>kpwd</code>

or <code>htpasswd</code>) must be set up. The account must have GID 0

to allow login to the <code>admin</code> door (the GID is

configurable). Alternatively, we recommend key-based

authentication.</p>



<p>The use of GID 0 also applies to the <code>webadmin</code>

service. Users with this GID have admin privileges

in <code>webadmin</code>. In the past <code>webadmin</code> used GID

1000, but the default has been changed.</p>



<h3>pcells</h3>



<p>A <a href="http://www.dcache.org/downloads/gui/index.shtml">pcells</a>

SSH subsystem was added. The current releases of pcells support this

subsystem.</p>



<h3>Help</h3>



<p>dCache is in the middle of a transition between two frameworks for

implementing the admin shell commands. The newer of these frameworks

provides much nicer help output. The format is similar to classic man

pages. In ANSI terminals the output uses highlighting to make the

output easier to glance over.</p>



<p>While transitioning from one implementation to the other, we have

added more documentation for each command. This is accessed

using <code>help <em>command</em></code>.</p>



<h2>Pool selection</h2>



<h3>Partition types</h3>



<p>Pool selection is controlled by pool manager partitions. Different

partition types provide different pool selection algorithms. This

section outlines changes to those partition types.</p>



<dl class="dl-horizontal">

<dt>classic</dt>

<dd>

<p>Some years ago, a new load balancing scheme called <em>weighted

available space selection</em> (wass) had been introduced. Since

dCache 2.2 this scheme was used by default for new installations. The

old scheme, dubbed <code>classic</code> has now been removed

and <code>wass</code> is the new default partition type. The change

has allowed quite some legacy code to be removed and enables future

development. In particular, the concept of space cost is more or less

gone from the entire code base.</p>



<p><span class="label label-warning">IMPORTANT</span> Sites still

using <code>classic</code> must manually

update <code>poolmanager.conf</code> to create <code>wass</code>

partitions instead. When switching from <code>classic</code>

to <code>wass</code>, it is important to

reset <code>cpucostfactor</code> and

<code>spacecostfactor</code>, as the interpretation of these

parameters has changed. We suggest to use the default value of 1.0 for

both parameters.</p>

</dd>



<dt>buffer</dt>

<dd>

<p>This new partition type was added and is intended for pools used as

transfer buffers. This algorithm chooses a pool based on weighted

random selection, with weights derived from the pools’ load only. Free

space has no effect as all pools with sufficient space to store the

file are considered. This partition type is suitable for pools which

do not hold files permanently, such as import and export pools.</p>



<p>The <code>wass</code> partition type is not suited for this use

case, as <code>wass</code> prioritizes balancing free space over

load.</p>



<p>The <code>buffer</code> partition type respects the <em>mover cost

factor</em> and

<em>performance cost factor</em> settings, using an interpretation similar to

<code>wass</code>.</p>

</dd>



<dt>wrandom</dt>

<dd>

<p>The <code>wrandom</code> partition type has been removed. The same

behavior may be achieved with <code>wass</code>.</p>

</dd>

</dl>



<h3>Space cost</h3>



<p>With the removal of the <code>classic</code>, the concept of space

cost is gone from dCache. This affects several admin shell

commands:</p>



<ul>

<li>Commands that could report space cost no longer do so.</li>

<li>The <code>rebalance pgroup</code> command

of <code>poolmanager</code> no longer accepts <em>sc</em> as a value

for the <code>-metric</code> option; <em>free</em> has been added

instead.</li>

<p>The migration module no longer recognizes the

<em>source.spaceCost</em> and <em>target.spaceCost</em> variables, and

it no longer accepts <em>best</em> as a value for the

<code>-select</code> option.</p>

</ul>



<h3>Performance cost</h3>



<p>For <code>wass</code> partitions, the algorithm for computing a

performance cost has been modified. The performance cost is used for

read pool selection.</p>



<p>In previous versions, tape queues (both flush and stage) have

contributed to the performance cost the same way as any other mover

queues. However, often the number of active flush and stage jobs on a

pool have no relationship with the actual load incurred by these jobs:

They only indicate how many concurrent instances of the HSM script to

create, while the number of streams to and from disk is controlled by

the number of tape drives available. Moreover, the number of queued

flush jobs is misleading, as the pool has several flush queues not

taken into account when computing the performance cost.</p>



<p>The cost calculation has been changed so that the maximum number of

active HSM jobs no longer influences the algorithm. Instead, an HSM

queue contributes with the cost 1 - 0.75^n, where n is the number of

active jobs, unless the queue has queued jobs, in which case the

contribution is 1.0. The final performance cost is the average of the

contribution of each queue.</p>



<p><span class="label label-default">NOTE</span> The performance cost

is only used for read pool selection. For write pool selection

(including which pool to stage a file to), the weighted available

space selection algorithm is used.</p>



<h3>Write pools</h3>



<p>Error messages for when no write pools are found for a transfer

have been improved. For FTP, these errors are now classified into

transient and permanent errors with an appropriate error code.</p>



<h3>Space management</h3>



<p>dCache supports SRM style space reservations through the use of the

<code>spacemanager</code> service. This service has undergone almost a

complete rewrite. The new version should scale better, be easier to

use, and require less space in the database. Extensive changes have

been made to the admin shell interface and the configuration

properties of space manager. Please consult the build

in <code>help</code> output and

the <code>spacemanger.properties</code> file for details. The admin

shell commands accept a great many options that alter their behavior,

so make sure to read the help output offered by each of them. The new

commands no longer expose the auto-generated link group id and file id

database keys. Instead link groups are identified by their name, and

files by their PNFS ID or path.</p>



<p>Third party scripts accessing the database directly will have to be

updated due to the extensive schema changes. The same goes for scripts

accessing the admin shell interface, since the space manager commands

and their output have been changed.</p>



<p>Despite the extensive changes, the basic concepts of space

reservations in dCache have not changed much. The most important

change is to how uploads outside space reservations interact with the

space manager service. To understand these changes we first have to

recall how space reservations are supported in dCache.</p>



<p>The set of pools in dCache is partitioned into non-overlapping link

groups. Each link group is a collection of one or more links, and the

pools accessible through those links provide the space of the link

group. This space is managed by space manager. When pool manager is

asked to select a write pool, it will either select among the links

that are not in any link group (unmanaged space) or among the links

within a particular link group (managed space). Space reservations are

created within link groups. <em>Link group capabilities</em>

and <em>link group authorization</em> control in which link group a

particular reservation can be made and who can make it. Reservations

created by the administrator are typically placed explicitly in a link

group, while reservations made by end users through SRM are matched to

link groups by space reservation parameters and the identity of the

user.</p>



<p>When files are uploaded to an existing reservation, either by

explicitly specifying the reservation as part of an SRM upload, or by

binding the directory to a reservation using the <em>WriteToken</em>

directory tag, the space manager can lookup the appropriate link group

from the reservation and inject that into the write pool selection

request before handing it over to pool manager. This way the file

will be written to the pools on which the space was reserved.</p>



<p>The above applies equally to dCache 2.6 and 2.10. What has changed

is how space manager deals with files that are not uploaded to an

existing reservation. In dCache 2.6 two configuration properties

controlled what would happen: The SRM could be configured to create a

reservation on the fly prior to the upload. Once this implicit

reservation was created, the rest of the upload would be as if done to

an existing reservation. The other option was to configure space

manager to do the same for non-SRM transfers. The reason for this

apparent duplication in functionality boiled down to implementation

details of the SRM service. Worse though was that enabling either

option prevented uploads to the unmanaged space (the links not in any

link groups). Thus enabling implicit reservation in SRM forced all SRM

uploads to go into a link group. Similarly, enabling this option for

space manager forced all non-SRM uploads to go into a link

group. Transfers that would have succeeded with these options disabled

could fail when enabling them.</p>



<p>The above problem has been resolved: There is now just a single

property in

spacemanager, <code>spacemanager.enable.unreserved-uploads-to-linkgroups</code>,

which controls the behavior for both SRM and non-SRM uploads. When

uploading a file outside any existing reservation, enabling this

property causes space manager to attempt to create a temporary

reservation for this file. If successful, the upload proceeds as if

this was a normal reservation. In case no such temporary reservation

can be made (either because the file cannot be served by any links in

link groups, or because the user isn't authorized to write to those

link groups), space manager falls back to using unmanaged space.</p>



<p>A related change is that only permanent reservations are published

by the info service and the webadmin. This prevents that time limited

(often implicit or short-lived) reservations bloat the output.</p>





<h2>Nearline storage</h2>



<p>The interface to nearline storage (tapes) has been

rewritten. Nearline storages are now supported through drivers. These

drivers can be packaged and shipped as dCache plugins. A driver that

supports the classic HSM scripts is shipped with dCache and will be

used by default for existing setups.</p>



<p>Nearline storage drivers solve many issues of classic HSM

scripts:</p>



<ul>

<li><p>A callout to an external script for every invocation was a

performance issue, as such a callout to an external interpreter was

associated with considerable overhead.</p></li>

<li><p>A callout to an external script was a tape efficiency issue, as it

would limit the number of concurrent callouts due to allocating a

process and four Java threads for every file. Thus one had to

balance how many processes and threads the host could handle with

how large batches one could submit to the tape system.</p></li>

<li><p>The stage queue was limited to available disk capacity, as the pool

had to reserve space for the file before calling the script. Thus the

tape reordering queue was limited by disk space.</p></li>

</ul>



<p>A nearline storage driver is written in a JVM-supported language

(for example, Java, Scala or Groovy) and is executed within

dCache. This avoids the overhead of calling out to an external

script. Request queuing is dealt with by the driver, which allows the

driver to reorder requests in a way that optimizes tape access.</p>



<p>Since nearline storage request queuing is no longer part of dCache,

the maximum active requests limits are no longer reported to

<code>poolmanager</code>. For some drivers, such a limit may not even

exist. Pool selection has been updated to no longer rely on these

values.</p>



<p>The <code>st</code>, <code>rh</code>, and <code>hsm</code> family

of commands in the <code>pool</code> service have been updated. The

nearline driver is specified when defining a new nearline storage. The

new <code>hsm create</code> command is used to define the nearline

storage, while the <code>hsm set</code> command has been updated to

allow the driver to be configured.</p>





<span class="badge">Default</span>

<h4>script driver</h4>



<p>dCache ships with a driver called <code>script</code>. This driver performs a

callout to the classic HSM integration script. The driver accepts a

number of arguments, settable through the <code>hsm set</code> command:</p>

<dl class="dl-horizontal">

<dt>-command</dt>

<dd>The path to the script.</dd>



<dt>-c:gets</dt>

<dd>Maximum number of concurrent reads.</dd>



<dt>-c:puts</dt>

<dd>Maximum number of concurrent writes.</dd>



<dt>-c:removes</dt>

<dd>Maximum number of concurrent removes.</dd>

</dl>



<p>To provide backwards compatibility with existing setups, the <code>script</code>

driver is the default. During initialization, the <code>rh set max active</code>,

<code>st set max active</code> and <code>rm set max active</code> commands are translated to

configuration parameters for instances of the <code>script</code> driver. Support

for these commands is however deprecated and it is recommended that

the pool setup file is regenerated using the <code>save</code> command.</p>




<h4>copy driver</h4>



<p>The <code>copy</code> driver is similar to the classic <code>hsmcp</code> script. It copies

files between the pool and some other directory. It accepts a single

configuration property:</p>

<dl class="dl-horizontal">

<dt>-directory</dt>

<dd>The path of the directory into which files are copied.</dd>

</dl>



<h4>link driver</h4>



<p>Similar to the <code>copy</code> driver, but creates hard links rather than

copying files. The directory in which hard links are created must be

on the same file system as the pool’s data directory. Like the <code>copy</code>

driver, the <code>link</code> driver only accepts a single configuration property:</p>

<dl class="dl-horizontal">

<dt>-directory</dt>

<dd>The path of the directory within which hard links are created.</dd>

</dl>


<h4>tar driver</h4>



<p>This is an experimental driver, provided mostly as a demonstration

right now. The driver bundles files into tarballs and stores those in

a configurable directory. The driver does currently not support

removing files.</p>

<dl class="dl-horizontal">

<dt>-directory</dt>

<dd>The path of the directory within which tarball files are created.</dd>

</dl>




<p>The HSM cleaner is enabled by default. It used to be disabled by

default because traditionally PNFS setups all had custom solutions for

how to remove files from tape. Now that cleaning from tape is an

integral part of dCache and PNFS is no longer supported, having the

HSM cleaner work out of the box is a sensible default. It can be

disabled by setting:</p>



<pre>cleaner.enable.hsm = false</pre>





<h2>IPv6</h2>



<p>dCache enables IPv6 by default. It still prefers to use IPv4

addresses on dual-stack machines (those with both IPv4 and IPv6

addresses) so the impact should be minor. The change implies that

services will now also listen on IPv6 interfaces. To disable this,

define</p>



<pre>dcache.java.options.extra=-Djava.net.preferIPv4Stack=true</pre>



<p>FTP Extensions for IPv6 (RFC 2428) have been implemented. These

extensions are incompatible with GridFTP v2. To allow IPv6 FTP

transfers to be redirected to pools, support for Globus delayed

passive has been added. This is an alternative to using GridFTP v2

GETPUT. Delayed passive allows the data channel to be created directly

between the client and the pool. In contrast to GridFTP v2, delayed

passive supports IPv6. Note that current clients often default to

disabling delayed passive, even when delayed passive is

implemented. Without delayed passive, connecting with IPv6 will cause

the data channel to be proxied by the door.</p>



<p>If the client connects to the door using IPv4 and the pool does not

support IPv4, then the data channel is proxied through the

door. Similarly, if the client connects to the door using IPv6 and the

pool does not support IPv6, then the data channel is proxied through

the door. This is the case even when the client is dual stacked. Like

with GridFTP v2, use of direct data channels is subject to

the <code>ftp.proxy.on-passive</code>

and <code>ftp.proxy.on-active</code> properties.</p>



<p>RFC 2428 is only supported on IPv6 connections. When clients

connect over IPv4 we pretend not to support the IPv6 extensions. This

is to avoid that IPv4 clients supporting RFC 2428 cause unnecessary

proxying of the data channel.</p>







<h2>NFS</h2>



<h3>NFS 4.0</h3>



<p>Added support for NFS v4.0. Note that there is no parallel NFS

(pNFS) extension for NFS v4.0; therefore, the NFS door will act as a

proxy. This means that all data will flow through the door for

clients using NFS v4.0.</p>



<h3>dot commands</h3>



<p>dot-commands are special file names that when opened trigger an

action in dCache. These are used to access additional meta data and

interact with dCache. dCache NFS supports dot commands. Most of these

date back all the way to PNFS (the predecessor of Chimera), but a few

new dot commands have been added in this release.</p>





<h4>.(get)(<em>filename</em>)(checksum)</h4>



<p>Retrieves all stored checksums for a file. The command takes the

forms <code>.(get)(<em>filename</em>)(checksum)</code>

or <code>.(get)(<em>filename</em>)(checksums)</code>, and both return

a comma-delimited list of <code>type:value</code> pairs for all

checksums stored in the Chimera database.</p>



<pre class="prettyprint">

$ cat '.(get)(dcache_2.6.5~SNAPSHOT-ndgf6_all.deb)(checksum)'

ADLER32:3046b37d

</pre>





<h4>.(fset)(<em>filename</em>)(pin)(<em>duration</em>)</h4>



<p>Pins or unpins a file. Files which are not on disk will be staged

when pinned. The command takes the

form <code>.(fset)(<em>filename</em>)(pin<em>|</em>stage<em>|</em>bringonline)(<em>duration</em>)<em>[</em>(SECONDS<em>|</em>MINUTES<em>|</em>HOURS<em>|</em>DAYS)<em>]</em></code>.</p>



<p>The variants of the third argument are equivalent in effect. The

last argument is optional and defaults to <code>SECONDS</code>. A

duration value of <code>0</code> will unpin the file. The command does

not allow the user to pin the file indefinitely as the duration value

must be a positive integer.</p>



<pre class=="prettyprint">

$ touch '.(fset)(dcache_2.6.5~SNAPSHOT-ndgf6_all.deb)(pin)(60)'

$ cat '.(id)(dcache_2.6.5~SNAPSHOT-ndgf6_all.deb)'

00001E687A901C16407AB6DBD5F8FF7DF95B

$ ssh -p 22224 -l admin localhost



dCache Admin (VII) (user=admin)





[dcache] (local) admin > cd PinManager

[dcache] (PinManager) admin > ls 00001E687A901C16407AB6DBD5F8FF7DF95B

[32460414] 00001E687A901C16407AB6DBD5F8FF7DF95B by 0:0 2014-10-23 11:21:52 to 2014-10-23 11:22:52 is PINNED on pool1:PinManager-3e734bfc-4276-4395-85a8-76fa7ac1757e

total 1

</pre>




<h3>Export options</h3>



<p>The dCache NFS door exports file systems per the directives in

the <code>/etc/exports</code>. A couple of new options for use in this

file have been introduced.</p>







<h4>all_squash</h4>

<p>Added support for <code>all_squash</code> export option, e.q. all

users are mapped to nobody.</p>





<h4>dcap and no_dcap</h4>



<p>Added new export options <code>dcap</code>

and <code>no_dcap</code>. The former is the default while the latter

hides the <code>.(get)(cursor)</code> dot command that DCAP clients

use to detect an NFS-mounted dCache. Using <code>no_dcap</code> will

force DCAP clients to read data through NFS instead of through

DCAP.</p>







<h3>Attribute caching</h3>



<p>Server side attribute caching drastically improves performance for

some workloads. Three new attributes have been added to configure the

cache: <code>nfs.namespace-cache.time</code>, <code>nfs.namespace-cache.time.unit</code>

and

<code>nfs.namespace-cache.size</code>.</p>



<h3>Pool resets</h3>



<p>The <code>pool reset id</code> command has been added to

the <code>nfs</code> door to reset pool’s device id. This command is

used to recover from unknown failures: the Linux kernel may choose to

ban a pool (due to some real or imagined protocol violation) and send

IO through the <code>nfs</code> door. This command allows the door to

simulate a pool being rebooted, triggering the client to reassess its

opinion of the pool.</p>



<h2>FTP</h2>



<h3>Control channel</h3>



<p>Added support for the <code>CREATE</code>, <code>UNIX.ctime</code>

and <code>UNIX.atime</code> facts for the <code>MLSD</code>

and <code>MLST</code> commands

(see <a href="https://www.ietf.org/rfc/rfc3659.txt">RFC 3659</a>).</p>



<p>Improved compatibility with the ncftp client by adding a leading zero

to the value of the <code>mode</code> fact.</p>



<p>Added support for the <code>MFMT</code>, <code>MFCT</code>

and <code>MFF</code> commands as described in

this <a href="http://tools.ietf.org/html/draft-somers-ftp-mfxx-04">internet

draft</a> to modify facts.</p>



<p>Added support for the <code>HELP</code> and <code>SITE HELP</code>

commands as defined

in <a href="https://www.ietf.org/rfc/rfc959.txt">RFC 959</a>. This

improves compatibility with some clients.</p>



<h3>Data channel</h3>



<p>The listening socket of a passive FTP data channel is now bound to

a single address rather than the wildcard address. The FTP protocol

only allows a single address to be returned to the client, so there is

no point in binding to the wildcard address. Binding to the wildcard

address had the problem that it could succeed even if the port on the

specific address returned to the client was already open. The change

does have observable effects in that previously the pool would submit

a hostname back to the door and the door would do a DNS lookup to find

the address to send to the client. Now the pool sends an IP

address.</p>





<h3>Configuration</h3>



<p>dCache user accounts can be configured with a personal root and home

directory. How these are interpreted depends on the door and protocol

used. For FTP, the account root directory forms the root of the name

space and the home directory is the initial directory of the FTP

session. For other doors, a configuration property usually defines a

directory to export as the root of that door, and the account root

directory is used as an additional authorization check to prevent

users from accessing any directory outside their root. This behavior

is now configurable for the FTP door using the new <code>ftp.root</code>

property. If left empty, the per account root is used as before. If

set to a path, that path is exported as the root of the door.</p>



<h2 id="service:webdav">HTTP/WebDAV</h2>



<h3>Proxy mode</h3>



<p>The webdav door allows uploads and downloads to be proxied through

the door as an alternative to redirecting the client to the pool. For

download we have used HTTP for the transfer between the door and the

pool, but for upload we used an FTP data channel. We did this because

originally the HTTP mover did not support upload. This has now been

changed such that proxied HTTP upload also uses HTTP between the door

and the pool. The primary admin visible change is that the TCP

connection is created from the door to the pool rather than from the

pool to the door. The configuration property

<code>webdav.net.internal</code> is now used as a hint for the pool to

select an interface facing the door. The property is respected by both

proxied downloads and proxied uploads.</p>



<h3>WebDAV properties</h3>



<p>Limited support for WebDAV properties has been implemented. WebDAV

provides an extensible mechanism for reporting additional meta data

about files and directories. These are known as properties and can

be queried through the PROPFIND HTTP method - the same mechanism used

to list WebDAV collection resources (directories in dCache). Currently

only support for checksums, access latency and retention policy is

provided.</p>



<p>An example follows.</p>



<pre class="prettyprint lang-xml">$ curl -X PROPFIND -H Depth:0 http://localhost:2880/public/test-1390395373-1 \

--data '&lt;?xml version="1.0" encoding="utf-8"?&gt;

&lt;D:propfind xmlns:D="DAV:"&gt;

&lt;D:prop xmlns:R="http://www.dcache.org/2013/webdav"

xmlns:S="http://srm.lbl.gov/StorageResourceManager"&gt;

&lt;R:Checksums/&gt;

&lt;S:AccessLatency/&gt;

&lt;S:RetentionPolicy/&gt;

&lt;/D:prop&gt;

&lt;/D:propfind&gt;'



&lt;?xml version="1.0" encoding="utf-8" ?&gt;

&lt;d:multistatus xmlns:cs="http://calendarserver.org/ns/" xmlns:d="DAV:" xmlns:cal="urn:ietf:params:xml:ns:caldav" xmlns:ns1="http://srm.lbl.gov/StorageResourceManager" xmlns:ns2="http://www.dcache.org/2013/webdav" xmlns:card="urn:ietf:params:xml:ns:carddav"&gt;

&lt;d:response&gt;

&lt;d:href&gt;/public/test-1390395373-1&lt;/d:href&gt;

&lt;d:propstat&gt;

&lt;d:prop&gt;

&lt;ns1:AccessLatency&gt;ONLINE&lt;/ns1:AccessLatency&gt;

&lt;ns2:Checksums&gt;adler32=6096c965&lt;/ns2:Checksums&gt;

&lt;ns1:RetentionPolicy&gt;REPLICA&lt;/ns1:RetentionPolicy&gt;

&lt;/d:prop&gt;

&lt;d:status&gt;HTTP/1.1 200 OK&lt;/d:status&gt;

&lt;/d:propstat&gt;

&lt;/d:response&gt;

&lt;/d:multistatus&gt;

</pre>



<h3>HTML styling</h3>



<p>The default HTML rendering of directory listings and error messages

has been updated to use the Bootstrap framework, which supports a rich

set of features. This new default provides a deliberately toned-down

presentation. The default page now contains two links for each file:

one that hints the browser should show the content and the other that

the browser should download the file. As before, admins may customize

the rendering of directory listings and error messages. To support

clients with poor or no Internet connection, all required JavaScript

libraries and Bootstrap files for the default layout are included with

dCache.</p>



<img class="img-responsive" src="webdav.png"/>



<h3>WLCG federated HTTP</h3>



<p>Support for WLCG federated HTTP transfers has been added. This allows

the webdav door to redirect a client to another replica if a local

copy was not found. Support for this relies on special URLs generated

by a central catalogue service. For all other URLs the behavior is

unchanged.</p>



<h3>Third-party transfers</h3>



<p>dCache v2.10 sees greatly improved support for HTTP third-party

transfers. These are transfers between dCache and some other HTTP

server, so that the traffic does not go through the client.</p>



<p>In keeping with gsiftp, http third-party transfers are initiated on

the pool. dCache supports both pull and push transfers. A pull

transfer is where the pool fetches a file from the remote server using

the HTTP GET method. A push request is where the pool uploads a file

to the remote server using the HTTP PUT method.</p>



<p>A transfer can use either an unencrypted transport (<code>http://...</code>) or

make use of SSL/TLS encryption (<code>https://...</code>). If an SSL/TLS

transport is used then the pool can use an X.509 credential when

establishing the SSL/TLS connection.</p>



<p>Both transfer directions (push and pull) will attempt to check the

integrity of the transferred data. For pull requests, all data

integrity information comes from the headers supplied in the GET

response. For push requests, the pool will make a subsequent HEAD

request and use the supplied information to verify the data was sent

correctly.</p>



<p>For push requests, if a PUT request is successful but the subsequent

HEAD request reveals data corruption then the pool will attempt to

delete the file with an HTTP DELETE request. If this DELETE fails

then the error message is updated accordingly. For pull requests, no

additional cleanup steps are needed.</p>



<p>File checksum values are discovered via the RFC 3230 extension to

HTTP. Unfortunately, this is not widely supported by HTTP servers;

therefore, dCache supports two levels of data integrity checking: weak

and strong. Weak data integrity is satisfied when</p>



<ul>

<li><p>the remote service and the dCache server agree on the content

length,</p></li>

<li><p>none of the checksums supplied by the remote server (if any)

disagree with the checksums known by dCache.</p></li>

</ul>



<p>Strong data integrity is satisfied when, in addition to satisfying the

weak conditions:</p>



<ul>

<li>there is at least one checksum supplied by the remote server that

agrees with a dCache-local checksum.</li>

</ul>



<p>Weak data integrity can be satisfied by any HTTP server whereas

strong data integrity requires an HTTP server with RFC 3230 support. A

transfer satisfying weak integrity might not check that the checksum

values match; strong integrity requires that checksums exist and

match.</p>



<p>Third-party HTTP transfers also allow the client to specify zero or

more (arbitrary) headers when requesting a file to be transferred. This

allows the client to customize the HTTP request the pool sends to the

remote server. Such headers could include authorization information

or some other information to steer how the remote server handles the

HTTP request.</p>



<p>Third-party transfers may be initiated by the <code>webdav</code> service and the

<code>srm</code> service. See the following sections on those services

for details on how to trigger third-party copying.</p>



<h4>HTTP third-party transfers using WebDAV COPY</h4>



<p>The <code>webdav</code> door supports requesting third-party file

transfers. This is an extension to the WebDAV COPY command, which is

normally limited to internal copies. A client may request a file be

transferred to a remote site by specifying the remote location as the

<code>Destination</code> HTTP request header. Currently supported transports are

GridFTP (destination URI starts <code>gsiftp://</code>) and HTTP. For HTTP both

plain (<code>http://</code>) and with SSL/TLS (<code>https://</code>) are supported.</p>



<p>The <code>Credential</code> HTTP request header may be used by the client to

describe whether or not the pool should use a delegated credential

when transferring the file. The accepted values are <code>none</code> and

<code>gridsite</code>. If <code>none</code> then no credential is to be used; if <code>gridsite</code>

then a delegated credential is to be used. If the <code>Credential</code> header

isn’t specified then a transport-specific default is used: for gsiftp

and https transports the default is <code>gridsite</code>; for http transport the

default is <code>none</code>. Some combinations are not supported: gsiftp with

<code>none</code> and http with <code>gridsite</code> are not supported.</p>



<p>If a delegated credential is to be used, the client must delegate a

credential to dCache using the delegation service, which is part of

the srm service. If no useful certificate could be found, the webdav

door will redirect the client to itself and include the

<code>X-Delegate-To</code> HTTP header in its response. This header contains a

space-separated list of delegation endpoints.</p>



<p>For HTTP and HTTPS transfers, the client may choose whether to

require weak or strong verification; see above for a definition of

these. The <code>RequireChecksumVerification</code> header controls

this behavior; if this header has a value <code>true</code>, strong

verification is required. If <code>false</code>, weak verification is

sufficient. If the header is not specified, a configurable default

value is used.</p>



<p>Again, for HTTP and HTTPS transfers, the client may specify

additional or replacement HTTP headers that the pool should use when

making the transfer. These are specified as headers that start

<code>TransferHeader</code>. This prefix is removed and the header used by the

pool. For example, to have the pool use basic authentication with

userid ‘Aladdin’ and password ‘open sesame’, the client would add the

following header to its request:</p>



<pre>TransferHeaderAuthentication: Basic QWxhZGRpbjpvcGVuIHNlc2FtZQ==</pre>



<p>Once the transfer is accepted, the client will receive periodic

progress information. If the client closes the TCP connection, the

transfer is canceled.</p>



<pre class="prettyprint lang-xml">

> curl -L -E "Gerd Behrmann" -k -X COPY -H Destination:https://localhost:2881/disk/foobar https://127.0.0.1:2881/disk/test-1414149424-1

&lt;html&gt;

&lt;head&gt;

&lt;meta http-equiv="Content-Type" content="text/html;charset=ISO-8859-1"/&gt;

&lt;title&gt;Error 401 &lt;/title&gt;

&lt;/head&gt;

&lt;body&gt;

&lt;h2&gt;HTTP ERROR: 401&lt;/h2&gt;

&lt;p&gt;Problem accessing /disk/test-1414149424-1. Reason:

&lt;pre&gt; client failed to delegate a credential&lt;/pre&gt;&lt;/p&gt;

&lt;hr /&gt;&lt;i&gt;&lt;small&gt;Powered by Jetty://&lt;/small&gt;&lt;/i&gt;

&lt;/body&gt;

&lt;/html&gt;



> delegation

Type 'help' for help on commands.

Type 'exit' or Ctrl+D to exit.

$ endpoint srm://localhost

[srm://localhost] $ delegate

Generated certificate expire Fri Oct 24 22:10:37 CEST 2014

Delegated credential has id 6BBBD539A5D5206861EEB1C0D9123C9FDA94E32A



> curl -L -E "Gerd Behrmann" -k -X COPY -H Destination:https://localhost:2882/disk/foobar https://127.0.0.1:2882/disk/test-1414149424-1

Perf Marker

Timestamp: 1414153228

State: 1

State description: querying file metadata

Stripe Index: 0

Total Stripe Count: 1

End

success: Created

</pre>





<h4>HTTP third-party transfers using SRM</h4>



<p>The <code>srm</code> service supports http and https transfers in

both pull (dCache pool makes an HTTP GET request) and pull (pool makes

an HTTP PUT request) operations. The SRM client can steer the transfer

by supplying ExtraInfo arguments. The ExtraInfo arguments are a set of

arbitrary key-value pairs that the client can specify when making the

request. The currently supported ExtraInfo keys are:</p>



<ul>

<li><code>verified</code> If set, takes a value of

either <code>true</code> or <code>false</code>. This controls whether

weak or strong verification is required. If set to false then weakly

verified transfers are successful. If set to true then a transfer must

be strongly verified to be successful.</li>

<li><code>header-</code>. All ExtraInfo elements that

start <code>header-</code> are converted into HTTP headers. The HTTP

header key is the ExtraInfo key without the

initial <code>header-</code>. The HTTP header value is the ExtraInfo

value. These HTTP headers are used when the pool makes a request.</li>

</ul>



<p>If the SRM client delegates a credential as part of the GSI

connection, this credential is used to authenticate when the pool

makes an SSL/TLS-based connection to the remote server. If the client

doesn’t delegate then dCache will attempt the transfer without any

client credential.</p>



<pre class="prettyprint">

$ srmcp -delegate srm://127.0.0.1/disk/test-1414149424-1 https://localhost:2882/disk/foobar2

$ srmls srm://localhost/disk/foobar2

628736 /disk/foobar2

</pre>



<h2>SRM</h2>



<p>The <code>srm</code> service has been heavily refactored, providing

improved persistence, standard compliance, logging, and robustness.</p>







<h3>Persistence</h3>



<p>Persistence of SRM requests to the database has been improved. The

consequence is that SRM database throughput should be much higher than

in earlier versions. Loading requests back from the database during

startup is faster, and the risk of database queue overflows should be

reduced. In particular when request history persistence is enabled, the

<code>srm</code> performs better than in earlier versions. We

recommend enabling request history persistence, as it makes it easier

to debug transfer issues.</p>



<p>Bring-online requests, as well as get and put requests for which a

transfer URL (TURL) was already prepared now survive an <code>srm</code>

restart.</p>



<h3>Absolute FTP TURLs</h3>



<p>The SRM protocol allows the client to negotiate a transfer URL

(TURL) for uploading or downloading a file. URLs for FTP transfers

are defined in <a href="http://www.ietf.org/rfc/rfc1738.txt">RFC

1738</a>. According to the standard, they are to be interpreted

relative to the user’s login directory (home directory) and not

relative to the root directory.</p>



<p>The <code>srm</code> service in previous versions of dCache

generated TURLs relative to the root directory. This will not work as

expected for RFC 1738-compliant clients if the user has a home

directory other than <code>/</code>.</p>



<p>This problem has now been fixed and the returned TURL will work for

users with a non-root home directory. Unfortunately neither JGlobus

nor Globus interpret RFC 1738 correctly. As a workaround we now

generate TURLs with an extra leading <code>/</code> in the path. This

provides the correct behavior with FTP clients typically used for SRM,

but would fail if a strictly standard compliant client would be

used.</p>



<h3>Protocol negotiation</h3>



<p>When negotiating a TURL, the <code>srm</code> service must choose

from a list of protocols provided by the client. dCache will use the

list of doors registered with a <code>loginbroker</code> to determine

the supported protocols.</p>



<p><code>loginbroker</code> now supports registering the root

directory of doors. As a consequence, <code>srm</code> no longer needs

to be configured with the root paths of each door and the

properties <code>srm.service.webdav.root</code> and

<code>srm.service.xrootd.root</code> are obsolete.</p>



<p>If doors are configured to use different root directories,

not all doors may be able to serve a file. This is now taken into

account when choosing the transfer protocol and door to use.</p>



<h3 id="unique-turls">Unique write TURLs</h3>



<p>In earlier versions, the dCache <code>srm</code> door has acted as

a redirector for regular dCache doors. This means that TURLs generated

by the <code>srm</code> service have been the same URLs you would have

used to access those files without SRM.</p>



<p>This has changed and for uploads each TURL is now unique. The

uploaded file remains invisible to users using non-SRM protocols until

the upload is committed by the SRM client

calling <code>srmPutDone</code>.</p>



<p>SRM upload requests have a finite lifetime; if the SRM client does

not call <code>srmPutDone</code> in time, the request will

timeout. Should this happen, any file uploaded using the corresponding

TURL will be deleted and any subsequent attempt to upload to the TURL

will fail.</p>



<p>There are many reasons for making this change. To name a few:</p>



<ul>

<li>The expected file size, access latency and retention policy provided

by the SRM client could not be supported without enabling the

<code>spacemanager</code> service. These parameters are now respected

even without space management.</li>

<li>Failure recovery was difficult, as dCache could never be certain

whether a file uploaded through a door happened as part of the SRM

upload or was done by another non-SRM client that incidentally

uploaded a file to the same path at the same time.</li>

<li>If an SRM upload was aborted and retried, we could not prevent the

first client from completing the second upload as we always generated

the same TURL. Thus we couldn’t properly isolate the two uploads from

each other.</li>

<li>Since the only way to bind file size, space token, access latency

and retention policy to a file before upload was through the

<code>spacemanager</code> service, space reservations were bound to

paths. Such reservations would prevent the <code>srm</code> from

creating concurrent uploads to the same SURL, but to work correctly,

the two services had to agree on the state. Wherever there is

distributed state, there is a risk that the state is

inconsistent. This problem was at the heart of the <em>“Already have

1 record(s)”</em> errors.</li>

</ul>



<p>To generate unique write TURLs, the <code>srm</code> creates a

unique upload directory for each upload. After the transfer completes,

the file is moved to the target path and the upload directory is

deleted. Parameters like expected file size, access latency, retention

policy and space token are bound to the directory using Chimera

directory tags.</p>



<p>In rare cases, typically if dCache components are restarted or get

disconnected, upload directories may be orphaned. Currently, the

administrator has to manually delete such directories.</p>



<p>By default, these temporary upload directories are created under the

<code>/upload</code> directory. Chimera automatically creates this

directory the first time it is needed. Ownership and permissions are

set such that nobody can list the directory and thus nobody can

discover the temporary upload directories.</p>



<p><span class="label label-warning">IMPORTANT</span> If the transfer

doors used for <code>srm</code> do no export the

<code>/upload</code> directory the upload will fail. In the following

we describe several solutions to this problem, in order of

preference.</p>






<h4>Define an explicit FTP root</h4>



<p>By default, FTP doors only expose the root directory of the account

of the user. If accounts have different root directories, one cannot

define a common directory visible through FTP for all users. One

solution is to change the behavior of the FTP doors to expose a fixed

directory as their root. The FTP door would still only allow access to

files under the root directory of the account, or within the upload

directory.</p>



<pre>

[domain]

[domain/pnfsmanager]

[domain/ftp]

ftp.authn.protocol = gsi

ftp.root = /

[domain/srm]

</pre>





<h4>Define a different upload directory</h4>



<p>In case doors already expose a common root directory that just

happens to be different from <code>/</code>, the solution is to alter

the <code>dcache.upload-directory</code> to a path that is exported by

all doors. A typical site value would

be <code>/pnfs/example.org/data/upload</code>. This property has to be

set for <code>pnfsmanger</code> and all doors used for SRM

transfers.</p>



<pre>

dcache.upload-directory = /pnfs/example.org/data/upload



[domain]

[domain/pnfsmanager]



[domain/ftp]

ftp.authn.protocol = gsi

ftp.root = /pnfs/example.org/data



[domain/webdav]

webdav.authn.protocol = https-jglobus

webdav.root = /pnfs/example.org/data



[domain/srm]

srm.root = /pnfs/example.org/data

</pre>







<h4>Define extra doors for SRM to use</h4>



<p>In the case that you cannot find a directory visible through all

doors used by the <code>srm</code>, you can introduce special door

instances only used for SRM transfers. Such doors can be configured to

only export the upload base directory. This approach works both when

the different root paths are defined per door and per user.</p>



<pre>

[domain]

[domain/pnfsmanager]



[domain/ftp]

ftp.authn.protocol = gsi

ftp.root = /pnfs/example.org/data/foo



[domain/ftp]

ftp.cell.name = FTP-SRM-${host.name}

ftp.net.port = 2812

ftp.authn.protocol = gsi

ftp.root = ${dcache.upload-directory}



[domain/srm]

</pre>



<p>This duplication is only necessary for protocols that do not expose

the upload directory already (typically FTP).</p>




<h4>Define per user upload directories</h4>



<p>The final solution is to specify a relative upload path, in which

case it is interpreted to be relative to the account root

directory. Assuming that the users' root directory are exposed through

all doors, these relative directories will all be exposed too.</p>



<pre>

dcache.upload-directory = upload



[domain]

[domain/pnfsmanager]



[domain/ftp]

ftp.authn.protocol = gsi



[domain/webdav]

webdav.authn.protocol = https-jglobus



[domain/srm]

</pre>



<p>An account with root

directory <code>/pnfs/example.org/data/foobar</code> would then use

the upload

directory <code>/pnfs/example.org/data/foobar/upload</code>. The

downsides of this approach are:</p>



<ul>

<li>the upload directories may clash with existing directories;</li>

<li>the user may alter the permissions of the upload directory, thus

bypassing the protection that unique TURLs were supposed to introduce;

and</li>

<li>the upload directories are created in many different places,

making it more difficult to clean orphaned upload directories.</li>

</ul>



<h3>Scheduling</h3>



<p>dCache v2.10 sees a major overhaul in how the <code>srm</code>

controls and limits its interaction with other dCache services. The

following sections describe these changes.</p>



<h4>Background</h4>



<p>The SRM protocol has the concept of a client’s request not being

processed immediately, with the request being queued prior to any work

being conducted. This is most apparent for asynchronous requests,

where the client reconnects periodically to discover what progress, if

any, has taken place. The following also applies for synchronous

requests (where the client waits to learn the result of the query);

however, the client is oblivious of these details.</p>



<p>In general, a successful request will start out in

a <em>queued</em> state. After dCache starts processing the request,

the request will have an <em>in-progress</em> state. For transfer

requests (GET or PUT), the request will be in a <em>ready</em> state

when there is a TURL for the client to use, and in a <em>success</em>

state after a successful transfer. For non-transfer requests (LS,

BRING-ONLINE, …) the request will go into the <em>success</em> state

once dCache finishes processing it, skipping the <em>ready</em>

state.</p>



<p>To answer most client-issued requests, the srm service must trigger

some activity in other dCache services. For the most part, the srm

service simply issues requests to other services, collects the

responses and converts them into a corresponding SRM reply.</p>



<p>The <code>srm</code> service has several execution pools to

throttle processing of requests. These limits are applied to

individual files, so, for example, from a single request to read 10

files, each of the files is scheduled as if there were 10 requests,

each reading a single file.</p>



<p>Prior to dCache v2.10, the <code>srm</code> throttled itself by

limiting the number of requests it can process concurrently. Once this

limit is reached, additional requests are placed in a queue with a

limited capacity. Once this queue limit is reached, subsequent

requests are rejected. The effect is to throttle the frequency of

messages being sent.</p>



<p>In practice, a single thread could easily saturate the rest of

dCache, which meant that this was not a particularly effective way to

throttle the <code>srm</code> service.</p>



<p>Furthermore, the queue limits would also affect requests that had

already begun processing. Thus under high load, one could observe

requests being failed even if they had already started processing. At

least in theory, this could lead to a starvation problem, in which a

lot of processing could take place while no requests would ever

succeed.</p>



<h4>New approach</h4>



<p>Rather than rate-limiting the delivery of internal messages, dCache

v2.10 provides the ability to limit the number of requests in each of

the different states mentioned above (“queued”, “in-progress” and

“ready”). This is taking into account “in flight” requests.</p>



<p>There are now three types of limits: max-requests, max-inprogress

and max-transfers.</p>



<dl class="dl-horizontal">

<dt>max-requests</dt>

<dd>

<p>Controls the total number of requests that are queued or being

actively worked on. Once this limit is reached, any more requests from

an SRM client are rejected. The limit allows the <code>srm</code>

service to protect against running out of memory.</p>

<p>Setting a value too low will result in the srm not fully utilizing

the available memory; setting it too high will risk running out of

memory under heavy load.</p>

</dd>

<dt>max-inprogress</dt>

<dd>

<p>Controls the concurrent activity within dCache; once this limit is

reached, subsequent requests are either queued or rejected, depending

on the max-requests limit. This allows the srm service to stop itself

from overloading core dCache services when processing SRM

requests. The max-inprogress limit also controls the maximum number of

staging requests for GET and BRING-ONLINE requests. For COPY requests,

it sets the maximum number of current transfers.</p>

<p>Setting the value too low will result in the srm artificially

limiting its performance, as requests will needlessly spend time

queued. Setting the value too high will risk overloading core

components when the srm service is under heavy load.</p>

</dd>

<dt>max-transfers</dt>

<dd>

<p>Controls the number of TURLs handed out to clients. Once this limit

is reached, the srm keeps subsequent requests that have a TURL in

the <em>in-progress</em> state - at least from the point of view of

the client. Internally, such requests are in the <em>ready queued</em>

state and no longer count towards the max-inprogress limit. Once the

SRM client completes transfers, those requests that have a TURL but

are in the <em>ready queued</em> state can become <em>ready</em>. This

limit is mostly to allow dCache to protect pools by limiting the

number of concurrent transfers. It will also provide some protection

for the transfer doors (typically <code>ftp</code>)

and <code>poolmanager</code>.</p>

<p>Since this limit type affects only transfers, setting the value too

low will result in artificially poor transfer rates (with client

requests spending a large amount of time in the <em>in-progress</em>

state despite having a TURL) while other SRM requests are processed

quickly. Setting the value too high risks overloading pools when

dCache is under heavy load.</p>

</dd>

</dl>



<p>There are request-specific properties that may be configured for each

of these three types of limit. These have names like

<code>srm.request.TYPE.{max-requests,max-inprogress,max-transfers}</code>,

where <code>TYPE</code> is one of <code>get</code>, <code>put</code>,

<code>ls</code>, <code>bring-online</code>, <code>copy</code> or

<code>reserve-space</code>.</p>



<p>For example:</p>



<ul>

<li><code>srm.request.bring-online.max-inprogress</code> controls the maximum

number of concurrent staging requests.</li>

<li><code>srm.request.get.max-transfers</code> controls the maximum number of

concurrent downloads (maximum number of TURLs handed out at any

time).</li>

<li><code>srm.request.ls.max-requests</code> controls how many file metadata and

directory listing queries to allow (either actively being processed

or queued) before rejecting new requests.</li>

</ul>



<p>The max-requests limit properties (<code>srm.request.get.max-requests</code>,

<code>srm.requests.put.max-requests</code>, etc) all take a common default value

controlled by the <code>srm.request.max-requests</code> property. The current

default value for <code>srm.request.max-requests</code> is 10,000. Note that the

<code>srm.request.max-requests</code> value applies to each SRM request type

(GET, PUT, BRING-ONLINE, …) independently. Therefore, the overall

maximum number of requests is six times the configured value.</p>



<p>The max-inprogress properties (<code>srm.request.get.max-inprogress</code>,

<code>srm.request.put.max-inprogress</code>, etc.) all take individual default

values. The current default values are to allow concurrent processing

of 10,000 BRING-ONLINE requests, 1,000 GET and COPY requests, 50 PUT

requests, 50 LS requests, and 10 RESERVE-SPACE requests.</p>



<p>The two max-transfers properties (<code>srm.request.get.max-transfers</code> and

<code>srm.request.put.max-transfers</code>) take pre–2.10 srm configuration

properties as default values.</p>



<p>As with prior versions of dCache, if a request suffers a transitory

failure, the srm will retry the operation after waiting awhile. Prior

to 2.10, such retries were treated specially. With 2.10, the retry is

treated as if it were a fresh request, thus is subject to the three

limits described above.</p>



<h2>Monitoring</h2>



<h3>Info</h3>



<p>The info service, which collects and collates information from various

dCache components, now supports presenting the gathered data in

different formats. Previous versions of dCache only supported a

dCache-specific XML format. With dCache v2.10 two additional formats

are available.</p>



<p>There are two ways the client can choose the format. The HTTP

client can specify the MIME type as the <code>Accept</code> request

header; JSON-specific clients may do this automatically. The

alternative is to append <code>?format=_some_format_</code> to the

URI. There are four supported MIME types

(<code>application/xml</code>,

<code>text/xml</code>, <code>application/json</code> and

<code>text/x-ascii-art</code>) and three supported formats for

<code>?format=</code> (<code>xml</code>, <code>json</code>

and <code>pretty</code>). The default format continues to be XML.</p>



<p>Additional attributes have been added to

the <code>domain/&lt;domain-name&gt;/static</code> node, including

information on the OS and the JVM.</p>



<pre class="prettyprint">

$ curl -H Accept:application/json http://127.0.0.1:2288/info/domains/dCacheDomain/static

{

"java": {

"vendor": "Oracle Corporation",

"vm": {

"vendor": "Oracle Corporation",

"name": "Java HotSpot(TM) 64-Bit Server VM",

"version": "25.20-b23",

"specification-version": "1.8",

"info": "mixed mode"

},

"class-version": "52.0",

"runtime-version": "1.8.0_20-b26",

"version": "1.8.0_20",

"specification-version": "1.8"

},

"os": {

"name": "Mac OS X",

"arch": "x86_64",

"version": "10.10"

},

"user": {

"country": "US",

"timezone": "Europe/Copenhagen",

"name": "behrmann",

"language": "en"

}

}

</pre>



<h3>JMX</h3>



<p>JMX, the Java Management Extensions, is a standard for providing

monitoring and management interfaces in Java applications. Third party

JMX clients may connect to the application and extract runtime

information and interact with the application.</p>



<p>Many components in dCache now report statistics through

JMX. Caching and request execution can be monitored and may be flushed

or reset through JMX.</p>



<p>Several third party libraries used by dCache are accessible through

JMX.</p>





<h2>Pools</h2>



<p>Introduced the new property <code>pool.check-health-command</code>,

which enables a callout to an external health check

script. Set <code>pool.check-health-command</code>=<code>path/to/script</code>

to enable it. As the command is executed frequently, it should not

perform any expensive checks, nor should the check take longer than at

most a few seconds. If the exit code is 0, the pool is assumed to be

okay. If the exit code is 1, the pool is marked read-only. Any other

exit code will disable the pool.</p>



<p>Modified permanent migration jobs to react to access time and sticky

flag changes. Thus migration jobs that filter by access time or sticky

flags may now pick up files when access time or sticky flags change.</p>



<h2>Billing</h2>



<h3>Billing database</h3>



<p>Added the possibility to obtain statistics (printed to billing log

and pinboard) via the dcache admin command: <code>display insert

statistics &lt;on|off&gt;</code>.</p>



<p>Turning this command on logs the following once a minute:</p>



<pre>

insert queue (last 0, current 0, change 0/minute)

commits (last 0, current 0, change 0/minute)

dropped (last 0, current 0, change 0/minute)

total memory 505282560; free memory 482253512

</pre>



<p><em>insert queue</em> refers to how many messages actually were put on the

queue; <em>commits</em> are the number of messages committed to the database;

<em>dropped</em> are the number of lost messages; <em>last</em> refers

to the figures at the last iteration. For insert queue, this is the

actual size of the queue; for commits and dropped, these are

cumulative totals.</p>



<h3>Billing record formatting</h3>



<p>Fixed a bug in how configurable billing format strings for the

billing log files are parsed. As a consequence of this fix, the format

strings are pre-processed by the dCache configuration system,

including processing of escape sequences. You may have to update

custom format strings by replacing <code>$$</code> sequences

with <code>$$$$</code>.</p>



<p>Some of the information about a transfer is written as a

colon-separated list of items. In previous versions of dCache, the

protocol version and client hostname were not separated, resulting in

entries like:</p>



<pre>{Http-1.1zitpcx6184.desy.de...}</pre>



<p>With dCache v2.10, this has been fixed for the http and xrootd

transfers, so entries now are correctly separated:</p>



<pre>{Http-1.1:zitpcx6184.desy.de...}</pre>



<h3>Indexing and searching</h3>



<p>A script, <code>/usr/sbin/dcache-billing-indexer</code>, to index

and compress billing files was added. For the Debian package,

a <code>cron.daily</code> file has been added that invokes this script

with the <code>-yesterday -compress</code> options. This means that

for Debian packages we compress and index yesterdays billing

file. Existing billing files may be indexed using

the <code>-all</code> option. This works even if the files were

compressed using <code>bzip2</code>.</p>



<p>The <code>dcache</code> script has been extended with a new command

to search billing files, using the index if available. The command can

search by path or path prefix, PNFS ID, DN or DN prefix. The search

may be limited by date using the <code>--since</code>

and <code>--until</code> options. The output may be formatted

as <em>raw</em> (uses the billing formatting patterns), <em>json</em>,

or <em>yaml</em>.</p>



<p>The search tool will use available CPU cores to search multiple

billing files concurrently and is much faster than a

sequential <code>bzgrep</code> on the same files - in particular when

billing files have been indexed.</p>



<pre class="prettyprint">

$ dcache billing --format=json /disk/test-1414149424-2

[

{

"date": "2014-10-24T13:17:06+02",

"transferred": "628736",

"storage.storageClass": "test:disk",

"cellName": "pool_write",

"created": "true",

"initiator": "door:GFTP-Gerds-MacBook-Pro-2-103@dCacheDomain:1414149426231000-1414149426327000",

"filesize": "628736",

"type": "transfer",

"message": "",

"path": "/disk/test-1414149424-2",

"rc": "0",

"protocol": "GFtp-1.0 127.0.0.1 49933",

"cellType": "pool",

"storage.hsm": "osm",

"pnfsid": "0000F292031988494F11A20ACE81578F3C79",

"connectionTime": "591"

},

{

"date": "2014-10-24T13:17:07+02",

"owner": "/O=Grid/O=NorduGrid/OU=ndgf.org/CN=Gerd Behrmann",

"gid": "1000",

"storage.storageClass": "test:disk",

"cellName": "GFTP-Gerds-MacBook-Pro-2-103@dCacheDomain",

"filesize": "628736",

"type": "request",

"transactionTime": "693",

"message": "",

"uid": "501",

"path": "/disk/test-1414149424-2",

"rc": "0",

"cellType": "door",

"storage.hsm": "osm",

"queuingTime": "0",

"client": "127.0.0.1",

"pnfsid": "0000F292031988494F11A20ACE81578F3C79"

},

{

"date": "2014-10-24T13:17:07+02",

"storage.storageClass": "test:disk",

"cellName": "pool_write",

"filesize": "628736",

"type": "hit",

"message": "",

"path": "/disk/test-1414149424-2",

"rc": "0",

"protocol": "GFtp-1.0 127.0.0.1 20",

"cellType": "pool",

"storage.hsm": "osm",

"cached": "true",

"pnfsid": "0000F292031988494F11A20ACE81578F3C79"

}

]

</pre>



<h2 id="upgradeprocedure">Upgrade procedure</h2>



<ol>

<li><p>If you use SRM, update to the latest SRM client version

available.</p></li>

<li><p>Upgrade to the latest patch level release of the dCache

release series you use.</p></li>

<li><p>Prior to upgrading, if you are using the <code>classic</code>

partition type for any partition in pool manager, change it

to <code>wass</code> or <code>buffer</code> (depending on the

specific use-case). If you use non-default values for performance

cost factor or space cost factor, then we suggest resetting these to

1.0.</p></li>

<li><p>Prior to upgrading, if you are using the <code>wrandom</code>

partition type for any partition in pool manager, change it

to <code>wass</code>, using the settings:</p>

<pre>

breakeven = 0

gap = 0

performancecostfactor = 0

spacecostfactor = 1

p2p = 0

alert = 0

halt = 0

fallback = 0

slope = 0

idle = 0

</pre></li>

<li><p>Prior to upgrading, verify that SSH 2 login works for

your <code>admin</code> service. You will likely have to inject your

SSH 2 public key or define a user name and password in gPlazma with

GID 0.</p></li>

<li><p>Prior to upgrading, run <code>dcache check-config</code> and

fix any warnings. Information about properties marked deprecated,

obsolete or forbidden in version 2.6 or earlier has been dropped in

2.10. Failing to do this before upgrading will mean that you will not

receive warnings or errors for using an old property.</p></li>

<li><p>If the node relies on any databases (you may check the output

of <code>dcache database ls</code> to recognize the services that do),

then tag the current schema version by running <code>dcache database

tag dcache-2.6</code>.</p></li>

<li><p>If you have installed any third party plugins that offer new

services (that you have instantiated in the layout file), then remove

these and check with the vendor for updated versions.</p></li>

<li><p>Run <code>dcache services</code> and compare the services with

the <a href="#tab:services">table listing changed services</a>. If any of

those services are used, replace them with the suggested

alternative after upgrading.</p></li>

<li><p>Install the dCache 2.10 package using your package manager.</p></li>

<li><p>Reset <code>/etc/dcache/logback.xml</code> to the default

file. How this is done depends on your package manager: Debian will

ask during package installation whether you want the new version from

the package (say yes). RPM will leave the new version

as <code>/etc/dcache/logback.xml.rpmnew</code> and expects you to copy

it over.</p></li>

<li><p>If you used either <code>head</code>, <code>pool</code>,

or <code>single</code> as the layout name, you should check that

the package manager hasn't renamed your layout file.</p></li>

<li><p>We have experienced upgrade problems with the webadmin

component of <code>httpd</code>. We recommend manually deleting the

content of <code>/var/lib/dcache/httpd/webadmin/</code> before

starting dCache.</p></li>

<li><p>Run <code>dcache check-config</code>. You will receive an error

for any forbidden property and a warning for any deprecated or

obsolete property. You will receive errors about unrecognized

services defined in the layout file. You will also receive

information about properties not recognized by dCache - if these are

typos, fix them. Fix any errors and repeat.</p>

<p>As a bare minimum, the following changes commonly have to be

applied during this step:</p>

<ul>

<li>Remove deprecated services.</li>

<li>Replace FTP, DCAP and NFS door services.</li>

<li>Update TCP port, pool name, and cell name definitions.</li>

<li>If SRM implicit space reservation was enabled,

then <code>spacemanager.enable.unreserved-uploads-to-linkgroups</code>

needs to be enabled in <code>spacemanager</code>.</li>

<li>Replace any gPlazma module configuration by

real <code>gplazma</code> instances. See the section

on <a href="embedding-gplazma">embedding gPlazma</a> for

details.</li>

</ul>

</li>

<li><p>Verify that your HSM script can handle the <code>remove</code>

command. If not, update the HSM script or disable the HSM

cleaner.</p></li>

<li><p>If you use the SRM service, and if any door uses a non-default

root directory or any account uses a root directory different than the

file system root, then carefully read the section

on <a href="#unique-turls">unique write TURLs and upload

directories</a> and adjust the configuration accordingly.</p></li>

<li><p>Verify that full path permission checks will work for your name

space. If not, update the permissions or

define <code>pnfsmanager.enable.full-path-permission-check</code>

to <code>false</code>.</p></li>

<li><p>If you use the LDAP gPlazma module, review

the <a href="#ldap">changes to the module</a> and update your configuration

accordingly.</p></li>

<li><p>If you have used proxied upload through HTTP/HTTPS, then you

should verify that the <code>webdav</code> door can establish TCP

connections to the pools in the WAN port range.</p></li>

<li><p>If you have customized the look of the <code>webdav</code>

door, you should reset the style to the default and reapply any

customizations.</p></li>

<li><p>If you have firewalled access to the <code>admin</code> door,

note that the new SSH 2 service runs on port 22224 rather than 22223.</p></li>

<li><p>If the node relies on any databases, then update the schemas by

running <code>dcache database update</code>.</p></li>

<li><p>Start dCache and verify that it works.</p></li>

<li><p>Run <code>dcache check-config</code> and fix any warnings.</p></li>

<li><p>Run <code>save</code> on any tape connected pools.</p></li>

</ol>



<p>Note that some properties that were previously used by several

services have to be replaced with a configuration for each service

type. Check the documentation

in <code>/usr/share/dcache/defaults</code> for any property you need

to change.</p>



<p><span class="label label-default">Important</span> This is in

particular true for (but not limited to) SRM database settings, that

were used by <code>pinmanager</code>, <code>transfermanagers</code>,

and <code>spacemanager</code> in addition to <code>srm</code>. The

deprecated legacy names are still used by all four services, however

when using the names following the new naming convention, these have

to be defined separately for each service type. This reflects that

these services do not share any data through the database and thus can

be operated in independent databases. In a future update we may

introduce common base settings for database configuration shared by

all services.</p>



<p>Also note that some properties have changed values or are

inverted. The deprecated properties retain their old interpretation,

however when replacing those with their new names, you have to update

the value. In particular boolean properties that used to accept values

like <em>yes</em>, <em>no</em>, <em>enabled</em>, <em>disabled</em>,

now only accept <em>true</em> and <em>false</em>.</p>



## Frequently Asked Questions



What is the cns service?


<p>It’s the cell naming service. When you use non-default cell

message brokers (ie. OpenMQ or ActiveMQ), this is how well known cells

are discovered. You hardly ever need to instantiate this yourself, as

one is automatically created in dCacheDomain if one is needed.</p>



As you have nicely explained in your migration guide, some

services have been merged/split, specifically the transfer protocol

related ones. Now I'm a bit confused by the respective

properties. E.g. for dcap, there are properties for setting a queue

length on each dcap variant

(dcap.mover.queue.(plain|auth|gsi|kerberos)), which are immutable, and

one property without specialization (dcap.mover.queue). So I take it,

that we have to change this one property in the layout file for every

door, in case we want to deviate from the standard, unrelated to which

variant is used? Instead, I like the idea of setting the specific

properties in the dcache.conf file and thanks to the default nested

variable substitution of dcap.mover.queue, each door will then figure

out the right setting for itself. So the default properties

demonstrate how one could use this layered configuration method, but

at the same time administrators are not allowed to apply it. Why?



<p>The immutable properties in this case only exist for backwards

compatibility. Because the old property names had different names for

different authentication schemes, we had to provide some way to make

those be used as long as they are only deprecated. We only do this for

the few properties that had different names per variant - most

properties didn’t have per variant names - just as webdav or xrootd

didn’t have per variant versions of these properties.</p>



<p>As you point out, you can in a relative straightforward manner

specialize all these properties yourself. In this process you are not

bound to only do this by authentication scheme. It could be by port

number or some other property. It could even be by a custom property

you introduce yourself (e.g. something that marks doors for lan or wan

use, or slow or fast transfers, or small or big files). You can then

use this custom property not only for specialising the mover.queue

property, but any of the properties. You can also apply this

customization to the doors that didn’t have such specializations

before, like webdav.</p>



<p>So the point is not to prevent you from using this, but rather than

we didn’t want to limit which properties are specializable, and what

the discriminator should be. The immutable variants only exist for our

backwards compatibility and you should ignore them - they may

eventually be removed.</p>



There seems to be no differentiation for ftp as previously with

dcap regarding the properties [for different authentication

schemes]. Is that on purpose?



<p>Yes, for the reason explained above: In 2.6, ftp did not have

specialization for the mover queue: All FTP doors used gsiftpIoQueue,

regardless of this being gridftp or not. Hence there is no need for

the workaround with immutable properties to provide backwards

compatible support for multiple old names. This is also a prime

example of why we cleaned this up - some properties that looked like

they only applied to one variant actually applied to

multiple. Internally the code is the same for all variants

anyway.</p>



Can I suppress somehow the INFO labeled statements from

<code>dcache check-config</code>? Yes, we have some properties, that

are not known to dCache, but please don't tell me that whenever I

check-config.




<p>The reason we output them is because they could be

typos. dCache cannot know (or isn’t clever enough to know) whether

it’s a typo or some custom property only you know about. To avoid lots

of head-scratching when somebody has a typo, we output them as INFO to

make them easier to spot.</p>



<p>What you could do is to add a custom ‘plugin’ to your dCache

installation to make the properties known. Just create

<code>/usr/local/share/dcache/plugins/sitelocal/sitelocal.properties</code>

and define the properties with some default values here - you can set

the real values in <code>dcache.conf</code> or the layout file. This

approach has the added benefit that if you actually do have a typo in

<code>dcache.conf</code> one day, you get an INFO level message

telling you about it.</p>



I noticed that some database columns have been renamed

(eg. freespaceinbytes vs. availablespaceinbytes in srmlinkgroup) but

this has not been documented. This column is used by one of our

scripts, that why I noticed this change.




<p>This upgrade guide does state that the database schema has

changed, however since the databases are not part of the public

interface, each individual change is not listed in the guide. All

admins are strongly encouraged to analyze the new schema if at any

point they bypass dCache and access the databases directly. Check the

individual release notes for more details - the release notes for 2.9

does list the change to availablespaceinbytes (although there is no

guarantee that every minor change in the schemas is listed).</p>



<p>Note that there are much bigger changes than

<code>freespaceinbytes</code> being replaced by

<code>availablespaceinbytes</code> (also note that the column was

<em>not</em> renamed - the values in those columns are different - the

semantics are not the same).</p>


Our Chimera/NFS headnode fails to start after upgrade. It shows:

<code>Migration failed for change set

org/dcache/chimera/changelog/changeset-2.8.xml::15.3::tigran: Reason:

Automatic schema migration is disabled. Please apply missing

changes.</code>






<p>The problem is likely caused by nfs being placed in the same

domain as pnfsmanager and being placed before pnfsmanager in the

layout file. Since pnfsmanager is the service that updates the schema,

and since nfs fails because the schema is not up to date, the schema

never gets updated. You can reorder the services or just apply the

change manually using the <code>dcache database update</code>

command.</p>

We upgraded to 2.10.8 and xrootd door does not work any more: The

plugins are not working. I suspect they are not even loaded. This is

how we were turning them on:

<code>xrootd/xrootdPlugins=gplazma:gsi,authz:atlas-name-to-name-plugin,redirector</code>

Is that still valid?


<p>Not at all. All properties have been renamed. Have a look at

<code>/usr/share/dcache/defaults/xrootd.properties</code>:</p>



<pre>

(forbidden)xrootdPlugins=Use xrootd.plugins and pool.mover.xrootd.plugins

</pre>



I just happen to notice, that the pinboard seems to be very noisy

with dCache 2.10. The log level for pinboards still is INFO, which is

one level more verbose than WARN and has been the default before 2.10,

too. However, now the pinboard is flooded with messages about

background communication, as far as I understand it... This is a

snippet from the PoolManager's pinboard while there is actually zero

activity for dCache (in terms of transfers): <code> 9:58:17 AM

[PoolManager-0] [httpd PoolManagerGetPoolMonitor]

ts=2014-11-21T09:58:17.058+0100 event=org.dcache.cells.deliver.begin

uoid=<1416560297057:5072026> lastuoid&lt;1416560297057:5072025> session=

message=PoolManagerGetPoolMonitor

source=[>httpd@httpdDomain:*@httpdDomain]

destination=[>PoolManager@local]</code>.




<p>This is a common problem when not resetting logback.xml to the

default that ships with dCache. Take the logback.xml from the RPM or

DEB and place it in etc/logback.xml. You may reapply local

modifications afterwards. Usually your package manager will do this

for you, but if you at some point modified your local copy, the

package manager may decide to keep your version.</p>


After upgrade SRM uploads fail with an error like: <code>ERROR:

Current transfer FAILED: Failed to prepare destination: File requests

have failed.: Cannot obtain TURL for file: Protocol(s) not supported:

[gsiftp, http, https, httpg, ftp]</code>.


<p>This is commonly caused by the doors not exposing the upload

directory. Reread the section in this guide about <a

href="#unique-turls">unique write TURLs</a>.</p>



It is not clear what is the default value of a property,

eg. <code>defaults/dcap.properties</code> contains



<pre>

(one-of?NONE|READONLY|FULL|${dcapAnonymousAccessLevel})dcap.authz.anonymous-operations=${dcapAnonymousAccessLevel}

</pre>

Is is always the first value in the list?



<p>The value is the part after the equals sign. So for this

particular property, the default value is

<code>${dcapAnonymousAccessLevel}</code>. The default value of

<code>dcapAnonymousAccessLevel</code> is defined in the same file:

</p>

<pre>

(deprecated,one-of?NONE|READONLY|FULL)dcapAnonymousAccessLevel=NONE

</pre>

<p>i.e. <code>NONE</code>.</p>



<p>In 2.11 the indirection to the old properties is gone, which makes

it a little easier to figure out. What you see in 2.10 is just to

maintain backwards compatibility.</p>



<p>If in doubt, you can always ask dCache to compile the entire

configuration:</p>



<pre>

$ dcache loader compile -debug|grep -A1 dcap.authz.anonymous-operations

dcap.authz.anonymous-operations = ${dcapAnonymousAccessLevel}

# NONE

</pre>



<p>This will tell you the value in your current configuration (not the

default, but the value actually used).</p>
