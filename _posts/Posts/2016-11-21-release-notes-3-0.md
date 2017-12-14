---
layout: post
title:  "dCache 3.0 Release Notes!"
date:   2016-11-21 10:27:23
author: Asif Mohiuddin
excerpt: The release notes for dCache 3.0. 
category: posts
---

# What’s new in dCache 3.0
## The release notes


Highlights


Experimental CEPH support.
Automatic detection of PostgreSQL master.
Self describing billing files.
Pool manager setup is stored in ZooKeeper.
Pool manager read-only state is stored in setup file and ZooKeeper.
New performance cost calculation for improved stability of hot spot replication.
Allow batching of flush to tape to be “disabled”.
Allow polling HSM scripts.
Mover queues can be created at runtime.
Abort upload when SRM TURL is invalidated.
Allow xrootd clients to select mover queues.
Support the HAProxy proxy protocol.
Production ready support for high availability deployments.


Incompatibilities


Compatibility with pools older than 2.16 has been dropped.
Properties marked deprecated in 2.16 are now obsolete.
Several deprecated or obsolete admin commands have been
 removed.
The admin door no longer supports DSA keys.
The billing service no longer output records for
 which no format string was defined.
The pool manager and pool configuration files now only
 support the commands considered setup commands.
Support for the legacy UDP discovery service used in
 2.15 and earlier has been dropped.
dCacheDomain no longer default are core domain.
DCAP doors no longer supportthe <code>dcapLock</code> feature to
 halt new requests.
Pool manager now automatically persists its setup in ZooKeeper
 uses it after a restart rather than <code>poolmanager.conf</code>.
The way pool manager calculates performance cost has changed
 and cost limits in pool manager may have to be retuned.
The pool to pool client queue in pools no longer has a
 configurable limit.
Return code 72 is now a special value for HSM scripts.
The failure semantics for empty uploads has changed.
The <code>https-jglobus</code> value has been removed for the
 <code>webdav.authn.protocol</code> property.


Acknowledgments

<p>Thanks to Onno Zweers for several contributions to this release.</p>

Release 3.0.27

<h3 id="cells">cells</h3>

<p>The current release improved handling of rogue domains with badly formatted dCache versions.</p>

<h3 id="configuration">configuration</h3>

<p>There are configuration options in zookeeper that may affect how well
the zookeeper cluster will work with dCache. The lack of documentation
of how dCache uses zookeeper prevents admins from tuning their zookeeper
instance. This is now fixed and zookeeper configuration is updated with
 hints on how dCache uses zookeeper, along with the corresponding zookeeper configuration properties.</p>

<h3 id="pool">pool</h3>

<p>The current release fixed loading <code>setup</code> that requires queues created by <code>pool.queues</code>.</p>

<h3 id="webdav">webdav</h3>

<p>The current release fixed the stack-traces on bad client input.</p>

<h3 id="changelog3.0.26..3.0.27">Changelog 3.0.26..3.0.27</h3>
<!-- git log 3.0.26..3.0.27 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->

- <a href="https://github.com/dcache/dcache/commit/2b591bf1b52c65be8b3b94da73f228cfabcc66e9">2b591bf</a>  [maven-release-plugin] prepare release 3.0.27
- <a href="https://github.com/dcache/dcache/commit/fa68a01877fc88ea081eb5a51b06e12630f77dbd">fa68a01</a>  cells: better handling of rogue domains with badly formatted dCache versions
- <a href="https://github.com/dcache/dcache/commit/c944c4710899485e5b483601475c7b203ee817aa">c944c47</a>  configuration: update zookeeper configuration with hints
- <a href="https://github.com/dcache/dcache/commit/cb033cb74fcb703445023eab8825865634607b6d">cb033cb</a>  pool: fix loading ‘setup’ that requires queues created by ‘pool.queues’
- <a href="https://github.com/dcache/dcache/commit/545d0721a3a2b86a120ac3eb07ecf09e091639db">545d072</a>  webdav: avoid stack-trace on bad user requests
- <a href="https://github.com/dcache/dcache/commit/47d18d7d9f5bbc2e0d533bfaf9d75fd7381eac1a">47d18d7</a>  alarms: guard against NPEs on LogEntry getters
- <a href="https://github.com/dcache/dcache/commit/7eb682771834201bc412e232a4f834e09889ff9a">7eb6827</a>  [maven-release-plugin] prepare for next development iteration



Release 3.0.26

admin

<p>While <code>migration move</code> tasks on pools were working correctly, for <code>migration info</code> command an error occurred,
 that the current user (root) wasn’t allowed to execute anything (due to missing ACLs). This is now fixed.</p>

<h3 id="changelog3.0.25..3.0.26">Changelog 3.0.25..3.0.26</h3>
<!-- git log 3.0.25..3.0.26 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->


- <a href="https://github.com/dcache/dcache/commit/722f000da8ea59599b057134eee81d4fbb45b915">722f000</a>  [maven-release-plugin] prepare release 3.0.26
- <a href="https://github.com/dcache/dcache/commit/43fcf9264c4fa0405abdc3dac6a43f0048395ac0">43fcf92</a>  resilience: restore extractor class value for extractor property
- <a href="https://github.com/dcache/dcache/commit/00a2da12da6b1ed79226006f6ba203d4846d48cb">00a2da1</a>  admin: Fix Inconsistent ACL enforcement, RT 9207
- <a href="https://github.com/dcache/dcache/commit/2c0cb3a70fe69ed3e912680711018096b1d2fd7a">2c0cb3a</a>  [maven-release-plugin] prepare for next development iteration



Release 3.0.25

configuration

<p>For some services it was unclear what were the admin’s responsibilities in
terms of consistent configuration. The current release updated the documentation describing what is needed to deploy redundant services.</p>

<h3 id="resilience">resilience</h3>

<p>The current relase improved configuration for namespace provider properties by making them immutable.</p>

<h3 id="srm">srm</h3>

<p>The current release improved configuration for <code>srmPing</code> responses.</p>

<h3 id="changelog3.0.24..3.0.25">Changelog 3.0.24..3.0.25</h3>
<!-- git log 3.0.24..3.0.25 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/ca0220a55a9413d969a1d34e901355021acb92a8">ca0220a</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.25</dd>

<dt><a href="https://github.com/dcache/dcache/commit/240fa42c37dfeb9a4ad4aae26c5b9ec683e1494c">240fa42</a></dt>
<dd>configuration: update description for replicable</dd>

<dt><a href="https://github.com/dcache/dcache/commit/583eadbb2871992f04c0ae038b6af490f15e5036">583eadb</a></dt>
<dd>resilience: remove reference to pnfsmanager property</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c73bf8ebe62b67a39ff38164e10152fa11031d47">c73bf8e</a></dt>
<dd>srm/srmmanager: fix srmPing confusion</dd>

<dt><a href="https://github.com/dcache/dcache/commit/da6bbf28f558c28740101caace6807b7eb8a5a45">da6bbf2</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/99c08d4e338e5f401914b4881a9ca81d9e5d41dd">99c08d4</a></dt>
<dd>resilience: make namespace provider properties immutable</dd>
</dl>


Release 3.0.24

<h3 id="billing">billing</h3>

<p>The current release added documentation that describes how a <code>CellAddress</code> and its fields
expand.</p>

<h3 id="config">config</h3>

<p>The current release improves documentation for dCache admins by adding <code>obsolete|forbidden</code> annotation for dropped properties.
This helps admins to discover changes that might affect their dCache
instance. This is both through manual inspection and through the
<code>dcache check-config</code> command.</p>

<h3 id="ftp">ftp</h3>

<p>It has been discovered that timestamp facts reported by dCache
GFTP server are expressed in local (to server) time.
This is now fixed. Timestamp facts are reported in GMT.
 Clients like <code>globus-url-copty -sync</code>
work properly and <code>ubefrtp -ls</code> returns correct timestamp.</p>

<h3 id="srm">srm</h3>

<p>The current release added new configuration properties to allow easy modification.</p>

<p>It upstated as well <code>srm/manager.properties</code> documentation to describe the relationship between <code>srmmanager.root</code> and <code>srm.loginbroker.root</code> properties.</p>

<h3 id="changelog3.0.23..3.0.24">Changelog 3.0.23..3.0.24</h3>
<!-- git log 3.0.23..3.0.24 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/c92bfa3b0a3cdbe59b22f04ad675c970440dc918">c92bfa3</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.24</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a775bcf23f9bc7af28a84770cc9e3cc27b22f50c">a775bcf</a></dt>
<dd>srm/srmmanager: update documentation about root path</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8ce10c14a1c1ce20b68b61f74dc9b1bca53c51c4">8ce10c1</a></dt>
<dd>ftp: convert timestamps to GMT (to follow RFC 3659)</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1521ad11586fce17d629d2cb5c5dc5d6df3fc7a9">1521ad1</a></dt>
<dd>config: use consistent terminology</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5f59a0fc029646f31cf604075400ea56ae7521f9">5f59a0f</a></dt>
<dd>billing: update documentation to describe CellAddress</dd>

<dt><a href="https://github.com/dcache/dcache/commit/216b127af82cc14c0de1375fb6da63c324a55858">216b127</a></dt>
<dd>srm,srmmanager: add configuration property to allow easy modification of srm root</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7bbcbd310200d0e2471dd01d7d73cfd982c47bb2">7bbcbd3</a></dt>
<dd>logback: make socket appender construction depend on log level</dd>

<dt><a href="https://github.com/dcache/dcache/commit/db2048af236dd953d8acce805f578b214a77ef34">db2048a</a></dt>
<dd>dcache: release dcache-view 1.1.5 for dcache 3.0</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e14e3166f8047e6a250ce7eaacdb3ae339d7a433">e14e316</a></dt>
<dd>config: add obsolete|forbidden annotation for dropped properties</dd>

<dt><a href="https://github.com/dcache/dcache/commit/24c8a5fa100ab23c9013db42f94f0dba2c4ff7d7">24c8a5f</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/454bb6d847399e8dc83959fa701eeecebf525654">454bb6d</a></dt>
<dd>config: add obsolete|forbidden annotation for dropped properties</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ea3c73d841946fb8f18f5e27f953532d41d28967">ea3c73d</a></dt>
<dd>pnfsmanager: remove obsolete comments from properties file</dd>
</dl>


Release 3.0.23

<h3 id="changesaffectingmultipleservices">Changes affecting multiple services</h3>

<p>Christoph Anton Mitterer submitted several corrections to the comment string in properties files.</p>

<h3 id="zookeeper">zookeeper</h3>

<p>A race condition in zookeeper caused irrelevant stacktraces to be logged on shutdowns.
Since this problem is not easily solvable with Zookeeper 3.4, we decided to change the log-level
threshold for NIOServerCnxnFactory. Note that the suppressed class is only used by ZooKeeper server (i.e.,
not the client). Therefore, only the ‘zookeeper’ service is affected.</p>

<h3 id="changelog3.0.22..3.0.23">Changelog 3.0.22..3.0.23</h3>
<!-- git log 3.0.22..3.0.23 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/2f93fd01a5bc24f3365f1afa00f9034e76783bc1">2f93fd01a5</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.23</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9bd1cac672cfa94d7ad49615c7e71533a213244a">9bd1cac672</a></dt>
<dd>use correct terminology</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c3fe563c9e781903db810e67f40d5f283713b357">c3fe563c9e</a></dt>
<dd>fixed several typos in the documentation</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d3dfad0fe542c9445f45bc2a1a16208ef1fc70c8">d3dfad0fe5</a></dt>
<dd>added hint that pnfsmanagers must use the same DB</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c19e087029d53c75d6fd475266e357c578e2b266">c19e087029</a></dt>
<dd>zookeeper: work-around race-condition in zookeeper server shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f87dd852a805109da2ae2d991b6462678dd326f3">f87dd852a8</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.22

<h3 id="httpd">httpd</h3>

<p>The “Disk Space Usage” webpage (<code>/usageInfo</code>) contains a table showing
information about each pool in the dCache cluster. The “Layout”
column showed the capacity usage graphically, with different colours
showing how much of that pool’s capacity is being used for different
tasks. This release fixes the Layout heading to describe a previously
undocumented colour.</p>

<h3 id="changelog3.0.21..3.0.22">Changelog 3.0.21..3.0.22</h3>
<!-- git log 3.0.21..3.0.22 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/9f91b2f8c436628530afb51ac2427dff1daf9736">9f91b2f</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.22</dd>

<dt><a href="https://github.com/dcache/dcache/commit/74c1bb29e9aeb909cd8d18cee39956a20f6453d9">74c1bb2</a></dt>
<dd>system-test: add series of functional test for frontend service</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1cef3259db619222c66474154ecf479d985aebec">1cef325</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/872a90670a0ade4a15c7debcfb2bd21f92357bd3">872a906</a></dt>
<dd>httpd: Fixed table headers in usageInfo</dd>
</dl>


Release 3.0.21

<h3 id="frontend">frontend</h3>

<p>Several improvements are added to frontend such as
restriction usage is improved and easily configurable JSON is now available via frontend.</p>

<h3 id="srm">srm</h3>

<p>The current release enforced restrictions on <code>srmSetPermission</code> operations.</p>

<h3 id="zookeeper">zookeeper</h3>

<p>The current release fixed race-condition when ZooKeeper server accepts requests before the server is fully
initialised.</p>

<h3 id="changelog3.0.20..3.0.21">Changelog 3.0.20..3.0.21</h3>
<!-- git log 3.0.20..3.0.21 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/6a0a31b8307a472214b27fc9dee552e48687c4d4">6a0a31b</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.21</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d1111930dd59642aab12a1b63464fe51e0bdcfe9">d111193</a></dt>
<dd>frontend: refactor static (configuration) data</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6a48e13c6a9507bad3ef19b564efd97e20f424b0">6a48e13</a></dt>
<dd>spacemanager: dont try to release expired spaces</dd>

<dt><a href="https://github.com/dcache/dcache/commit/52f2075c7ebd80c388f365eb6cb159c9ac659f9a">52f2075</a></dt>
<dd>srmmanager: use path to support srmSetPermission operations</dd>

<dt><a href="https://github.com/dcache/dcache/commit/da193372bbe0aa7f51250ab0050805c5d83e28c8">da19337</a></dt>
<dd>frontend: fix Restriction usage</dd>

<dt><a href="https://github.com/dcache/dcache/commit/29478e417b76c8ca5f69791a5c4f103b38754cfa">29478e4</a></dt>
<dd>zookeeper: work-around SessionTracker racy initialisation on startup</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d65d5b8f76b8c47990d958d47e28c5ebb661a3a4">d65d5b8</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.20

<h3 id="changesaffectingmultipleservices">Changes affecting multiple services</h3>

<p>dCache previously shipped both log4j and log4j-over-slf4j libraries. This patch simplifies deployment and prevents possible problems due to non-deterministic
library loading sequences by removing log4j dependencies.</p>

<h3 id="frontend">frontend</h3>

<p>If frontend was asked to create a directory listing while a file was being uploaded into the directory being listed,
previously, an error would occur. This patch addresses that issue.</p>

<p>This release includes a new dCacheView version.</p>

<h3 id="info">info</h3>

<p>The info cell can occasionally send messages before it is properly registered. This can lead to <code>Cannot send message with callback in state...</code> messages that
do not correspond to any valid error condition. This patch ensures that messages are only sent as soon as the cell is properly registered.</p>

<h3 id="pool">pool</h3>

<p>If the communication between a pool and PnfsManager times out, the error message is not well suited to diagnosing the problem:
<code>Failed to instantiate mover due to unsupported checksum type: Request to [&gt;PnfsManager@local] timed out.</code> The checksum type is
not playing an important role here. Hence, this patch updates the error message.</p>

<h3 id="zookeeper">zookeeper</h3>

<p>Embedded Zookeeper instances would occasionally log stack-traces on startup. This patch adds a work-around.</p>

<p>Zookeeper logs a stack-trace in cases where the client disconnects unexpectedly. This is unnecessary and potentially confusing, so this patch changes
Zookeeper’s behaviour to just logging the incident.</p>

<h3 id="changelog3.0.19..3.0.20">Changelog 3.0.19..3.0.20</h3>
<!-- git log 3.0.19..3.0.20 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/bb7d0aa83836942b7f76fd74aab9c7ebb3556377">bb7d0aa838</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.20</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7af2a80aff729424a6ac4aea9c604b323cd55bbe">7af2a80aff</a></dt>
<dd>dcache: release dcache-view 1.1.4 for dcache 3.0</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3002758a02823384ae944d70ce09872dc2490e01">3002758a02</a></dt>
<dd>zookeeper: work-around racy startup</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0ee8801ff522a3c91018ccc053c798051896dccb">0ee8801ff5</a></dt>
<dd>zookeeper: silence ZK server errors</dd>

<dt><a href="https://github.com/dcache/dcache/commit/67fc64b64268cd55163a1d393ac43d30dfb8477f">67fc64b642</a></dt>
<dd>dependencies: remove log4j jar</dd>

<dt><a href="https://github.com/dcache/dcache/commit/47e98838a4ef75e29a3ab05d524e1e3f65c2a0bc">47e98838a4</a></dt>
<dd>frontend: fix “Attribute is not defined: SIZE” bug</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9f75784527fd98ce9b8a1f683bcf2f9e181dbffe">9f75784527</a></dt>
<dd>pool: fix error message on timeout</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6407eb9180350f086cf3ea80448dd0e6e7133598">6407eb9180</a></dt>
<dd>info: avoid sending messages too early.</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9c518fbedf1929c809477fedb60a35be7ee73015">9c518fbedf</a></dt>
<dd>frontend,webdav: add supress-wwwauthenticate to allow headers</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e65c4bedec1226cd37ecdbd2778dd0d2107a5417">e65c4bedec</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.19

<h3 id="frontend">frontend</h3>

<p>Clients can now send a <code>Suppress-WWW-Authenticate</code> header in order to avoid the native login dialog in browsers.</p>

<h3 id="hsm">hsm</h3>

<p>A potential space leak in staging requests has been mitigated.</p>

<h3 id="pool">pool</h3>

<p>Since there are various reasons for why a mover may be terminated, the previous log message “Transfer was
forcefully killed” is not detailed enough to deduce the reason behind the problem. This patch enables more
detailed error messages both in the log files and in billing. Note, however, that the door’s report of the failed
transfer may duplicate this information.</p>

<h3 id="webdav">webdav</h3>

<p>A recent update, commit 5abc0e1c, improved the behaviour of the Milton WebDAV libraries if an IOException occurs
during an upload. That patch, unfortunately, did not address all issues, and when non-spec-conformant clients
are used against dCache, stacktraces can be triggered.</p>

<p>This patch corrects that behaviour. Also, in case of errors, the error code returned in case of any problems
was changed from 400 to 500, which should signal cliens that they are free to retry the transfer after a timeout.</p>

<p>In case of failing transfers, doors will log more accurate information.</p>

<h3 id="changelog3.0.18..3.0.19">Changelog 3.0.18..3.0.19</h3>
<!-- git log 3.0.18..3.0.19 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/b5a645ede80bb3adb2e23cc77ed8fdf5cc5364d0">b5a645ede8</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.19</dd>

<dt><a href="https://github.com/dcache/dcache/commit/32ee8c45425e949e06cfc3fa35c963f03fd410e2">32ee8c4542</a></dt>
<dd>authentication: suppress WWW-Authenticate if requested</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4506319d50817297591d133251392d53a0ec83ef">4506319d50</a></dt>
<dd>webdav: improve logging on transfer failures</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3758693ce475997844ee9e7e5cd1104dd5931e0b">3758693ce4</a></dt>
<dd>pool: log why a transfer was forcefully aborted</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3446c4b8da79642b728687ffa941d4f26482af82">3446c4b8da</a></dt>
<dd>webdav: make Milton work-around more robust</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0f5c9f7b177e9c86ed0c0f8d5afa4b471d52d82a">0f5c9f7b17</a></dt>
<dd>script-nearline-spi: fix space leak when polling script is used</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4466f0d37c8674f41c51a00727887a3e6f918f17">4466f0d37c</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.18

<h3 id="http">http</h3>

<p>In an HA setup with multiple pool managers, the httpd (old) service failed to
fetch the list of restore requests from all instances. Instead the service
would query one of the instances, possibly alternating depending on the
grouping of services in domains. This behaviour has been corrected, so that
the http interface now shows all restored entries even in HA configurations.</p>

<h3 id="webdav">webdav</h3>

<p>File transfers through WebDAV doors could potentially bypass any Restrictions
checks in PnfsManager. This patch ensures that Restrictions are always checked
and observed, and improves PnfsManager’s logging to give information in case
a Restrictions check is not posssible.</p>

<h3 id="changelog3.0.17..3.0.18">Changelog 3.0.17..3.0.18</h3>
<!-- git log 3.0.17..3.0.18 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/04ac75e09d99e8ddfaabf8794f2a3625a9915282">04ac75e09d</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.18</dd>

<dt><a href="https://github.com/dcache/dcache/commit/335b645fbf4a44e40625108cfbca2f54bf3f9256">335b645fbf</a></dt>
<dd>webdav: Fix restriction check when downloading a file</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5502db75afc9fb9dcb7842630499938547ba3d10">5502db75af</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/79073fcda7cfd92056c524eede3501fbd0410163">79073fcda7</a></dt>
<dd>httpd: Fix incomplete restore list in HA setup</dd>
</dl>


Release 3.0.17

<h3 id="frontend">frontend</h3>

<p>OpenID connect can now be enabled from dCacheView. This change introduces three new
properties in the <code>frontend.properties</code> file,
<code>frontend.dcache-view.oidc-provider-name-list</code>,
<code>frontend.dcache-view.oidc-client-id-list</code> and
<code>frontend.dcache-view.oidc-authz-endpoint-list</code>,
all of which are documented in the properties file.</p>

<h3 id="pinmanager">pinmanager</h3>

<p>Upgrades from dCache 2.13 could occasionally fail during the Liquibase update stage.
The database table <code>pinsv3</code> can not be dropped if it is still referenced by foreign
keys of other tables. This modification adds a <code>cascadeConstraints=true</code> modifier to
the dropTable command used during the conversion process. Thereby, updates are possible
without errors and PinManager starts without issues after an upgrade.</p>

<h3 id="rest-api">rest-api</h3>

<p>Requests to /api/v1/user now include the username of the requestor. This is intended
to make working with OpenID Connect tokens easier.</p>

<h3 id="changelog3.0.16..3.0.17">Changelog 3.0.16..3.0.17</h3>
<!-- git log 3.0.16..3.0.17 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/44f602a94edae8162bdc6832da68bf8830f1bc8e">44f602a94e</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.17</dd>

<dt><a href="https://github.com/dcache/dcache/commit/33fd02c29820a9cac552e6301975e35ef48a8689">33fd02c298</a></dt>
<dd>httpd, admin: Fix some hard-coded cell names</dd>

<dt><a href="https://github.com/dcache/dcache/commit/fb5520975e66acd57a4110a2f21a6f6852d93581">fb5520975e</a></dt>
<dd>frontend: expose open-id connect to dcache-view</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7fec3318d9b1a35357f1c75e8e05cd6e8d292caa">7fec3318d9</a></dt>
<dd>rest-api: include username to the user attributes</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3c465934ee2bec5d1ac20a653f98ed3559f66c5d">3c465934ee</a></dt>
<dd>Add cascadeConstraints=“true” to liquibase dropTable action on pinsv3 table</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8083ea91bdeb62054744a539f20e7775ab7256a5">8083ea91bd</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.16

<h3 id="nfs">nfs</h3>

<p>Invalidation of VFS caches has been improved, so that there is no stale information left for
dot files.</p>

<h3 id="pool">pool</h3>

<p>Error handling in pools was improved for systems using CEPH backends.</p>

<h3 id="changelog3.0.15..3.0.16">Changelog 3.0.15..3.0.16</h3>
<!-- git log 3.0.15..3.0.16 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/37e2ad1eac4a0f35f3c7ea594e05eca22b2dda93">37e2ad1eac</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.16</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6d56e52d2dddf44fcd23697960dba09ecd6651dd">6d56e52d2d</a></dt>
<dd>nfs: bind vfs cache invalidation with file’s layout</dd>

<dt><a href="https://github.com/dcache/dcache/commit/89a192ae18bb65c56e78055f2b6ad92d5456151c">89a192ae18</a></dt>
<dd>ceph: map RadosException to corresponding IOException</dd>

<dt><a href="https://github.com/dcache/dcache/commit/63d766b88995f955aaa61aa1cfb4cfd1381cd79c">63d766b889</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.15

<h3 id="nfs">nfs</h3>

<p>Debugging of stuck transfers has been facilitated by adding the status of transfers to the output of the <code>show transfers</code> command.</p>

<p>The assignment of movers to NFS doors has been made more robust.</p>

<h3 id="system-test">system-test</h3>

<p>The system-test module, used for demonstration or testing purposes, comes with a built-in X.509 infrastructure. With this release, expired certificates are replaced by new ones.</p>

<h3 id="changelog3.0.14..3.0.15">Changelog 3.0.14..3.0.15</h3>
<!-- git log 3.0.14..3.0.15 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/7c9d20a04241bb26d9f3eec2fa310bc11f43cf0c">7c9d20a042</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.15</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a3005ede587331a1313884e210d4ce10cb70bd56">a3005ede58</a></dt>
<dd>nfs: show transfer status when displayed</dd>

<dt><a href="https://github.com/dcache/dcache/commit/605db8097b50d07cb6d7f2a4bee8e790890a735a">605db8097b</a></dt>
<dd>system-test: update disposable-CA generated credentials</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a45eb26bb35b1de13b6d087af06dd3b2bc12324c">a45eb26bb3</a></dt>
<dd>nfs: fix loosing movers due to short timeout</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d17e6332f2c28c8ba001ecee9cffa80b8c3a3e84">d17e6332f2</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.14

<h3 id="changesaffectingmultipleservices">Changes affecting multiple services</h3>

<p>The version of the PostgreSQL driver used by dCache internally was brought up to 9.4.1212. This fixes the issue described in <a href="https://liquibase.jira.com/browse/CORE-2939">liquibase bug 2939</a>
.</p>

<h3 id="chimera">chimera</h3>

<p>In order to improve IO performance, the way dCache updates <code>atime</code> values was modified.</p>

<h3 id="nfs">nfs</h3>

<p>An internal change in the NFS door code helps reducing irrelevant exceptions being logged.</p>

<h3 id="srm">srm</h3>

<p>SRM no longer times out file requests.
This alleviates a rare race condition where timeouts for the file request and file access competed.
Requests that time out now always return SRM_REQUEST_TIMED_OUT at request
level and SRM_FAILURE for the SURLs in that request.</p>

<h3 id="changelog3.0.13..3.0.14">Changelog 3.0.13..3.0.14</h3>
<!-- git log 3.0.13..3.0.14 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/7a614f2cebf3e1085bbc8f302d3e7f4ea1d459df">7a614f2ceb</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.14</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ace6b59de139dc0b9c2a39beaeadd848ed44c591">ace6b59de1</a></dt>
<dd>ceph: log repository IO error</dd>

<dt><a href="https://github.com/dcache/dcache/commit/706795f5b66da163a0039a1fc362372bd7700c89">706795f5b6</a></dt>
<dd>update postgresql driver to version 9.4.1212 to address issue with liquibase changeset and postgresql 9.6 (see <a href="https://liquibase.jira.com/browse/CORE-2939">liquibase bug 2939</a>)</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f6b7af5112172cd6c53597cb45a29ab5263b795f">f6b7af5112</a></dt>
<dd>srm: remove file-level timeout</dd>

<dt><a href="https://github.com/dcache/dcache/commit/95c465df9f3045b73e8ba6f621f48de8c308ec3a">95c465df9f</a></dt>
<dd>chimera: do not update inode generation on atime only update</dd>

<dt><a href="https://github.com/dcache/dcache/commit/08a3b4cb104471b47c6dfb2d74411164c584dca2">08a3b4cb10</a></dt>
<dd>nfs: do not add Origin to read-only subject</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a3df429db1993acad06eeb1d87e4702f17284a5c">a3df429db1</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2434f8375ae0a935f45fe663a7a18feb6da50b46">2434f8375a</a></dt>
<dd>parent/dcache: add mail jar to deployment</dd>
</dl>


Release 3.0.13

<h3 id="pool">pool</h3>

<p>Current release improves handling of CEPH exceptions, so that pools can react appropriately when request for a missing file.</p>

<p>Fixes double close on p2p.</p>

<h3 id="changelog3.0.12..3.0.13">Changelog 3.0.12..3.0.13</h3>
<!-- git log 3.0.12..3.0.13 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/484a88dc3366177cd4237328cf546083e194f58e">484a88d</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.13</dd>

<dt><a href="https://github.com/dcache/dcache/commit/65626432a3af17e5cab9630c40dcc44971a7a3d9">6562643</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/194c54afcbb36eda093182c4b5f1f92bc37fa1ed">194c54a</a></dt>
<dd>pool: handle CEPH exceptions</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7f7d6e279288f40572835a7b12fe35e686d3f472">7f7d6e2</a></dt>
<dd>pool: fix double close on p2p</dd>
</dl>


Release 3.0.12

<h3 id="chimera">chimera</h3>

<p>There was an issue with a symbolic link to a directory where destination
where destination contained trailing slash. This is now fixed.</p>

<h3 id="nfs">nfs</h3>

<p>The current release fixed interoperability with RHEL7-based clients
 and handling of invalid principals on SETATTR sent
by OSX client. </p>

<h3 id="changelog3.0.11..3.0.12">Changelog 3.0.11..3.0.12</h3>
<!-- git log 3.0.11..3.0.12 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/4770eea602c44d14be92c56557fb68284d794468">4770eea</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.12</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9acdb7e7f9685bd30417725df9fc6bac236f5098">9acdb7e</a></dt>
<dd>libs: update to bug fix release nfs4j–0.13.1</dd>

<dt><a href="https://github.com/dcache/dcache/commit/bd98067743e80f9e2d6bc49b19c30e05ccadbef4">bd98067</a></dt>
<dd>srmclient: fix handling of checksum options</dd>

<dt><a href="https://github.com/dcache/dcache/commit/be5101d4ae9eba3ad94775ba2052994cfe1400b2">be5101d</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0be540844e776a4c1f8d9b9c6569292f8884e5f3">0be5408</a></dt>
<dd>chimera : handle empty paths elements path2inumber stored procedure</dd>
</dl>


Release 3.0.11

<h3 id="chimera">chimera</h3>

<p>The current release fixed database query for storing multiple checksums for a file.</p>

<h3 id="ftp">ftp</h3>

<p>The Socket <code>read</code> method may return zero to indicate that no bytes were
read. Although this is not an error, such occurances will result
in a transfer failing.</p>

<p>This is now fixed.</p>

<h3 id="srmclient">srmclient</h3>

<p>Directory listing for CASTOR was resulting in a <code>NullPointerException</code> when the request
size is too large, due to the fact that the CASTOR SRM interface limits the maximum number of responses to 1024.
This is now fixed.</p>

<h3 id="changelog3.0.10..3.0.11">Changelog 3.0.10..3.0.11</h3>
<!-- git log 3.0.10..3.0.11 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/57ebca36e91b41d9c8c6466d8fd1c418ad54ac1d">57ebca3</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.11</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8e607b660a1b3b938113c73cce1905f0f2c83f30">8e607b6</a></dt>
<dd>srmclient: fix compatibility with castor</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3389013f1806cfc3fdc510a896e5159a7cd8e940">3389013</a></dt>
<dd>ftp: prevent execution of most commands when unwrapped</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c422b7a9170c9c5c60078d99591f534a3ec1bb30">c422b7a</a></dt>
<dd>chimera: fixed database query for storing multiple checksums for a file.</dd>

<dt><a href="https://github.com/dcache/dcache/commit/71a6ac9f11d13b7650c4043b4d746eea89404618">71a6ac9</a></dt>
<dd>ftp: do not fail proxy transfer if read returns zero bytes</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c480738e98f64b6cb225d508638fbded90a494ef">c480738</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.10

<h3 id="ftp">ftp</h3>

<p>The current release added implementation of MLSC. As a result Globus is able to query the contents of dCache directories using FTP and
without creating additional TCP connections.</p>

<h3 id="lm">lm</h3>

<p>The current release fixed the issue with duplicate location manager connectors.</p>

<h3 id="changelog3.0.9..3.0.10">Changelog 3.0.9..3.0.10</h3>
<!-- git log 3.0.9..3.0.10 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/2b4e595f0125c2b45760bfead90a40849a3bb240">2b4e595</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.10</dd>

<dt><a href="https://github.com/dcache/dcache/commit/301142f95c5d288a2e2dd298a05f7bca1ad4c054">301142f</a></dt>
<dd>lm: Do not rely on thread interrupt for shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6b93af98ce68df9cb3e9db567db2308ca7a50ab4">6b93af9</a></dt>
<dd>ftp: implement the MLSC command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/363149a317488de19bbf2f74df45f5e26b14a742">363149a</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.9

<h3 id="ftp">ftp</h3>

<p>The current release improves compatibility between dCache FTP client and Globus GridFTP server.</p>

<h3 id="resilience">resilience</h3>

<p>When a file has no readable replicas, the default behavior of resilience
is to raise an alarm. Files marked <code>CUSTODIAL</code> were excluded from this.
The current release fixed this in a way that an alarm is raised for all files without readable disk copies, whether the file is <code>CUSTODIAL</code> or not.</p>

<h3 id="restful">restful</h3>

<p>dCache has the concept of a home directory: each user may have a
directory that is somehow “theirs”. This information was not
available to clients accessing dCache via the REST interface.
The current release fixed this and querying <code>/api/v1/user</code> provides the user’s home directory in addition to other user-centric information.</p>

<p>The RESTful interface exposed some namespace-targeted
information through /api/v1/namespace, and QoS information through
/api/v1/qos-management/namespace. This was undesirable as dCache exposes
namespace-targeted operations in two places.
This is now fixed and the client may obtain information by querying
<code>/api/v1/namespace</code>.</p>

<p>The current release improves the error handling for RESTful interface. Currently the error JSON object contains potentially useful information in the message and the bugs are logged.</p>

<h3 id="srm">srm</h3>

<p>During an ATLAS stress-test of tape recalls, it was discovered that
various sites had relatively short request lifetimes. However, the SRM
spec provides the opportunity for the server to inform the client (FTS,
in this case) of what lifetime a request actually has.
The current release includes the requests remaining lifetime in the response from the server.</p>

<p>The current release improves the documentation to help Admins to have a better understanding how to configure dCache correctly.</p>

<h3 id="changelog3.0.8..3.0.9">Changelog 3.0.8..3.0.9</h3>
<!-- git log 3.0.8..3.0.9 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/b243cb0c7a05265e2bb815b7413f11581bd0253b">b243cb0</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.9</dd>

<dt><a href="https://github.com/dcache/dcache/commit/926bf7cfd8a1f73c65d9e603b21f7edf16d95e62">926bf7c</a></dt>
<dd>srm-client: use default GridFTP port if not specified</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6b65522be556c21a3b1aee42a056e7f03d34acc1">6b65522</a></dt>
<dd>ftp: Add support for SITE WHOAMI command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d3d12b9435ecae950791db4ec1cb636ce01b9db6">d3d12b9</a></dt>
<dd>resilience: remove check on CUSTODIAL for inaccessible files</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8b4ab7cd9d25a14685341e33bded1d7094df59bd">8b4ab7c</a></dt>
<dd>ftp: update parsing of CLIENTINFO command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5911a18376f3929e42607e7c67c68914f43045af">5911a18</a></dt>
<dd>srm: include remaining request lifetime in various responses</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c3662f2417190e3cdf26d472864010d63a37f199">c3662f2</a></dt>
<dd>srm: update srm request.*.lifetime configuration properties documentation</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0284bac4e37f36270cba5cce43e99ac8b81cd8e2">0284bac</a></dt>
<dd>ftp: modify facts describing namespace ownership</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4136c762cd0b612c0ab26770540017af39365686">4136c76</a></dt>
<dd>ftp: add support for SITE TASKID command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f8c16f5a7fafd3328b29a2cd5d2fe42ae8ff4369">f8c16f5</a></dt>
<dd>ftp: add initial support for checksum performance markers</dd>

<dt><a href="https://github.com/dcache/dcache/commit/031862e90b60084baa392cfc8da82c687bd5b599">031862e</a></dt>
<dd>restful: support querying QoS through namespace</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8d746846d82bb9067e423a4a645fdb3c7fac53ed">8d74684</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/393ba5dfdf5e4ac1c8db63d3008894d7a0f71098">393ba5d</a></dt>
<dd>rest: add home directory to user info</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b5c8a70f74c1aff920f2ecdb6a26e07fd0d52cd1">b5c8a70</a></dt>
<dd>restful: improve error handling</dd>

<dt><a href="https://github.com/dcache/dcache/commit/fccd7bfb2a352c954bd3f70365331c917d63e2f8">fccd7bf</a></dt>
<dd>ftp: add support in OPTS RETR for specifying performance marker frequency</dd>

<dt><a href="https://github.com/dcache/dcache/commit/19367b779c1858ac003bc6f3efd83128f1866dec">19367b7</a></dt>
<dd>ftp: show SIZE facts for directories</dd>

<dt><a href="https://github.com/dcache/dcache/commit/bbf1c08b2166fa8273ff67cf1fe14becee9e9375">bbf1c08</a></dt>
<dd>ftp: add support for paths relative to home directory</dd>
</dl>


Release 3.0.8

<h3 id="frontend">frontend</h3>

<p>This release of dCache ships with an updated dCache View version. </p>

<h3 id="xrootd">xrootd</h3>

<p>In https://github.com/xrootd/xrootd/issues/459, it became apparent that dCache could improve xrdcp compatibility by sending
checksum information in lower case. This release contains this change, which should improve xrootd operations.</p>

<h3 id="changelog3.0.7..3.0.8">Changelog 3.0.7..3.0.8</h3>
<!-- git log 3.0.7..3.0.8 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/b856742ad28ba4b14aae3492ae796236b56629e1">b856742</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.8</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2056dd7b67a50cd7ef6dc7bbfcee523f2e631c9d">2056dd7</a></dt>
<dd>xrootd : use lower case for checksum algorithm names when replying to checksum queries.</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a87a7c6994c0d35bac361e5271f71823b2c9f2b0">a87a7c6</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/cb40a599b2f79b6777de5b8057338e88e8be8b40">cb40a59</a></dt>
<dd>dcache: update dcache-view version to 1.0.5</dd>
</dl>


Release 3.0.7

<h3 id="cleaner">cleaner</h3>

<p>The list of Delete Notification targets that the Cleaner will inform when a file’s content has been cleaned is admin-configurable.
In order to facilitate this configuration, the ‘show info’ command has been modified to also show Delete Notification targets.</p>

<h3 id="srm">srm</h3>

<p>The SRM code has been made more robust against races between file deletions and copies.</p>

<h3 id="systemtest">systemtest</h3>

<p>The ‘system-test’ script was updated to ensure anonymous dcap tests succeed.</p>

<h3 id="changelog3.0.6..3.0.7">Changelog 3.0.6..3.0.7</h3>
<!-- git log 3.0.6..3.0.7 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/a6c09328a14f65feeeef9fc5003fca5109829882">a6c0932</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.7</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4e2514735263439282d307e6685e9bf965a5bd1d">4e25147</a></dt>
<dd>cleaner: show delete notification targets</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4d707288a2004a02ff394e7f83042f8d9df8d60c">4d70728</a></dt>
<dd>systemtest: allow anonymous dcap activity</dd>

<dt><a href="https://github.com/dcache/dcache/commit/fa18be9a740b43d1f9d907a0205ffe86901e6a32">fa18be9</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/54038a326b3143254a020c60efde138ab58a4dea">54038a3</a></dt>
<dd>srm: fix recovery procedure in internal copy if source is deleted</dd>
</dl>


Release 3.0.6

cells

<p>Fixed a race condition and logging bug affecting cells relying on zookeeper. This
could affect location manager, space manager and pool manager.</p>

<h3 id="gplazma-ldap">gplazma-ldap</h3>

<p>Wrong quoting of two gplazma property strings could occasionally cause IllegalArgumentExceptions to be thrown when using LDAP-based logins. This problem has now been fixed.</p>

<h3 id="locationmanager">locationmanager</h3>

<p>Fixed a problem in Location Manager in which it would fail to shut down
and could leave two overlapping connectors running.</p>

<h3 id="pool">pool</h3>

<p>The process of deleting files on pools has been made more robust against potential problems. This further decreased the likelyhood of repository corruption during file deletion.</p>

<p>This release improves transactional stability of the built-in Berkeley database in pools.</p>

<h3 id="srmclient">srmclient</h3>

<p>SRM Client v1 received improved error handling. Most noticeably, expired credentials no longer cause a RuntimeException but an IOException.</p>

<h3 id="changelog3.0.5..3.0.6">Changelog 3.0.5..3.0.6</h3>
<!-- git log 3.0.5..3.0.6 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/92c752dab7db95ef2acb3fe187e1df89fd892051">92c752d</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.6</dd>

<dt><a href="https://github.com/dcache/dcache/commit/52becab9cb3b8e2f2d98f559c32b53eae4895816">52becab</a></dt>
<dd>pool: Fix race and nested transaction problem during deletion</dd>

<dt><a href="https://github.com/dcache/dcache/commit/cc8eb746b46d88c26e267b526a3c5e331b9bb437">cc8eb74</a></dt>
<dd>pool: Fix transactional behaviour with Berkeley DB</dd>

<dt><a href="https://github.com/dcache/dcache/commit/042c8efb80345a9cf492c3be73af3e23e23ed80b">042c8ef</a></dt>
<dd>lm: Fix lost thread interrupt that prevents shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b3d670f30ca5582fcd596bf1fab0aea6dbb62907">b3d670f</a></dt>
<dd>cells: Schedule watcher notifications on cell event thread</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b0bab0c4a482a737cbaeffc94a07db3ad61cdfe9">b0bab0c</a></dt>
<dd>gplazma-ldap: fix default properties for root and home</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a21d861e661f303e097dabfbcaf34287b2db63e5">a21d861</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ecdf153644fe1a80a92ddf4fadf1f103cf1724e6">ecdf153</a></dt>
<dd>srmclient: consolidate credential expiry, don’t use RuntimeException</dd>
</dl>


Release 3.0.5

<h3 id="frontend">frontend</h3>

<p>Included a new version of dCacheView with minor improvements.</p>

<h3 id="nfs">nfs</h3>

<p>The handling of NFS requests for offline files has been improved.
Such requests will no longer attempt unneccessary retries.</p>

<h3 id="changelog3.0.4..3.0.5">Changelog 3.0.4..3.0.5</h3>
<!-- git log 3.0.4..3.0.5 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/6b4ef4c641b21ff8c838c6dc7138f92d16f8423e">6b4ef4c</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.5</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0b6d777e45ede71e7d05424deeb462948e17bc85">0b6d777</a></dt>
<dd>dcache: update dcache-view version to 1.0.4</dd>

<dt><a href="https://github.com/dcache/dcache/commit/123b47c187b185985db6b2df51c508dfe8b29b13">123b47c</a></dt>
<dd>resilience: fix fairness algorithm bugs in file operation map</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3c04c2d566a3964198d06b797211a6334b3b1ecc">3c04c2d</a></dt>
<dd>nfs: rework pool selection to get rid of too many retries</dd>

<dt><a href="https://github.com/dcache/dcache/commit/61e8ed1a6ac1aa799682413f98a9011805f095f9">61e8ed1</a></dt>
<dd>minor typo corrections</dd>

<dt><a href="https://github.com/dcache/dcache/commit/44ad5c2190f04e64c10fdb384ac261f2663516f4">44ad5c2</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.4

<h3 id="dcache">dcache</h3>

<p>The current release updated dcache-view version.</p>

<h3 id="pool">pool</h3>

<p>In the current release changes <code>hsm ls</code> command so that it lists all configured HSMs if no argument is provided.</p>

<p>The current release fixed URISyntaxException in ceph backend.</p>

<h3 id="poolmanager">poolmanager</h3>

<p>Ability to restrict staging to specific protocol was missing in
stage protection specification. Additionally it was not possible to
specify DN, FQAN, storage group and protocol that are not allowed
to stage. </p>

<p>This is now fixed and stage protection configuration can be used as a blacklist. </p>

<h3 id="changelog3.0.3..3.0.4">Changelog 3.0.3..3.0.4</h3>
<!-- git log 3.0.3..3.0.4 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/21783c203290401434c8ec1830a612420854cf80">21783c2</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.4</dd>

<dt><a href="https://github.com/dcache/dcache/commit/531430143a8b7619be5255d883c1167716b46faa">5314301</a></dt>
<dd>stage protection : minor correction for test to pass</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9882a8f85bae8f4a27922ec5f589d75343eabc59">9882a8f</a></dt>
<dd>3.0 compatibility changes for stage protection</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1f7e1c2259189fd3ee4f56f01c55b2f7e1124155">1f7e1c2</a></dt>
<dd>pool: fix URISyntaxException in ceph backend</dd>

<dt><a href="https://github.com/dcache/dcache/commit/df629f2a200595ba8f7aff86115dc7b70b474074">df629f2</a></dt>
<dd>PoolManager : stage protection add protocol to the list of discriminators</dd>

<dt><a href="https://github.com/dcache/dcache/commit/26c0f5fe582d40570a4e5a4e9cacc121b1b9304f">26c0f5f</a></dt>
<dd>dcache: correct the output directory</dd>

<dt><a href="https://github.com/dcache/dcache/commit/efd258c78f71f5d5a0b94abb929114d3c49800d9">efd258c</a></dt>
<dd>dcache: update dcache-view version</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c850ff0185b0afb0093f11feb342ee8beccd0436">c850ff0</a></dt>
<dd>pool: ‘hsm ls’ must show all configured hsm if no argument is provided</dd>

<dt><a href="https://github.com/dcache/dcache/commit/03d34348b933584a293bd7dd8b1c8db31140cab4">03d3434</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.3

<h3 id="cells">cells</h3>

<p>The current release fixed an issue causing doors to log a stack trace on startup.</p>

<h3 id="nfs">nfs</h3>

<p>Remote I/O error was generated on the client side accompanied by stack trace on server side when user fumbled .(get) command.
The is fixed now and client side sees no such file or directory error and no stack trace in log file.</p>

<h3 id="srmclient">srmclient</h3>

<p>The current release fixed out of memory issue for <code>srmls -l</code>
 showing particular directory. </p>

<h3 id="srm-common">srm-common</h3>

<p>The current release improved user experience by ensuring that bugs and JVM-critical errors
do not trigger a retry of the operation, but favour a fail-fast approach.</p>

<h3 id="transfermanager">transfermanager</h3>

<p>The output of <code>info</code>, <code>queue</code>, <code>ls internal</code> and <code>ls external</code> admin
commands in RemoteTransferManager has been improved.</p>

<h3 id="changelog3.0.2..3.0.3">Changelog 3.0.2..3.0.3</h3>
<!-- git log 3.0.2..3.0.3 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/e0c5ab97e03e28f39159a9b395dacafbff0f082c">e0c5ab9</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.3</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a832e715757f3162976d67852bf8f8cb7044a7a5">a832e71</a></dt>
<dd>srm-common: don’t retry when JVM runs out of memory</dd>

<dt><a href="https://github.com/dcache/dcache/commit/104d79a50629106d1dc6d4fd32a4d887740e2865">104d79a</a></dt>
<dd>transfermanager: tidy up output from ‘info’ ‘queue’ and the two ‘ls’ commands</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c814f545ad6cc82bb4243eaf20b32f05787f79fb">c814f54</a></dt>
<dd>cells: fix ‘This stopwatch is already stopped’ error</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3859a07e893ec0732478eb6fca1ae82723a14c0c">3859a07</a></dt>
<dd>srmclient: use streaming deserialisation, allow more memory.</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a1e2ffbb2da27a26b9ef724010c7762e8fe7e318">a1e2ffb</a></dt>
<dd>chimera-enstore: specify fields order on insert</dd>

<dt><a href="https://github.com/dcache/dcache/commit/90021ddb961b4d168bcd1a45f35f91404d299bce">90021dd</a></dt>
<dd>NFS: throw FileNotFoundHimeraFsException in case of fumbled “.(get)” command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8768838d79c9c7e6e7dec803aee6ed199291ee6e">8768838</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.2

<h3 id="cleaner">cleaner</h3>

<p>Users reported that they wanted to see space freed up by cleaner processes
to be reported as free as soon as possible. This patch sends notifications
about freed up space more often, resulting in quicker status updates.</p>

<h3 id="doors">doors</h3>

<p>Log when the list of auto-discovered NIC interfaces changes. Support
logging the time taken to acquire NIC information. Update logged
messages to indicate the context.</p>

<h3 id="nfs">nfs</h3>

<p>The NFS implementation was updated, improving spec compliance.</p>

<h3 id="pool">pool</h3>

<p>A problem was fixed that could cause the csm check to fail on pools
containing broken files.</p>

<p>When deleting files, the cleaner submits batches of files to delete to a pool,
but this batch is then processed sequentially. In order to improve deletion
performance, such deletion tasks are now run concurrently. The
increase in concurrency can reduce the overhead of syncing the meta data to
disk after every deletion, thus increasing the deletion rate.</p>

<h3 id="srmclient">srmclient</h3>

<p>While srmfs’s ‘-debug’ option already provided lots of information,
including the SOAP request sent to the server, it did not provide
the server’s response until now. This has been added, making
troubleshooting easier for some problem classes.</p>

<p>The SRM client has been updated to work correctly if it has been
installed in a path containing spaces.</p>

<p>Glob expansion in SRM client has been overhauled, allowing much faster namespace operations on DPM when globbing is in use.</p>

<p>srmfs would not work with paths that require special characters to be percent-encoded.
This included path names with spaces or hash symbols. After this update to srmfs,
such path names are permissible and all namespace operations and file transfers on them
will succeed.</p>

<p>srmfs now accepts single commands directly as command-line arguments, e.g.
‘srmfs srm://srm.example.org/path ls’</p>

<p>Exiting will block if there are ongoing transfers. Notifications are
printed, which should provide feedback on activity.</p>

<p>The user can force an exit by using Ctrl+C, which will still result in a
clean exit.</p>

<h3 id="changelog3.0.1..3.0.2">Changelog 3.0.1..3.0.2</h3>
<!-- git log 3.0.1..3.0.2 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/6a23d46c2816ab6a6a10a9b6bdaeee063d63a8db">6a23d46</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.2</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a2f59a5a6ecef7b81a03ece8b34d566537b495ed">a2f59a5</a></dt>
<dd>nfs41: fix open-stateid leak introduced in 0702d73</dd>

<dt><a href="https://github.com/dcache/dcache/commit/affa1b49169430b7f5e597b45a87ba50b37c47ac">affa1b4</a></dt>
<dd>srmclient: support srmfs with command on command-line</dd>

<dt><a href="https://github.com/dcache/dcache/commit/97f2f8dc875cd59b917d4218b407eb412c40c399">97f2f8d</a></dt>
<dd>srmclient: show SOAP response from server when debug enabled</dd>

<dt><a href="https://github.com/dcache/dcache/commit/842f8f0b877bd7e92513accaba0364f7838faf41">842f8f0</a></dt>
<dd>srmclient: percent-encode paths that require it</dd>

<dt><a href="https://github.com/dcache/dcache/commit/20ffed08900fdff25088d67bfdc12f77c4a42399">20ffed0</a></dt>
<dd>srmclient: fix stat/ls caching for glob expansion for DPM</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d2d4b4c38f18d303af1d3b027a26673f492904c2">d2d4b4c</a></dt>
<dd>srmclient: fix deploying srm-client in path with spaces</dd>

<dt><a href="https://github.com/dcache/dcache/commit/192462c23afe29cac5cac5896171b60c1eff29b1">192462c</a></dt>
<dd>srmclient: fix Java 7 compatibility for srmfs</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ba8b836c2040e5ff7e4520547270e1ae046b863e">ba8b836</a></dt>
<dd>doors: add diagnostic information for NIC auto-discovery</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8a8b83d8d3b6e752c21e1e1cf51c13b75bfed4ba">8a8b83d</a></dt>
<dd>pool: Delete files concurrently</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8d77acc785997229b7dfb98daeaf81bf0ed72ddf">8d77acc</a></dt>
<dd>cleaner: Send notification more often</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7a542d2542e7d9c331cfd9bf7138c45ece277dbc">7a542d2</a></dt>
<dd>pool: Fix csm check command in the pressence of broken files</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1fdb6438d11e6abab029e7a3e533f05df40470bc">1fdb643</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a6f5d401a37d1f52180b2d1409ce718c7c9c87be">a6f5d40</a></dt>
<dd>nfs: discover open-stateid during layout return</dd>
</dl>


Release 3.0.1

<h3 id="cells">cells</h3>

<p>The current release improves reply handling in batch processing.</p>

<h3 id="ftpclient">ftpclient</h3>

<p>The current release improves compatibility between dCache FTP client and Globus GridFTP
server.</p>

<p>The dCache GridFTP client was not working with Globus FTP server. This is now fixed.</p>

<h3 id="pool">pool</h3>

<p>The current release introduces a new pool.mover.nfs.thread-policy property, which add a spossibility to control<br>
nfs request processing policies.
dCache admins could choose one of the strategies for nfs request processing.<br>
Please note, that by default the request processing policy is set to same-thtead strategy.</p>

<h3 id="srmclient">srmclient</h3>

<p><code>srmfs</code> was issuing <code>SRM</code> requests that <code>DPM</code> did not accept. <code>srmfs</code>
also did not accept the responses from DPM. This was preventing any file
transfers for succeeding.
This is now fixed and srmPrepareToGet and srmStatusOfGetRequest operations work as expected with DPM.</p>

<p>The two <code>ls</code> commands (<code>lls</code> and <code>ls</code>) was not supporting multiple
arguments or glob expansion. Both were taking an optional, single
argument, which was limiting while discovering what content is
available and was not matching the expectation of the users.
The current releases fixes this limitation and Multiple arguments and glob expansion are now supported for the <code>ls</code> and <code>lls</code> commands.</p>

<p>Correct information displayed about directories from DPM.</p>

<p>This release of dCache improves the readability of the error returned to the client when server declines to add an explanation.</p>

<h3 id="changelog3.0.0..3.0.1">Changelog 3.0.0..3.0.1</h3>
<!-- git log 3.0.0..3.0.1 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/0f643c0d9f2f22035d1700180fbd660858eaee17">0f643c0</a></dt>
<dd>[maven-release-plugin] prepare release 3.0.1</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3e2e814afb5acf88508c89abe84f30db57bf0fcf">3e2e814</a></dt>
<dd>cells+dcache: fix Reply handling in batch processing</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9f5745f82bbf50a4220a9ab598adc622b59181a4">9f5745f</a></dt>
<dd>ftpclient: fix compatibility with Globus FTP server</dd>

<dt><a href="https://github.com/dcache/dcache/commit/16706228a76825ec156ffe1dcaa85c33d077ff30">1670622</a></dt>
<dd>pool: optimize checksum channel calculation</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b6f591c0dfffaa7c339d61dc97ef726be48fc03b">b6f591c</a></dt>
<dd>pool: simplify checksum channel logic</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a2375f18fa0f39a12961b360179b6c3c381b2a3f">a2375f1</a></dt>
<dd>srmclient: ensure a reasonable error message</dd>

<dt><a href="https://github.com/dcache/dcache/commit/330e9f5b15523a59d1eb63013620c65681e0d66d">330e9f5</a></dt>
<dd>srmclient: fix DPM compatibility with SRM transfer requests</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6d7b7e604ba7fce08a050e2507e5621ec51b057d">6d7b7e6</a></dt>
<dd>ftpclient: fix multiline ADAT reponses</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9abf787ee0fe1bb6b75ef6b31ab6df42ee9ec018">9abf787</a></dt>
<dd>ftpclient: encrypt SITE CLIENTINFO command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7279b09222d9e9c7ee261029724795f61f66fe9d">7279b09</a></dt>
<dd>pool: add a possibility to control nfs movers threading policy</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8db0380b833cb3d50f8ca3ef3d06ac311172a942">8db0380</a></dt>
<dd>srmclient: add glob support for lls and ls</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8cb2378d60aaa3c9ce1782edf1bcdf48ee1aa99f">8cb2378</a></dt>
<dd>srmclient: avoid NPE when stat directory with DPM</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d12117ab68ab1c0f27652bbfe48317bae6cfb32e">d12117a</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>


Release 3.0.0

<p>The most obvious change is the transition to a new versioning scheme
that better reflects our existing release and compatibility policy.</p>

<p>Once a year, dCache.org releases a golden release. The golden release
maintains compatibility with pools of the previous golden release and
any intermediate version. The release after the golden release drops
compatibility with pools older than the golden release it surpasses.
The new versioning scheme reflects the incompatibility by incrementing
the major version number in the release <em>after</em> a golden release. Thus
the golden release marks the last release of a particular major
version. Like before, patch level releases are identified by a third
number in the version.</p>

<p>As always, this dCache release contains many internal changes, many
performance improvements and many cosmetic changes that will not be
explicitly described in the release notes. The changelog at the end
contains the complete list.</p>

<p>As always in a release after a golden release (an .0 release in the
new versioning scheme), configuration properties previously marked
obsolete have been dropped. Configuration properties previously marked
deprecated are now obsolete. You should run <code>dcache check-config</code>
before upgrading and fix any warnings. Rerun <code>dcache check-config</code>
after upgrading.</p>

<p>The following are noteworthy changes or changes that you as an admin
should know about when upgrading. The changes are described in no
particular order.</p>

<h4 id="admin:nolongersupportsdsakeys">admin: no longer supports DSA keys</h4>

<p>Upon upgrade, the post installation script will automatically generate
RSA keys instead. Your ssh client may warn you about the changed
server key. The <code>admin.paths.dsa-host-key.private</code> and
<code>admin.paths.dsa-host-key.public</code> properties are obsolete.</p>

<h4 id="automaticdetectionofcurrentpostgresqlmaster">Automatic detection of current PostgreSQL master</h4>

<p><code>dcache.db.host</code> and derived properties now accept a comma separated
list of host names when used with PostgreSQL. This is intended for use
with a cluster of PostgreSQL servers using streaming replication. The
JDBC driver automatically detects and uses the current master
server. In case a slave is promoted to master, the JDBC driver
automatically discovers and reconnects to the new master without
requiring a dCache restart.</p>

<h4 id="canl2.1">caNl 2.1</h4>

<p>Although this change should be transparent, the update of the Common
Authentication Library, the Bouncy Castle cryptographic library, the
ARGUS library, and the VOMS library is critical and you never
know if this breaks something. Keep an eye out for CA and client
problems.</p>

<p>On the positive side, this upgrade allowed us to update the Apache
SSHD library which hopefully fixes a number of compatibility problems
observed with some Python SSH libraries.</p>

<h4 id="billing:emptyformatstringssuppressesoutput">billing: empty format strings suppresses output</h4>

<p>Previously, if a formatting string was undefined, billing records would
be logged using a default format. This has been changed such that
billing records with an undefined or empty formatting string are not
added to the billing file. This allows specific record types to be
suppressed.</p>

<h4 id="billing:makebillingfilesself-describing">billing: make billing files self-describing</h4>

<p>Upon startup or when rolling over to a new billing file, the billing
service now outputs formatting instructions to the billing file. These
are lines starting with <code>##</code> followed by the message type and the
configured formatting string. Parsers may make use of the
instructions to recognize the format. At the very least, third party
parsers should be updated to ignore lines starting with a hash symbol.</p>

<p>The billing indexing utility has been updated to recognize these
formatting instructions and thus can parse the billing files even when
the output format is changed and billing files thus contain a mix of
different formats.</p>

<p>Configuration properties with the common prefix
<code>billing.parser.format</code> were added to define the default format for
old billing files without formatting instructions. Thus the output
format can be changed while still maintaining compatibility with old
billing files.</p>

<h4 id="billing:exposefulladdressinbillingrecord">billing: expose full address in billing record</h4>

<p>Previously, some billing records were logged with a full cell address
while others only included a cell name. The default format retains
this behaviour, however the full cell address is now exposed in the
formatting string. The cell name and domain name are also exposed
separately, making it possible to output these as separate
fields. Check the instructions in <code>billing.properties</code> for details.</p>

<h4 id="billing:makeservicereplicable">billing: make service replicable</h4>

<p>It is now possible to add multiple billing services if all components
(including pools) have been updated to version 3.0. All instances of
<code>billing</code> receive all billing records.</p>

<p>Introduced <code>dcache.queue.billing</code> and <code>dcache.topic.billing</code>
properties and marked <code>dcache.service.billing</code> obsolete.</p>

<h4 id="setupfilesarenowrestrictedtosetupcommands">Setup files are now restricted to setup commands</h4>

<p>The setup files of various services, in particular <code>poolmanager.conf</code>
and <code>setup</code> on pools, are now restricted to setup commands. These are
the commands the services themselves use when generating the setup
files. Previously any cell command could be included, even though the
command would be lost when the setup file was regenerated.</p>

<h4 id="setupfilesyntaxisnowcheckedbeforeitisloaded">Setup file syntax is now checked before it is loaded</h4>

<p>When reloading a setup file at runtime using the <code>reload</code> command, the
file is now checked for syntactic errors before being applied to the
running service. If an error is found, the file is not loaded and the
service is unaffected. Previously, such errors would leave the service
in an inoperable state.</p>

<h4 id="legacycelltopologysupporthasbeendropped">Legacy cell topology support has been dropped</h4>

<p>dCache 2.16 introduced the use of ZooKeeper for topology discovery as
well as the use of core domains as message brokers and satellite
domains connect to core domains. For backwards compatibility, 2.16
included the legacy UDP discovery service in <code>dCacheDomain</code> and
<code>dCacheDomain</code> was a core domain by default. This UDP service is no
longer included and compatibility with pools older than 2.16 has been
dropped. <code>dCacheDomain</code> no longer defaults to being a core domain and
it is in fact no longer a special name - you may call it whatever you
like.</p>

<p>This however means that unless you define some domain as a core
domain, none of your dCache domains will be connected and you will be
left with an inoperative dCache. If you haven’t already done so in
2.16, upon upgrade designate one of your domains as a core domain by
defining <code>dcache.broker.scheme = core</code> for it. Your former
<code>dCacheDomain</code> would be an obvious candidate for such a domain.</p>

<h4 id="lotsofimprovementstoservicelife-cyclemanagement">Lots of improvements to service life-cycle management</h4>

<p>We made lots of changes to the life cycle of dCache cells. These
changes are mostly internal, but the short story is that we try to
improve how dCache starts and in particular how it can cleanly shut
down.</p>

<p>In the past, clean shutdown wasn’t all that important as the service
would be inoperable anyway when shut down. With the addition of high
availability deployments, this assumption is no longer true and we
would like to be able to shut down cleanly. The goal has not been
achieved yet in dCache 3.0, as there are still plenty of issues
causing exceptions on shutdown, but the situation should be better than
in previous releases.</p>

<p>As an admin, the obvious change you will observe is that errors in the
log files have changed. In particular we log more stack traces when
detecting errors and we log cells that shut down slowly; even though
slow shutdown isn’t necessarily an error as many services now do more
work while shutting down.</p>

<h4 id="newwireprotocolforcellcommunication">New wire protocol for cell communication</h4>

<p>A new wire protocol for interdomain TCP connections for cell
communication has been introduced. This protocol has lower overhead
than the old protocol. Connections with 2.16 domains are detected
automatically and the old protocol is used as a fallback.</p>

<h4 id="dcap:fewerthreadsandfaster">dcap: fewer threads and faster</h4>

<p>The DCAP door was refactored. Compared to the earlier version it got:</p>


about half the number of threads than before,
reuse of threads to reduce the overhead,
detects client disconnects even if the door is busy,
the legacy feature to block a DCAP door by defining the <code>dcapLock</code>
 entry in the domain context has been removed.


<h4 id="spacemanager:improvedlatencyonnon-spacemanagertransfers">spacemanager: improved latency on non-spacemanager transfers</h4>

<p>Space manager is sort of a proxy for pool manager. When enabled, doors
send requests they usually would send to pool manager to space manager
instead. This had the effect of adding a little extra latency to all
transfers, even reads and unmanaged transfers.</p>

<p>The interaction between pool manager, space manager and doors has been
heavily refactored. One consequence is that the space manager can
inject its own behaviour into the doors. This allows the requests to
be sent directly to pool manager if it can be determined that space
manager is not involved in processing it.</p>

<h4 id="poolmanager:persistsetupfileinzookeeper">poolmanager: persist setup file in ZooKeeper</h4>

<p>The pool manager setup is now preserved across restarts even without
saving the setup to disk. This is achieved by persisting the setup in
ZooKeeper whenever it changes. Upon restart, the setup is loaded back
from ZooKeeper.</p>

<p>The consequence is that <code>poolmanager.conf</code> is only loaded when either
no setup can be found in ZooKeeper, or when the admin explicitly uses
the <code>reload</code> command. Restarting pool manager will not reload
<code>poolmanager.conf</code>. As before, the <code>save</code> command is used to update
<code>poolmanager.conf</code> and the file is not updated automatically.</p>

<p>This feature forms the basis of synchronizing the setup between
multiple instances of the pool manager in a high availability
deployment of dCache: Whenever the setup changes in one pool manager,
the setup is stored in ZooKeeper and other instances discover the
change and apply the update locally.</p>

<h4 id="poolmanager:persistpoolread-onlystatusinpoolmanagersetup">poolmanager: persist pool read-only status in pool manager setup</h4>

<p>When using the <code>psu set pool -rdonly</code> command to mark a pool as read
only, this restriction was not persisted in the pool manager
configuration file. Consequently, the read only status would be reset
by a pool manager restart.</p>

<p>The read only status is now stored in both <code>poolmanager.conf</code> and
in ZooKeeper and thus the read only status of a pool survives restarts.</p>

<p>Note that the read-only status in pool manager is a separate concept
from the <code>pool disable</code> state defined in pools.</p>

<h4 id="poolmanager:maketheservicereplicable">poolmanager: make the service replicable</h4>

<p>Pool manager is now a replicable service. This means one can create
multiple redundant instances of pool manager and the load will be
distributed over the available instances. The pool manager
configuration is synchronized through ZooKeeper. For a given set of
pool managers, a particular file is always processed by the same
instance.</p>

<h4 id="poolmanager:allowdecentralizedpoolselection">poolmanager: allow decentralized pool selection</h4>

<p>Pool manager has traditionally been the central place in which all
pool selection (assigning transfers to pools) has been performed. Pool
manager allows great flexibility in how this selection is performed,
including cost based replication, load and space triggered fallbacks,
staging from tape or to export pools, etc.</p>

<p>To accurately enforce the different selection strategies and the
various cost limits, it was essential that pool manager had a
complete picture of the load of all pools. Cost updates from pools are
only distributed every 30 seconds, so to obtain the necessary accuracy,
pool manager would update its internal cost estimates whenever it
selected a pool and it would also intercept messages between doors and
pools indicating the beginning and end of a transfer.</p>

<p>This model falls apart if pool selection is distributed over several
components as any adjustments to the internal cost state would be
local to the component selecting the particular pool. Such distributed
pool selection could be found in a high availability deployment of
dCache in which multiple redundant pool managers each perform pool
selection for a shard of the files. Another, not currently
implemented, scenario is delegating pool selection to doors to reduce
the latency of pool selection.</p>

<p>dCache 3 reimplements how the various cost limits of pool manager are
enforced. Rather than assuming that a pool manager has perfect
knowledge, pool selection is performed under the assumption of
reasonably, but not perfectly, accurate data. Whenever the pool
manager selects a pool it also encodes the <em>assumptions</em> under which
this pool was selected (e.g. load is below a certain threshold, pool
has enough free space, etc). This assumption is forwarded by the door
to the pool and checked by the pool before enqueuing a mover. If the
assumption fails, a cost update is prematurely submitted to pool
manager and the mover creation request is rejected. The door will
resubmit the pool selection request to pool manager, which now has
more accurate cost information.</p>

<p>This change is mostly invisible, although it may certainly affect the
dynamic behaviour of pool manager, replication and assignment of
transfers to pools.</p>

<p>By the way, the <code>cm info</code> command of pool manager has been removed as
there is nothing useful for it to report now. The commands <code>cm set
active</code>, <code>cm set update</code>, <code>cm set debug</code>, <code>cm set magic</code> are
obsolete. These should be removed from <code>poolmanager.conf</code> on upgrade.</p>

<h4 id="poolmanager:improvestabilityofhotspotreplication">poolmanager: improve stability of hot spot replication</h4>

<p>Pool manager can be configured to trigger replication of files when
the source pool exceeds a certain load threshold.</p>

<p>Unfortunately, the load was defined in terms of the average relative
queue length of the various mover queues on the pool, including the
queues of pool to pool transfers. Since pool to pool queues typically
(and wisely) have low limits, the relative weight in the load
calculation of pool to pool transfers is often high. The consequence
is that triggering a replication may itself push the calculated load
of the pool higher, triggering even more replications. This is bound
to generate an unstable system.</p>

<p>dCache 3 changes how the load of a pool is calculated to exclude the
two pool to pool queues as well as the HSM stage queue from the pool
calculation. Existing cost cut limits may have to be retuned as the
calculated performance cost has changed.</p>

<h4 id="pool:dropthelimitonpooltopoolreceivequeues">pool: drop the limit on pool to pool receive queues</h4>

<p>A pool has two queues dedicated to pool to pool transfers; one for
sending files and one for receiving files. The receiving end does not
limit the number of concurrent transfers to avoid deadlocks in pool to
pool transfers. For purposes of calculating a performance cost, the
pool did however define a limit anyway (as the load was determined as
the average queue length <em>relative</em> to the queue limit).</p>

<p>As described in the previous section, load no longer considers the
pool to pool queues and thus the unenforced limit on the receive queue
has been dropped. The pool <code>pp set max active</code> command has been
deprecated. The queued and max columns of the pool to pool receive
queue in <code>webadmin</code> and <code>httpd</code> are now empty.</p>

<h4 id="pool:logwhyamoveriskilled">pool: log why a mover is killed</h4>

<p>The pool has been extended with support for injecting a message when
killing a mover. Components and services that kill movers make use of
this feature to document why the mover was killed. This information is
included in billing and depending on the protocol it may also be
propagated to the client.</p>

<h4 id="pool:allowcontinuousflushingtotape">pool: allow continuous flushing to tape</h4>

<p>Traditionally, flush to tape on pools was batched by storage
class. Once a batch of files began to flush, new files arriving on the
pool would not begin flushing until the running batch would complete.
For HSM subsystems that do their own batching, the batching in dCache
is typically counterproductive as the driver or some external
component may wait for more files even though such files would be held
back by the pool to be included in the next batch.</p>

<p>To resolve this issue, dCache 3 adds an <code>-open</code> option to the <code>queue
define class</code> command in the <code>pool</code> service. This option alters the
logic such that newly created files are added to an existing batch
immediately.</p>

<h4 id="pool:supportpollingscriptswiththehsmscriptdriver">pool: support polling scripts with the HSM script driver</h4>

<p>The classic <code>script</code> HSM driver invokes an external script to flush,
stage or remove files from tape. Usually, this operation is blocking,
meaning that many concurrent instances of this script will run at the
same time.</p>

<p>Some clever admins have found a workaround for this scalability issue
by letting the script poll for the completion of the operation. Rather
than block, the script terminates with a failure. This relies on
dCache pools retrying HSM operations. This works well, except that it
fills the billing files and log files with error messages.</p>

<p>To support this type of script, dCache 3 extends the <code>script</code> driver
to recognize 72 as a special return code. When the script exits with
this return code, the driver places the request back into its queue
and retries it without propagating the error to dCache. The result is
that the operation is retried without spamming the log files and
billing files. The retry period can be configured using the new
-p:delay option.</p>

<p>Note that for flush, the retry triggered by exit code 72 is within the
same batch. Thus new files will not be added to the queue until the
batch completes, except if the flush queue is defined with continuous
flushing (see the <code>-open</code> option in the previous section).</p>

<h4 id="pool:alterfailuresemanticsforemptyfiles">pool: alter failure semantics for empty files</h4>

<p>When upload to a pool fails, the file is usually registered in the
name space like any other upload - if a checksum or file size was
predefined, the file may optionally be marked broken. In either case,
the file would be considered “complete” in the sense that no further
modifications to the file are allowed.</p>

<p>One common failure mode for uploads is when no data is uploaded at
all. This could be because the mover was killed before it could be
started, that is, while it is queuing; or because the client didn’t
connect to the mover; or because the mover failed to connect to the
client. Networking issues could be a common source of such
failures. Due to the failure semantics, such movers could not be
retried by the door.</p>

<p>In dCache 3 the failure semantics for such empty uploads has changed
such that the replica on the pool is instead deleted and not
registered in the name space. The name space entry is left in its
“virgin state”. Protocols like NFS and DCAP can open such files for
writing, allowing the upload to be retried.</p>

<p>Eventually, other doors will be updated to retry write mover creation,
but the current release doesn’t do that yet.</p>

<h4 id="pool:allowruntimemanagementofmoverqueues">pool: allow runtime management of mover queues</h4>

<p>Pools allow movers to be placed on queues. Several queues may be
created, e.g. to treat internal and external transfers differently, or
to queue transfers by protocol.</p>

<p>Previously, custom queues were defined using the <code>pool.queues</code>
configuration property, requiring a pool restart to change the defined
queues.</p>

<p>In dCache 3, the admin shell commands <code>mover queue create</code> and <code>mover
queue delete</code> have been added instead. The existing <code>pool.queues</code>
property is deprecated. The queue definitions are persisted to the
pool setup file when issuing the <code>save</code> command.</p>

<p>By the way, the unused <code>mover remove</code> command has been removed.</p>

<h4 id="pool:deprecatedcommandsforhsmlimitshavebeenremoved">pool: deprecated commands for HSM limits have been removed</h4>

<p>The deprecated <code>rh set max active</code>, <code>st set max active</code> and <code>rm set
max active</code> are no longer support in pool setup files. Use the
equivalent provider specific options instead. Upon upgrade we
recommend running the pool <code>save</code> command before upgrading - at least
if this has not been done since upgrading to 2.9.</p>

<h4 id="pool:optimizeberkeleydbmetadataupdates">pool: optimize Berkeley DB meta data updates</h4>

<p>The part of the pool abstracting file and meta data operations - the
repository - has been heavily refactored. One consequence is that
Berkeley DB updates are now transactional, improving consistency and
hopefully performance too as updates are batched together.</p>

<h4 id="pool:allowcephtobeusedasastoragebackend">pool: allow CEPH to be used as a storage backend</h4>

<p>One consequence of the heavily refactored repository component in
pools is that it has become easy to plug in alternative backends.
CEPH is a distributed block storage that has gained popularity in
recent years. In dCache 3, CEPH can be used as a backend for pools,
allowing the file data to be stored in CEPH. The meta data is kept in
the traditional Berkeley DB format.</p>

<p>See the documentation of the <code>pool.backend</code> property for choosing an
alternative backend. Several CEPH related properties starting with
<code>pool.backend.ceph</code> have been added. Consult the documentation in
<code>pool.properties</code> for details.</p>

<p>One consequence of the change is that HSM drivers can no longer expect
replicas to be stored as files on the local file system. Instead
replicas in a pool are now identified by a URI. When developing HSM
drivers or HSM scripts, this should be taken into
consideration. Backwards compatibility is however important to the
dCache team and as long as a local file system is used, the HSM driver
and HSM scripts are passed a regular path rather than a URI.</p>

<p>It has to be stressed that CEPH support is considered an experimental
feature. The more encouraging news is maybe that this shows that it is
fairly easy to hook alternate storage backends into dCache.</p>

<h4 id="pool:sortedlistingofmovers">pool: sorted listing of movers</h4>

<p>In the <em>nice to have</em> category, dCache 3 supports options in the
<code>mover ls</code> admin shell command to sort the output by mover’s last
access time and transferred data size.</p>

<h4 id="ftp:portdoortonetty">ftp: port door to Netty</h4>

<p>Netty is an non-blocking I/O framework used by xrootd doors and for
xrootd and http movers in pools. In dCache 3.0 ftp doors make use of
Netty too. This is pretty much transparent, but it allows the
door to scale to more concurrent connections with lower resource
usage.</p>

<p>By the way, we also upgraded to Netty 4.1 with buffer pooling enabled
- this should reduce Java garbage collection overhead.</p>

<h4 id="ftp:abortuploadifsrminvalidatesturl">ftp: abort upload if SRM invalidates TURL</h4>

<p>Previously, when the transfer URL generated by the SRM was invalidated,
either because it expired, the request was aborted, or the SURL was
deleted, the underlying FTP upload would be allowed to continue. The
upload would eventually fail when the last byte had been transferred,
wasting bandwidth and generating a misleading error.</p>

<p>This has been changed such that the SRM will kill an FTP upload when
it invalidates a TURL.</p>

<h4 id="srm:addedextrafieldstothesrmaccesslog">srm: added extra fields to the srm access log</h4>

<p>The srm access log contains a description of every client request. In
dCache 3, several extra fields have been added. In particular for
single file requests, the access log now contains the path of the file
to which the request applies.</p>

<h4 id="webdav:userelativelinksingeneratedhtml">webdav: use relative links in generated HTML</h4>

<p>The default templates for the HTML view of the <code>webdav</code> door now use
relative links. This should make it easier to use the door behind a
reverse proxy or load balancer.</p>

<h4 id="webdav:allowtemplatetobereloadedatruntime">webdav: allow template to be reloaded at runtime</h4>

<p>The <code>webdav</code> service generates the HTML view from admin configurable
template files. A <code>reload template</code> command was added to trigger the
template to be reloaded at runtime. The new
<code>webdav.enable.auto-reload.templates</code> configuration property may be
used to enable automatic reloading whenever the template changes.</p>

<h4 id="xrootd:selectmoverqueuebyapplicationname">xrootd: select mover queue by application name</h4>

<p>The <code>xrootd</code> door can now select a pool mover queue by client application
name. See the documentation of the <code>xrootd.app-ioqueue</code> configuration
prefix in <code>xrootd.properties</code> for details.</p>

<p>It should be stressed that the application name is submitted by the
client and is easy to fake.</p>

<h4 id="xrootd:recognizeoss.asizeparameter">xrootd: recognize oss.asize parameter</h4>

<p>Xrootd clients submit the file size upon upload as an <code>oss.asize</code>
property. dCache now recognizes this property and uses it in space
reservations, pool selection, and file verification. If the uploaded
file does not match the specified size, the file is marked as broken.</p>

<h4 id="nfs:autodiscoveryofnfs4domainforidmapping">nfs: autodiscovery of nfs4domain for idmapping</h4>

<p>For correct user id mapping nfs4 requires that server and client use
the same naming scope, called nfs4domain. This implies a consistent
configuration on both sides. To lower deployment overhead a special
auto-discovery mechanism was introduced by SUN Microsystems - a DNS
TXT record. Staring from version 3.0 dcache supports this discovery
mechanism. When <code>nfs.domain</code> property is set, it gets used. If it’s
left unset, then DNS TXT record for <code>_nfsv4idmapdomain</code> is taken or
the default <code>localdomain</code> is used when DNS record is absent.</p>

<p>See <a href="http://docs.oracle.com/cd/E19253-01/816-4555/epubp/index.html">nfsmapid and DNS TXT Records</a> for more information.</p>

<h4 id="nfs:improvedprotocolcompatibilityandstability">nfs: improved protocol compatibility and stability</h4>

<p>Nfs door now can share a single mover between multiple transfers to a
file by the same user coming from the same host. This should improve
compatibility with existing clients as they expect such behavior which
is allowed by nfs protocol specification.</p>

<h4 id="nfs:addedsupportforflexfilefilelayout">nfs: added support for flexfile file layout</h4>

<p>Flexfile layout type aims to be an extension to pNFS to allow the use of
storage devices in a fashion such that they require only a quite limited
degree of interaction with the metadata server. The RHEL 7.2 and it’s
derivatives are providing experimental support for flexfile layout
type. With this release, dcache starts to issue flexfile layouts if
requested by a client.</p>

<h4 id="addsupportforthehaproxyproxyprotocol">Add support for the HAProxy proxy protocol</h4>

<p>The <code>ftp</code>, <code>xrootd</code>, <code>webdav</code>, <code>srm</code>, <code>httpd</code>, and <code>frontend</code> services
have been extended with support for the HAProxy proxy
protocol. HAProxy or similar load balancers are essential components
of a high availability deployment.</p>

<p>These load balancers act as frontends for redundant services in
dCache. One problem of using such a proxy is that the real IP address
of the client is hidden from dCache, thus obscuring dCache log files
and hindering network based pool selection.</p>

<p>The HAProxy proxy protocol is an adhoc standard supported by many load
balancers and proxy servers. It adds a small header to the connection
between the proxy and the backend service revealing the IP address of
the client to the backend. The new configuration properties
<code>.enable.proxy-protocol</code> enable support for this protocol. <em>Note</em>:
Once enabled, direct access from client to the respective door must be
blocked as clients would otherwise be able to conceal their real address
to the service.</p>

<p>Check the documentation in the relevant default <code>.properties</code> files
for information of which versions of the proxy protocol are supported.</p>

<h4 id="newmechanismfordeterminingservicestomonitor">New mechanism for determining services to monitor</h4>

<p>The <code>httpd</code> service - both the old style and the newer <code>webadmin</code>
interfaces - monitor other services in dCache. The mechanism for
determining which services to monitor has changed. In the past the
list of services was configured in <code>httpd</code>; this has been replaced by
a multi-cast topic. Any service subscribing to this topic will be
monitored and shown in the web interface.</p>

<p>The name of the topic is defined by the property
<code>dcache.topic.watched</code>, although there shouldn’t be a need to change
this (maybe if one wants to partition the services to be monitored by
multiple <code>httpd</code> instances, one could consider introducing multiple
topics, but why one may want to do this eludes me). The important part
is that this is the topic a service should subscribe to if it should
be monitored. By default, <code>gplazma</code>, <code>pnfsmanager</code>, <code>poolmanager</code>,
<code>spacemanager</code>, and <code>srmmanager</code> subscribe to this topic. Doors and
pools are discovered through other means and are monitored despite not
subscribing to the topic.</p>

<h4 id="productionreadysupportforhighavailabilitydeployments">Production ready support for high availability deployments</h4>

<p>As may have been obvious from several of the changes above, lots of
work went into enabling high availability (HA) deployments with
dCache. Some benefits of such a deployment are:</p>


No single point of failures
Rolling updates
Horizontal scaling
Symmetric deployments


<p>For most parts, there isn’t much to configure for an HA deployment as
one can simply deploy several instances of the various services. There
are however several pitfalls, e.g. which databases should be shared
and which should not. Available documentation should be studied
carefully and any deployment should be tested before it is rolled out
on the production system.</p>

<p>Several external components are required for a true HA deployment to
load balance between doors (e.g. HAProxy) and handle HA for PostgreSQL
(repmgr).</p>

<p>Also, there are still a few components that do not handle redundant
deployments well, eg. resilience and replica manager. It may be argued
that redundancy of these components is not essential. </p>

<p>Controlled draining of services is currently not automated and
requires some knowledge of the inner workings of dCache. Although
support for HA may be production ready, it should currently be
considered an expert feature.</p>


<a href="http://github.com/dcache/dcache/commit/4e58e4c6377cd2ad3575975bef63c935fdd0760f">alarms: convert log entry handling to use plugin extensions</a>
<a href="http://github.com/dcache/dcache/commit/39306c2e6b0ca019296d6910c9672d6cd3fb6d5b">alarms: force alarms-only-option</a>
<a href="http://github.com/dcache/dcache/commit/f356de5326df4de0a473a913f4850609954d210e">dcache-restful-api: change protocol to HTTP</a>
<a href="http://github.com/dcache/dcache/commit/5d0825d197d13c0cc18c625e3ebdf023f96491cf">dcap: bump max command size sent by client to 8MB</a>
<a href="http://github.com/dcache/dcache/commit/b40b8bdc1a16d1eae0ca6ab723bd8484a2aa9b20">gplazma: Make gplazma.x509.use-policy-principals obsolete</a>
<a href="http://github.com/dcache/dcache/commit/09abff118fa2a255d77568e213ddf558584f7432">mespace/chimera: allow optionally disable move to directory having differnt storage class (and cache class)</a>
<a href="http://github.com/dcache/dcache/commit/135522e3b97a059d021b29a9e07b7445aa7b6e4d">pool: close dcap accepter thread and server socket after client connects</a>
<a href="http://github.com/dcache/dcache/commit/91d183227dd04796c197b3edbda83bdcc7dc4a5d">restful-api: add create, move and rename resources</a>
<a href="http://github.com/dcache/dcache/commit/3b355d122a16118b9df48571b60e5fd5afd34f78">webadmin: remove error and autorefresh options from alarms page</a>
<a href="http://github.com/dcache/dcache/commit/159c42257703d227583268b59dbd3066ec9570a9">webdav: add Spnego based Kerberos authentication mechanism for SSO capabilities</a>
<a href="http://github.com/dcache/dcache/commit/9969b3b7691f078ed985818b8543a2de5a50a67b">webdav: add cors support for uploading files</a>
<a href="http://github.com/dcache/dcache/commit/b3594f06a2dbe3cd0773f185d968a2063cef350a">webdav: add support for ownCloud mtime header</a>


<h3 id="changelogfrom2.16.0to3.0">Changelog from 2.16.0 to 3.0</h3>
<!-- git log 2.16.0..3.0 -no-merges -format='[%h](https://github.com/dcache/dcache/commit/%H)%n:   %s%n' -->
<dl class="dl-horizontal">
<dt><a href="https://github.com/dcache/dcache/commit/45fed81acea1e6e7e565bf9afebd8ff4b4bb7807">45fed81</a></dt>
<dd>srmclient: by default show only CN of owner in ‘ls -l’ output</dd>

<dt><a href="https://github.com/dcache/dcache/commit/10aa51cb3588c5c20ae9838ffa72e41cb24bbea3">10aa51c</a></dt>
<dd>resilience: python script for making database changes necessary for migration from old replica manager setup</dd>

<dt><a href="https://github.com/dcache/dcache/commit/12a45fa43215ba96781ffc72376621df85bf3908">12a45fa</a></dt>
<dd>pool: Reduce lock contention in migration module</dd>

<dt><a href="https://github.com/dcache/dcache/commit/564442eca96c72c34418b25316f17cee6f548ece">564442e</a></dt>
<dd>srmmanager: Adjust semantics of concurrent upload detection</dd>

<dt><a href="https://github.com/dcache/dcache/commit/90e8d7b99cb7b6496fa57f02385e24b8ccb4da85">90e8d7b</a></dt>
<dd>spacemanager: Fix shutdown bug causing a file to leak from a reservation</dd>

<dt><a href="https://github.com/dcache/dcache/commit/88ec2b3e27ebb9cfba59e04829322c75999ffdaf">88ec2b3</a></dt>
<dd>spacemanager: Fixes a message bounce bug</dd>

<dt><a href="https://github.com/dcache/dcache/commit/bd00ac70eadcfa9bd51b53617f61956146bed4ff">bd00ac7</a></dt>
<dd>srmclient: add SRM call statistics</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4f1d904864adad517073363ff1a47c095b34d548">4f1d904</a></dt>
<dd>srmclient: update command names in srmfs</dd>

<dt><a href="https://github.com/dcache/dcache/commit/71192e51db3d415a08448caa23bdb8a08a5e4650">71192e5</a></dt>
<dd>srmclient: fix srmfs ‘get permission’ command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/25c313e6e9f858461702778b3ee6eec4af6e588f">25c313e</a></dt>
<dd>srmclient: fix compatibility with Bestman</dd>

<dt><a href="https://github.com/dcache/dcache/commit/951fb06a1d45efbd240ec055b6db88adadb1312b">951fb06</a></dt>
<dd>srm: Sumbit token less releaseFiles requests to all backends</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0d6e02f2b54bc52b943808a3268aea7f486c8a61">0d6e02f</a></dt>
<dd>srmmanager: Support upload detection in clustered environments</dd>

<dt><a href="https://github.com/dcache/dcache/commit/28f79b6f7fc2c8e74ba57ae643ba95c7b7812666">28f79b6</a></dt>
<dd>srm: Redefine the semantics of active upload checks</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e320cee8c915ac80d7433d05373d0d8aad7f79fb">e320cee8c</a></dt>
<dd>srmmanager: Refactor how various operations handle active transfers</dd>

<dt><a href="https://github.com/dcache/dcache/commit/321a38000945a102f854b9a9c18cfd7bf4c1e6ea">321a380</a></dt>
<dd>srmclient: probe for SRM endpoint parameters that the user doesn’t specify</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2844429bae23b0249d5f06ffca9395e49cd4d43d">2844429</a></dt>
<dd>Resilience: separate out the data structures for handling storage units from those for pool groups</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ced428677e86a57ca3fc58dd13a54273d4e50f01">ced4286</a></dt>
<dd>Resilience: Support matching the universal and class default storage unit expressions</dd>

<dt><a href="https://github.com/dcache/dcache/commit/87b5e57f4f0165273c67a77808d87c2601c80406">87b5e57</a></dt>
<dd>dcap: don’t create stack-trace if tunnel fails due to bad client</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ce0b9e34dc6741da22a4ada2f27fe35feb39dcda">ce0b9e3</a></dt>
<dd>PoolManager : stage protection, fix error in stage.fragment</dd>

<dt><a href="https://github.com/dcache/dcache/commit/26fa950d6d102c83f51c35cc36b9d0c7bc9da4d0">26fa950</a></dt>
<dd>webdav: fix thrown NPE when CORS is set</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c44504431eb25d4e29b8a09b9c9de264f298ec82">c445044</a></dt>
<dd>dcap: expose dcap client version limit</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d60ec2666bb6c8dcb0c03ce2951edb09eee1ce95">d60ec26</a></dt>
<dd>dcap: Register DCAP interpreter as a command listener</dd>

<dt><a href="https://github.com/dcache/dcache/commit/833505725ba98e5b8bfc1b72d57c75ec36118bd0">8335057</a></dt>
<dd>dcap: fix Kerberos dcap if principal contains a ‘-’</dd>

<dt><a href="https://github.com/dcache/dcache/commit/fd7b21c3df4483fa353cbbb33b75a736b2296b20">fd7b21c</a></dt>
<dd>dcap: fix regression in handling old version</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1d14d809954c7f0ab36a627664fb363ef82fb297">1d14d80</a></dt>
<dd>cells: Fix NPE in location manager</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a1d7b4d41966de00e6ecae68064bb5ec088b3adb">a1d7b4d</a></dt>
<dd>srmmanager: Add interface to query and abort transfers</dd>

<dt><a href="https://github.com/dcache/dcache/commit/cee5a6a75925801033470e8b84dc590ce8545365">cee5a6a</a></dt>
<dd>cells: Remove resubmission to event thread in location manager</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5a082797bb2778aa27ab2eb392fd43bde339b53c">5a08279</a></dt>
<dd>cells: Add safe guards to connector create and process update events</dd>

<dt><a href="https://github.com/dcache/dcache/commit/cc9b845cb649db62afa8dbda699017a099d7c542">cc9b845</a></dt>
<dd>srmclient: fix ‘cd’ compatibility with StoRM</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c35fc89253468208c45168f2222d440a00b4642e">c35fc89</a></dt>
<dd>poolmanager: Log pool name rather than SelectPool object id</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b6855d43b7c1fe42d1221275e902641e5c0f663d">b6855d4</a></dt>
<dd>pool: Suppress two stack traces in nearline storage handling</dd>

<dt><a href="https://github.com/dcache/dcache/commit/802f2d8b5339306446b925345bc3e3e6c43a1acd">802f2d8</a></dt>
<dd>srm: Log correct request token in access log</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b75e224fe84b98e8f8a9dd7f5efd772a75750a9d">b75e224</a></dt>
<dd>httpd: Enable X-Forwarded-For processing in httpd</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4d5eed56f7a3d5209591df664e058d6162313a6f">4d5eed5</a></dt>
<dd>httpd: Don’t insist on using http for unauthenticated webadmin pages</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a671d74ff78ec34660de6d485587a4a1678da8ef">a671d74</a></dt>
<dd>nfs: allow dCache to start up without DNS</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ad802f85aec14b4b8079baff25165fd4d14913c0">ad802f8</a></dt>
<dd>srmclient: add initial support for glob expansion</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f7007f10e8a6a7184887356c066d7dfb392654b7">f7007f1</a></dt>
<dd>billing: fix stacktrace and slow shutdown if in refresh</dd>

<dt><a href="https://github.com/dcache/dcache/commit/13881625794c19c4ea8e1bb06474463384247de7">1388162</a></dt>
<dd>common: fix alignment of abbreviated byte column in ColumnWriter</dd>

<dt><a href="https://github.com/dcache/dcache/commit/dc23d883ee665b7666d9b024fbe07ed8aba0975e">dc23d88</a></dt>
<dd>cleaner: Send notifications concurrently</dd>

<dt><a href="https://github.com/dcache/dcache/commit/bb4f08bb0bd8f67294d50d837ddbdc03e0720823">bb4f08b</a></dt>
<dd>poolmanager,spacemanager: Do not reply to pool manager query replies</dd>

<dt><a href="https://github.com/dcache/dcache/commit/cb4133066ca64ea9550b7b549fd08f42ed76b476">cb41330</a></dt>
<dd>doors: Allow setting an empty list of login broker tags</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5abed5917d831e90842f795d61435ebbf12a8700">5abed59</a></dt>
<dd>dcache: Add column to <code>dcache services</code> for proxy-protocol</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2072783868433f1a1012e697bc3e6f04a9c65797">2072783</a></dt>
<dd>srmclient: add additional help text to srmfs</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6b9b5dbc27562b689c06fae66d817bdd76f79d43">6b9b5db</a></dt>
<dd>common: update ColumnWriter to remove any trailing whitespace</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b66123204174f2e0c639b953748704a4f232064b">b661232</a></dt>
<dd>spacemanger: Fix interception of PoolAcceptFileMessage</dd>

<dt><a href="https://github.com/dcache/dcache/commit/40314011506ed2015229f5edfcfbdb02272b57fc">4031401</a></dt>
<dd>xrootd: Upgrade to xrootd4j 3.2.1</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f6313084cc867c7a4ce3637c965c652a3c782995">f631308</a></dt>
<dd>admin: Send requests to a fully qualified address once connected to a cell</dd>

<dt><a href="https://github.com/dcache/dcache/commit/46e4e17a53a91f07cea9bbf0fc5f4e6e60c92b64">46e4e17</a></dt>
<dd>webdav: Fix initialization of html template</dd>

<dt><a href="https://github.com/dcache/dcache/commit/39a2baceb31d33a718c684b1dc666e4e1bf1f84d">39a2bac</a></dt>
<dd>common: do not markup ellipses as a user-value</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a6ad18ab900a1668fb84bedef5f73d3e0b9ad9e3">a6ad18a</a></dt>
<dd>frontend: reinstate support for truly anonymous access</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b567bc7b4c3f6ea6f768d7ad08162f23773df4d4">b567bc7</a></dt>
<dd>spacemanager: Propagate PoolManagerHandler errors as is</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b07f800b7879b265acf9e842f605f373168325e4">b07f800</a></dt>
<dd>dcache: Fix detection of message errors in doors and space manager</dd>

<dt><a href="https://github.com/dcache/dcache/commit/08d69d6328380f93a3e5452c64a64f5af8d9ce25">08d69d6</a></dt>
<dd>dcache: Fix detection of message errors in poolmanager and admin</dd>

<dt><a href="https://github.com/dcache/dcache/commit/54ba7fe3104575e34063fb29b612c60f26e2d8d5">54ba7fe</a></dt>
<dd>doors: Ensure that pool selection context survives between retries</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5458effef4c3d6030c2bc27cd84a446d801ba366">5458eff</a></dt>
<dd>poolmanager: Propagate subscriber failures</dd>

<dt><a href="https://github.com/dcache/dcache/commit/61f6ea2c4d7fcf97eace82a2e776b50a4b481162">61f6ea2</a></dt>
<dd>cells: Avoid an infinite loop when executing deferred tasks</dd>

<dt><a href="https://github.com/dcache/dcache/commit/494732c08f93c23bce4ff5d42866ef00d20cc33b">494732c</a></dt>
<dd>cells: Do not add source name when resending a message</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4be45bd6a0882adb86db5c94f74dedbe5c90fb72">4be45bd</a></dt>
<dd>srmclient: fix checksum mismatch when uploading small files</dd>

<dt><a href="https://github.com/dcache/dcache/commit/785680248fc05ec54534ceca4eb6ab085046ea4a">7856802</a></dt>
<dd>libs: update to nfs4j–0.13.0</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1f6e34794e8c6f20088b6af5dd5d44f13212b721">1f6e347</a></dt>
<dd>srmclient: fix srmfs to shutdown cleanly if user issues Ctrl-C</dd>

<dt><a href="https://github.com/dcache/dcache/commit/98fb6f6a0a27463a612b2c99c246c8ad343d7033">98fb6f6</a></dt>
<dd>srmclient: clean shutdown srmfs after transfer</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d93af74fd83305d91e13c3d4f9d6bcb1892e782e">d93af74</a></dt>
<dd>srmclient: avoid stack-trace if lcd with incorrect path</dd>

<dt><a href="https://github.com/dcache/dcache/commit/79db3472ecf06e4a1c7fafc929c1f8013584d7f9">79db347</a></dt>
<dd>Active Transfers: substitute ? for &lt;unknown&gt; on html pages</dd>

<dt><a href="https://github.com/dcache/dcache/commit/881a582aae8a507fddf77662dde13e3ae08701a0">881a582</a></dt>
<dd>dcache: Fix output of domain ports for ‘dcache ports’ command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/bffb2488241242c943d0ea59c79cebf02524b144">bffb248</a></dt>
<dd>dcap,ftp: Allow root path and socket address to be overridden for loginbroker info</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0a402301c95dbd94121d05ba8fc5d9ea277d2633">0a40230</a></dt>
<dd>cells: Minor optimization to routing manager when processing GetAllDomain requests</dd>

<dt><a href="https://github.com/dcache/dcache/commit/666ddf39a1e9025dac083c7cedc7dbd1246d3c48">666ddf3</a></dt>
<dd>cells: Kill tunnel earlier in case of IO failures</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f38f9067c3951b9a8a17a56fdcb150de4b2cd5af">f38f906</a></dt>
<dd>cells: Fix a couple of locking issues in the routing manager</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a274ac80a63670783a71ff7e8e5630faf582ff82">a274ac8</a></dt>
<dd>cells: Less aggressive use of stack traces on slow cell shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/290517d8a9fd5b87b0d8635fe36e3d53e282b0e2">290517d</a></dt>
<dd>cells: Fix race between publishing and killing a cell</dd>

<dt><a href="https://github.com/dcache/dcache/commit/603bbce4c6a4a005df0736d76d27381dbd2f85d4">603bbce</a></dt>
<dd>srmclient: give meaningful error message if credential is missing</dd>

<dt><a href="https://github.com/dcache/dcache/commit/07db10ce8581ac1a70f17c9db3d952bd60ccee6e">07db10c</a></dt>
<dd>common: add support for UserNamePrincipal as user:&lt;name&gt;</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b063e96c1126779169e10909931547f4bf6d7102">b063e96</a></dt>
<dd>srmclient: provide better error message if credential has expired</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a49cc502b4638d198eb9dbcdd3b758169f7eef19">a49cc50</a></dt>
<dd>Added ‘explain login’ examples to help text in Gplazma2LoginStrategy.java</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3e868c2031763e005b4f72092cbf8534711c02b0">3e868c2</a></dt>
<dd>info, webadmin: Check for null version</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3f56a0eefd58feb62d3335844e10caeab2857074">3f56a0e</a></dt>
<dd>httpd,srm,statistics: Parameterize billing service name</dd>

<dt><a href="https://github.com/dcache/dcache/commit/25292750d89d2b35058ec65ee2ea42c29e1dc122">2529275</a></dt>
<dd>billing: Strip format string from attribute name</dd>

<dt><a href="https://github.com/dcache/dcache/commit/90bc41c1ba9e9e4f5e5cb7da9913f137640c357a">90bc41c</a></dt>
<dd>transferObserverV1: replace Args with Joiner to construct transfers.txt lines</dd>

<dt><a href="https://github.com/dcache/dcache/commit/67dea34fb170d715ca5f051c9f2914536df91727">67dea34</a></dt>
<dd>billing: Make billing indexer work with custom format strings</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2b262f6c069943392cc6356b6d03000e80966e7a">2b262f6</a></dt>
<dd>cells: Fix NPE in unit tests</dd>

<dt><a href="https://github.com/dcache/dcache/commit/99babcdc6e60aae51e880dc4a108546b0ce74d1c">99babcd</a></dt>
<dd>dcache: update dcache-view version to 1.0.2</dd>

<dt><a href="https://github.com/dcache/dcache/commit/417887f9f5c47fcb6573bda59c1249143640ab4a">417887f</a></dt>
<dd>Revert “dcache: update dcache-view version”</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4d8d1221e2c39821456e4ef2e3c2636f3f6408a0">4d8d122</a></dt>
<dd>dcache: update dcache-view version</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e8d6d400798d19c9c539ee831cddfdba58bc5bdc">e8d6d40</a></dt>
<dd>dcap: add support for clients presenting more version metadata</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7c2fdda9dc0db35c8e7ed15da6791eea2c312445">7c2fdda</a></dt>
<dd>srmclient: update checkPermissions to be more robust</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5fb5f465e60f1110af80ff3b4d460baabd8fcd79">5fb5f46</a></dt>
<dd>srmclient: print friendly message on SRMException</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f74b140a616bf12134b464039a69e3979551acf0">f74b140</a></dt>
<dd>srmclient: update ls to be more robust</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0a50d58d7c3185c5631b23c2779c03ad1d016d1d">0a50d58</a></dt>
<dd>commons: log bugs with stack-trace and instructions</dd>

<dt><a href="https://github.com/dcache/dcache/commit/46f986c4ade14477fe1447c63c4088cf1c01ed7c">46f986c</a></dt>
<dd>webdav: support template reloading</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b3594f06a2dbe3cd0773f185d968a2063cef350a">b3594f0</a></dt>
<dd>webdav: add support for ownCloud mtime header</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8ade13437f5ca8b82d88a76bc8f526c9dfacb006">8ade134</a></dt>
<dd>gplazma2-xacml: remove erroneous creation of placeholder extensions</dd>

<dt><a href="https://github.com/dcache/dcache/commit/91d183227dd04796c197b3edbda83bdcc7dc4a5d">91d1832</a></dt>
<dd>restful-api: add create, move and rename resources</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a63ae6a00ebf66221bb911b89c69e74ffb8a7856">a63ae6a</a></dt>
<dd>cells: add event logging on cell lifecycle events</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8aff8524e0fbfb9ec5c1c3e3075cfcf65c163795">8aff852</a></dt>
<dd>srm: remove trailing dot from reverse lookup result</dd>

<dt><a href="https://github.com/dcache/dcache/commit/00d782e879d61fadd814b0135d22928b567bef93">00d782e</a></dt>
<dd>ftp: add support for SRM cancelling an active upload</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9969b3b7691f078ed985818b8543a2de5a50a67b">9969b3b</a></dt>
<dd>webdav: add cors support for uploading files</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c5aa25e91c8771ae1d3cce854edc545ba954d4ac">c5aa25e</a></dt>
<dd>srmclient: fix async stat command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/88a9fcf36ab69794f238a5284588fb679bd20e54">88a9fcf</a></dt>
<dd>srmclient: implement useful subset of local filesystem commands</dd>

<dt><a href="https://github.com/dcache/dcache/commit/03cca243d4f8557f6895fe5c0e18e8160cf1d6c4">03cca24</a></dt>
<dd>srmclient: fix error message for ls</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7ce53ee079f826f914d9cb0f926481f6990a1303">7ce53ee</a></dt>
<dd>srmclient: refrain from adding default port to SURL in srmcp</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9f084d5c5bcecc872677150dbfae5208569be26f">9f084d5</a></dt>
<dd>namespace: fix permissions of auto-generated directories</dd>

<dt><a href="https://github.com/dcache/dcache/commit/032f833c2a9481855fe262c5b1d3b9619168e02d">032f833</a></dt>
<dd>cells: New wire and payload protocols for cell message</dd>

<dt><a href="https://github.com/dcache/dcache/commit/61d575313055703d13088b40d50ad0647e0d946a">61d5753</a></dt>
<dd>cells: Minor paranoia refactoring in shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f6cdc1f1ddd53793df30394ca7411ce8226952f1">f6cdc1f</a></dt>
<dd>cells: Deliver cell events from the cell event thread</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3b2ca6f8406bc6f3979159ab2d4584a0ec4a0fee">3b2ca6f</a></dt>
<dd>poolmanager: Stop adjusting pool cost</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4a70ec140a774b85d2bbf16a0277cb3a276d9fef">4a70ec1</a></dt>
<dd>poolmanager: Define assumptions on pool selection</dd>

<dt><a href="https://github.com/dcache/dcache/commit/354aa1a37c5a5b442f14a3cd57a154d104c566fe">354aa1a</a></dt>
<dd>pool: Add infrastructure for pool assumptions</dd>

<dt><a href="https://github.com/dcache/dcache/commit/095f1f5ae494335c355c6f0ac80d38a9b395a65c">095f1f5</a></dt>
<dd>cells: Stop ZooKeeper recipies in stopping rather than stopped</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6f892035e463a9bdbed1031fddb10293eba7dad7">6f89203</a></dt>
<dd>poolmanager: Delay zookeeper publication of pool manager</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0d0ea8f3f4454370ae86856b393b5958f17358ac">0d0ea8f</a></dt>
<dd>cells: Minor cleaning of location manager</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c0ac545f7355db83a7f0fc866c2534c27845a27e">c0ac545</a></dt>
<dd>srmclient: fix -debug mode</dd>

<dt><a href="https://github.com/dcache/dcache/commit/05d3b56ff8bb2a89b7d2dae732d032b294ac8c59">05d3b56</a></dt>
<dd>srmclient: support SIGKILL</dd>

<dt><a href="https://github.com/dcache/dcache/commit/03afafa15b8b54a2b5b49f30a14dd9e8a1210e60">03afafa</a></dt>
<dd>cells: Guarantee event order for cell even listeners</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d5f1fdb00e66a45a037e33cef4ee8986333a9c65">d5f1fdb</a></dt>
<dd>cells: Remove race in routing manager</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2e9e81c88eec2c08c9e56792b68fcd555e2c644e">2e9e81c</a></dt>
<dd>poolmanager: do not use string concatenation with logging</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e3503f4ef205002382eeae12a9f16ec1743b3227">e3503f4</a></dt>
<dd>replicamanager: Fix race during shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/54b3a9c553005957f5b119e57f487312ca56cb59">54b3a9c</a></dt>
<dd>cells: Fix lost interrupt exception</dd>

<dt><a href="https://github.com/dcache/dcache/commit/bd87c3de71eb3fe065bebc47f4aab7ab548fb277">bd87c3d</a></dt>
<dd>cells: Ensure that newly created threads are non-daemon normal priority threads</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ff537569e2a2f0ecaeecd11f17e4f6f981221f4e">ff53756</a></dt>
<dd>webdav: fix Unauthorized vs Forbidden response</dd>

<dt><a href="https://github.com/dcache/dcache/commit/70f66028dd5fe16363cd65069414c5fe7d3727c1">70f6602</a></dt>
<dd>pom: Update third party dependencies</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ef0aaa1a13611c24f89805637db1daaaea6558b0">ef0aaa1</a></dt>
<dd>doors: Fix a minor race in LoginBrokerPublisher</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6d43a767375748dbc279e604343cf546d2273ca2">6d43a76</a></dt>
<dd>dcache: Fix more cells that do not shut down cleanly</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5809df2cc423ebd0556a3dad61a07fed2c2b9601">5809df2</a></dt>
<dd>cells: Add remote domain to NDC of location manager tunnel</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e96c0b22905f676b93c400e79cfa24affac05c6f">e96c0b2</a></dt>
<dd>cells: Increase timeout on tunnel shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ebfb1bca95454398f0fc5d1f5cac2730f45ba686">ebfb1bc</a></dt>
<dd>cells: Propagate startup failures to caller</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1509b2b6d0e1bfba7f155ff261de533318f406b5">1509b2b</a></dt>
<dd>cells: Fix race when adding routes</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e0b11957e6b213175cfa6791dee970ad335b2a51">e0b1195</a></dt>
<dd>cells: Remove delayed default route if tunnel shuts down</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c6358e3d7a3b48500a9751ab4fddf257d68d04f9">c6358e3</a></dt>
<dd>cells: Fix race in cell shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/bf563f9d8c11f327ba1e7b57cea63fea9e4d56ce">bf563f9</a></dt>
<dd>srmclient: add support in srmfs for uploading and downloading files</dd>

<dt><a href="https://github.com/dcache/dcache/commit/799698cb6493719f8ceb71277962df927719001a">799698c</a></dt>
<dd>poolmanager: Log errors in subscriber</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9f9bcfacce60ad45d64a36833a710359aaf20254">9f9bcfa</a></dt>
<dd>spacemanager: Revert decision to only import link groups in leader</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d0c35361e5b3a8d378f3496cf269cb088c70651e">d0c3536</a></dt>
<dd>dcache: Generate proper exit code for check-config command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a474a77ee177ddb29f1649feb85b1c2e63d68051">a474a77</a></dt>
<dd>spacemanager: Fix SpaceManagerHandler#toString</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0806d879175acef23ad8f848ddba785135e6d2e7">0806d87</a></dt>
<dd>doors: Prevent PoolMgrGetUpdateHandler storm on shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/077d1e5598dbe383c70f477f38faec1640b47620">077d1e5</a></dt>
<dd>pool: Drop pretend limit on p2p client queue</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3348726f05578b0406d6ed4d3eb992e804f992d2">3348726</a></dt>
<dd>poolmanager: Improve stability of cost cuts</dd>

<dt><a href="https://github.com/dcache/dcache/commit/53d185b7531ba347109fde239bbe94c4a2e87dc1">53d185b</a></dt>
<dd>cells: Refactor interaction between LocationManager and LoginManager</dd>

<dt><a href="https://github.com/dcache/dcache/commit/71796a5c0e7f861a4019df9ea6d28ceb12961bba">71796a5</a></dt>
<dd>cells: Fix potential deadlock in login manager shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3a251fdc427416befb8b98e7784cfdcfa47d9f45">3a251fd</a></dt>
<dd>cells: Fix regression in shutdown timeout</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a064ba90a41c2a19c155b826d0a1217081b7917c">a064ba9</a></dt>
<dd>srm: support configuring job expiry checking period</dd>

<dt><a href="https://github.com/dcache/dcache/commit/cc806ed16fd98bc496d460b4bdc94bfdb708d38b">cc806ed</a></dt>
<dd>gplazma2-ldap: add embedded jdap server for unit testing</dd>

<dt><a href="https://github.com/dcache/dcache/commit/05f327a3160857716b55305442346a86e4f191c7">05f327a</a></dt>
<dd>nfs4: autodiscover nfsv4 domain used by idmapper</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2fe6e945bc644dcb8ccd02a298355b3f9a27ab99">2fe6e94</a></dt>
<dd>commons: fix Args string parsing and toString method</dd>

<dt><a href="https://github.com/dcache/dcache/commit/355fc086fa9537efb94897e85ed856615225032a">355fc08</a></dt>
<dd>pool: ReplicaStoreCache updated to describe inner ReplicaStore</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c08f8fe37e6aa44f2446f58c744c380a339d8e79">c08f8fe</a></dt>
<dd>vehicles: use FileAttributes when creating namespace entries</dd>

<dt><a href="https://github.com/dcache/dcache/commit/366182bffc8fbee454745a820f23e50afe4ae453">366182b</a></dt>
<dd>Change version to 3.0.0-SNAPSHOT</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4fefd4d794bf6b82a4b2793187da93b635ebe4b4">4fefd4d</a></dt>
<dd>chimera: update postgres driver to recognize alpha/beta/rc builds</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9582a7107c5a56ff533d93cf120f0f1c6c9ba8f8">9582a71</a></dt>
<dd>ceph: make configurable rados pool name</dd>

<dt><a href="https://github.com/dcache/dcache/commit/459ddceb57fd74bbbcc065e97fbe4e2d87421bf3">459ddce</a></dt>
<dd>dcap: use String.getBytes(UTF_8) to generate error reply</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d509d7734224993ae63c5fe26bb0320622abce0e">d509d77</a></dt>
<dd>ceph: use object’s xattrs to store files creation and atime/mtime</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d56eee290930c6c96b5a1c5f23081d9d8d620f24">d56eee2</a></dt>
<dd>doors: Include IO queue in pool selection request</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a29ba61b15bcceb887c2b03da14e1e385c8ee143">a29ba61</a></dt>
<dd>ceph: cleanly close rados connection on pool shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5609c21e0f3b4be5aa4b0a0973d58284f48776ce">5609c21</a></dt>
<dd>ceph: use RadosClusterInfo to provide total and available sizes</dd>

<dt><a href="https://github.com/dcache/dcache/commit/cc4820052628fdc70e1283b77fd6db9d92aff159">cc48200</a></dt>
<dd>ceph: use PoolInfo to check repository status</dd>

<dt><a href="https://github.com/dcache/dcache/commit/59a0995336105c846ba6544ba5ff0b64b85f6958">59a0995</a></dt>
<dd>pool: added CEPH back-ended FileStore implementation</dd>

<dt><a href="https://github.com/dcache/dcache/commit/56363473cd37e9a1324d8c3c6bdec61bd0b248dc">5636347</a></dt>
<dd>nfs: addresses returned to client must match clients address ‘type’</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8a8a2abc648f99f519b420d04d07119d41b81422">8a8a2ab</a></dt>
<dd>nfs: add support for flexfile layout type</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a48496b47b1a360fb3c86bf3b920b35aad4aa205">a48496b</a></dt>
<dd>srm-manager: explain cancellation of upload</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e5068a1a89a1e93f53437b57addcbf143b77ac94">e5068a1</a></dt>
<dd>ftp: Fix unit test regression</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7bd08481e46be05ec2a77e3a44efce44482d7eac">7bd0848</a></dt>
<dd>cells: Drop some dead code</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c9d3b2c94005aecb024c28d6d02ba2dbf12bff12">c9d3b2c</a></dt>
<dd>cells: Add context information to connector cell</dd>

<dt><a href="https://github.com/dcache/dcache/commit/bede5c8dd1b7309aaf17f006462dca2fdba311ef">bede5c8</a></dt>
<dd>cells: Let tunnel shut down wait for its processing thread to terminate</dd>

<dt><a href="https://github.com/dcache/dcache/commit/182a655f873eb356ff991cce71a32ebcc318cbc3">182a655</a></dt>
<dd>cells: Add default methods to CellEventListener interface</dd>

<dt><a href="https://github.com/dcache/dcache/commit/78db8cf9762c3eb6ea7cd64d92cabe4b77c5e118">78db8cf</a></dt>
<dd>pool: Make inner class of PoolCostInfo static</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7727b2828c1fa49cf32b863def2ad7170a2cab58">7727b28</a></dt>
<dd>pools: Drop legacy field in PoolCostInfo</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9854e5d6924992d087edd8637daf10f10d2ff612">9854e5d</a></dt>
<dd>ftp: Add support for the HAProxy Proxy Protocol</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4a8bc2939f04d480c77c722053ae72628d51b5ff">4a8bc29</a></dt>
<dd>ftp: Port FTP door to Netty</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9f59b051d5582a158bb1ca4d452e1e715845038c">9f59b05</a></dt>
<dd>cells: Decouple StreamEngine from LoginManager</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c8a1a38d27274bc3e05fbf2ad3ee1c04b026a109">c8a1a38</a></dt>
<dd>xrootd: Add support for the HAProxy Proxy Protocol</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6c7692258c8e378f284ccb479d65f48211618b91">6c76922</a></dt>
<dd>xrootd,pool: Upgrade to Netty 4.1</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b0e85c63ee9e608175c2f1d1b4cfc26f764aabc9">b0e85c6</a></dt>
<dd>webdav: optimise directory creation</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f0918e2cbb55c6410524a0d9679890f9afe51ce1">f0918e2</a></dt>
<dd>vehicles: add fluent and single-item construction to FileAttributes</dd>

<dt><a href="https://github.com/dcache/dcache/commit/66127161810dca9836e9145c290ce059f2339cd9">6612716</a></dt>
<dd>cells: Fix more shutdown bugs and reject send with callback on shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2b0cbb4ba46986ba4eddf6fc030ebb1f48b809a4">2b0cbb4</a></dt>
<dd>cells: Use ConcurrentHashMap for callback objects</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f509447b990a022b2017bc6b37926750799cdefb">f509447</a></dt>
<dd>pool: Ensure that post transfer service shuts down before repository</dd>

<dt><a href="https://github.com/dcache/dcache/commit/135522e3b97a059d021b29a9e07b7445aa7b6e4d">135522e</a></dt>
<dd>pool: close dcap accepter thread and server socket after client connects</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5679b208e90f24c4c0f32e187b0b708d79f109a7">5679b20</a></dt>
<dd>pool: allow sort output of ‘mover ls’ by access time and size</dd>

<dt><a href="https://github.com/dcache/dcache/commit/26a2bd7d88b5444f7c35042aeba0b6d959ffda8d">26a2bd7</a></dt>
<dd>poolmanager,spacemanager: Do not log delivery failure of PoolMgrGetUpdatedHandler</dd>

<dt><a href="https://github.com/dcache/dcache/commit/04c5a8c138df8177631a7caa716e4b0ce741f0d8">04c5a8c</a></dt>
<dd>cells: Fix regression in message ID in replies</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c5770fd54f52ccf9f9a397830e2d8e9eb5b0023d">c5770fd</a></dt>
<dd>cells: Fix several shutdown related problems</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e7323a05327808c20d58b3639e763b6dd843bcce">e7323a0</a></dt>
<dd>dcache-webadmin: synchronize client-side filtering with server-side selection of rows on pages using picnet table filters</dd>

<dt><a href="https://github.com/dcache/dcache/commit/71034aaa796d1637de04143ffdb6175c09a6e719">71034aa</a></dt>
<dd>dcache-webadmin: disable saving table filter settings to browser cookies</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c8bc39dadabf82cdc05bde26d07da332b9cae3b1">c8bc39d</a></dt>
<dd>dcache-webadmin: disable AJAX autorefresh on pages using picnet table filter library</dd>

<dt><a href="https://github.com/dcache/dcache/commit/dea17649349faf48086d1f58578182ddf672dc25">dea1764</a></dt>
<dd>namespace: support querying information about deleted objects</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7318a65f1398a0f1bd205002ab69af178fee0947">7318a65</a></dt>
<dd>doors: include explanation when killing mover</dd>

<dt><a href="https://github.com/dcache/dcache/commit/249cb9927e8ef909ae1951d7156d7a4b1bacc689">249cb99</a></dt>
<dd>namespace: add nlink as an attribute</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f4e5691a5144f502cdb9e735d68a013818a5d9e4">f4e5691</a></dt>
<dd>pool: explain why a mover was killed</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ac50167d713d8991c4393de3a38208631b38f5d3">ac50167</a></dt>
<dd>alarms: reset count history on reopened alarm</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1eec7f572b729b2bcd41b7fb80a1a56a26720248">1eec7f5</a></dt>
<dd>pool: Resolved circular bean dependencies leading to bugs during shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/eb31c0e2b0e0aa857cbf2c5c9597d811deadd1da">eb31c0e</a></dt>
<dd>cells: Lowered log level of failure to deliver delivery failure notifications</dd>

<dt><a href="https://github.com/dcache/dcache/commit/bb4ddd170c3752bca5ab7b187f3630d8a37f3471">bb4ddd1</a></dt>
<dd>cells: Bind pre-removal notification to beforeStop lifecycle callback</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d16926e6c7b83a70c7c207984db32db2c47c7a70">d16926e</a></dt>
<dd>doors: Announce to login broker subscribers when a door is shutting down</dd>

<dt><a href="https://github.com/dcache/dcache/commit/83c62cab5a8ee32a41b5c6e4dd6a82d866992f14">83c62ca</a></dt>
<dd>cells: Log killer threads too when cell shutdown is slow</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4a2f9789b89b690a1498d4d1ffa783ca380036b0">4a2f978</a></dt>
<dd>cells: Log when cells have to interrupt threads to shut them down</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f2b6b24f4dcfabba38d5139987b2079774d3b999">f2b6b24</a></dt>
<dd>doors: Abort transfer if file is deleted during pool selection</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ef5ff6abb9d141a9181fa5864fb6e246e7833a2d">ef5ff6a</a></dt>
<dd>chimera: Fix IllegalStateException in inode cache</dd>

<dt><a href="https://github.com/dcache/dcache/commit/02c5b8b57d9e41fa33cdba7c9375294e8b741cd0">02c5b8b</a></dt>
<dd>poolmanager: Fix shutdown regression</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9d7493d6ecf517cfb8844364faf9bc567956efb7">9d7493d</a></dt>
<dd>cells: Add pre removal callback</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9f7752a3bebfc00735f9800ba27b217a3b514b85">9f7752a</a></dt>
<dd>cells: Ensure sequential execution of lifecycle callbacks</dd>

<dt><a href="https://github.com/dcache/dcache/commit/42d8ccf6dca961df154d60efa13505e3b6243575">42d8ccf</a></dt>
<dd>cells: Guard shutdown of setup manager against partial initialization</dd>

<dt><a href="https://github.com/dcache/dcache/commit/928548332d148454ba684160f4f717d01a76ae42">9285483</a></dt>
<dd>poolmanager: Fix design flaw in PoolManagerHandler implementations</dd>

<dt><a href="https://github.com/dcache/dcache/commit/98f293fefb53f5ba40ec6ce4756f196aca985825">98f293f</a></dt>
<dd>cells: Expose SendFlag to suppress addition of a source path</dd>

<dt><a href="https://github.com/dcache/dcache/commit/759a8974b628afd0b570d1d5b042be3b594aad5f">759a897</a></dt>
<dd>cells: Fix problem with duplicate entries in source path</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b43a7059fac47aa3b94d76059d1fef69dcb6816e">b43a705</a></dt>
<dd>Enable automatic detection of Postgresql master</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2c8ee66e6ea405926dc9bc91f200300735c574b4">2c8ee66</a></dt>
<dd>webdav,frontend: Drop support for https-jglobus</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5593c87cebc2e2335cf9baa19ee4b561891e9892">5593c87</a></dt>
<dd>webdav,frontend,httpd: Add proxy protocol support</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e69b0facb0dc0262c8fc3d370675390771936df6">e69b0fa</a></dt>
<dd>dcache: Extend CanlConnectorFactoryBean to also support plain connectors</dd>

<dt><a href="https://github.com/dcache/dcache/commit/285a673e0af0cfbc71847ca33bc309fd4294a4c0">285a673</a></dt>
<dd>nfs: Upgrade nfs4j</dd>

<dt><a href="https://github.com/dcache/dcache/commit/bbc5ea0090f85901284132b2e3e9da7de0af81b2">bbc5ea0</a></dt>
<dd>srm: make out-of-date historic data deletion more robust</dd>

<dt><a href="https://github.com/dcache/dcache/commit/dffe01a8b3189e6bd4dde48894daf70cb47cda34">dffe01a</a></dt>
<dd>srm: Add support for the proxy protocol</dd>

<dt><a href="https://github.com/dcache/dcache/commit/740f86374f5429409a1fb3e7a0eb640a5e2bebcb">740f863</a></dt>
<dd>cells: Do not call shutdown from message thread</dd>

<dt><a href="https://github.com/dcache/dcache/commit/65a044f811f6d252b5ae0b3d798c9d547b0ee580">65a044f</a></dt>
<dd>xrootd: Remove serialization compatibility with pre 2.11 domains</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6e240c28c6b8fcc744ebe3aadad80b1349c57d1d">6e240c2</a></dt>
<dd>dcache-vehicles: Remove serialization compatibility with pre 2.15 domains</dd>

<dt><a href="https://github.com/dcache/dcache/commit/16907b52d05acbd683e95165f253bdb3bd01611a">16907b5</a></dt>
<dd>dcache-vehicles: Remove serialization compatibility with pre–2.12 domains</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f8b06aa029e186393d2de2ddaf7b76a3ce0a6e78">f8b06aa</a></dt>
<dd>cells: Remove serialization compatibility with pre–2.16 domains</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c919c99159be5c3290600488daab83ad4e23c529">c919c99</a></dt>
<dd>pnfsmanager: Remove support for legacy pools</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2e255bb5ff4bba432e84bfbf04cfd40fe2eaf7a2">2e255bb</a></dt>
<dd>cells: Drop support for legacy route updates</dd>

<dt><a href="https://github.com/dcache/dcache/commit/73d67b87b9683214bbcdfea1d73bc27475c7e6f2">73d67b8</a></dt>
<dd>billing: Make service replicable</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b5974a8117fa4eaa81ca5846557c76d02e19db9f">b5974a8</a></dt>
<dd>webadmin: Use topic to discover services to watch</dd>

<dt><a href="https://github.com/dcache/dcache/commit/92b22f794d80e1a7b295286e1e8ecaff152a1d8a">92b22f7</a></dt>
<dd>httpd: Introduce topic for discovering services to monitor</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2a3e40165ed9934fb58531eafb5a0b8d9f464a54">2a3e401</a></dt>
<dd>zookeeper: avoid one race in shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ac036b40d7fe23622ae23b6e41cef24be2663e17">ac036b4</a></dt>
<dd>zookeeper: work-around slow shutdown of SessionTrackerImpl</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d3f34ae30a8e2e762c590267e5a3cfec38594640">d3f34ae</a></dt>
<dd>webadmin: silence warning about future change in wicket</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1ee61f9cb486ebe855c71a6738385b4cd6d2e19c">1ee61f9</a></dt>
<dd>poolmanager: Reduce risk of pool manager handler update during shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ee859847cb5add84f84290df193e7ef10e5b353e">ee85984</a></dt>
<dd>billing: Optimize regular expressions of billing parser</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b56ea8c2a9dbcb60d9f5b247d21151b08218d882">b56ea8c</a></dt>
<dd>billing: Minor optimizations to path prefix computation</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4f68ccb9ba8655a608b7aa15e36d37302d4a2f79">4f68ccb</a></dt>
<dd>billing: Extend billing parser to recognize formatting headers</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d9f086b3c09b56c8f5c2d14f2973c764fe8e4ef8">d9f086b</a></dt>
<dd>billing: Let ParallelizingLineProcessor consider comments as barriers</dd>

<dt><a href="https://github.com/dcache/dcache/commit/aa747393f70b2440847c4a8d4c6eec6c3191b4e8">aa74739</a></dt>
<dd>pool: Adjust JavaDoc of ReplicaStore</dd>

<dt><a href="https://github.com/dcache/dcache/commit/dd1f4932c5d61ffa8889af31ef230faf4c5a673a">dd1f493</a></dt>
<dd>billing: Make billing text files self describing with format headers</dd>

<dt><a href="https://github.com/dcache/dcache/commit/17556819468a3c40f0a99eff00d064aaa3c0fcab">1755681</a></dt>
<dd>billing: Do not log record if format string is empty or undefined</dd>

<dt><a href="https://github.com/dcache/dcache/commit/860122710279ef7444822b6dc4554e2a3f3f74e1">8601227</a></dt>
<dd>billing: Harmonize representation of cell name</dd>

<dt><a href="https://github.com/dcache/dcache/commit/86dd4fece833a7f999d344b5460398c8e5cd90eb">86dd4fe</a></dt>
<dd>cells: Prepare to change representation of unqualified cell addresses</dd>

<dt><a href="https://github.com/dcache/dcache/commit/92788e9103a8b4ed9ffc4d88706479ee371e79d9">92788e9</a></dt>
<dd>cells: Fix IllegalArgumentException when reversing a terminal cell path</dd>

<dt><a href="https://github.com/dcache/dcache/commit/618c3b6909191c54218a32aeb7529e4b708c3ea0">618c3b6</a></dt>
<dd>cells: Fix RejectedExecutionException during shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2954441c367a2ccc147b9602d31e14d0c4147b75">2954441</a></dt>
<dd>billing: Removing erroneous stack trace output</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a2fd0be43648e5a9c3415220456c1b50ccdfd000">a2fd0be</a></dt>
<dd>billing: Wrap cellName attribute to allow access to the cell and domain components</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a81dec3a23c0efeb1827df66913fbb77bc101eb2">a81dec3</a></dt>
<dd>xrootd: add support for oss.asize on upload</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e74520d891af8a3cf3c7f86b4ad5ee23c5a22e6c">e74520d</a></dt>
<dd>xrootd: add per-application io-queue</dd>

<dt><a href="https://github.com/dcache/dcache/commit/06a8baa0dc948c57db5e44d8178b8666bef0707e">06a8baa</a></dt>
<dd>pool: update FileStore interface to handle all back-end specific operations</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7d558aeef5b7ac87ab39af746764f961512fca35">7d558ae</a></dt>
<dd>ftp: improve compatibility with Apache Commons FtpClient</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7951b59309885436c8877a505e93cc614661d1a8">7951b59</a></dt>
<dd>srm: refactor container status update and readying turls</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ed44be40a408db62df8440278ba9021dd509f847">ed44be4</a></dt>
<dd>dcache-restful-api/pinmanager: modify current QoS fom disk+tape to tape</dd>

<dt><a href="https://github.com/dcache/dcache/commit/bd52f0ab88775e6bc277910b64105a310f07302a">bd52f0a</a></dt>
<dd>pool: Adjust failure semantics for empty client uploads</dd>

<dt><a href="https://github.com/dcache/dcache/commit/410c9d7217113e8b62282f47c6b23564db8e68c4">410c9d7</a></dt>
<dd>dcache-nearline-spi: Add @since tags for newly added features</dd>

<dt><a href="https://github.com/dcache/dcache/commit/07090fc4a1f1eb591a0607001bcedf1ba4b1ab15">07090fc</a></dt>
<dd>nfs: Fix pool manager subscriber startup</dd>

<dt><a href="https://github.com/dcache/dcache/commit/798b7b62d9caf815bded45a874c82d1e57b8fdf1">798b7b6</a></dt>
<dd>chimera,nfs: avoid byte -&gt; string -&gt; byte conversions</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4e58e4c6377cd2ad3575975bef63c935fdd0760f">4e58e4c</a></dt>
<dd>alarms: convert log entry handling to use plugin extensions</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f8fcd311e08a825c514040b53e0aa07da94b3bbb">f8fcd31</a></dt>
<dd>pom: Update 3rd party dependencies</dd>

<dt><a href="https://github.com/dcache/dcache/commit/27c8720e153785e312b5aff98b98b6bb796bec82">27c8720</a></dt>
<dd>srm: Include session identifier in error message when srmRm aborts an upload</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e2ff948310d8bb965df2ccbdc99402706f4533ce">e2ff948</a></dt>
<dd>dcache: IntelliJ code inspection refactoring</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e3d552bc6b9ec5d4e3812d1b9b7b5ffd3a0e7312">e3d552b</a></dt>
<dd>chimera: IntelliJ refactoring</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c27dcdf23762bc9d124ae9e8b5d517af3e489c41">c27dcdf</a></dt>
<dd>common-security,dcache-vehicles: IntelliJ refactoring</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4d132b0d15f3a5703370cd1c903ae2262bb4a05f">4d132b0</a></dt>
<dd>common: Various automated refactoring</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6b66b04de1e5158af3a43d2f83b865401374210d">6b66b04</a></dt>
<dd>cells: More semi automatic refactoring</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c7c52860a0848cd84307bbef409f6934fabb78d7">c7c5286</a></dt>
<dd>cells: Various automatic refactoring to clean up the code</dd>

<dt><a href="https://github.com/dcache/dcache/commit/aa0bcb94d72454cd7b989e65523397bc4d8b548e">aa0bcb9</a></dt>
<dd>cells: Reduce reliance on AbstractCellComponent</dd>

<dt><a href="https://github.com/dcache/dcache/commit/76cde04b0d3fb63eb3fffe3ab66c8ef8f2c505b8">76cde04</a></dt>
<dd>billing: Expose property to subscribe to topics</dd>

<dt><a href="https://github.com/dcache/dcache/commit/bc33cddad4a12b9274bfd5e0cc94ff43435946f2">bc33cdd</a></dt>
<dd>dcache-nearline-spi: Move AbstractBlockingNearlineStorage to dcache-nearline-spi</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c1b2f5a68af9b085dd05eb2757fed431793a6178">c1b2f5a</a></dt>
<dd>cells: IOException is not a bug in create command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4e1ce030894db560d3dfca1a3af4ba6dd9fb93e4">4e1ce03</a></dt>
<dd>cells: update CellMessage to work with initially empty messages</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f90ced010b58e9a4f99ed80b2ad77bc16ffe975b">f90ced0</a></dt>
<dd>transfermanager: fix querying of 3rd-party transfer</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8e449b6ccd0099fb78e8464196f7e0e2c1f46d05">8e449b6</a></dt>
<dd>pool: fix hsm unset command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3f074dc354c6bc3d87c5637a85a7bdb5e7935ebd">3f074dc</a></dt>
<dd>doors: enforce restriction in all PnfsManager operations</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1390c0c13472376a10997d7e757567bc6cd8f3b2">1390c0c</a></dt>
<dd>srm: remove ‘priority’ support</dd>

<dt><a href="https://github.com/dcache/dcache/commit/818b04ba1c7918cdbf9ed557cdd26f6472c8c3fe">818b04b</a></dt>
<dd>common: include filename in error message</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7f280f60fcab370853e9c0fdc57489b6ab900d9c">7f280f6</a></dt>
<dd>srmclient: do not rely on -f option of readlink</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8f472c0ca6d1ee259df322d2b56b08181af008dc">8f472c0</a></dt>
<dd>spacemanager: Refine errors sent on shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2de19e3bc98bad2f324e0bd424fcb8d5d5da85d5">2de19e3</a></dt>
<dd>poolmanager: Make pool manager replicable</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0b94ca041c657858cef2cb0e24d27e03a5ec2de7">0b94ca0</a></dt>
<dd>doors: Update doors to use PoolManagerHandler</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c68b78162c6a96f8d7bd5f082a7bf2d09ed8785b">c68b781</a></dt>
<dd>Upgrade to CANL 2.1 and BC 1.50</dd>

<dt><a href="https://github.com/dcache/dcache/commit/73969aa5c84fd9faee92928704cdf2c226d01d5d">73969aa</a></dt>
<dd>scripts: update canonicalising function</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3b355d122a16118b9df48571b60e5fd5afd34f78">3b355d1</a></dt>
<dd>webadmin: remove error and autorefresh options from alarms page</dd>

<dt><a href="https://github.com/dcache/dcache/commit/39306c2e6b0ca019296d6910c9672d6cd3fb6d5b">39306c2</a></dt>
<dd>alarms: force alarms-only-option</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0d6e9ab4a888711eaf6b28630066736131011289">0d6e9ab</a></dt>
<dd>dcache: Add framework for dynamic pool manager handlers</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7bcf59280d79e019806072aafff9083142a39738">7bcf592</a></dt>
<dd>poolmanager: Fix incorrect correction of pool cost</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a4ab7ed2ccfad4ac8a90136a4575a885c2a3cda7">a4ab7ed</a></dt>
<dd>dcap: Factor out configuration option parsing</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1a60fc09dfdb840d22b4147c7562d610857dbd7e">1a60fc0</a></dt>
<dd>dcap: Port DCAP door to the LineBasedDoor</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d4fb646e1396f9fd991ed073541b114302bfc76a">d4fb646</a></dt>
<dd>cells: handle empty string pool value on staging in TransferObserver</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ca199231933344fcab11646491a6639b9db5b2ab">ca19923</a></dt>
<dd>dcache: Move components of line based doors to dcache-core</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a266f9f4ddfebfba59de623b41df51132ee3db5e">a266f9f</a></dt>
<dd>cells: Refactor message forwarding logic</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5919c928a4d3a468862ce7e2e74e8806d5851c33">5919c92</a></dt>
<dd>cells: Retry RETRY_ON_NO_ROUTE_TO_CELL messages when a route is added</dd>

<dt><a href="https://github.com/dcache/dcache/commit/731cf8d2c445083ee97282d1168f4f0ea1cf55e0">731cf8d</a></dt>
<dd>cells: Expose SendFlag in CellStub</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a90151e5c48177d2af0ecd572d14339b1f796f42">a90151e</a></dt>
<dd>cells: Add SendFlag parameter to CellEndpoint#sendMessage</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b482c562a3e84a0f08d96bb1b92e37675867b3ff">b482c56</a></dt>
<dd>dcache: Refactor message forward logic</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3f8cca5f51c29977d2bd9748e826b2d929105793">3f8cca5</a></dt>
<dd>pool: include the original IOException info DiskErrorCacheException</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e9bf69ead6c4b4a6c10fe444d957221605f8429c">e9bf69e</a></dt>
<dd>cells: Extend CellLifeCycleAware with setup change notification</dd>

<dt><a href="https://github.com/dcache/dcache/commit/43c757c105732fb3ff7d5ed30a2411de8f3f74fa">43c757c</a></dt>
<dd>cells: Separate setup notifications from setup providers</dd>

<dt><a href="https://github.com/dcache/dcache/commit/73846b1e3780c1a5638a66191223d96f13588065">73846b1</a></dt>
<dd>poolmanager: Persist pool manager setup in ZooKeeper</dd>

<dt><a href="https://github.com/dcache/dcache/commit/16e72bc4d0a678cc0bfa356b2ffca6a6ffeeb26a">16e72bc</a></dt>
<dd>dcache: Allow UniversalSpringCell to persist setup in zookeeper</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d76e7d9a7977ccd1ce2f6f82f0152ef9a82217fd">d76e7d9</a></dt>
<dd>poolmanager: Persist pool read only status in setup file</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2e58fb2041130b70027f7b8414dddbb5157e89e1">2e58fb2</a></dt>
<dd>cells: Drop support for the setup manager</dd>

<dt><a href="https://github.com/dcache/dcache/commit/adb5c04c42d31f709b37f15bfe877ddafabc2ec0">adb5c04</a></dt>
<dd>cells: Check setup file syntax before applying it to the running cell</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0254bf4477e569a753d770dde83037f1ae6721ef">0254bf4</a></dt>
<dd>alarms: add ndc info to alarm info</dd>

<dt><a href="https://github.com/dcache/dcache/commit/25a125d47f46ef1b43bb7d17c9b39c547c3fd887">25a125d</a></dt>
<dd>resilience: fix alarm log level</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2baf078d9337f95ccf528f780c051242b7e80660">2baf078</a></dt>
<dd>packages/dcache-view: depolyment of dcache-view through nexus</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f356de5326df4de0a473a913f4850609954d210e">f356de5</a></dt>
<dd>dcache-restful-api: change protocol to HTTP</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e3887032adf7b212d5b8ce74685c8761aee91bf2">e388703</a></dt>
<dd>dcache-restful-api: RestfulAPI for QoS(CDMI) CHANGE current QoS for the specified file</dd>

<dt><a href="https://github.com/dcache/dcache/commit/46d091d47f976955d85415cbd022c4db4f1580ec">46d091d</a></dt>
<dd>dcache-restful-api: RestfulAPI for QoS(CDMI) CHANGE current QoS for the specified file</dd>

<dt><a href="https://github.com/dcache/dcache/commit/574cf496afec0ffc66dff89378f27d806c07ddaa">574cf49</a></dt>
<dd>dcache-nearline-plugin-archetype: Include correct service loader definition</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5d0825d197d13c0cc18c625e3ebdf023f96491cf">5d0825d</a></dt>
<dd>dcap: bump max command size sent by client to 8MB</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4a57c27e1d21839a2866a0ac68980805c8de3117">4a57c27</a></dt>
<dd>frontend/dcache-restful-api: remove www-authenticate header</dd>

<dt><a href="https://github.com/dcache/dcache/commit/874661c787f1dc02f8e49d95a5968580ddf151a8">874661c</a></dt>
<dd>gplazma2-argus: Update to Argus client 2.2.0 to fix dependency on VOMS library</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9b23e689acce0b9b46c9f0b3df495b02a9e3b553">9b23e68</a></dt>
<dd>util: expose timestamp when the instance of Transfer is created</dd>

<dt><a href="https://github.com/dcache/dcache/commit/09abff118fa2a255d77568e213ddf558584f7432">09abff1</a></dt>
<dd>mespace/chimera: allow optionally disable move to directory having differnt storage class (and cache class)</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2cd391fdd9cf98f9c4fd6d0c8ac6c5fc40f42f53">2cd391f</a></dt>
<dd>pom: use project.version instead of derived dcache.version</dd>

<dt><a href="https://github.com/dcache/dcache/commit/767cf9260a2431a9d5b35dc586512b6923fa6f10">767cf92</a></dt>
<dd>cells: Introduce annotation to flag setup affecting commands</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d9316fd6996063ae651d9e51d062622e25adb4a6">d9316fd</a></dt>
<dd>cells: Preserve CommandThrowableException</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f113664bff511ae1cb39240075d1831ea8708820">f113664</a></dt>
<dd>cells: Add default methods to CellInfoProvider and CellLifecycleAware</dd>

<dt><a href="https://github.com/dcache/dcache/commit/11720e41ce1012e1140c0e69374e0fbf83b28bfb">11720e4</a></dt>
<dd>pool: Cancel permanent migration jobs when reload pool setup file</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d12ce817e74e9a4c35ac3c354fb4b8d7b618d7bc">d12ce81</a></dt>
<dd>pool: Allow runtime mover queue management</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2fdbaf39c2bda7039f24031fdc70f1c6fbbfe84d">2fdbaf3</a></dt>
<dd>dcache-restful-api: fix data type for cdmi_geographic_placement</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5a5ed28f209332197a9efd341349ac6271b10a0f">5a5ed28</a></dt>
<dd>dcache-restful-api: RestfulAPI for QoS(CDMI) get current QoS for the specified file</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e8f091b22e7eeb54b4d8b4e60400520dcf89efe9">e8f091b</a></dt>
<dd>dcache-restful-api: RestfulAPI for QoS(CDMI)</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f4338810627e505ebf9c3fe6e2adc59d245f69a7">f433881</a></dt>
<dd>srm: add hint to escape IDs</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f4ad20be8272bedfd3e27feb04d0fb4ae9d178c4">f4ad20b</a></dt>
<dd>archetype: Add archetype for creating nearline storage plugins</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e71d9afdcb56aaec13ed62c723aae6c7c0cc0c92">e71d9af</a></dt>
<dd>poolmanager: Fix compilation regression</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9f991f46dc1b0c4d94e1eeb63b125eaabcf51963">9f991f4</a></dt>
<dd>nfs: Fix race condition in transfer startup</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ab358bac3892a6ac171c81a40e4984281c4bc706">ab358ba</a></dt>
<dd>poolmanager: Remove dead functionality from cost module</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2dcc9cb7c40e7bd4cea00a30c849561f83e609b7">2dcc9cb</a></dt>
<dd>pool: Port hsm commands to annotated command structure</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c4346018a2a6a8696e311b81579cf73fc401cba4">c434601</a></dt>
<dd>common-cli: Refactor allowAnyOption flag</dd>

<dt><a href="https://github.com/dcache/dcache/commit/94af2f903ed1dd4c57ea070770e2a11e26c9485a">94af2f9</a></dt>
<dd>pool: Remove deprecated nearline concurrency limit commands</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b9f9c8c1623be3b64d35b97938a3ce18966bbae4">b9f9c8c</a></dt>
<dd>common-cli: Fix compatibility with Java 7</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a97221d736c2669a0be4bfe3834df3cd04fdd984">a97221d</a></dt>
<dd>cells: Minor refactoring of command interpreters</dd>

<dt><a href="https://github.com/dcache/dcache/commit/87a0046b59c532c956859e1f9a125bf59113684f">87a0046</a></dt>
<dd>SrmShell.java: changed ‘rx-’ to ‘r-x’</dd>

<dt><a href="https://github.com/dcache/dcache/commit/83f0bffe681a3901b96ca846d43a2a820905c4c2">83f0bff</a></dt>
<dd>SrmShell.java: changed ‘rw–’ to ‘rw-’ in case TPermissionMode._RW</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5dcfbfbb9821b304a7857ad378fe65917f38a45e">5dcfbfb</a></dt>
<dd>info: fix broken unit-test</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b20cc35d073d2a9a5bc6e35d70f7ab7c72dca401">b20cc35</a></dt>
<dd>srm: Resolve message thead blocking issues with SRM third party copy</dd>

<dt><a href="https://github.com/dcache/dcache/commit/197009c7e471d369f23472706ff3aefa9507269d">197009c</a></dt>
<dd>restful-api: make exception and error handling resful</dd>

<dt><a href="https://github.com/dcache/dcache/commit/547308408b240abbf03361b95b9c7bcf0c67688e">5473084</a></dt>
<dd>pool: Fix compilation error</dd>

<dt><a href="https://github.com/dcache/dcache/commit/12ab3b1486244a288224393607c69fc4e91d0f64">12ab3b1</a></dt>
<dd>spacemanager: Work around for doors resubmitting PoolAcceptFileMessage</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5a9db09c1609abddb99711c32b6a8ce7e7b1dfd3">5a9db09</a></dt>
<dd>pool: Rename repository and store related classes</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d1fab177046cbeb97fdb8fe71bea8f6403ce3628">d1fab17</a></dt>
<dd>pool: Eliminate thread in mover scheduler</dd>

<dt><a href="https://github.com/dcache/dcache/commit/923fbe5a150f95472ae054340cd211dfdf887c6f">923fbe5</a></dt>
<dd>pool: Refactor BerkeleyDB meta data store to enable reuse</dd>

<dt><a href="https://github.com/dcache/dcache/commit/dc45cb72e986c9211f732970ac9bf3f024150afc">dc45cb7</a></dt>
<dd>pool: Expose URI rather than File to NearlineStorage implementations</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8ebdb0dfa96d1e9680a8cd045ec4f730a095adb3">8ebdb0d</a></dt>
<dd>pool: Refactor MetaDataStore and FileStore to use Path rather than File</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f91e92ac93a359cc402bef4f8f1b1fc0dc511802">f91e92a</a></dt>
<dd>pool: Avoid direct file access in post processing</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6282e3ede95eba24bbf3f64c2ce439de01c44b70">6282e3e</a></dt>
<dd>pool: Extend script driver for polling scripts</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b8f961d804f02f3517ea1df47b3d31012f841817">b8f961d</a></dt>
<dd>vehicles: remove unused constructors</dd>

<dt><a href="https://github.com/dcache/dcache/commit/30f36d03fa7e2519ca83e42320557ec850e1b815">30f36d0</a></dt>
<dd>cells: Propagate CommandExceptions as is on cell startup</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c246de6cefbe63633ec6f0e972672b33e19dadae">c246de6</a></dt>
<dd>pool: Fix several race conditions in migration module</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ca6c53119f6a4d12421936e016b40544d86f54c8">ca6c531</a></dt>
<dd>pool: Fix regression in mover set max active command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9b7b6799633216c114bc42627c0f086f272187d6">9b7b679</a></dt>
<dd>pool: Fix mover leak</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c03c4893c7f6a055e68bf2c0e6783123dc9de782">c03c489</a></dt>
<dd>pool: Fix synchronization regression in jtm</dd>

<dt><a href="https://github.com/dcache/dcache/commit/856f126632aef74a114d7bddd19461376b101a08">856f126</a></dt>
<dd>pool: Decouple checksum module from checksum scanner</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4deb0025107e747a020e0b7935a6f87240065936">4deb002</a></dt>
<dd>poolmanager: Move selection unit commands back into the selection unit</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d20dc636ff3bc5bd4161e8abbf2345f128b9d459">d20dc63</a></dt>
<dd>poolmanager: Drop resilience decorator of pool selection unit</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a6ed2e8f99564f89f9b925bff0d7cd29a22d8f33">a6ed2e8</a></dt>
<dd>pool: Let CellSetupProviders use setter injection</dd>

<dt><a href="https://github.com/dcache/dcache/commit/94c738fd719a889d45a95068e1270c6202976ef5">94c738f</a></dt>
<dd>cell: Only implement CellSetupProvider if needed</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f2f35f131916e576034d1c8d4e26a384c562f148">f2f35f1</a></dt>
<dd>dcache: Isolate setup file processing from primary cells command interpreter</dd>

<dt><a href="https://github.com/dcache/dcache/commit/de9fbf696656032b176248d28cf16f8fcc55b14a">de9fbf6</a></dt>
<dd>pool: Make RepositoryChannel extend SeekableByteChannel</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2f24b071ce8f3eee721acb1ef671a8153a980217">2f24b07</a></dt>
<dd>pool: Make checksum calculation independent of file system backend</dd>

<dt><a href="https://github.com/dcache/dcache/commit/79138be2e1e3d1a901878158b89f588e885b6489">79138be</a></dt>
<dd>pool: Refactor handling of replica size in the repository</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4a7a21dd65906c0e9dc523e8de3abe629fab831b">4a7a21d</a></dt>
<dd>pool: Reduce number of stat calls in Bekeley DB backend</dd>

<dt><a href="https://github.com/dcache/dcache/commit/40a06c148e4738889a98a668549e8048f2cf0d7f">40a06c1</a></dt>
<dd>pool: avoid NPE when querying status of a 3rd-party HTTP transfer</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c8cf22989e412089cbda8944015dad369a7e494d">c8cf229</a></dt>
<dd>resilience: finish the renaming of ‘pnfs(id) operation’ to ‘file operation’</dd>

<dt><a href="https://github.com/dcache/dcache/commit/077e8ec2bbae066da30c2e5a8309e618b85281d8">077e8ec</a></dt>
<dd>resilience: eliminate unnecessary update calls and fix synchronization of file op registration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/776c0f91532b6675a59d891bfca68682f3a50d33">776c0f9</a></dt>
<dd>resilience: repair (subtle) bug in target selection</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e2790b07b2dbc955eba997cb733eaa3f1af5251f">e2790b0</a></dt>
<dd>resilience: fix error in file operation updating</dd>

<dt><a href="https://github.com/dcache/dcache/commit/99d74a9b688e386d2b7a147d5ad5e0a418b8a566">99d74a9</a></dt>
<dd>resilience: fix the way removal of a pool from a resilient group is handled</dd>

<dt><a href="https://github.com/dcache/dcache/commit/63bf4f76cbaf290cd1174114f3ec47d7a5036db2">63bf4f7</a></dt>
<dd>resilience: fix several related bugs in transition checking when scheduling scans</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3f88a0a17a634d386fe41f2226016ff9ad485664">3f88a0a</a></dt>
<dd>resilience: remove restriction on storage unit linkage</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7114a15eca41d84836ac7b3fde3186822f1d24a5">7114a15</a></dt>
<dd>resilience: remove pool from operation table when it has been removed from a resilient group</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2e75f7510b40acdde9ce6d86096a5167a0af8339">2e75f75</a></dt>
<dd>resilience: allow file consumer to propagate Exception</dd>

<dt><a href="https://github.com/dcache/dcache/commit/96abb3d3f0a279e07032f7455981e63c2e9329ab">96abb3d</a></dt>
<dd>httpd: change condition from numeric inequality to non-null check on TransferInfo value</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8c2b57f18c5c12169ba316e8f62aa2ed208be56a">8c2b57f</a></dt>
<dd>poolmanager.properties: mentioned creation of .bak file</dd>

<dt><a href="https://github.com/dcache/dcache/commit/239ab6c304f7f0665b89aa10828a278e856b5d4b">239ab6c</a></dt>
<dd>alarms: fix NPE in type setter</dd>

<dt><a href="https://github.com/dcache/dcache/commit/871e82846fee94f237324d3d429f710943bd174e">871e828</a></dt>
<dd>src: change literal package strings to org.dcache.util</dd>

<dt><a href="https://github.com/dcache/dcache/commit/eca97e9606bc0a77294929ac7874b5c56b5ffae0">eca97e9</a></dt>
<dd>chimera: update unit-test to log ChimeraFsExceptions</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2ef6d449966eac872503caa0560b4a3a71e0f3fa">2ef6d44</a></dt>
<dd>src: consolidate org.dcache.commons.util, org.dcache.utils and org.dcache.util</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ca60c8761f674893c455da47d6dc1c8f122a7033">ca60c87</a></dt>
<dd>admin: Deprecate DSA keys</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c43acae48323d29879ae3f6231068996736c1893">c43acae</a></dt>
<dd>pool: Transactional bulk update meta data state in Berkeley DB</dd>

<dt><a href="https://github.com/dcache/dcache/commit/17575e44cd0f38c044df83332169ca505ccd5ad1">17575e4</a></dt>
<dd>pool: Eliminate MetaDataStore#copy method</dd>

<dt><a href="https://github.com/dcache/dcache/commit/13a1c7aac39fafb690ed0d74ae4be6f984af98d0">13a1c7a</a></dt>
<dd>pool: Fix bug that disables pools on non-critical errors</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1ab5e5cb90c83d3a35761140e81ea229ec91061f">1ab5e5c</a></dt>
<dd>webdav: avoid NPE if client fails to send a User-Agent header</dd>

<dt><a href="https://github.com/dcache/dcache/commit/472acb6a9a6c4345a907fd5302ea860173211b9d">472acb6</a></dt>
<dd>pool: use a single ByteBuffer when calculating the checksum of a hole</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7650505cf4ae285addea5d0cffe6d26d041fed02">7650505</a></dt>
<dd>chimera: avoid extra byte array creation during inode2bytes conversion</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e4f1b42cdf1a057ae51cb978f9572c29294425b5">e4f1b42</a></dt>
<dd>cells: Allow local delivery of messages through queue routes</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d3d5fc2a42ca812c9ef70217a68d107b2abe213c">d3d5fc2</a></dt>
<dd>zookeeper: avoid race in creating log directories</dd>

<dt><a href="https://github.com/dcache/dcache/commit/08ee55bfe42d5af4e3feb1055c97a4ba7fd58c3a">08ee55b</a></dt>
<dd>cells: Improve indentation of help text</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b1a9edd440ebec18fc30822274a9fdb72b21957c">b1a9edd</a></dt>
<dd>Make FsPath Serializable</dd>

<dt><a href="https://github.com/dcache/dcache/commit/3a943efd68c0bee6e83377a6cc0dfb1cd0a2053e">3a943ef</a></dt>
<dd>pool: Port remaining rep commands to annotated command framework</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5fc92a66dd8783e3e8bf1e00dd56874395ac18fb">5fc92a6</a></dt>
<dd>pool: Port list commands to new command structure</dd>

<dt><a href="https://github.com/dcache/dcache/commit/af43905ab69ec7043b8f7add51382a35b78347f6">af43905</a></dt>
<dd>build: add code-coverage reports</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9830f2d28c741136e82771ae5702af9d6d9985d7">9830f2d</a></dt>
<dd>pool: Eliminate MetaDataRecord#touch</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7d600c54a5b9b558ee46bf6992558f3b5e6b3b5b">7d600c5</a></dt>
<dd>pool: Refactor meta data store interface to allow bulk updates</dd>

<dt><a href="https://github.com/dcache/dcache/commit/39c05d1fa2411f25ea2eb7c8142777aeb31675c4">39c05d1</a></dt>
<dd>pool: Refactor IllegalTranstionException hierarchy</dd>

<dt><a href="https://github.com/dcache/dcache/commit/259a34abc4691076f62399308337aaf849d0d623">259a34a</a></dt>
<dd>pool: Refactor callback executor for flush queues</dd>

<dt><a href="https://github.com/dcache/dcache/commit/9e9a2abec6d5fe169eb06b5bcfb5c62b1caa7538">9e9a2ab</a></dt>
<dd>cells: Fix local delivery to queues</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7e0baec7bfd6c26c2ff549b6b0b7098d2c4d5074">7e0baec</a></dt>
<dd>pool: Report file in transient state as locked when setting sticky flag</dd>

<dt><a href="https://github.com/dcache/dcache/commit/92fbe53f16b302c91c88d2da22301d868eabfa44">92fbe53</a></dt>
<dd>admin: Fix compatibility with OpenSSH 7</dd>

<dt><a href="https://github.com/dcache/dcache/commit/219b9700ac429a9d3ce4bd86202b94ed50c19457">219b970</a></dt>
<dd>pool: Fix documentation error for -storage option of rep ls command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5180b992f585278c1c54b532d49c0327eb30d8e8">5180b99</a></dt>
<dd>script: Do not claim success if meta data conversion failed</dd>

<dt><a href="https://github.com/dcache/dcache/commit/942cca1feaa680d39ce2c5c0cdd7062780d0aded">942cca1</a></dt>
<dd>frontend: add support for user ‘anonymous’</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a8d9592fb768d1606f92cfce123131794a7d6b41">a8d9592</a></dt>
<dd>httpd: check for null Subject in Transfer info</dd>

<dt><a href="https://github.com/dcache/dcache/commit/dd15a13ee24ea00d9eae397fdd2878bc3734efec">dd15a13</a></dt>
<dd>resilience: fix incomplete behavior for pools intentionally marked “excluded”</dd>

<dt><a href="https://github.com/dcache/dcache/commit/291dbb10aa229863519797d2b88805705f879873">291dbb1</a></dt>
<dd>admin: refactor login strategy</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1dbfbe5a8e09da9d7e86d3c75d50c0fce5b0fa25">1dbfbe5</a></dt>
<dd>webdav: fix bean creation in webdav.xml for spnego handler</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b21b4b45016c738f8ed0ec6c65c8b410a8880da7">b21b4b4</a></dt>
<dd>frontend: always fail request if wrong credentials are presented</dd>

<dt><a href="https://github.com/dcache/dcache/commit/159c42257703d227583268b59dbd3066ec9570a9">159c422</a></dt>
<dd>webdav: add Spnego based Kerberos authentication mechanism for SSO capabilities</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7b770bced8c87384cb05082483f69ffe29f0d3cf">7b770bc</a></dt>
<dd>common: add ByteUnit enum and ByteUnits utility class</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e461d408adea551858e9f426d1e6ee6fa6b21d71">e461d40</a></dt>
<dd>restful: add ability to discover information about current user</dd>

<dt><a href="https://github.com/dcache/dcache/commit/070a543ae612f80d66eeeb4ae4744365f848fb19">070a543</a></dt>
<dd>srm: enrich access log</dd>

<dt><a href="https://github.com/dcache/dcache/commit/c93dc6cc2d21c4aad9aa09df4e22ab83fbd9148f">c93dc6c</a></dt>
<dd>resilience: simplify code for handling resilience requests on pools</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d154a5fdb721d4d17cbe711c0aca53ebf37a33d3">d154a5f</a></dt>
<dd>resilience: fix classification of file incomplete and other errors</dd>

<dt><a href="https://github.com/dcache/dcache/commit/73bb943c989b2bd93e36b5b5d8362db26478e852">73bb943</a></dt>
<dd>pool: Don’t use transient error for a broken file</dd>

<dt><a href="https://github.com/dcache/dcache/commit/78ee625dbd0d4893af6eb6036e2f81c0394a6a2e">78ee625</a></dt>
<dd>admin: Drop old ssh 1 keys</dd>

<dt><a href="https://github.com/dcache/dcache/commit/85811a2303115e3ff60efc1bfc714c68bdb2fc06">85811a2</a></dt>
<dd>pool: Add error codes to p2p failures</dd>

<dt><a href="https://github.com/dcache/dcache/commit/61ee15f577515fcd95848285083d4caeadcb282d">61ee15f</a></dt>
<dd>pool: Make final state update after upload atomic</dd>

<dt><a href="https://github.com/dcache/dcache/commit/586e62f60fb94fe30d5fc11080da6fe6357f3711">586e62f</a></dt>
<dd>pool: Lower log level of certain failures to create mover</dd>

<dt><a href="https://github.com/dcache/dcache/commit/56fb782d5bc75b218ae55112bd49def78829cedf">56fb782</a></dt>
<dd>chimera-nfs: fix broken commit 4682fd3</dd>

<dt><a href="https://github.com/dcache/dcache/commit/4682fd3b77e122815f6eb4a208f24f8dc99b7a5e">4682fd3</a></dt>
<dd>chimera: move byte &lt;=&gt; FsInode conversion into nfs specific part</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e5a00425abc41e6feda3278aa98ddc811498bd84">e5a0042</a></dt>
<dd>pool: fix staging for CopyNearlineStorage</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b34c3de750d23b15a1abe6291403772f2c74118d">b34c3de</a></dt>
<dd>REST-api: fix permission denied.</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8b1d1e1784305a4af53c23622df0631253dfdd53">8b1d1e1</a></dt>
<dd>frontend: remove prompt login onloading dCacheView</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e717ffe42a1ebb804425bea58e96b98bb2de9b66">e717ffe</a></dt>
<dd>resilience: add checked location selection exception</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8ddded0b6dd829587bec3c4ed48ae054858a0e23">8ddded0</a></dt>
<dd>resilience: fail when source retry is requested with only one possible source</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6f3dfc7950888740f618e4a1f70f53dc1285be09">6f3dfc7</a></dt>
<dd>pools: restore correct command names</dd>

<dt><a href="https://github.com/dcache/dcache/commit/12eeda4bdc98ba665b7e90635b12b928fc4d8eca">12eeda4</a></dt>
<dd>pool: Add open flush mode</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b40b8bdc1a16d1eae0ca6ab723bd8484a2aa9b20">b40b8bd</a></dt>
<dd>gplazma: Make gplazma.x509.use-policy-principals obsolete</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ddfdbd0d49657dc9ac3a7039c9baca5999acfdfe">ddfdbd0</a></dt>
<dd>cells: Drop legacy cells communication</dd>

<dt><a href="https://github.com/dcache/dcache/commit/459680da7cb95dd5496e8da9106c4090a10aa18c">459680d</a></dt>
<dd>Mark deprecated properties obsolete</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0d2f9c06875e2232c192e269e165cc109b5d4ee3">0d2f9c0</a></dt>
<dd>webdav: Fix error reporting when client is unauthorized</dd>

<dt><a href="https://github.com/dcache/dcache/commit/61d13ef39c81009693a32a450f0e8edb1356bc7f">61d13ef</a></dt>
<dd>srm: Fix job expiration during service startup</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a7860b37e654e488a426eca1aa41e5ea13ef4659">a7860b3</a></dt>
<dd>pool: Minor refactoring of flush classes</dd>

<dt><a href="https://github.com/dcache/dcache/commit/887b4d339374589fa6054f53f162d756e8e6dd97">887b4d3</a></dt>
<dd>Remove deprecated code</dd>

<dt><a href="https://github.com/dcache/dcache/commit/abdae030555286716ebad6f13ce5c33bbc756bb6">abdae03</a></dt>
<dd>system-test: Enable automatic schema management for replicamanager</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b9792c79d193ed5b9739c7223a9d801dd1836703">b9792c7</a></dt>
<dd>billing: use in-memory buffer for hourly aggregate data</dd>

<dt><a href="https://github.com/dcache/dcache/commit/13a009ba27262d0115e01c870b4e585986983699">13a009b</a></dt>
<dd>webdav: make links relative in standard template</dd>

<dt><a href="https://github.com/dcache/dcache/commit/95b114ef2f650e668fc1e0273e7d7de5b9272dbc">95b114e</a></dt>
<dd>billing : fix issue wih HSQLDB backend</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d790aa84b97ef48ab46b586c6b6b921ca4a2a217">d790aa8</a></dt>
<dd>gplazma: don’t generate a stack-trace if htaccess is malformed</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ff48c27bdf2580ce1ae5087bc9ba93d8560237f8">ff48c27</a></dt>
<dd>pool: Fix race in pool initialization</dd>

<dt><a href="https://github.com/dcache/dcache/commit/62fd2004f8c942e50ca64dc20e4d07a7e223fb1b">62fd200</a></dt>
<dd>Revert “srmmanager: Enable multiple instances to share a database”</dd>

<dt><a href="https://github.com/dcache/dcache/commit/7deb9f0a8e52dd680d33e13f9180b26d4e135f2f">7deb9f0</a></dt>
<dd>system-test: Fix Linux compatibility for populate script</dd>

<dt><a href="https://github.com/dcache/dcache/commit/43e7ad0ae3e898298848bb4e82068f867369cb03">43e7ad0</a></dt>
<dd>system-test: Fix regression in populate script</dd>

<dt><a href="https://github.com/dcache/dcache/commit/86c8c322cc1e9b260333519e99e73602e23ed97e">86c8c32</a></dt>
<dd>pool: Close stores after use in meta data utilities</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2900cf9dc7d29289c61bd0981c63016cb456ef15">2900cf9</a></dt>
<dd>Revert “pool: Close stores after use in meta data utilities”</dd>

<dt><a href="https://github.com/dcache/dcache/commit/504e37fb13de86d353775e724cf31bed0d1911ac">504e37f</a></dt>
<dd>pool: Close stores after use in meta data utilities</dd>

<dt><a href="https://github.com/dcache/dcache/commit/cc2eb798560574699ed24492315fc8e0d4a05ee7">cc2eb79</a></dt>
<dd>pool: Fix regressions in meta data utilities</dd>

<dt><a href="https://github.com/dcache/dcache/commit/0d10b6d6281edeb7c08e8ca761372889552c5763">0d10b6d</a></dt>
<dd>system-test: Speed up liquibase update</dd>

<dt><a href="https://github.com/dcache/dcache/commit/74f09171b7125f04cc3c12d651a57d995864a572">74f0917</a></dt>
<dd>Disable OCSP by default</dd>

<dt><a href="https://github.com/dcache/dcache/commit/ec6df2f9489b4e0adc75da8b51b768908be30229">ec6df2f</a></dt>
<dd>srm: Fix listing of completed list requests</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8e4253dd3c85bbee77dc7302e0f9af0666302554">8e4253d</a></dt>
<dd>billing: re-implement population of aggregate tables</dd>

<dt><a href="https://github.com/dcache/dcache/commit/97290f606c5090a38b84d61069adf2a8b4c291da">97290f6</a></dt>
<dd>dcache restful-api: adjust the response header</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6cf3f9566be94eba40f6e9c495dd859e6e2e51f7">6cf3f95</a></dt>
<dd>billing: Fix NoClassDefFoundError when invoking dcache billing command</dd>

<dt><a href="https://github.com/dcache/dcache/commit/5b92ef434694a86b2a69f89185f5ae326d60d0a8">5b92ef4</a></dt>
<dd>httpd: Fail gracefully in case of missing options</dd>

<dt><a href="https://github.com/dcache/dcache/commit/870a5b7aac7f6fa54ee3badc6ea15ef77cdd8d7e">870a5b7</a></dt>
<dd>httpd: Update cell info view for named queues and make srmmanager monitored</dd>

<dt><a href="https://github.com/dcache/dcache/commit/20725411a7f80e23ef69256be83d121201c35e59">2072541</a></dt>
<dd>cells: Suppress RejectedExecutionException on shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/93c223ed030ceb0aa768d156a4bbfade8b12ae96">93c223e</a></dt>
<dd>cells: Fix NPE during shutdown</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a09a461c98b9eebbeaa3b5e3046a623623bf98ff">a09a461</a></dt>
<dd>gplazma: Add PrefixRestriction and use it to validate root and upload paths</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1b7fb03ba50b26447dc336940144feb536f460ea">1b7fb03</a></dt>
<dd>zookeeper: Document ports used by embedded zookeeper</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f748eba241ea6f316b10ee8fdf3d8985b6c87543">f748eba</a></dt>
<dd>ftp: Fix regression in resolving path</dd>

<dt><a href="https://github.com/dcache/dcache/commit/a31c5cdf862deaaf14b1e5d8910339efc3ea1a4a">a31c5cd</a></dt>
<dd>frontend: Expose dCacheView configuration in dCache configuration</dd>

<dt><a href="https://github.com/dcache/dcache/commit/89be067283805263096a251616e173e8b2259296">89be067</a></dt>
<dd>zookeeper: Add automatic purging of old snapshots</dd>

<dt><a href="https://github.com/dcache/dcache/commit/6623081fa27009ccd6bc63d0d6b60cb608606143">6623081</a></dt>
<dd>Remove example.org values from configuration defaults</dd>

<dt><a href="https://github.com/dcache/dcache/commit/e63d821579a5e0adf355625c24ccfc787decb26e">e63d821</a></dt>
<dd>dCacheView: new end-user web interface for dCache</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f47224c6dd361648fc2577dfad8089fc8f4131a4">f47224c</a></dt>
<dd>api: Rename service to frontend</dd>

<dt><a href="https://github.com/dcache/dcache/commit/1aa3afd3dcbe3ef564e4061a37e6fc0b359a577c">1aa3afd</a></dt>
<dd>api: Move rest API to separate service</dd>

<dt><a href="https://github.com/dcache/dcache/commit/8cd3d3e8aafd835b6d15c465a90ec6c578c51835">8cd3d3e</a></dt>
<dd>billing: fix issue with database change rollback</dd>

<dt><a href="https://github.com/dcache/dcache/commit/370fc72b60b44691e340511fa09bd05c24c520ad">370fc72</a></dt>
<dd>src: remove unused class AbstractNameSpaceProvider</dd>

<dt><a href="https://github.com/dcache/dcache/commit/f7511cbf0280dc840cc2923bd9de779635c66070">f7511cb</a></dt>
<dd>srmmanager: Make scheduler ID configurable and compatible with older versions</dd>

<dt><a href="https://github.com/dcache/dcache/commit/2f6abfd0305e01c3cac9e74248439c17adfc5164">2f6abfd</a></dt>
<dd>pool: Upgrade to Berkeley DB Java Edition 6.4.25</dd>

<dt><a href="https://github.com/dcache/dcache/commit/b81732d96e95c7d79a2571c748f7f0871801301f">b81732d</a></dt>
<dd>httpd: restore original fields and format to the TransferObserverV1 ascii output</dd>

<dt><a href="https://github.com/dcache/dcache/commit/d8ab725f5cfb231fc4d27146aefd0b01d74b80e9">d8ab725</a></dt>
<dd>[maven-release-plugin] prepare for next development iteration</dd>
</dl>

