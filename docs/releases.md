---
layout: pages
title: DCACHE RELEASES
permalink: /docs/releases/
date: 2017-2-22T00:00
---

# RELEASE POLICY

dCache follows a time-boxed two dimensional release
policy. Every four months we produce a feature
release. Feature releases have version numbers like
2.x.0, where <tt>x</tt> is a positive integer. A new
feature release marks the start of a <i>branch</i>; for example,
the release of dCache <tt>2.10.0</tt> marked the start of the
<tt>2.10</tt>-branch.

A feature release is followed up by a number of <i>maintenance
releases</i> containing bug fixes or high priority feature
tweaks. Maintenance releases for release <tt>2.x.0</tt> have
version numbers <tt>2.x.y</tt>, with <tt>y</tt> being some
number larger than 0; for example, <tt>2.10.0</tt> is a feature
release, <tt>2.10.1</tt> is the first maintenance release for
the <tt>2.10</tt>-branch and <tt>2.10.2</tt> is the second
maintenance release.

Maintenance releases are provided approximately weekly for the
duration of that branch's support period. Once the support
period has elapsed no futher maintenance releases will be made
for that branch. You are encouraged to upgrade your dCache
instance to a newer branch before support for your current
branch elapses.


<a href="https://asifmoh.github.io/dcacheorg/docs/timeline-dCache.svg"> <img src="../timeline-dCache.svg" width="100%" height="540"></a>


## Support period

Typically once a year, we designate one branch a long-term
supported release: a <i>Golden Release</i>. The only difference
between long-term releases and other branches is the support
period. A golden release is supported until the second
subsequent long-term release, which is typically two years.
Other branches are supported until the end of the previous
golden release support period.
Choosing between golden releases and other branches is a matter
of site policy and a matter of taste. Newer branches contain
newer features, but they also have shorter support periods and
often fewer dCache instances using them. However, upgrading
from a golden release to a non-golden branch does not affect the
end-of-support date.
Some sites use dCache that is repackaged by another
distribution. Such distribution may recommend a specific
version. Sites should follow their distribution's recommended
version.
The support periods are shown in the time-line above. Click on
the image for a larger view of the image.

## Upgrading and compatibility

We support sites upgrading releases either to the next golden
release or to a regular release without skipping a golden
release. Upgrading in a bigger jump may be possible, but sites
should take extra care as configuration may have changed in a
non-backwards-compatible fashion. If in doubt, contact dCache
support for help.
For the purposes of describing compatibility, we call those
computers in a dCache cluster that host only one or more pool
services <i>pool nodes</i> and all other computers in the
cluster <i>non-pool nodes</i>.
All non-pool nodes must run dCache from the same feature release
but, unless indicated differently in the release notes,
individual nodes may run any maintenance release from the same
feature release (e.g., dCache version 2.x.y is compatible with
version 2.x.z for any values of x, y and z). In general, we
advise sites to run the most recent maintenance release from
their deployed series, but understand upgrading dCache impacts
the running service.
The pool nodes do not need to run the same feature release as
the non-pool nodes; they also do not need to run the same
feature release as each other. Pool nodes must run either the
same version or an earlier version as the non-pool nodes and the
version must not be earlier than the previous golden release.
For example, if a dCache cluster has non-pool nodes running
v2.12.2 then the cluster may simultaneously contain pool nodes
with dCache v2.12.5, v2.11.3 and v2.10.20. The cluster may not
contain pools running v2.9.x as this is an earlier release than
the previous golden release (2.10). The cluster may not contain
pools running v2.13.1 as this is newer than the non-pool nodes.
The effect of this policy is that a site may upgrade just the
non-pool nodes to a newer version without upgrading the pool
nodes, provided no golden release is skipped. However, once the
non-pool nodes are upgraded to a golden release, the pools must
also be upgraded to that golden release before the non-pool
nodes may be upgraded further.
The release notes for each release includes a compatibility
matrix that describes this information in detail.
While we try to avoid configuration and database-schema changes
in maintenance (bug-fix) releases, moving from one feature
release to another often requires some configuration changes.
Wherever possible, new configuration properties take existing
(deprecated) properties as default values. In general, these
changes are fully described in the release notes.
To simplify sites upgrading between golden releases, we provide
upgrade guides targeted at sites jumping from one golden release
to the next:
 
- [1.9.12 to 2.2]({{site.baseurl}}/docs/upgrade-1.9.12-to-2.2/). 
- [2.2 to 2.6]({{site.baseurl}}/docs/upgrade-2.2-to-2.6/). 
- [2.6 to 2.10]({{site.baseurl}}/docs/upgrade-2.6-to-2.10/). 

  
# Downloads
server-3.1
	
dCache 3.1 features the following highlights and architectural improvements:
- Plenty of NFS door improvements.
- Chimera can track file upload status.
- OpenID connect support for WebDAV 3rd party copy.
- Allow regular expression matching of storage units in resilience manager.


<p xmlns="">
          dCache v3.1 requires a JVM supporting Java 8.
      </p>
<table xmlns="" class="releases">
<thead>
<tr>
	<th>Download</th>
	<th>Rel. Date</th>
	<th>md5 hash</th>
	<th>Release Notes</th>
</tr>
</thead>
<tbody>
<tr id="3.1.15" class="rec">
	<td class="link"><a href="repo/3.1/dcache_3.1.15-1_all.deb">dCache 3.1.15 (Debian package)</a></td>
	<td class="date">10.8.2017</td>
	<td class="hash">9868c16133996565989166a3aef7b4ae</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml">3.1.15</a></td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/3.1/dcache-3.1.15-1.noarch.rpm">dCache 3.1.15 (rpm)</a></td>
	<td class="date">10.8.2017</td>
	<td class="hash">804223e3845083c57890fea173b61ef0</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/3.1/dcache-3.1.15.tar.gz">dCache 3.1.15 (tgz)</a></td>
	<td class="date">10.8.2017</td>
	<td class="hash">412bc5ebe7f0977032ebce805dad614e</td>
</tr>
<tr id="3.1.14" class="odd">
	<td class="link"><a href="repo/3.1/dcache_3.1.14-1_all.deb">dCache 3.1.14 (Debian package)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">a5dc7f360b02a5ffc3ac571077ed97cd</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#14">3.1.14</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.14-1.noarch.rpm">dCache 3.1.14 (rpm)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">d55743649723a6f772bebfd3f2247423</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.14.tar.gz">dCache 3.1.14 (tgz)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">aca52c9ccc89068ba9c7b54f4156a228</td>
</tr>
<tr id="3.1.13" class="even">
	<td class="link"><a href="repo/3.1/dcache_3.1.13-1_all.deb">dCache 3.1.13 (Debian package)</a></td>
	<td class="date">26.7.2017</td>
	<td class="hash">0375f42852c041b5a768938f4f3588d0</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#13">3.1.13</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.13-1.noarch.rpm">dCache 3.1.13 (rpm)</a></td>
	<td class="date">26.7.2017</td>
	<td class="hash">60bcb408136818e9395bb5bcfd3a14b0</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.13.tar.gz">dCache 3.1.13 (tgz)</a></td>
	<td class="date">26.7.2017</td>
	<td class="hash">632791c341d370d19ff93d71b9dcbabd</td>
</tr>
<tr id="3.1.12" class="odd">
	<td class="link"><a href="repo/3.1/dcache_3.1.12-1_all.deb">dCache 3.1.12 (Debian package)</a></td>
	<td class="date">18.7.2017</td>
	<td class="hash">d6350ac4ee920314ecf89c270bfa976a</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#12">3.1.12</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.12-1.noarch.rpm">dCache 3.1.12 (rpm)</a></td>
	<td class="date">18.7.2017</td>
	<td class="hash">8509e42fdf762d32942ece593a8aca2d</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.12.tar.gz">dCache 3.1.12 (tgz)</a></td>
	<td class="date">18.7.2017</td>
	<td class="hash">8a7df1fc5e01561bcbd3990892ec71d6</td>
</tr>
<tr id="3.1.11" class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.11-1.noarch.rpm">dCache 3.1.11 (rpm)</a></td>
	<td class="date">11.7.2017</td>
	<td class="hash">44e56ac1cbba195af048128e88af92da</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#11">3.1.11</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.11.tar.gz">dCache 3.1.11 (tgz)</a></td>
	<td class="date">11.7.2017</td>
	<td class="hash">b392ba10783a7d411644043e3918a15b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache_3.1.11-1_all.deb">dCache 3.1.11 (Debian package)</a></td>
	<td class="date">11.7.2017</td>
	<td class="hash">0b2e299e96f7a4d2f46dd665fb60788c</td>
</tr>
<tr id="3.1.10" class="odd">
	<td class="link"><a href="repo/3.1/dcache_3.1.10-1_all.deb">dCache 3.1.10 (Debian package)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">3a3cbdd9d6e1531335e7e1000a210825</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#10">3.1.10</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.10-1.noarch.rpm">dCache 3.1.10 (rpm)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">c3e47d58392c7cf02cce2726cef746a7</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.10.tar.gz">dCache 3.1.10 (tgz)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">bd4abc0a8b2ca20192b2fde8eb6d6693</td>
</tr>
<tr id="3.1.9" class="even">
	<td class="link"><a href="repo/3.1/dcache_3.1.9-1_all.deb">dCache 3.1.9 (Debian package)</a></td>
	<td class="date">28.6.2017</td>
	<td class="hash">3b54bccca7d3db3ef3d1e9019b68f50b</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#9">3.1.9</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.9-1.noarch.rpm">dCache 3.1.9 (rpm)</a></td>
	<td class="date">28.6.2017</td>
	<td class="hash">e771cc488b5fb52715990a58bb940052</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.9.tar.gz">dCache 3.1.9 (tgz)</a></td>
	<td class="date">28.6.2017</td>
	<td class="hash">1a551fd50cc98f22d3428a346ee27104</td>
</tr>
<tr id="3.1.8" class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.8-1.noarch.rpm">dCache 3.1.8 (rpm)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">b64bfe6c27aec296cd3fecf2652ae463</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#8">3.1.8</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.8.tar.gz">dCache 3.1.8 (tgz)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">4d6698072c829be2d8c932387b36bee2</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache_3.1.8-1_all.deb">dCache 3.1.8 (Debian package)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">c79ce23f6ae96c15fe7bef632c6243cb</td>
</tr>
<tr id="3.1.7" class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.7-1.noarch.rpm">dCache 3.1.7 (rpm)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">afe619bd63e04b5af330eda64c8ce8b5</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#7">3.1.7</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.7.tar.gz">dCache 3.1.7 (tgz)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">ce21e43393d7ae6c9f75b2dd45a5e4b1</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache_3.1.7-1_all.deb">dCache 3.1.7 (Debian package)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">eaffc0ff417668f969c383dea789769a</td>
</tr>
<tr id="3.1.6" class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.6-1.noarch.rpm">dCache 3.1.6 (rpm)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">50bfc846f97abe3516e91b17bf9c0b8e</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#6">3.1.6</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.6.tar.gz">dCache 3.1.6 (tgz)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">bc11676cf84d627108fca5eeb945a070</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache_3.1.6-1_all.deb">dCache 3.1.6 (Debian package)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">074d1227155d3fe7547fb477c9474282</td>
</tr>
<tr id="3.1.5" class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.5-1.noarch.rpm">dCache 3.1.5 (rpm)</a></td>
	<td class="date">23.5.2017</td>
	<td class="hash">208acd724a678cbbfd64ad51caed94ef</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#5">3.1.5</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.5.tar.gz">dCache 3.1.5 (tgz)</a></td>
	<td class="date">23.5.2017</td>
	<td class="hash">4a0014e57a89d0e37b207ea390b9943a</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache_3.1.5-1_all.deb">dCache 3.1.5 (Debian package)</a></td>
	<td class="date">23.5.2017</td>
	<td class="hash">e2e742ac6fe31c612d769a3a9baa267d</td>
</tr>
<tr id="3.1.4" class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.4-1.noarch.rpm">dCache 3.1.4 (rpm)</a></td>
	<td class="date">16.5.2017</td>
	<td class="hash">ec97ffad382456628144fbfd6c86f98c</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#4">3.1.4</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.4.tar.gz">dCache 3.1.4 (tgz)</a></td>
	<td class="date">16.5.2017</td>
	<td class="hash">5381d836285e94f67badef52137c2202</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache_3.1.4-1_all.deb">dCache 3.1.4 (Debian package)</a></td>
	<td class="date">16.5.2017</td>
	<td class="hash">547457ae6e74aae24756016112e4fe88</td>
</tr>
<tr id="3.1.3" class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.3-1.noarch.rpm">dCache 3.1.3 (rpm)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">b13e54ec6c4091fccf02f8999208c9d1</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#3">3.1.3</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.3.tar.gz">dCache 3.1.3 (tgz)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">26dc356e00ee83404976331631fedb24</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache_3.1.3-1_all.deb">dCache 3.1.3 (Debian package)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">fb7ffceaa6383a9168b7dee5dfcb1a23</td>
</tr>
<tr id="3.1.2" class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.2-1.noarch.rpm">dCache 3.1.2 (rpm)</a></td>
	<td class="date">3.5.2017</td>
	<td class="hash">3c91c0b0041fcefb1daf532fa2f3df0a</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#2">3.1.2</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.2.tar.gz">dCache 3.1.2 (tgz)</a></td>
	<td class="date">3.5.2017</td>
	<td class="hash">503755db383d971a1ee9e76521c879ef</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache_3.1.2-1_all.deb">dCache 3.1.2 (Debian package)</a></td>
	<td class="date">3.5.2017</td>
	<td class="hash">77509a9df09d8763ff0266452b098f11</td>
</tr>
<tr id="3.1.1" class="even">
	<td class="link"><a href="repo/3.1/dcache_3.1.1-1_all.deb">dCache 3.1.1 (Debian package)</a></td>
	<td class="date">20.4.2017</td>
	<td class="hash">5dfa05de7f3aee0e36bbe1cbf4750a71</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#1">3.1.1</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.1-1.noarch.rpm">dCache 3.1.1 (rpm)</a></td>
	<td class="date">20.4.2017</td>
	<td class="hash">69c786c7d36c6404aa3acddca32ebc43</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.1/dcache-3.1.1.tar.gz">dCache 3.1.1 (tgz)</a></td>
	<td class="date">20.4.2017</td>
	<td class="hash">b395366cda89bad2951c2f6ab762e8ce</td>
</tr>
<tr id="3.1.0" class="odd">
	<td class="link"><a href="repo/3.1/dcache_3.1.0-1_all.deb">dCache 3.1.0 (Debian package)</a></td>
	<td class="date">3.4.2017</td>
	<td class="hash">294014482b1fb023365888c19c42ffac</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.1.shtml#0">3.1.0</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.0-1.noarch.rpm">dCache 3.1.0 (rpm)</a></td>
	<td class="date">3.4.2017</td>
	<td class="hash">0dbc79770f8c83a9e8ff37ba925823ee</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.1/dcache-3.1.0.tar.gz">dCache 3.1.0 (tgz)</a></td>
	<td class="date">3.4.2017</td>
	<td class="hash">e44397f3e62bb4c6fc4c75c70278c75c</td>
</tr>
</tbody>
</table>
<br xmlns="">
<a xmlns="" name="server-3.0"></a> <a name="server-3.0">server 3.0.x</a> <a href="rss-server-3.0-releases.xml" type="application/rss+xml"><img class="rss-icon" src="{{site.baseurl}}/images/rss-icon-14x14.png" alt="RSS" title="RSS feed for dCache server 3.0.x releases"></a>
		
dCache 3.0 features the following highlights and architectural improvements:
  
<ul xmlns="">
        <li>Production-ready support for high availability setups and rolling updates.</li>
	<li>Automatic detection of PostgreSQL master.</li>
	<li>Support the HAProxy proxy protocol.</li>
	<li>Self describing billing files.</li>
	<li>Pool manager setup is stored in ZooKeeper.</li>
	<li>Pool manager read-only state is stored in setup file and ZooKeeper.</li>
	<li>New experimental support for Ceph</li>
	<li>New performance cost calculation for improved stability of hot spot replication.</li>
	<li>Batching of flush to tape can be disabled.</li>
	<li>Mover queues can be created at runtime.</li>
	<li>Abort upload when SRM TURL is invalidated.</li>
	<li>Allow xrootd clients to select mover queues.</li>
      </ul>
<p xmlns="">
          dCache v3.0 requires a JVM supporting Java 8.
      </p>
<table xmlns="" class="releases">
<thead>
<tr>
	<th>Download</th>
	<th>Rel. Date</th>
	<th>md5 hash</th>
	<th>Release Notes</th>
</tr>
</thead>
<tbody>
<tr id="3.0.27" class="rec">
	<td class="link"><a href="repo/3.0/dcache_3.0.27-1_all.deb">dCache 3.0.27 (Debian package)</a></td>
	<td class="date">10.8.2017</td>
	<td class="hash">d4289f8dcf02aede3b0a0f95d99fa36e</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml">3.0.27</a></td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/3.0/dcache-3.0.27-1.noarch.rpm">dCache 3.0.27 (rpm)</a></td>
	<td class="date">10.8.2017</td>
	<td class="hash">9c2d207fb04ed87258a76dce22c26b69</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/3.0/dcache-3.0.27.tar.gz">dCache 3.0.27 (tgz)</a></td>
	<td class="date">10.8.2017</td>
	<td class="hash">acd62a5abdb2220971e5edd2bb8cd440</td>
</tr>
<tr id="3.0.26" class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.26-1_all.deb">dCache 3.0.26 (Debian package)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">c4f7f777b870c2fdea82963ea7686dff</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#26">3.0.26</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.26-1.noarch.rpm">dCache 3.0.26 (rpm)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">cc336af1f10bf198a08fc0754c8cc017</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.26.tar.gz">dCache 3.0.26 (tgz)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">453d3e3cdd461cc1b58614b4af40a2dd</td>
</tr>
<tr id="3.0.25" class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.25-1_all.deb">dCache 3.0.25 (Debian package)</a></td>
	<td class="date">26.7.2017</td>
	<td class="hash">080561f40e6a854227f336d495a4ba61</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#25">3.0.25</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.25-1.noarch.rpm">dCache 3.0.25 (rpm)</a></td>
	<td class="date">26.7.2017</td>
	<td class="hash">4fdcc318b8884f088aa244257bf6540b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.25.tar.gz">dCache 3.0.25 (tgz)</a></td>
	<td class="date">26.7.2017</td>
	<td class="hash">2dc16f346d6b4fb36ed6b35fea437194</td>
</tr>
<tr id="3.0.24" class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.24-1_all.deb">dCache 3.0.24 (Debian package)</a></td>
	<td class="date">18.7.2017</td>
	<td class="hash">0f4afd35f8df0d9046011d6ff5d7a2ff</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#24">3.0.24</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.24-1.noarch.rpm">dCache 3.0.24 (rpm)</a></td>
	<td class="date">18.7.2017</td>
	<td class="hash">96c66eca23e7d2e0e02be37e814d1859</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.24.tar.gz">dCache 3.0.24 (tgz)</a></td>
	<td class="date">18.7.2017</td>
	<td class="hash">95692f4bf8f4a37b410a42e992c54628</td>
</tr>
<tr id="3.0.23" class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.23-1.noarch.rpm">dCache 3.0.23 (rpm)</a></td>
	<td class="date">11.7.2017</td>
	<td class="hash">f412d2fce1e8fc3769294fc275128503</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#23">3.0.23</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.23.tar.gz">dCache 3.0.23 (tgz)</a></td>
	<td class="date">11.7.2017</td>
	<td class="hash">2011c217e3600abc38cb2d2495b3e9f5</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.23-1_all.deb">dCache 3.0.23 (Debian package)</a></td>
	<td class="date">11.7.2017</td>
	<td class="hash">46efe6256df896c874df68d89b763acd</td>
</tr>
<tr id="3.0.22" class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.22-1_all.deb">dCache 3.0.22 (Debian package)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">99e992a1be6b619913508c5d58297a82</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#22">3.0.22</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.22-1.noarch.rpm">dCache 3.0.22 (rpm)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">e56723a7dbbfde069b16d56ebe36e675</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.22.tar.gz">dCache 3.0.22 (tgz)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">b1e550ff352b7f47b2297b5bafddf6c8</td>
</tr>
<tr id="3.0.21" class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.21-1_all.deb">dCache 3.0.21 (Debian package)</a></td>
	<td class="date">28.6.2017</td>
	<td class="hash">0e142d0204b60de158dc38fb2f416588</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#21">3.0.21</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.21-1.noarch.rpm">dCache 3.0.21 (rpm)</a></td>
	<td class="date">28.6.2017</td>
	<td class="hash">5c09b059aad0e907462e17559338b27c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.21.tar.gz">dCache 3.0.21 (tgz)</a></td>
	<td class="date">28.6.2017</td>
	<td class="hash">ba87af21b1514cceb98398b915668d33</td>
</tr>
<tr id="3.0.20" class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.20-1.noarch.rpm">dCache 3.0.20 (rpm)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">2df3cc8e40b985e69b78a916f32cfc66</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#20">3.0.20</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.20.tar.gz">dCache 3.0.20 (tgz)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">70b31bcadbef007ebb8d35c6bc326f7b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.20-1_all.deb">dCache 3.0.20 (Debian package)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">856abab0c49650ea937e1f690f3eaecb</td>
</tr>
<tr id="3.0.19" class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.19-1.noarch.rpm">dCache 3.0.19 (rpm)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">53cccb755fe42f939424c8a3294a6790</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#19">3.0.19</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.19.tar.gz">dCache 3.0.19 (tgz)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">377497eb4dc4144024fd4a3112390055</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.19-1_all.deb">dCache 3.0.19 (Debian package)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">ad15d46425b7d3751d919f71cd2add6e</td>
</tr>
<tr id="3.0.18" class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.18-1.noarch.rpm">dCache 3.0.18 (rpm)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">a7d92fdc8625b2d9e5b2ff6f402bbe9d</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#18">3.0.18</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.18.tar.gz">dCache 3.0.18 (tgz)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">22372fb49811e0b8376e89643e6d2118</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.18-1_all.deb">dCache 3.0.18 (Debian package)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">f2c40fb066617d266aa6e091c8402a0f</td>
</tr>
<tr id="3.0.17" class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.17-1.noarch.rpm">dCache 3.0.17 (rpm)</a></td>
	<td class="date">23.5.2017</td>
	<td class="hash">5fcec0cb403aef0629d6cc82389ccba7</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#17">3.0.17</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.17.tar.gz">dCache 3.0.17 (tgz)</a></td>
	<td class="date">23.5.2017</td>
	<td class="hash">b16f6032befe46863e3cfe1d22d19a04</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.17-1_all.deb">dCache 3.0.17 (Debian package)</a></td>
	<td class="date">23.5.2017</td>
	<td class="hash">e4c13c89466355e97e198c9da5b6d6fb</td>
</tr>
<tr id="3.0.16" class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.16-1.noarch.rpm">dCache 3.0.16 (rpm)</a></td>
	<td class="date">16.5.2017</td>
	<td class="hash">2bd435926de33a1723060e6607f6819b</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#16">3.0.16</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.16.tar.gz">dCache 3.0.16 (tgz)</a></td>
	<td class="date">16.5.2017</td>
	<td class="hash">d83f217b5aeb2f5ccc61daeccfa01a6a</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.16-1_all.deb">dCache 3.0.16 (Debian package)</a></td>
	<td class="date">16.5.2017</td>
	<td class="hash">df5795ccb26a714dc4acf44217622bfb</td>
</tr>
<tr id="3.0.15" class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.15-1.noarch.rpm">dCache 3.0.15 (rpm)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">137bc25a96dcd8af23e9abccce4f9b91</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#15">3.0.15</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.15.tar.gz">dCache 3.0.15 (tgz)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">30470cae67294f63f17df4243cc333e7</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.15-1_all.deb">dCache 3.0.15 (Debian package)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">9dc9354dd8ba149bc4053aee9688a644</td>
</tr>
<tr id="3.0.14" class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.14-1.noarch.rpm">dCache 3.0.14 (rpm)</a></td>
	<td class="date">3.5.2017</td>
	<td class="hash">7af6ea8b43a429b01c46611abc7d1fb3</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#14">3.0.14</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.14.tar.gz">dCache 3.0.14 (tgz)</a></td>
	<td class="date">3.5.2017</td>
	<td class="hash">88b46a987c93f1b48bac52c3f43701ea</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.14-1_all.deb">dCache 3.0.14 (Debian package)</a></td>
	<td class="date">3.5.2017</td>
	<td class="hash">8155137ce78cfaf93739b02b6ded5a6c</td>
</tr>
<tr id="3.0.13" class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.13-1_all.deb">dCache 3.0.13 (Debian package)</a></td>
	<td class="date">20.4.2017</td>
	<td class="hash">748621d997078ba0a9cfef2000564d87</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#13">3.0.13</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.13-1.noarch.rpm">dCache 3.0.13 (rpm)</a></td>
	<td class="date">20.4.2017</td>
	<td class="hash">1e63770a6af07a910b528548aed3a372</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.13.tar.gz">dCache 3.0.13 (tgz)</a></td>
	<td class="date">20.4.2017</td>
	<td class="hash">e63d18a8aad3c6728e9f17d92e8312bd</td>
</tr>
<tr id="3.0.12" class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.12-1_all.deb">dCache 3.0.12 (Debian package)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">17bef66309c51df2dd5e1e4465037903</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#12">3.0.12</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.12-1.noarch.rpm">dCache 3.0.12 (rpm)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">a01d673ac1d99544fd92f2a99afd2d4f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.12.tar.gz">dCache 3.0.12 (tgz)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">cfbf052e78810d1499281ba86ccfa778</td>
</tr>
<tr id="3.0.11" class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.11-1_all.deb">dCache 3.0.11 (Debian package)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">5b49d38110a75682da3c20d56ac7d18c</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#11">3.0.11</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.11-1.noarch.rpm">dCache 3.0.11 (rpm)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">b768c5f632f5b1ad172123f7f6a7087b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.11.tar.gz">dCache 3.0.11 (tgz)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">1b146a4c8079f34257f9a81111c81607</td>
</tr>
<tr id="3.0.10" class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.10-1_all.deb">dCache 3.0.10 (Debian package)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">13edc79f8fd2bbc5f25103b33f1617ae</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#10">3.0.10</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.10-1.noarch.rpm">dCache 3.0.10 (rpm)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">d17e342cb74783df2e79e3df863d1b00</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.10.tar.gz">dCache 3.0.10 (tgz)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">e23556e06b880eb4b6859b714470b380</td>
</tr>
<tr id="3.0.9" class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.9-1_all.deb">dCache 3.0.9 (Debian package)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">9cc6364b3b99b4ef69bcd8577a673de7</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#9">3.0.9</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.9-1.noarch.rpm">dCache 3.0.9 (rpm)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">4c78e0e2d8fc64cb8d7dadf8774b4729</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.9.tar.gz">dCache 3.0.9 (tgz)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">8b030c282fd61b0f3144c178b0070ac5</td>
</tr>
<tr id="3.0.8" class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.8-1.noarch.rpm">dCache 3.0.8 (rpm)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">791b8cf24a2002de4df3ffaf8e2cb605</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#8">3.0.8</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.8.tar.gz">dCache 3.0.8 (tgz)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">1912afdfb356deadaae4a6dba3046cc0</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.8-1_all.deb">dCache 3.0.8 (Debian package)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">0b792bdcd11fa31163d0a1b46da3cca7</td>
</tr>
<tr id="3.0.7" class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.7-1.noarch.rpm">dCache 3.0.7 (rpm)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">ee5d60c1aea44c520d801c22250fe551</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#7">3.0.7</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.7.tar.gz">dCache 3.0.7 (tgz)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">4d92f2aae79f4fe34a572a02b61fcddf</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.7-1_all.deb">dCache 3.0.7 (Debian package)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">0b21ee4a09d832defddf0ecb82137117</td>
</tr>
<tr id="3.0.6" class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.6-1.noarch.rpm">dCache 3.0.6 (rpm)</a></td>
	<td class="date">31.1.2017</td>
	<td class="hash">222658b5a360fab14fb316c604b8b479</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#6">3.0.6</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.6.tar.gz">dCache 3.0.6 (tgz)</a></td>
	<td class="date">31.1.2017</td>
	<td class="hash">357bed961c1df5500d963794ea90fa65</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.6-1_all.deb">dCache 3.0.6 (Debian package)</a></td>
	<td class="date">31.1.2017</td>
	<td class="hash">a888605893d103121dbf4597519e01f9</td>
</tr>
<tr id="3.0.5" class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.5-1.noarch.rpm">dCache 3.0.5 (rpm)</a></td>
	<td class="date">26.1.2017</td>
	<td class="hash">d86793c5617319bbcf20282ad0c8b01e</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#5">3.0.5</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.5.tar.gz">dCache 3.0.5 (tgz)</a></td>
	<td class="date">26.1.2017</td>
	<td class="hash">111ec6313cde46f6419838b909ad52c6</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.5-1_all.deb">dCache 3.0.5 (Debian package)</a></td>
	<td class="date">26.1.2017</td>
	<td class="hash">b05dbc981e076aeb0b99a4a311b731c4</td>
</tr>
<tr id="3.0.4" class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.4-1_all.deb">dCache 3.0.4 (Debian package)</a></td>
	<td class="date">17.1.2017</td>
	<td class="hash">3d0eec29642a4fcb7b180b9a1a83e14b</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#4">3.0.4</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.4-1.noarch.rpm">dCache 3.0.4 (rpm)</a></td>
	<td class="date">17.1.2017</td>
	<td class="hash">95ec4bd7ef779416a7c6cd40616d35b9</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.4.tar.gz">dCache 3.0.4 (tgz)</a></td>
	<td class="date">17.1.2017</td>
	<td class="hash">8d9252a9572c12300769e88e6e92eb2b</td>
</tr>
<tr id="3.0.3" class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.3-1_all.deb">dCache 3.0.3 (Debian package)</a></td>
	<td class="date">13.12.2016</td>
	<td class="hash">19f21e23cdf794ffc6f08b039aa3e97f</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#3">3.0.3</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.3-1.noarch.rpm">dCache 3.0.3 (rpm)</a></td>
	<td class="date">13.12.2016</td>
	<td class="hash">c0a52c690d8463b782d118248a9d07c5</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.3.tar.gz">dCache 3.0.3 (tgz)</a></td>
	<td class="date">13.12.2016</td>
	<td class="hash">4c3452da726d47c1747579e7ab41b769</td>
</tr>
<tr id="3.0.2" class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.2-1.noarch.rpm">dCache 3.0.2 (rpm)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">725e85d498eadf6a7353142e2ff6ab7c</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#2">3.0.2</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.2.tar.gz">dCache 3.0.2 (tgz)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">cd25c8aa1c70c2602be1024166889a46</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.2-1_all.deb">dCache 3.0.2 (Debian package)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">c24290cfa03f980cf7b5ba49296fdc4f</td>
</tr>
<tr id="3.0.1" class="even">
	<td class="link"><a href="repo/3.0/dcache_3.0.1-1_all.deb">dCache 3.0.1 (Debian package)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">d8569eddf54da5a50a4af8923f1eb37d</td>
	<td class="notes" rowspan="4"><a href="release-notes-3.0.shtml#1">3.0.1</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.1-1.noarch.rpm">dCache 3.0.1 (rpm)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">a1a525c0bafe2eb106a08c4218983539</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.1-1.pkg">dCache 3.0.1 (Solaris package)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">c9f7efe04fc6926ac9f1a02220c43ed9</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/3.0/dcache-3.0.1.tar.gz">dCache 3.0.1 (tgz)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">1fc6f0c56da7c3c2c3a364851b6a1032</td>
</tr>
<tr id="3.0.0" class="odd">
	<td class="link"><a href="repo/3.0/dcache_3.0.0-1_all.deb">dCache 3.0.0 (Debian package)</a></td>
	<td class="date">21.11.2016</td>
	<td class="hash">ffc1888699a6e524bea8392fe2ef0cc2</td>
	<td class="notes" rowspan="3"><a href="release-notes-3.0.shtml#0">3.0.0</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.0-1.noarch.rpm">dCache 3.0.0 (rpm)</a></td>
	<td class="date">21.11.2016</td>
	<td class="hash">e476188f337353d9a15355028450e20a</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/3.0/dcache-3.0.0.tar.gz">dCache 3.0.0 (tgz)</a></td>
	<td class="date">21.11.2016</td>
	<td class="hash">87b9567509e104dd7d68ecb4e934f01a</td>
</tr>
</tbody>
</table>
<br xmlns=""> <a xmlns="" name="server-2.16"></a> <a name="server-2.16">server 2.16.x</a> <a href="rss-server-2.16-releases.xml" type="application/rss+xml"><img class="rss-icon" src="{{site.baseurl}}/images/rss-icon-14x14.png" alt="RSS" title="RSS feed for dCache server 2.16.x releases"></a>
	

In addition to the usual improvements and bug fixes, dCache
2.16 features the following highlights:
    
<ul xmlns="">
          <li>New experimental RESTful API.</li>
          <li>New experimental end user web interface called dCacheView.</li>
          <li>New experimental support for redundant cell communication using multiple message brokers.</li>
          <li>New resilience service for managing file replicas. Will eventually replace the replica manager.</li>
          <li>New experimental support for replicable services.</li>
          <li>Scalable SRM frontend service.</li>
          <li>Limited OpenID Connect support.</li>
      </ul>
<p xmlns="">
          dCache v2.16 requires a JVM supporting Java v8.
      </p>
<table xmlns="" class="releases">
<thead>
<tr>
	<th>Download</th>
	<th>Rel. Date</th>
	<th>md5 hash</th>
	<th>Release Notes</th>
</tr>
</thead>
<tbody>
<tr id="2.16.46" class="rec">
	<td class="link"><a href="repo/2.16/dcache_2.16.46-1_all.deb">dCache 2.16.46 (Debian package)</a></td>
	<td class="date">10.8.2017</td>
	<td class="hash">c911ad00d25ffb6f14f2a467d91a668b</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml">2.16.46</a></td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.16/dcache-2.16.46-1.noarch.rpm">dCache 2.16.46 (rpm)</a></td>
	<td class="date">10.8.2017</td>
	<td class="hash">3ce70fa5f57232621eb260fff3adb109</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.16/dcache-2.16.46-1.pkg">dCache 2.16.46 (Solaris package)</a></td>
	<td class="date">10.8.2017</td>
	<td class="hash">2105d161ae058d7b26d27ca5dbd701fb</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.16/dcache-2.16.46.tar.gz">dCache 2.16.46 (tgz)</a></td>
	<td class="date">10.8.2017</td>
	<td class="hash">dc99ef787bddc98abbe2edcd67ffab81</td>
</tr>
<tr id="2.16.45" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.45-1_all.deb">dCache 2.16.45 (Debian package)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">42559b0b52d55057395b3c4925e40954</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#45">2.16.45</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.45-1.noarch.rpm">dCache 2.16.45 (rpm)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">1be84d939f8981d99d26738c33ca8af7</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.45-1.pkg">dCache 2.16.45 (Solaris package)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">5a8b2dac24a865749ed19b798279c7f3</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.45.tar.gz">dCache 2.16.45 (tgz)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">af047b100584cf65e078522479080d0b</td>
</tr>
<tr id="2.16.44" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.44-1_all.deb">dCache 2.16.44 (Debian package)</a></td>
	<td class="date">26.7.2017</td>
	<td class="hash">87907b5fe44da8e03ac7c9e21b42f9d0</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#44">2.16.44</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.44-1.noarch.rpm">dCache 2.16.44 (rpm)</a></td>
	<td class="date">26.7.2017</td>
	<td class="hash">32872f88565fb587da9f763aeb7a7a5e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.44-1.pkg">dCache 2.16.44 (Solaris package)</a></td>
	<td class="date">26.7.2017</td>
	<td class="hash">26bef0366212bfadb9945d33b2767863</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.44.tar.gz">dCache 2.16.44 (tgz)</a></td>
	<td class="date">26.7.2017</td>
	<td class="hash">d910f50b5bd9eeb7af51c875b258968d</td>
</tr>
<tr id="2.16.43" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.43-1_all.deb">dCache 2.16.43 (Debian package)</a></td>
	<td class="date">18.7.2017</td>
	<td class="hash">a891571b021b42263100d06dfe3bf302</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#43">2.16.43</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.43-1.noarch.rpm">dCache 2.16.43 (rpm)</a></td>
	<td class="date">18.7.2017</td>
	<td class="hash">89761a2f582618ffc3b6551aa6892e2d</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.43-1.pkg">dCache 2.16.43 (Solaris package)</a></td>
	<td class="date">18.7.2017</td>
	<td class="hash">88a00bb7712a5067b6d6435bcaabffbc</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.43.tar.gz">dCache 2.16.43 (tgz)</a></td>
	<td class="date">18.7.2017</td>
	<td class="hash">dab5e5e0e9035af03747de3cd76df88d</td>
</tr>
<tr id="2.16.42" class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.42-1.noarch.rpm">dCache 2.16.42 (rpm)</a></td>
	<td class="date">11.7.2017</td>
	<td class="hash">1bbacbc7df96f3813533ee7dacaf1066</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#42">2.16.42</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.42-1.pkg">dCache 2.16.42 (Solaris package)</a></td>
	<td class="date">11.7.2017</td>
	<td class="hash">36605872baf70a6f72ba32ca246cb81e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.42.tar.gz">dCache 2.16.42 (tgz)</a></td>
	<td class="date">11.7.2017</td>
	<td class="hash">b1be00799c63cca52f2fe39fa17b2075</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.42-1_all.deb">dCache 2.16.42 (Debian package)</a></td>
	<td class="date">11.7.2017</td>
	<td class="hash">c38677261bd691cfd2e5ddeadd1f3cc9</td>
</tr>
<tr id="2.16.41" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.41-1_all.deb">dCache 2.16.41 (Debian package)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">a63319c1b3696ec73920ef667f6dfa30</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#41">2.16.41</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.41-1.noarch.rpm">dCache 2.16.41 (rpm)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">d92abe3912d20c722b3a7da5877bad60</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.41-1.pkg">dCache 2.16.41 (Solaris package)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">67d26285379f2f034c45faf379f06f9c</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.41.tar.gz">dCache 2.16.41 (tgz)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">cde725135177db3ca581f3c516612f17</td>
</tr>
<tr id="2.16.40" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.40-1_all.deb">dCache 2.16.40 (Debian package)</a></td>
	<td class="date">28.6.2017</td>
	<td class="hash">95bd236196d8007692e979a8599a97e0</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#40">2.16.40</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.40-1.noarch.rpm">dCache 2.16.40 (rpm)</a></td>
	<td class="date">28.6.2017</td>
	<td class="hash">39c93f3f3ecb0474b2fd64772ed28c41</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.40-1.pkg">dCache 2.16.40 (Solaris package)</a></td>
	<td class="date">28.6.2017</td>
	<td class="hash">5401aa527cd98f47e845a64b8ba31cc0</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.40.tar.gz">dCache 2.16.40 (tgz)</a></td>
	<td class="date">28.6.2017</td>
	<td class="hash">ce9b6949dd27da80c7e92272b23f651c</td>
</tr>
<tr id="2.16.39" class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.39-1.noarch.rpm">dCache 2.16.39 (rpm)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">c249839e85af1b3576d23aba1fda8f59</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#39">2.16.39</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.39-1.pkg">dCache 2.16.39 (Solaris package)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">975283dcd09e7d3fece4c9262d9402c5</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.39.tar.gz">dCache 2.16.39 (tgz)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">417ae012d728a7bb374569800dce6ac3</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.39-1_all.deb">dCache 2.16.39 (Debian package)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">3a400bf8a818c16276c85d73653b5cf7</td>
</tr>
<tr id="2.16.38" class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.38-1.noarch.rpm">dCache 2.16.38 (rpm)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">78def3234adf5507696f3cc64b857c85</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#38">2.16.38</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.38-1.pkg">dCache 2.16.38 (Solaris package)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">6fa0b1e68b093421f79ac1fdd01c1055</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.38.tar.gz">dCache 2.16.38 (tgz)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">0ded7e0104204b1f1cf9a0c6a569a4c8</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.38-1_all.deb">dCache 2.16.38 (Debian package)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">2baedcd83f5b66df88b81d92fb3c7e80</td>
</tr>
<tr id="2.16.37" class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.37-1.noarch.rpm">dCache 2.16.37 (rpm)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">cf649cb44e2794db05d1b176a4824f5f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#37">2.16.37</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.37-1.pkg">dCache 2.16.37 (Solaris package)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">58ee37ce9b72c6609bf54d967cc59b7e</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.37.tar.gz">dCache 2.16.37 (tgz)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">2e2617a3f85dce3d3160a54dbbc570a6</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.37-1_all.deb">dCache 2.16.37 (Debian package)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">2c091a624d8518d13994b73dba19999a</td>
</tr>
<tr id="2.16.36" class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.36-1.noarch.rpm">dCache 2.16.36 (rpm)</a></td>
	<td class="date">23.5.2017</td>
	<td class="hash">927714161b3d50ed0c128f67e5b21d9c</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#36">2.16.36</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.36-1.pkg">dCache 2.16.36 (Solaris package)</a></td>
	<td class="date">23.5.2017</td>
	<td class="hash">a9561ecc136f5f870fb1f3194981d383</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.36.tar.gz">dCache 2.16.36 (tgz)</a></td>
	<td class="date">23.5.2017</td>
	<td class="hash">4b64b044ead670c69f392759072cc838</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.36-1_all.deb">dCache 2.16.36 (Debian package)</a></td>
	<td class="date">23.5.2017</td>
	<td class="hash">28e9a0b36e54d348ef1fcd53df25b56a</td>
</tr>
<tr id="2.16.35" class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.35-1.noarch.rpm">dCache 2.16.35 (rpm)</a></td>
	<td class="date">16.5.2017</td>
	<td class="hash">07476e489fbf8ca3b7365d32e4903006</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#35">2.16.35</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.35-1.pkg">dCache 2.16.35 (Solaris package)</a></td>
	<td class="date">16.5.2017</td>
	<td class="hash">7d5ab40001c2e3520ad94829d8eeacc6</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.35.tar.gz">dCache 2.16.35 (tgz)</a></td>
	<td class="date">16.5.2017</td>
	<td class="hash">34d19846550635421c5e92a7c0ccb94b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.35-1_all.deb">dCache 2.16.35 (Debian package)</a></td>
	<td class="date">16.5.2017</td>
	<td class="hash">507303378f723699f3fc2b1b833e1733</td>
</tr>
<tr id="2.16.34" class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.34-1.noarch.rpm">dCache 2.16.34 (rpm)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">3fa263dbeb9427699a1b7893f8f326bf</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#34">2.16.34</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.34-1.pkg">dCache 2.16.34 (Solaris package)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">feefe1be9ad0de90c6e953cce0f4c828</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.34.tar.gz">dCache 2.16.34 (tgz)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">85f76da19257df1932d6c45035c8dbdc</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.34-1_all.deb">dCache 2.16.34 (Debian package)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">edcae4ac69da96c23d5dcec311e7e7c3</td>
</tr>
<tr id="2.16.33" class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.33-1.noarch.rpm">dCache 2.16.33 (rpm)</a></td>
	<td class="date">3.5.2017</td>
	<td class="hash">d6d697eaec3fe9d6da699617dfc30414</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#33">2.16.33</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.33-1.pkg">dCache 2.16.33 (Solaris package)</a></td>
	<td class="date">3.5.2017</td>
	<td class="hash">c5cd89740b6b4b9fcd051740e87da66b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.33.tar.gz">dCache 2.16.33 (tgz)</a></td>
	<td class="date">3.5.2017</td>
	<td class="hash">1b89fba1e20c1e6f852c37f01dc0a8ae</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.33-1_all.deb">dCache 2.16.33 (Debian package)</a></td>
	<td class="date">3.5.2017</td>
	<td class="hash">c5d4d02185708612fa54e0ee4f2f259a</td>
</tr>
<tr id="2.16.32" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.32-1_all.deb">dCache 2.16.32 (Debian package)</a></td>
	<td class="date">20.4.2017</td>
	<td class="hash">e54af60867ff59300e674e1ef1865c75</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#32">2.16.32</a></td>
</tr>server
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.32-1.noarch.rpm">dCache 2.16.32 (rpm)</a></td>
	<td class="date">20.4.2017</td>
	<td class="hash">d768b617b771f811369d835f3a66d7a7</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.32-1.pkg">dCache 2.16.32 (Solaris package)</a></td>
	<td class="date">20.4.2017</td>
	<td class="hash">928c29d89493b5a48cdeaf338e1e2324</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.32.tar.gz">dCache 2.16.32 (tgz)</a></td>
	<td class="date">20.4.2017</td>
	<td class="hash">b1fe4ad92240cdb7f75eef95ae348b21</td>
</tr>
<tr id="2.16.31" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.31-1_all.deb">dCache 2.16.31 (Debian package)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">9add1ca6df3c8a0896d5fc7a199331c3</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#31">2.16.31</a></td>
</tr>server
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.31-1.noarch.rpm">dCache 2.16.31 (rpm)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">2f73dc41c3cf71db0dcf928cfc4d1707</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.31-1.pkg">dCache 2.16.31 (Solaris package)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">91bd71247245074a5406f09a3f5dc391</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.31.tar.gz">dCache 2.16.31 (tgz)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">56ceeae2b264f8fbb508ba69c41c1d12</td>
</tr>
<tr id="2.16.30" class="even">
	<td class="link"><a href="serverrepo/2.16/dcache_2.16.30-1_all.deb">dCache 2.16.30 (Debian package)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">d0ee647b33c14cc61714996bcb7e2c8c</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#30">2.16.30</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.30-1.noarch.rpm">dCache 2.16.30 (rpm)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">5572b8ac53c527142d175d69496f7ef5</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.30-1.pkg">dCache 2.16.30 (Solaris package)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">0a00a6ccee4be27123dc1e36a69df1f1</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.30.tar.gz">dCache 2.16.30 (tgz)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">3227485c726954ce2b73bc73d7516f72</td>
</tr>
<tr id="2.16.29" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.29-1_all.deb">dCache 2.16.29 (Debian package)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">1de2260c9aba2ac14bbe1498411b226c</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#29">2.16.29</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.29-1.noarch.rpm">dCache 2.16.29 (rpm)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">bb3301eb7ef485c54640859e2b4b2a72</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.29-1.pkg">dCache 2.16.29 (Solaris package)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">e0cbab82208f81f24ab2a72cc143da7c</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.29.tar.gz">dCache 2.16.29 (tgz)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">a49f9fa0a81b4c46c430023c6d6d8030</td>
</tr>
<tr id="2.16.28" class="even">
	<td class="link"><a href="serverrepo/2.16/dcache_2.16.28-1_all.deb">dCache 2.16.28 (Debian package)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">485db0b26cf9fe13dba36f67fb704089</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#28">2.16.28</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.28-1.noarch.rpm">dCache 2.16.28 (rpm)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">454ebebdf74882c9a9f8f6b241a4f4cf</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.28-1.pkg">dCache 2.16.28 (Solaris package)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">bcc2829f7f4ca17151d768139e25eb8d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.28.tar.gz">dCache 2.16.28 (tgz)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">ce0490b2574acf66ca004e4ae21e9830</td>
</tr>
<tr id="2.16.27" class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.27-1.noarch.rpm">dCache 2.16.27 (rpm)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">af0d47b7226335dabd24354918b96fba</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#27">2.16.27</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.27-1.pkg">dCache 2.16.27 (Solaris package)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">a5a63bdec1da16359ae016143a5edc5d</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.27.tar.gz">dCache 2.16.27 (tgz)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">4f1c824e56e39b9347cb658e8efd33eb</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.27-1_all.deb">dCache 2.16.27 (Debian package)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">ab1c14d4d74bde6a6d9d08049ac71be8</td>
</tr>
<tr id="2.16.26" class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.26-1.noarch.rpm">dCache 2.16.26 (rpm)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">e658985cbf3a005853bd1c838e4889fc</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#26">2.16.26</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.26-1.pkg">dCache 2.16.26 (Solaris package)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">a086e4074f2ac7f5d25988eb2ec04e2d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.26.tar.gz">dCache 2.16.26 (tgz)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">023e12ed4436d1cf7c58be06b357a9b0</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.26-1_all.deb">dCache 2.16.26 (Debian package)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">0b152f12970e3032297a7df0176b92f9</td>
</tr>
<tr id="2.16.25" class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.25-1.noarch.rpm">dCache 2.16.25 (rpm)</a></td>
	<td class="date">31.1.2017</td>
	<td class="hash">0ec0b08779168b57f4802e760ae88ead</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#25">2.16.25</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.25-1.pkg">dCache 2.16.25 (Solaris package)</a></td>
	<td class="date">31.1.2017</td>
	<td class="hash">1688ba0f31c773a823187b0c4754c5ab</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.25.tar.gz">dCache 2.16.25 (tgz)</a></td>
	<td class="date">31.1.2017</td>
	<td class="hash">36b3504ce368243b1490264447b6b9e3</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.25-1_all.deb">dCache 2.16.25 (Debian package)</a></td>
	<td class="date">31.1.2017</td>
	<td class="hash">0808e63016b96b630e538dd0b5e21ac3</td>
</tr>
<tr id="2.16.24" class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.24-1.noarch.rpm">dCache 2.16.24 (rpm)</a></td>
	<td class="date">26.1.2017</td>
	<td class="hash">ee342fc5eb29a742caa46f08d0c81929</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#24">2.16.24</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.24-1.pkg">dCache 2.16.24 (Solaris package)</a></td>
	<td class="date">26.1.2017</td>
	<td class="hash">d2491fec8dd3669aeea5cd1ffe466a84</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.24.tar.gz">dCache 2.16.24 (tgz)</a></td>
	<td class="date">26.1.2017</td>
	<td class="hash">3a7d993ba5430490994bf3953c07c047</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.24-1_all.deb">dCache 2.16.24 (Debian package)</a></td>
	<td class="date">26.1.2017</td>
	<td class="hash">e01ea33c587ab7e112ca998e6c4ad416</td>
</tr>
<tr id="2.16.23" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.23-1_all.deb">dCache 2.16.23 (Debian package)</a></td>
	<td class="date">17.1.2017</td>
	<td class="hash">937a28676748d29f5fa19c57a1d4857f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#23">2.16.23</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.23-1.noarch.rpm">dCache 2.16.23 (rpm)</a></td>
	<td class="date">17.1.2017</td>
	<td class="hash">ec2cbb68ea6a479e44dd01b1e87feb63</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.23-1.pkg">dCache 2.16.23 (Solaris package)</a></td>
	<td class="date">17.1.2017</td>
	<td class="hash">5b60a7bd0e1265994bfbdf5777964b66</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.23.tar.gz">dCache 2.16.23 (tgz)</a></td>
	<td class="date">17.1.2017</td>
	<td class="hash">c1df54df504ed18f10ac53d07ca1b606</td>
</tr>
<tr id="2.16.22" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.22-1_all.deb">dCache 2.16.22 (Debian package)</a></td>
	<td class="date">13.12.2016</td>
	<td class="hash">0886873a9c395b62d563cb8fae6eb0c6</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#22">2.16.22</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.22-1.noarch.rpm">dCache 2.16.22 (rpm)</a></td>
	<td class="date">13.12.2016</td>
	<td class="hash">27b0c268ad8f4df398c209d9e4fcbf13</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.22-1.pkg">dCache 2.16.22 (Solaris package)</a></td>
	<td class="date">13.12.2016</td>
	<td class="hash">ee8a64da55caa370e49819c25d2aa610</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.22.tar.gz">dCache 2.16.22 (tgz)</a></td>
	<td class="date">13.12.2016</td>
	<td class="hash">f53f9786e2292867fdad5392c69e99c0</td>
</tr>
<tr id="2.16.21" class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.21-1.noarch.rpm">dCache 2.16.21 (rpm)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">7a1fee715b14192324acc24ab1f40d9f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#21">2.16.21</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.21-1.pkg">dCache 2.16.21 (Solaris package)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">95fb1fc7e7e5162ab977f2f59e9b4ed3</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.21.tar.gz">dCache 2.16.21 (tgz)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">e83271f69e37c0c32461e5395dd6dd70</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.21-1_all.deb">dCache 2.16.21 (Debian package)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">3e57ccdbc6d3cdead41cf52768ada2ec</td>
</tr>
<tr id="2.16.20" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.20-1_all.deb">dCache 2.16.20 (Debian package)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">a67410232b38e560b44d7ab4865437f8</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#20">2.16.20</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.20-1.noarch.rpm">dCache 2.16.20 (rpm)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">ff82647c98d199a6c0d20d7317c4b7f9</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.20-1.pkg">dCache 2.16.20 (Solaris package)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">6aedcbc6ec7f277aa6ec019578a88959</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.20.tar.gz">dCache 2.16.20 (tgz)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">18a5db97be9d7fa359a706095861e2c8</td>
</tr>
<tr id="2.16.19" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.19-1_all.deb">dCache 2.16.19 (Debian package)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">bc4384b3821937d9a6970beb66bf8627</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#19">2.16.19</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.19-1.noarch.rpm">dCache 2.16.19 (rpm)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">7b1fb015a94565995a0546977b19f794</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.19-1.pkg">dCache 2.16.19 (Solaris package)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">a4c88299dbd3d48ba54ad08e212fc438</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.19.tar.gz">dCache 2.16.19 (tgz)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">ce670893308f954f6d609502df7b9e93</td>
</tr>
<tr id="2.16.18" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.18-1_all.deb">dCache 2.16.18 (Debian package)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">ebe83a3d73bc05b85b3916ce034a69ed</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#18">2.16.18</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.18-1.noarch.rpm">dCache 2.16.18 (rpm)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">7332813b839b76600480b69eb2ddc5ea</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.18-1.pkg">dCache 2.16.18 (Solaris package)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">023cbf4879a35bacbf058f14f1ae6c7f</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.18.tar.gz">dCache 2.16.18 (tgz)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">fb66ae2b663911bc5a5ebfd5023084a5</td>
</tr>
<tr id="2.16.17" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.17-1_all.deb">dCache 2.16.17 (Debian package)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">b83d71e0589972eaed0b321d5012bb8e</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#17">2.16.17</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.17-1.noarch.rpm">dCache 2.16.17 (rpm)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">b5b8d1bf32278bab536f975d05b81e89</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.17-1.pkg">dCache 2.16.17 (Solaris package)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">a16ca6792beb063a9e0709dc62cbbae0</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.17.tar.gz">dCache 2.16.17 (tgz)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">2ba1f6a277c28bec51adbbe5edd7af0f</td>
</tr>
<tr id="2.16.16" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.16-1_all.deb">dCache 2.16.16 (Debian package)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">e67d45a142d7962549cbb726eab01806</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#16">2.16.16</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.16-1.noarch.rpm">dCache 2.16.16 (rpm)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">b89fc7674e360376a7cae5bea2a4ebf5</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.16-1.pkg">dCache 2.16.16 (Solaris package)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">dc81d0167880fa953d36c707a3d3f019</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.16.tar.gz">dCache 2.16.16 (tgz)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">5be84cba91deb51f21e09ce9dbf61060</td>
</tr>
<tr id="2.16.15" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.15-1_all.deb">dCache 2.16.15 (Debian package)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">2d4cf767d9b7b5b4751edef8c1a3dc5c</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#15">2.16.15</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.15-1.noarch.rpm">dCache 2.16.15 (rpm)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">49b1df8dbdf9379896587e61ca7c418f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.15-1.pkg">dCache 2.16.15 (Solaris package)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">2d09f0914d72746162617f4fb0559450</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.15.tar.gz">dCache 2.16.15 (tgz)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">54fde20ede86f4fe384b80c0fa95ca22</td>
</tr>
<tr id="2.16.14" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.14-1_all.deb">dCache 2.16.14 (Debian package)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">1aabde3810522ddba2da03c57a6cb6b3</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#14">2.16.14</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.14-1.noarch.rpm">dCache 2.16.14 (rpm)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">0c196bf0aa017366d5c2f0fee17ae375</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.14-1.pkg">dCache 2.16.14 (Solaris package)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">757bcad849eeb7c3573d5a720eff50e4</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.14.tar.gz">dCache 2.16.14 (tgz)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">1f94f52648725ca69a2e9560de8b069e</td>
</tr>
<tr id="2.16.13" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.13-1_all.deb">dCache 2.16.13 (Debian package)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">3f54099b92b6b2c8eebe3a64b8db4ebf</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#13">2.16.13</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.13-1.noarch.rpm">dCache 2.16.13 (rpm)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">bdbc9dd8ba084155167a2424425432c4</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.13-1.pkg">dCache 2.16.13 (Solaris package)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">7c4298e7bc489e0af7325f95429af33e</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.13.tar.gz">dCache 2.16.13 (tgz)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">bddc65f82aaf4cbd2df64f31ee62639e</td>
</tr>
<tr id="2.16.12" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.12-1_all.deb">dCache 2.16.12 (Debian package)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">0b4d408149048a88e1d6f6c1590a7098</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#12">2.16.12</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.12-1.noarch.rpm">dCache 2.16.12 (rpm)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">96370bf7b8f17627e0b62e689cdb4027</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.12-1.pkg">dCache 2.16.12 (Solaris package)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">4a7f3e6a83ec18df112cb5627b41606e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.12.tar.gz">dCache 2.16.12 (tgz)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">2d8205131209dde6b11511193f04bfec</td>
</tr>
<tr id="2.16.11" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.11-1_all.deb">dCache 2.16.11 (Debian package)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">eaad7a43f91c571c4f99ea3efd28ef74</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#11">2.16.11</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.11-1.noarch.rpm">dCache 2.16.11 (rpm)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">fcc30ddd4cb907e28a911bd9e207dd42</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.11-1.pkg">dCache 2.16.11 (Solaris package)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">0422d8f7577acf08e8da498a8bce4ed2</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.11.tar.gz">dCache 2.16.11 (tgz)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">84feb5171123b51c801deddeb1f02e76</td>
</tr>
<tr id="2.16.10" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.10-1_all.deb">dCache 2.16.10 (Debian package)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">6588cb9f47fcd2b5b633738601077da6</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#10">2.16.10</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.10-1.noarch.rpm">dCache 2.16.10 (rpm)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">3d0316a985ca7857ebf52a1591b410bb</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.10-1.pkg">dCache 2.16.10 (Solaris package)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">86cff438564a175f299752bc9e2e796c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.10.tar.gz">dCache 2.16.10 (tgz)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">29fc806da1174e72e80463c4b7d64cbc</td>
</tr>
<tr id="2.16.9" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.9-1_all.deb">dCache 2.16.9 (Debian package)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">425bfdb80609a6bc721e52a38b98bda0</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#9">2.16.9</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.9-1.noarch.rpm">dCache 2.16.9 (rpm)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">711cc5de1ae8652127f8526a9c34c403</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.9-1.pkg">dCache 2.16.9 (Solaris package)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">34eb22a8a975f383b78d99d2f866ba4c</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.9.tar.gz">dCache 2.16.9 (tgz)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">450a010cd4b3d960612ebe565b7e36fc</td>
</tr>
<tr id="2.16.8" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.8-1_all.deb">dCache 2.16.8 (Debian package)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">1a6fe3e981b23b53db3ecea64ed07399</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#8">2.16.8</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.8-1.noarch.rpm">dCache 2.16.8 (rpm)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">0f8bef0ffc4fd7be6708604285a49c5b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.8-1.pkg">dCache 2.16.8 (Solaris package)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">904aec1028e5129b64075d650e6bc2e6</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.8.tar.gz">dCache 2.16.8 (tgz)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">fd69c01ec4883275d00d006b96403e14</td>
</tr>
<tr id="2.16.7" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.7-1_all.deb">dCache 2.16.7 (Debian package)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">cad3bc9108adb95632eb42a8f802af63</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#7">2.16.7</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.7-1.noarch.rpm">dCache 2.16.7 (rpm)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">f833adea44d1483b9215850f6ef01326</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.7-1.pkg">dCache 2.16.7 (Solaris package)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">dbaad7d8b28815fb6c649346eeb5cabb</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.7.tar.gz">dCache 2.16.7 (tgz)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">d3e2dceb331ab23c0268d9c196e077a4</td>
</tr>
<tr id="2.16.6" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.6-1_all.deb">dCache 2.16.6 (Debian package)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">00ddd19db18915c76013a8cc66d79a57</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#6">2.16.6</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.6-1.noarch.rpm">dCache 2.16.6 (rpm)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">1abe72db467eb90b360fac140fcd1469</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.6-1.pkg">dCache 2.16.6 (Solaris package)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">33e58b99f492ebc2b0e428e50dde47ca</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.6.tar.gz">dCache 2.16.6 (tgz)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">aff34e3dc842613eb53122b04a659982</td>
</tr>
<tr id="2.16.5" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.5-1_all.deb">dCache 2.16.5 (Debian package)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">c6f8d9305c331a353824658556082ee3</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#5">2.16.5</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.5-1.noarch.rpm">dCache 2.16.5 (rpm)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">113a997b49939cb3cd4ca00b39008c11</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.5-1.pkg">dCache 2.16.5 (Solaris package)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">662dc71cc4738e2dcf3bdf7b842afe5f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.5.tar.gz">dCache 2.16.5 (tgz)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">804da5252a2fcf23f90311365d4fc9d0</td>
</tr>
<tr id="2.16.4" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.4-1_all.deb">dCache 2.16.4 (Debian package)</a></td>
	<td class="date">28.6.2016</td>
	<td class="hash">b613340a18e66c7615bcc58ded1bfbb6</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#4">2.16.4</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.4-1.noarch.rpm">dCache 2.16.4 (rpm)</a></td>
	<td class="date">28.6.2016</td>
	<td class="hash">016920b1970524e06a97f16f0b55f434</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.4-1.pkg">dCache 2.16.4 (Solaris package)</a></td>
	<td class="date">28.6.2016</td>
	<td class="hash">023cbaff0f6903aad9deddcbdbd2fd38</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.4.tar.gz">dCache 2.16.4 (tgz)</a></td>
	<td class="date">28.6.2016</td>
	<td class="hash">010fc09e2701f982eeb64bbbbbb77942</td>
</tr>
<tr id="2.16.3" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.3-1_all.deb">dCache 2.16.3 (Debian package)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">df575cceb26ee09923c69bb1894a1955</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#3">2.16.3</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.3-1.noarch.rpm">dCache 2.16.3 (rpm)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">14a6c6ce4494b7fedc680ec49922b1f5</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.3-1.pkg">dCache 2.16.3 (Solaris package)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">11dd1c8a292edaf1522bbede90d17455</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.3.tar.gz">dCache 2.16.3 (tgz)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">2bcffb0e32eff9f12fd8d8dfec5de873</td>
</tr>
<tr id="2.16.2" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.2-1_all.deb">dCache 2.16.2 (Debian package)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">d429ae5e19ff96ad08e26edb2a7acf95</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#2">2.16.2</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.2-1.noarch.rpm">dCache 2.16.2 (rpm)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">6c1f16bc5a2465e0af93ebdcefaa4bb7</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.2-1.pkg">dCache 2.16.2 (Solaris package)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">e3a359bea07a6c8f6d1571b8242ee7c1</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.2.tar.gz">dCache 2.16.2 (tgz)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">f86b1a9e89117b08eb8fff415b8f0b56</td>
</tr>
<tr id="2.16.1" class="odd">
	<td class="link"><a href="repo/2.16/dcache_2.16.1-1_all.deb">dCache 2.16.1 (Debian package)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">14538b2e703e13e1f264fb52f0a8be54</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#1">2.16.1</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.1-1.noarch.rpm">dCache 2.16.1 (rpm)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">1217a4ec3b5cbf1ecf4fa1d53f6d123b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.1-1.pkg">dCache 2.16.1 (Solaris package)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">42ac297a3479424080f0cc689f53da90</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.16/dcache-2.16.1.tar.gz">dCache 2.16.1 (tgz)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">a632dd819fa185a492ebb766988eb7e2</td>
</tr>
<tr id="2.16.0" class="even">
	<td class="link"><a href="repo/2.16/dcache_2.16.0-1_all.deb">dCache 2.16.0 (Debian package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">05ef1390d78f0824703b1417c549c850</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.16.shtml#0">2.16.0</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.0-1.noarch.rpm">dCache 2.16.0 (rpm)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">820fda1559c57ea873bbcfffcfae787f</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.0-1.pkg">dCache 2.16.0 (Solaris package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">307ea0feaf2da050ddb7c4ffc61bd0da</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.16/dcache-2.16.0.tar.gz">dCache 2.16.0 (tgz)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">6035522f0879bdd5aa8e45808808b039</td>
</tr>
</tbody>
</table>
<br xmlns=""> <a xmlns="" name="server-2.15"></a> <a name="server-2.15">server 2.15.x</a> <a href="rss-server-2.15-releases.xml" type="application/rss+xml"><img class="rss-icon" src="{{site.baseurl}}/images/rss-icon-14x14.png" alt="RSS" title="RSS feed for dCache server 2.15.x releases"></a>
	
In addition to the usual improvements and bug fixes, dCache
2.15 features the following highlights:
    
<ul xmlns="">
          <li>Improved glob patterns,</li>
          <li>More robust handling of over load situations,</li>
          <li>fsck for Chimera on upgrade,</li>
          <li>Reduced storage requirements for Chimera,</li>
          <li>Chimera can store multiple checksum for a file,</li>
          <li>Admin shell documentation updates,</li>
          <li>gPlazma restriction attributes,</li>
          <li>Set ACLs through DCAP.</li>
          <li>Pool startup improvements.</li>
      </ul>
<p xmlns="">
          dCache v2.15 requires a JVM supporting Java v8.
      </p>
<table xmlns="" class="releases">
<thead>
<tr>
	<th>Download</th>
	<th>Rel. Date</th>
	<th>md5 hash</th>
	<th>Release Notes</th>
</tr>
</thead>
<tbody>
<tr id="2.15.40" class="rec">
	<td class="link"><a href="repo/2.15/dcache_2.15.40-1_all.deb">dCache 2.15.40 (Debian package)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">fe063731f9f2c0045aae08ee37c124ac</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml">2.15.40</a></td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.15/dcache-2.15.40-1.noarch.rpm">dCache 2.15.40 (rpm)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">a216a51b7fa197b16592a94b6d981c64</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.15/dcache-2.15.40-1.pkg">dCache 2.15.40 (Solaris package)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">7e907a9e45ccc807cdd7ff184ff648b2</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.15/dcache-2.15.40.tar.gz">dCache 2.15.40 (tgz)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">53ccd69dc775e1a76704e2712904ef6a</td>
</tr>
<tr id="2.15.39" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.39-1_all.deb">dCache 2.15.39 (Debian package)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">14b416c4f019f29bf65c88bd12712f36</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#39">2.15.39</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.39-1.noarch.rpm">dCache 2.15.39 (rpm)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">7d9c895826247e792a664ed907c6b6a3</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.39-1.pkg">dCache 2.15.39 (Solaris package)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">071dcf9cbdf4b1380adf6e5457fd39c8</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.39.tar.gz">dCache 2.15.39 (tgz)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">029f46d2632fbbaf1adea5ffc38e1b1c</td>
</tr>
<tr id="2.15.38" class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.38-1.noarch.rpm">dCache 2.15.38 (rpm)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">9fa4ffad6b175313163409397411d98e</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#38">2.15.38</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.38-1.pkg">dCache 2.15.38 (Solaris package)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">d72a337735d45d6d7f564e5d6e5f4724</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.38.tar.gz">dCache 2.15.38 (tgz)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">34c236f19d988f0e1af0249a9e99a29b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.38-1_all.deb">dCache 2.15.38 (Debian package)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">b0055bfe0aee16a9d565ae0bcc989088</td>
</tr>
<tr id="2.15.37" class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.37-1.noarch.rpm">dCache 2.15.37 (rpm)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">6cbe59a5bb0cad1946f592566ab969df</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#37">2.15.37</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.37-1.pkg">dCache 2.15.37 (Solaris package)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">6efd0e1e4f6f2dafa7051a88e43f343a</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.37.tar.gz">dCache 2.15.37 (tgz)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">e7e7bf052922805bb5ae7d570d354f08</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.37-1_all.deb">dCache 2.15.37 (Debian package)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">5500f492bf22f6e8f5246ac0e53cbd65</td>
</tr>
<tr id="2.15.36" class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.36-1.noarch.rpm">dCache 2.15.36 (rpm)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">d863aa6e6adc3484b2bb12448d7f12a1</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#36">2.15.36</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.36-1.pkg">dCache 2.15.36 (Solaris package)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">0a79f326a1c7172172583231a17fd6d7</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.36.tar.gz">dCache 2.15.36 (tgz)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">2a327739d58255ca1b60fb793c789ead</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.36-1_all.deb">dCache 2.15.36 (Debian package)</a></td>
	<td class="date">6.6.2017</td>
	<td class="hash">8330b2d815f2a371b5bce91b6a631017</td>
</tr>
<tr id="2.15.35" class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.35-1.noarch.rpm">dCache 2.15.35 (rpm)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">9bd65e26470801ad92cf8d1d87404467</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#35">2.15.35</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.35-1.pkg">dCache 2.15.35 (Solaris package)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">a24c63792fa802c6881010752ed0512c</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.35.tar.gz">dCache 2.15.35 (tgz)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">106374271c314ff7fa015d74aa84f003</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.35-1_all.deb">dCache 2.15.35 (Debian package)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">7cc360065445a3189a6709f110ce1c67</td>
</tr>
<tr id="2.15.34" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.34-1_all.deb">dCache 2.15.34 (Debian package)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">a44702fcb2fa4c842d69dae72fa17069</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#34">2.15.34</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.34-1.noarch.rpm">dCache 2.15.34 (rpm)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">2e4ca6e817fa3fbf3f58539e971313a9</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.34-1.pkg">dCache 2.15.34 (Solaris package)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">9cbdeb59a7c84d4467b22feffeb5963e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.34.tar.gz">dCache 2.15.34 (tgz)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">b622e865ec5812764213542b733bcc64</td>
</tr>
<tr id="2.15.33" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.33-1_all.deb">dCache 2.15.33 (Debian package)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">4809ffe742271cc56ff21016cc780235</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#33">2.15.33</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.33-1.noarch.rpm">dCache 2.15.33 (rpm)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">b783314ce9660beedb9f68fe26eced36</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.33-1.pkg">dCache 2.15.33 (Solaris package)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">95c5363a29dabd2c10d993666ba85226</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.33.tar.gz">dCache 2.15.33 (tgz)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">480aa9eb94c4f4d1d151f9b951f2df81</td>
</tr>
<tr id="2.15.32" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.32-1_all.deb">dCache 2.15.32 (Debian package)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">7f7c98486258582b81778f97efdf1751</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#32">2.15.32</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.32-1.noarch.rpm">dCache 2.15.32 (rpm)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">04a80ca4199dfdc25b47c4750ad3d342</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.32-1.pkg">dCache 2.15.32 (Solaris package)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">42d0a5b0b3f4c190b9d5350d5c2edf3f</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.32.tar.gz">dCache 2.15.32 (tgz)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">b9f1f2fb9f11f719f51e66b08ca515e9</td>
</tr>
<tr id="2.15.31" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.31-1_all.deb">dCache 2.15.31 (Debian package)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">6b925793f6e96e3790c05bc8e1aff8fd</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#31">2.15.31</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.31-1.noarch.rpm">dCache 2.15.31 (rpm)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">0e79baeef187e50c190924f5281efa47</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.31-1.pkg">dCache 2.15.31 (Solaris package)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">8082a3e486ed391c948fe1a0d1748226</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.31.tar.gz">dCache 2.15.31 (tgz)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">a263e3df394625241630b09e41c58d5e</td>
</tr>
<tr id="2.15.30" class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.30-1.noarch.rpm">dCache 2.15.30 (rpm)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">5844508bdea7acffb16fa0a6f192e8f8</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#30">2.15.30</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.30-1.pkg">dCache 2.15.30 (Solaris package)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">27668d0f63f9bb4eaba3114f12861fff</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.30.tar.gz">dCache 2.15.30 (tgz)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">ef765f65034728ae996974ba363dcb38</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.30-1_all.deb">dCache 2.15.30 (Debian package)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">3af25991fe925d9f7ac66e9ff80ba183</td>
</tr>
<tr id="2.15.29" class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.29-1.noarch.rpm">dCache 2.15.29 (rpm)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">c2f4422519da87afb0dfdfd46b609e95</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#29">2.15.29</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.29-1.pkg">dCache 2.15.29 (Solaris package)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">e6d2e40bbd692f1d4f129a10fa664517</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.29.tar.gz">dCache 2.15.29 (tgz)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">ed59457288c1f4013dd1f67d08955532</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.29-1_all.deb">dCache 2.15.29 (Debian package)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">fe615d6e5ec181c2280042868e5e911a</td>
</tr>
<tr id="2.15.28" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.28-1_all.deb">dCache 2.15.28 (Debian package)</a></td>
	<td class="date">13.12.2016</td>
	<td class="hash">83677b64ba6dc4bc589f6419e414c043</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#28">2.15.28</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.28-1.noarch.rpm">dCache 2.15.28 (rpm)</a></td>
	<td class="date">13.12.2016</td>
	<td class="hash">b04ccebd0df509562ef1cc0400f626ae</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.28-1.pkg">dCache 2.15.28 (Solaris package)</a></td>
	<td class="date">13.12.2016</td>
	<td class="hash">977d7a8b7a94f7f1f181b7362084ad4f</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.28.tar.gz">dCache 2.15.28 (tgz)</a></td>
	<td class="date">13.12.2016</td>
	<td class="hash">cf4d0b7432ea08ab5625aff0c757f17f</td>
</tr>
<tr id="2.15.27" class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.27-1.noarch.rpm">dCache 2.15.27 (rpm)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">c68e7c2351534df2d88cab886f61bf49</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#27">2.15.27</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.27-1.pkg">dCache 2.15.27 (Solaris package)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">aee109250ff00aef9563cf676535afdd</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.27.tar.gz">dCache 2.15.27 (tgz)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">025f6589eb7ccd06b4568967b8bf1f79</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.27-1_all.deb">dCache 2.15.27 (Debian package)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">6edbc9ce0dccd6962c0c81e2643299d5</td>
</tr>
<tr id="2.15.26" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.26-1_all.deb">dCache 2.15.26 (Debian package)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">7f0aefba0cac323ee5331cc1a067c10f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#26">2.15.26</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.26-1.noarch.rpm">dCache 2.15.26 (rpm)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">9f0a96e9dc6389b00c6e33aadd16eb36</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.26-1.pkg">dCache 2.15.26 (Solaris package)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">fae1d845bebd773e443ad19fe00e8cb5</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.26.tar.gz">dCache 2.15.26 (tgz)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">591c1d575fcd70f635a2d5cda4a2359a</td>
</tr>
<tr id="2.15.25" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.25-1_all.deb">dCache 2.15.25 (Debian package)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">7d195be6c743f7170628451a8b31e305</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#25">2.15.25</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.25-1.noarch.rpm">dCache 2.15.25 (rpm)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">2d99047ad3909571d0855b5e01f5a80f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.25-1.pkg">dCache 2.15.25 (Solaris package)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">c080820de80d2f2fa0b955e9dee61086</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.25.tar.gz">dCache 2.15.25 (tgz)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">0f98ab7c35f542f5ce4657e65efcda6a</td>
</tr>
<tr id="2.15.24" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.24-1_all.deb">dCache 2.15.24 (Debian package)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">c1d2d55113e182b618a8d63350b01617</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#24">2.15.24</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.24-1.noarch.rpm">dCache 2.15.24 (rpm)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">c4e7a07a9b7476d0dea02ff1adefd9f6</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.24-1.pkg">dCache 2.15.24 (Solaris package)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">e6db19a85a5b9f00d77cec1195f51504</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.24.tar.gz">dCache 2.15.24 (tgz)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">9c5f739592ce94b6160b5164fc45f525</td>
</tr>
<tr id="2.15.23" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.23-1_all.deb">dCache 2.15.23 (Debian package)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">b4020738ccdb3e279b8967a0ff4a141f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#23">2.15.23</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.23-1.noarch.rpm">dCache 2.15.23 (rpm)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">0822fb05c0fd05e1b58e59fb25ff9f6d</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.23-1.pkg">dCache 2.15.23 (Solaris package)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">e04026f377b27e2d9376359cca3afd31</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.23.tar.gz">dCache 2.15.23 (tgz)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">b1c9dc33665417058a7f0758471f7e6d</td>
</tr>
<tr id="2.15.22" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.22-1_all.deb">dCache 2.15.22 (Debian package)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">f9a5e0afb84a8bb54c00430d12a4582a</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#22">2.15.22</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.22-1.noarch.rpm">dCache 2.15.22 (rpm)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">9823c4f76d6f1c5faa929432abd5ab21</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.22-1.pkg">dCache 2.15.22 (Solaris package)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">5280ac97db44f18e9b11618d7c042a0c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.22.tar.gz">dCache 2.15.22 (tgz)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">bde71dfb1132f00583332ded9b674af3</td>
</tr>
<tr id="2.15.21" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.21-1_all.deb">dCache 2.15.21 (Debian package)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">148613fb68ccb2b6576ff61b7bcceed3</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#21">2.15.21</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.21-1.noarch.rpm">dCache 2.15.21 (rpm)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">4ff9a94c8f854eb5edefd5149e79cc56</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.21-1.pkg">dCache 2.15.21 (Solaris package)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">0fc3f85a6c44e323b7a500dcc964d54a</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.21.tar.gz">dCache 2.15.21 (tgz)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">48ee297b50c9eddffe75547e642b369d</td>
</tr>
<tr id="2.15.20" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.20-1_all.deb">dCache 2.15.20 (Debian package)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">65c85ed1210de66ac303abf4d282d9b8</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#20">2.15.20</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.20-1.noarch.rpm">dCache 2.15.20 (rpm)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">ce5e3302cd4bbf59732cc86c5d0648b8</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.20-1.pkg">dCache 2.15.20 (Solaris package)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">dc372a0d847d32d188209503346ff7d9</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.20.tar.gz">dCache 2.15.20 (tgz)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">10450f4282e19ccd1bd0fe19fd6ba38a</td>
</tr>
<tr id="2.15.19" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.19-1_all.deb">dCache 2.15.19 (Debian package)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">071d53751364a775e55bac786b37884a</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#19">2.15.19</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.19-1.noarch.rpm">dCache 2.15.19 (rpm)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">3959d47858468667be7364c549496a98</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.19-1.pkg">dCache 2.15.19 (Solaris package)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">fd83cb215985c8f97acb3fc33585da2d</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.19.tar.gz">dCache 2.15.19 (tgz)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">1d41ae5047e6869bbb82a18c3003a610</td>
</tr>
<tr id="2.15.18" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.18-1_all.deb">dCache 2.15.18 (Debian package)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">66671c019b9d2ee7d992056d2f53f0c5</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#18">2.15.18</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.18-1.noarch.rpm">dCache 2.15.18 (rpm)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">9814fdbf7af8e0727ab2b95e8531ddb4</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.18-1.pkg">dCache 2.15.18 (Solaris package)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">56c9be672a6ae5f134fe71bfe0ce9e99</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.18.tar.gz">dCache 2.15.18 (tgz)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">098d9dfa054b67123f0afed98ca7d870</td>
</tr>
<tr id="2.15.17" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.17-1_all.deb">dCache 2.15.17 (Debian package)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">e1ccfd085ab9d2a35f818ff236753a52</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#17">2.15.17</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.17-1.noarch.rpm">dCache 2.15.17 (rpm)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">312ae3c1c049e82b6f36da4ee7d25dbe</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.17-1.pkg">dCache 2.15.17 (Solaris package)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">36bf2f6613f2e035203b8d14735eecea</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.17.tar.gz">dCache 2.15.17 (tgz)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">07f2d809d96fd4282d3aad43ef42f45c</td>
</tr>
<tr id="2.15.16" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.16-1_all.deb">dCache 2.15.16 (Debian package)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">5488c342413f76aeb3969d7d86510a2f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#16">2.15.16</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.16-1.noarch.rpm">dCache 2.15.16 (rpm)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">e5cddc398abee8ccb17a30a2cf01b1c4</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.16-1.pkg">dCache 2.15.16 (Solaris package)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">72a925b2a88bd645c538ddbac49164fe</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.16.tar.gz">dCache 2.15.16 (tgz)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">67bb48cf343af3a91d6336c5bc89d21d</td>
</tr>
<tr id="2.15.15" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.15-1_all.deb">dCache 2.15.15 (Debian package)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">521c6933a89c0fd1e679c9bcd5b505ae</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#15">2.15.15</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.15-1.noarch.rpm">dCache 2.15.15 (rpm)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">1a8aeb564c1ae49be2a002e171ed5679</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.15-1.pkg">dCache 2.15.15 (Solaris package)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">b18ca76c89019a62107e8b223d3321a2</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.15.tar.gz">dCache 2.15.15 (tgz)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">eaa483db487eed858ee515eb7535a4c9</td>
</tr>
<tr id="2.15.14" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.14-1_all.deb">dCache 2.15.14 (Debian package)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">a55c50acb8cd10913bb8dd5a991eaf62</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#14">2.15.14</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.14-1.noarch.rpm">dCache 2.15.14 (rpm)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">e60d06402d7ad78b3f2a3967114e2abe</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.14-1.pkg">dCache 2.15.14 (Solaris package)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">79ac04e4cb49df211e7e588ed76cce14</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.14.tar.gz">dCache 2.15.14 (tgz)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">5ec26858cea5ab4224ac355a48aa4ab1</td>
</tr>
<tr id="2.15.13" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.13-1_all.deb">dCache 2.15.13 (Debian package)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">936e914dbafaabe8648c9a116fb4ac09</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#13">2.15.13</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.13-1.noarch.rpm">dCache 2.15.13 (rpm)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">9e6d600968cb52754c9b95544752fb81</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.13-1.pkg">dCache 2.15.13 (Solaris package)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">18a5c15929bff12796e65f1b454fa83d</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.13.tar.gz">dCache 2.15.13 (tgz)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">bcb0f9a060b269bae92b3cfa9cfcb797</td>
</tr>
<tr id="2.15.12" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.12-1_all.deb">dCache 2.15.12 (Debian package)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">747eb63c7f50a72c4e4710a5c452e820</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#12">2.15.12</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.12-1.noarch.rpm">dCache 2.15.12 (rpm)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">051f0a1a812a6b38e47894373c7ef82d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.12-1.pkg">dCache 2.15.12 (Solaris package)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">6ef50ceda2b44091f4eb11756f551922</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.12.tar.gz">dCache 2.15.12 (tgz)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">d920488d4d318828efca4aee5295d6e6</td>
</tr>
<tr id="2.15.11" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.11-1_all.deb">dCache 2.15.11 (Debian package)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">f3fd675f984bd5213b2d8119faa966f8</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#11">2.15.11</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.11-1.noarch.rpm">dCache 2.15.11 (rpm)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">8dfc5e07908b0413cd0c9e0c8f2e0791</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.11-1.pkg">dCache 2.15.11 (Solaris package)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">5c3d8f6d8e8815145c21b24607fab3fa</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.11.tar.gz">dCache 2.15.11 (tgz)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">e4e80ec95cc5efaafa188a24e0cb17c3</td>
</tr>
<tr id="2.15.10" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.10-1_all.deb">dCache 2.15.10 (Debian package)</a></td>
	<td class="date">28.6.2016</td>
	<td class="hash">87ebb481f062e31d189af9ab76481262</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#10">2.15.10</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.10-1.noarch.rpm">dCache 2.15.10 (rpm)</a></td>
	<td class="date">28.6.2016</td>
	<td class="hash">e3619d814505d0a2f2457fd7467b3f0b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.10-1.pkg">dCache 2.15.10 (Solaris package)</a></td>
	<td class="date">28.6.2016</td>
	<td class="hash">2fc47de4aeb0e3f9250e89685fed3a9b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.10.tar.gz">dCache 2.15.10 (tgz)</a></td>
	<td class="date">28.6.2016</td>
	<td class="hash">9c45847243fb8b575e836112e9d70497</td>
</tr>
<tr id="2.15.9" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.9-1_all.deb">dCache 2.15.9 (Debian package)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">0d1d9cb402499ce414ca7974c266ee64</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#9">2.15.9</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.9-1.noarch.rpm">dCache 2.15.9 (rpm)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">f329efcb7ebbd389986a36dd7ef8f746</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.9-1.pkg">dCache 2.15.9 (Solaris package)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">e3c4d42fdae5f4f47217b62ac775039b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.9.tar.gz">dCache 2.15.9 (tgz)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">59bfd8c1dde428cd6fe2587bae48bc10</td>
</tr>
<tr id="2.15.8" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.8-1_all.deb">dCache 2.15.8 (Debian package)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">39901e0bee90bc11d33865c5ecb8a2d9</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#8">2.15.8</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.8-1.noarch.rpm">dCache 2.15.8 (rpm)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">f8b8307cc468d181664ae0c3034b3210</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.8-1.pkg">dCache 2.15.8 (Solaris package)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">5b5bce7263a795f8a8fffcda8470aecf</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.8.tar.gz">dCache 2.15.8 (tgz)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">d2298e1737e427b77c14bcddb894df25</td>
</tr>
<tr id="2.15.7" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.7-1_all.deb">dCache 2.15.7 (Debian package)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">b618799b257a1cea8121a410a76975fc</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#7">2.15.7</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.7-1.noarch.rpm">dCache 2.15.7 (rpm)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">0d35722df496f4a9f246901fd64083c6</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.7-1.pkg">dCache 2.15.7 (Solaris package)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">d900b064c6c8db715eba49d508b46f52</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.7.tar.gz">dCache 2.15.7 (tgz)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">fd6cf6a9eb8584cf726fe8e17c4f0720</td>
</tr>
<tr id="2.15.6" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.6-1_all.deb">dCache 2.15.6 (Debian package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">a77141309b50016e8599f82ad0f0cd4b</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#6">2.15.6</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.6-1.noarch.rpm">dCache 2.15.6 (rpm)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">59722b39eedb276fd0bc4121d09f98f0</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.6-1.pkg">dCache 2.15.6 (Solaris package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">af494f6774717f6ef788fdde419e92a8</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.6.tar.gz">dCache 2.15.6 (tgz)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">4c195fc46638e0c598f1708e2f914ed3</td>
</tr>
<tr id="2.15.5" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.5-1_all.deb">dCache 2.15.5 (Debian package)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">5881038df8aaa550ac07466703790e88</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#5">2.15.5</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.5-1.noarch.rpm">dCache 2.15.5 (rpm)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">579b67830fb970020041fa62d058bdfe</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.5-1.pkg">dCache 2.15.5 (Solaris package)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">568aff89f862628fdc04a13a75199e56</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.5.tar.gz">dCache 2.15.5 (tgz)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">2cbdf66d7007764a53d60c63bf0abea8</td>
</tr>
<tr id="2.15.4" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.4-1_all.deb">dCache 2.15.4 (Debian package)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">e1f8b5998d61cc59bf00b33e6838e1c3</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#4">2.15.4</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.4-1.noarch.rpm">dCache 2.15.4 (rpm)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">a2ba9fb0169d71b84cbc2ef7d4ae4c83</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.4-1.pkg">dCache 2.15.4 (Solaris package)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">d7ece2e987c9c119340360e3cfe4e2e6</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.4.tar.gz">dCache 2.15.4 (tgz)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">c073552d7e64fcee1499512ec41aa11f</td>
</tr>
<tr id="2.15.3" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.3-1_all.deb">dCache 2.15.3 (Debian package)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">50ed0244f82f7bab0b50c86e47a23cf2</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#3">2.15.3</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.3-1.noarch.rpm">dCache 2.15.3 (rpm)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">84920afdee12d11709f536a523f14693</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.3-1.pkg">dCache 2.15.3 (Solaris package)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">19cc21278c95178c3898f99d4b1dbabc</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.3.tar.gz">dCache 2.15.3 (tgz)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">9e3c0f24e6bb56a5e9b38168db37e4e2</td>
</tr>
<tr id="2.15.2" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.2-1_all.deb">dCache 2.15.2 (Debian package)</a></td>
	<td class="date">15.3.2016</td>
	<td class="hash">61989a5b66a55a7e108d273b62bbf336</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#2">2.15.2</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.2-1.noarch.rpm">dCache 2.15.2 (rpm)</a></td>
	<td class="date">15.3.2016</td>
	<td class="hash">0f29723b0552b0243a7b4263403638b2</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.2-1.pkg">dCache 2.15.2 (Solaris package)</a></td>
	<td class="date">15.3.2016</td>
	<td class="hash">5a6af248fbe5f5f5bb6b7341b04227f5</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.2.tar.gz">dCache 2.15.2 (tgz)</a></td>
	<td class="date">15.3.2016</td>
	<td class="hash">0ba55b674df4f1b1631e56fe426a6a2d</td>
</tr>
<tr id="2.15.1" class="odd">
	<td class="link"><a href="repo/2.15/dcache_2.15.1-1_all.deb">dCache 2.15.1 (Debian package)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">b35f22197e9b4854a9e776b4e2e9cd37</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#1">2.15.1</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.1-1.noarch.rpm">dCache 2.15.1 (rpm)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">878d833c2deb31a0a25ab4880d586ce6</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.1-1.pkg">dCache 2.15.1 (Solaris package)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">0d3afc037d0ad7aca2c234cff446f8a5</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.15/dcache-2.15.1.tar.gz">dCache 2.15.1 (tgz)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">2f6d7ad0bd8416629b36ad0ae7b781ac</td>
</tr>
<tr id="2.15.0" class="even">
	<td class="link"><a href="repo/2.15/dcache_2.15.0-1_all.deb">dCache 2.15.0 (Debian package)</a></td>
	<td class="date">4.3.2016</td>
	<td class="hash">2e5b8402894437072c8a8ba5fe5ab5a0</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.15.shtml#0">2.15.0</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.0-1.noarch.rpm">dCache 2.15.0 (rpm)</a></td>
	<td class="date">4.3.2016</td>
	<td class="hash">b64dd2ef538fed789760720ae200fd0d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.0-1.pkg">dCache 2.15.0 (Solaris package)</a></td>
	<td class="date">4.3.2016</td>
	<td class="hash">5722df503c741a23ce6adb525f252696</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.15/dcache-2.15.0.tar.gz">dCache 2.15.0 (tgz)</a></td>
	<td class="date">4.3.2016</td>
	<td class="hash">0253c02525cb69d15df4a2ee9d15c913</td>
</tr>
</tbody>
</table>
<br xmlns=""> <a xmlns="" name="server-2.14"></a> <a name="server-2.14">server 2.14.x</a> <a href="rss-server-2.14-releases.xml" type="application/rss+xml"><img class="rss-icon" src="{{site.baseurl}}/images/rss-icon-14x14.png" alt="RSS" title="RSS feed for dCache server 2.14.x releases"></a>
	
	
In addition to the usual improvements and bug fixes, dCache
2.14 features the following highlights:

<ul xmlns="">
	  <li>Significant performance and storage space improvements in Chimera,</li>
	  <li>OCSP support and EUGRIDPMA name space support,</li>
	  <li>Concurrent request processing in gPlazma,</li>
	  <li>Pool group patterns in admin shell,</li>
	  <li>Improved UberFTP support,</li>
	  <li>WebDAV door can report file locality,</li>
	  <li>Fair share scheduling for SRM transfers,</li>
	  <li>SRM database managed by liquibase,</li>
	  <li>Configurable kXR_Qconfig support for xrootd.</li>
      </ul>
<p xmlns="">
	  dCache v2.14 requires a JVM supporting Java v8.
      </p>
<table xmlns="" class="releases">
<thead>
<tr>
	<th>Download</th>
	<th>Rel. Date</th>
	<th>md5 hash</th>
	<th>Release Notes</th>
</tr>
</thead>
<tbody>
<tr id="2.14.51" class="rec">
	<td class="link"><a href="repo/2.14/dcache_2.14.51-1_all.deb">dCache 2.14.51 (Debian package)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">31fc507554f404afff6804b1ea6e13aa</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml">2.14.51</a></td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.14/dcache-2.14.51-1.noarch.rpm">dCache 2.14.51 (rpm)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">ddb6e27ec02084875b9bb6a64b4b720a</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.14/dcache-2.14.51-1.pkg">dCache 2.14.51 (Solaris package)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">1d0c10974b9e99cc09431f3610ad6596</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.14/dcache-2.14.51.tar.gz">dCache 2.14.51 (tgz)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">a5fe36eda8a8f66ffffee009a8c8fece</td>
</tr>
<tr id="2.14.50" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.50-1_all.deb">dCache 2.14.50 (Debian package)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">f12a8cd35e88366a1bdc600a8a09b6c8</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#50">2.14.50</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.50-1.noarch.rpm">dCache 2.14.50 (rpm)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">3ab54891d42d36e84f9fbd0de2928a10</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.50-1.pkg">dCache 2.14.50 (Solaris package)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">a67e179209026e48f3eb31fca6550c21</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.50.tar.gz">dCache 2.14.50 (tgz)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">7c42de5158560def7ea10ae8381448ec</td>
</tr>
<tr id="2.14.49" class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.49-1.noarch.rpm">dCache 2.14.49 (rpm)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">07fcdd569cba6165fa6372aff84117d1</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#49">2.14.49</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.49-1.pkg">dCache 2.14.49 (Solaris package)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">28ba73571270cc4703dae9b642917af0</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.49.tar.gz">dCache 2.14.49 (tgz)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">365f49b22d6025785017cc122060d151</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.49-1_all.deb">dCache 2.14.49 (Debian package)</a></td>
	<td class="date">21.6.2017</td>
	<td class="hash">e022957d86fa21e35a998d72f865597a</td>
</tr>
<tr id="2.14.48" class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.48-1.noarch.rpm">dCache 2.14.48 (rpm)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">fce688d60cb257fe42a3262e24fd8189</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#48">2.14.48</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.48-1.pkg">dCache 2.14.48 (Solaris package)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">6c00795fdc6ca07f0374529e53e77127</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.48.tar.gz">dCache 2.14.48 (tgz)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">fe2439ecdbd46062eb977e48eb627547</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.48-1_all.deb">dCache 2.14.48 (Debian package)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">adcbc8aec2181d96d6aec93c16b51f3f</td>
</tr>
<tr id="2.14.47" class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.47-1.noarch.rpm">dCache 2.14.47 (rpm)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">29ca5886169f70a57da4464b84f656f8</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#47">2.14.47</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.47-1.pkg">dCache 2.14.47 (Solaris package)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">22910eddaa159df9ab03d73898508146</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.47.tar.gz">dCache 2.14.47 (tgz)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">516d623fc271c915b3745b549dfa1da7</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.47-1_all.deb">dCache 2.14.47 (Debian package)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">875025c3c35b6fb024f99574e9ca9475</td>
</tr>
<tr id="2.14.46" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.46-1_all.deb">dCache 2.14.46 (Debian package)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">eab814d466a37d737b9ced3f6e1c3df9</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#46">2.14.46</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.46-1.noarch.rpm">dCache 2.14.46 (rpm)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">2088a29ac235c1642f296670aa48ebea</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.46-1.pkg">dCache 2.14.46 (Solaris package)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">79618ebbefc42337677055da5104bd00</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.46.tar.gz">dCache 2.14.46 (tgz)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">3405dc1072beb5e795f8fd8d970f408d</td>
</tr>
<tr id="2.14.45" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.45-1_all.deb">dCache 2.14.45 (Debian package)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">fb65e2651b4e8d37fb6eef7602acaea7</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#45">2.14.45</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.45-1.noarch.rpm">dCache 2.14.45 (rpm)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">97969ec240c459e5122b406fef344b50</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.45-1.pkg">dCache 2.14.45 (Solaris package)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">8d3d3d44c8bdd054bd0e00a692f54b7c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.45.tar.gz">dCache 2.14.45 (tgz)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">f725c2c6c859777b11a2369fce4de12c</td>
</tr>
<tr id="2.14.44" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.44-1_all.deb">dCache 2.14.44 (Debian package)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">99f6a85ab2bd2ad0b1e687673c5fbdf5</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#44">2.14.44</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.44-1.noarch.rpm">dCache 2.14.44 (rpm)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">0782def74911416136e549a056156470</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.44-1.pkg">dCache 2.14.44 (Solaris package)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">7b77079a9b8778383e477bac6f9c14ba</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.44.tar.gz">dCache 2.14.44 (tgz)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">0f5689065f539643a58e7cf8325c517f</td>
</tr>
<tr id="2.14.43" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.43-1_all.deb">dCache 2.14.43 (Debian package)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">628de8f92592c0b046a5cc24ac81fdfe</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#43">2.14.43</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.43-1.noarch.rpm">dCache 2.14.43 (rpm)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">ccb94a42bcf49d1572fb32c1fce8de5b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.43-1.pkg">dCache 2.14.43 (Solaris package)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">d55eedea4e884ebbb122bbc95ed09437</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.43.tar.gz">dCache 2.14.43 (tgz)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">63b9a9945f0f2bfffc0484f0a24825b3</td>
</tr>
<tr id="2.14.42" class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.42-1.noarch.rpm">dCache 2.14.42 (rpm)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">27d37375f5e0f8743426e49431516056</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#42">2.14.42</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.42-1.pkg">dCache 2.14.42 (Solaris package)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">234e41a23b7678b35c771f266b3ee67b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.42.tar.gz">dCache 2.14.42 (tgz)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">009483e827fda1a02ff16dc6e480582f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.42-1_all.deb">dCache 2.14.42 (Debian package)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">2e24021990818495262eaeabc8ef3bba</td>
</tr>
<tr id="2.14.41" class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.41-1.noarch.rpm">dCache 2.14.41 (rpm)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">beac3a6490b850521b27b456760f0ec7</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#41">2.14.41</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.41-1.pkg">dCache 2.14.41 (Solaris package)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">a0c6439989f6d9322d9b7cf25e6a0d9c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.41.tar.gz">dCache 2.14.41 (tgz)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">963075c2da9898e3bbcb1d3ce7a689e0</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.41-1_all.deb">dCache 2.14.41 (Debian package)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">15e89dcd874b3850fe154a9086a39c47</td>
</tr>
<tr id="2.14.40" class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.40-1.noarch.rpm">dCache 2.14.40 (rpm)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">c2c0fe2d9e1523b4561c5d83e2dfeb23</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#40">2.14.40</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.40-1.pkg">dCache 2.14.40 (Solaris package)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">6336db973a319eef0efc4a0c8d9ea7a5</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.40.tar.gz">dCache 2.14.40 (tgz)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">e8198e6f245cbeb9b4aa842cb515d539</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.40-1_all.deb">dCache 2.14.40 (Debian package)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">2ac8e39f6abe849b5f575bb7a990d597</td>
</tr>
<tr id="2.14.39" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.39-1_all.deb">dCache 2.14.39 (Debian package)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">bf49e1957ecd6cfb51d49c4551ff277f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#39">2.14.39</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.39-1.noarch.rpm">dCache 2.14.39 (rpm)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">68b61af0ad02b8f574690b67f77e3a85</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.39-1.pkg">dCache 2.14.39 (Solaris package)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">e23220f8735a75de8cd46f5b02c80800</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.39.tar.gz">dCache 2.14.39 (tgz)</a></td>
	<td class="date">29.11.2016</td>
	<td class="hash">f675036b02f4c5cb3cac4f48bb8aac97</td>
</tr>
<tr id="2.14.38" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.38-1_all.deb">dCache 2.14.38 (Debian package)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">3ea9079fc9d23be3232c726cdeb142b4</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#38">2.14.38</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.38-1.noarch.rpm">dCache 2.14.38 (rpm)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">d5611e522bda3b3c2e9b3e6733a61832</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.38-1.pkg">dCache 2.14.38 (Solaris package)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">247d92796c44f9835a640508e2bda3d1</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.38.tar.gz">dCache 2.14.38 (tgz)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">c5b333af7d282dea51363231176a4cf0</td>
</tr>
<tr id="2.14.37" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.37-1_all.deb">dCache 2.14.37 (Debian package)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">aac61e63303b30c00d235ff567bb8241</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#37">2.14.37</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.37-1.noarch.rpm">dCache 2.14.37 (rpm)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">9a01a98f78c00c3a9d433fa0c2fdb0bd</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.37-1.pkg">dCache 2.14.37 (Solaris package)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">3f909b96c6f7e0bc37e067da9fd85c66</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.37.tar.gz">dCache 2.14.37 (tgz)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">8f839218e70d26bb41bb56b2a5f9af2e</td>
</tr>
<tr id="2.14.36" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.36-1_all.deb">dCache 2.14.36 (Debian package)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">6f3f510e7eac79eb7c3a2a1911e51651</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#36">2.14.36</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.36-1.noarch.rpm">dCache 2.14.36 (rpm)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">541c263cdecbecf49e0eedc11d24604e</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.36-1.pkg">dCache 2.14.36 (Solaris package)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">40aea88280bd8628afe183661f4a620f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.36.tar.gz">dCache 2.14.36 (tgz)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">259e0e85af920247531dbd4a4e9fec60</td>
</tr>
<tr id="2.14.35" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.35-1_all.deb">dCache 2.14.35 (Debian package)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">d4cf74484172c95cdee25d1ad64046de</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#35">2.14.35</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.35-1.noarch.rpm">dCache 2.14.35 (rpm)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">ea4804bb7532b8ab39757e17145d8ef9</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.35-1.pkg">dCache 2.14.35 (Solaris package)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">274410473ef2e52116f82a9fd0cca405</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.35.tar.gz">dCache 2.14.35 (tgz)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">e4e07930704e98b5b807e3c633c4f865</td>
</tr>
<tr id="2.14.34" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.34-1_all.deb">dCache 2.14.34 (Debian package)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">0138012419bc0c0a21b6eabd68984e62</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#34">2.14.34</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.34-1.noarch.rpm">dCache 2.14.34 (rpm)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">56aa47caf0070952cda88239148bda5b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.34-1.pkg">dCache 2.14.34 (Solaris package)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">79d8431c05192dbde52679fc2411f83a</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.34.tar.gz">dCache 2.14.34 (tgz)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">e4f6b3f58ab8bb4a4530503782f2bd2c</td>
</tr>
<tr id="2.14.33" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.33-1_all.deb">dCache 2.14.33 (Debian package)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">970e6cfcfab14d72a63de786480d4b01</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#33">2.14.33</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.33-1.noarch.rpm">dCache 2.14.33 (rpm)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">f94f4a31c1d61e8468075c03f400179d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.33-1.pkg">dCache 2.14.33 (Solaris package)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">40af5968c58933316c385f060830bd1a</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.33.tar.gz">dCache 2.14.33 (tgz)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">fd4ad18b5bec01ecf7d676fd9efd5081</td>
</tr>
<tr id="2.14.32" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.32-1_all.deb">dCache 2.14.32 (Debian package)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">da410ecf30d34989745e7a034659cfde</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#32">2.14.32</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.32-1.noarch.rpm">dCache 2.14.32 (rpm)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">85cfee7c3eafcc5c2fc3d77725c3e5d7</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.32-1.pkg">dCache 2.14.32 (Solaris package)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">546d97b6072f3efaf0aac562464c0e84</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.32.tar.gz">dCache 2.14.32 (tgz)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">9343a69b00e4bff979f994da27701764</td>
</tr>
<tr id="2.14.31" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.31-1_all.deb">dCache 2.14.31 (Debian package)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">08315a11e7c6b848c276666dfeed2b97</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#31">2.14.31</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.31-1.noarch.rpm">dCache 2.14.31 (rpm)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">39570ca408669867a32a64a9e59845e1</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.31-1.pkg">dCache 2.14.31 (Solaris package)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">31575a9dcffd39ad2573d7c45d9595ad</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.31.tar.gz">dCache 2.14.31 (tgz)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">2cc9ef903727116e1edb02c985cf6de8</td>
</tr>
<tr id="2.14.30" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.30-1_all.deb">dCache 2.14.30 (Debian package)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">0317a33ba9bb4a3bb45571818c85117e</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#30">2.14.30</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.30-1.noarch.rpm">dCache 2.14.30 (rpm)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">aad246fab1f5a35685fd19c0b8847f9b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.30-1.pkg">dCache 2.14.30 (Solaris package)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">aa0209a4816f85e66fae71b3e665e229</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.30.tar.gz">dCache 2.14.30 (tgz)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">68c553e08815b16125e244f48765cc1c</td>
</tr>
<tr id="2.14.29" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.29-1_all.deb">dCache 2.14.29 (Debian package)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">1cca92a7fd684c545d93b1c7c8761dd7</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#29">2.14.29</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.29-1.noarch.rpm">dCache 2.14.29 (rpm)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">c4f6ad37006228244b4383bbcdf7889e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.29-1.pkg">dCache 2.14.29 (Solaris package)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">cfdb22fa4fa258366555c2fc786282fd</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.29.tar.gz">dCache 2.14.29 (tgz)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">6f97cf3c2cc367a5f35bbda06e74629c</td>
</tr>
<tr id="2.14.28" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.28-1_all.deb">dCache 2.14.28 (Debian package)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">1bd2aa8fabfe593cd43ef1496c6b9345</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#28">2.14.28</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.28-1.noarch.rpm">dCache 2.14.28 (rpm)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">d110642722ae7cf78d4e40236b828fa8</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.28-1.pkg">dCache 2.14.28 (Solaris package)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">f178a47fab01ae5fca8341f3e584be50</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.28.tar.gz">dCache 2.14.28 (tgz)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">af0b1cc2141dd357ac01df2e419e9696</td>
</tr>
<tr id="2.14.27" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.27-1_all.deb">dCache 2.14.27 (Debian package)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">2700c211ba9922a21eba9a4391ad7f2c</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#27">2.14.27</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.27-1.noarch.rpm">dCache 2.14.27 (rpm)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">1666d0e08d95bb5c2217e21c35c88e3c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.27-1.pkg">dCache 2.14.27 (Solaris package)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">0479ad2a94ef108a7e4212d77efd42e4</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.27.tar.gz">dCache 2.14.27 (tgz)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">0b38ff1ebddfac7dd373e6efdab9ed2c</td>
</tr>
<tr id="2.14.26" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.26-1_all.deb">dCache 2.14.26 (Debian package)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">66a96a6bde98333fff1636f84497de2c</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.14.shtml#26">2.14.26</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.26-1.noarch.rpm">dCache 2.14.26 (rpm)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">6fd5ac28924a0c123b51eec205cb7975</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.26.tar.gz">dCache 2.14.26 (tgz)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">124e1bb2da0f8f5fa2d9fe72400b9c70</td>
</tr>
<tr id="2.14.25" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.25-1_all.deb">dCache 2.14.25 (Debian package)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">d0377e10a979ab5376b4ceb663995063</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#25">2.14.25</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.25-1.noarch.rpm">dCache 2.14.25 (rpm)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">e184c5ccff987185ab6230e8021d4e8e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.25-1.pkg">dCache 2.14.25 (Solaris package)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">0f768ab4af0c93d067ab085b82b5d58e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.25.tar.gz">dCache 2.14.25 (tgz)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">4375398e94a275c9407e3c7d0bb4fcd9</td>
</tr>
<tr id="2.14.24" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.24-1_all.deb">dCache 2.14.24 (Debian package)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">cb740cc952e90d201d1b5d778c742e82</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#24">2.14.24</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.24-1.noarch.rpm">dCache 2.14.24 (rpm)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">375ad044e72136f3c5021ba4129a574f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.24-1.pkg">dCache 2.14.24 (Solaris package)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">0a7d1a798283ff9e467b36824bba6a37</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.24.tar.gz">dCache 2.14.24 (tgz)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">0d6776bbd5a27c3cfdde99ec187b52c6</td>
</tr>
<tr id="2.14.23" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.23-1_all.deb">dCache 2.14.23 (Debian package)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">4919ece0653af0e27b95e2ffd423ff19</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#23">2.14.23</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.23-1.noarch.rpm">dCache 2.14.23 (rpm)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">eda4f55eb66043c3d587af79691b9693</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.23-1.pkg">dCache 2.14.23 (Solaris package)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">964060ea24140e649108f8525c54cd4e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.23.tar.gz">dCache 2.14.23 (tgz)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">9c0a02e02e95753c7192981877e58631</td>
</tr>
<tr id="2.14.22" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.22-1_all.deb">dCache 2.14.22 (Debian package)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">d5021dcd7ddbd5fdfbf6c7cc172ed1e7</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#22">2.14.22</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.22-1.noarch.rpm">dCache 2.14.22 (rpm)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">5dd1310f5a620c597c00389bc90005c1</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.22-1.pkg">dCache 2.14.22 (Solaris package)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">7f4d94d1d173c8a2e1f9185223077c90</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.22.tar.gz">dCache 2.14.22 (tgz)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">0beaf1b679bf72b1b4a086ef9b0aab5f</td>
</tr>
<tr id="2.14.21" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.21-1_all.deb">dCache 2.14.21 (Debian package)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">28702e7078fc536284eb9d88423c28d4</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#21">2.14.21</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.21-1.noarch.rpm">dCache 2.14.21 (rpm)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">aba2fedbe05c8b5cf64d083e57534b03</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.21-1.pkg">dCache 2.14.21 (Solaris package)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">7f3d8018a39565cd03f3aaec85a0fcb3</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.21.tar.gz">dCache 2.14.21 (tgz)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">96604d181d5f4a0f3884c21c1566d81b</td>
</tr>
<tr id="2.14.20" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.20-1_all.deb">dCache 2.14.20 (Debian package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">07a6994a623f633fd2764da2819c316d</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#20">2.14.20</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.20-1.noarch.rpm">dCache 2.14.20 (rpm)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">47c83219d953f06844d0cbd4cef40524</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.20-1.pkg">dCache 2.14.20 (Solaris package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">b0a79acb56494e609cb2c56b0c270528</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.20.tar.gz">dCache 2.14.20 (tgz)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">b89853416d9e4495db3a21fcd1dfebf3</td>
</tr>
<tr id="2.14.19" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.19-1_all.deb">dCache 2.14.19 (Debian package)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">19a7332ed8d18449a1166f5b77ca63ae</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.14.shtml#19">2.14.19</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.19-1.noarch.rpm">dCache 2.14.19 (rpm)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">b38af98df4d84a75a57870f5f2c445c0</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.19.tar.gz">dCache 2.14.19 (tgz)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">973a03262d83ff54e8e4205ff019cca9</td>
</tr>
<tr id="2.14.18" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.18-1_all.deb">dCache 2.14.18 (Debian package)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">671c21befc8141b837157477fdc71225</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#18">2.14.18</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.18-1.noarch.rpm">dCache 2.14.18 (rpm)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">6d5662b54116e628ff8db68f1c81db1f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.18-1.pkg">dCache 2.14.18 (Solaris package)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">19b9201197f4c0282b12adbeacced7ed</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.18.tar.gz">dCache 2.14.18 (tgz)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">77612c2d8396384ccbc9b40d3954aef5</td>
</tr>
<tr id="2.14.17" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.17-1_all.deb">dCache 2.14.17 (Debian package)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">22285b38369fbcfda41ec76972b8542b</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#17">2.14.17</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.17-1.noarch.rpm">dCache 2.14.17 (rpm)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">d5c167533d8dc731e49e884955aac795</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.17-1.pkg">dCache 2.14.17 (Solaris package)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">1523373891cd63ac50d48b611f8fc47d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.17.tar.gz">dCache 2.14.17 (tgz)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">1ec9869c2a902955b7f804e6d58a8edc</td>
</tr>
<tr id="2.14.16" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.16-1_all.deb">dCache 2.14.16 (Debian package)</a></td>
	<td class="date">15.3.2016</td>
	<td class="hash">882d9922749fd4fbb54ca82c8e05a18c</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#16">2.14.16</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.16-1.noarch.rpm">dCache 2.14.16 (rpm)</a></td>
	<td class="date">15.3.2016</td>
	<td class="hash">406f678753a0bc9f978f906b8659fb31</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.16-1.pkg">dCache 2.14.16 (Solaris package)</a></td>
	<td class="date">15.3.2016</td>
	<td class="hash">f49fc5c270b3bd201c2667f0ec91d984</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.16.tar.gz">dCache 2.14.16 (tgz)</a></td>
	<td class="date">15.3.2016</td>
	<td class="hash">a71bfde2394ab0253ed41e4a60d82411</td>
</tr>
<tr id="2.14.15" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.15-1_all.deb">dCache 2.14.15 (Debian package)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">04492b70c0a30ee4eefcde441a7e85cb</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.14.shtml#15">2.14.15</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.15-1.noarch.rpm">dCache 2.14.15 (rpm)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">742eae3d831bed6665d13a65d5e7921d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.15.tar.gz">dCache 2.14.15 (tgz)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">ec5b0d78343bf390b02fd8583216cb30</td>
</tr>
<tr id="2.14.14" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.14-1_all.deb">dCache 2.14.14 (Debian package)</a></td>
	<td class="date">4.3.2016</td>
	<td class="hash">95830d8fdfaedee080e1095f8f7b2954</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#14">2.14.14</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.14-1.noarch.rpm">dCache 2.14.14 (rpm)</a></td>
	<td class="date">4.3.2016</td>
	<td class="hash">6936b5953e8a72ca59fd84a04cadeb49</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.14-1.pkg">dCache 2.14.14 (Solaris package)</a></td>
	<td class="date">4.3.2016</td>
	<td class="hash">c5da5302399c20e89ad042ebb09ec3d1</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.14.tar.gz">dCache 2.14.14 (tgz)</a></td>
	<td class="date">4.3.2016</td>
	<td class="hash">0241ef94cc6bcaf0e08aad5b4433bf56</td>
</tr>
<tr id="2.14.13" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.13-1_all.deb">dCache 2.14.13 (Debian package)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">95dde1ef80791380f1b14808da32d5e1</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#13">2.14.13</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.13-1.noarch.rpm">dCache 2.14.13 (rpm)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">52f85584991c8906882b249a8266a51e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.13-1.pkg">dCache 2.14.13 (Solaris package)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">0940f99df886f5307c6cdcce5db15036</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.13.tar.gz">dCache 2.14.13 (tgz)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">cd1fb93424650d7bcf453566c44de4db</td>
</tr>
<tr id="2.14.12" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.12-1_all.deb">dCache 2.14.12 (Debian package)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">34e44ce2156914bec9349d02516e0e61</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#12">2.14.12</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.12-1.noarch.rpm">dCache 2.14.12 (rpm)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">33f4131ec31b95f57c96e37a7f7e13e0</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.12-1.pkg">dCache 2.14.12 (Solaris package)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">4f88fecafea3a785434c3862f7720de8</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.12.tar.gz">dCache 2.14.12 (tgz)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">3e9cc659b143c4bd86ac5828e7552472</td>
</tr>
<tr id="2.14.11" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.11-1_all.deb">dCache 2.14.11 (Debian package)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">b15bef8195ddc3287f6420c4b47a56af</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#11">2.14.11</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.11-1.noarch.rpm">dCache 2.14.11 (rpm)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">186f1defcc0543e042e030864621a213</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.11-1.pkg">dCache 2.14.11 (Solaris package)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">a1d5cc3d40ce19e978f279115b730159</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.11.tar.gz">dCache 2.14.11 (tgz)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">7a9bbbab3f9b98e8a14b2901155f934c</td>
</tr>
<tr id="2.14.10" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.10-1_all.deb">dCache 2.14.10 (Debian package)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">de4c97d6123080e6a530d15b31dc723b</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#10">2.14.10</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.10-1.noarch.rpm">dCache 2.14.10 (rpm)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">1d8d9ed53998fae0c583a63fc79b39ce</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.10-1.pkg">dCache 2.14.10 (Solaris package)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">a4cd69b37ff18c202794f4cd7ff89dec</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.10.tar.gz">dCache 2.14.10 (tgz)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">885d510b622cc5b7b61d8fbbeedb4e5e</td>
</tr>
<tr id="2.14.9" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.9-1_all.deb">dCache 2.14.9 (Debian package)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">5223841ac7f65adf37adf0072dcd6307</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#9">2.14.9</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.9-1.noarch.rpm">dCache 2.14.9 (rpm)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">6644c6f4d0febedbdc2790eb7b10c8a8</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.9-1.pkg">dCache 2.14.9 (Solaris package)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">7d39567d0bec01ec269fe48bc4f8e90e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.9.tar.gz">dCache 2.14.9 (tgz)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">efedfadaaa01d8fd6f2155a8ef0f637d</td>
</tr>
<tr id="2.14.8" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.8-1_all.deb">dCache 2.14.8 (Debian package)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">377599f00f8898e64d799677b0d94449</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#8">2.14.8</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.8-1.noarch.rpm">dCache 2.14.8 (rpm)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">3d53acffcc4d562b83aa1dc348cbc7ee</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.8-1.pkg">dCache 2.14.8 (Solaris package)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">ce56711c66e6ae70effd84891b996b91</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.8.tar.gz">dCache 2.14.8 (tgz)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">5ba213e04542638616d6c6fec119c5e2</td>
</tr>
<tr id="2.14.7" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.7-1_all.deb">dCache 2.14.7 (Debian package)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">b8bd53670174e2127f102070195e4281</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#7">2.14.7</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.7-1.noarch.rpm">dCache 2.14.7 (rpm)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">cbfa7cd055e4e095e92fc4475710725c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.7-1.pkg">dCache 2.14.7 (Solaris package)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">a405854fc965752c080f5a29477931ab</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.7.tar.gz">dCache 2.14.7 (tgz)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">db6526c5b1874f4f4bc8c1d3ce7888a2</td>
</tr>
<tr id="2.14.6" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.6-1_all.deb">dCache 2.14.6 (Debian package)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">6fc9459736313838c68a1962bedb037d</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#6">2.14.6</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.6-1.noarch.rpm">dCache 2.14.6 (rpm)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">b64f52293fafb5643ee857b8efe49cbd</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.6-1.pkg">dCache 2.14.6 (Solaris package)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">26d2857a4715251a933f92429424a1d6</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.6.tar.gz">dCache 2.14.6 (tgz)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">df2ca0467341cbf79eab898dfafc336c</td>
</tr>
<tr id="2.14.5" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.5-1_all.deb">dCache 2.14.5 (Debian package)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">41f99e1d3a26e17c98968b4f555c3f08</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#5">2.14.5</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.5-1.noarch.rpm">dCache 2.14.5 (rpm)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">dfd29ac80fb5de325dbd8cf57eaf553f</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.5-1.pkg">dCache 2.14.5 (Solaris package)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">0ab0a43546fc5023bef3befd323e7e21</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.5.tar.gz">dCache 2.14.5 (tgz)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">272e47b584c95fd4802436d5854430e2</td>
</tr>
<tr id="2.14.4" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.4-1_all.deb">dCache 2.14.4 (Debian package)</a></td>
	<td class="date">11.12.2015</td>
	<td class="hash">9a99071d2835e1341018274832d8dc7d</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#4">2.14.4</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.4-1.noarch.rpm">dCache 2.14.4 (rpm)</a></td>
	<td class="date">11.12.2015</td>
	<td class="hash">535ea863460ea5c020afeaa1074ceeb0</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.4-1.pkg">dCache 2.14.4 (Solaris package)</a></td>
	<td class="date">11.12.2015</td>
	<td class="hash">794f86d1d9ca8ae6a1c55e81babe37a5</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.4.tar.gz">dCache 2.14.4 (tgz)</a></td>
	<td class="date">11.12.2015</td>
	<td class="hash">757ee8703fb58fdaf90b73499af0b5e9</td>
</tr>
<tr id="2.14.3" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.3-1_all.deb">dCache 2.14.3 (Debian package)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">a468a71d11ca552084baac190263784c</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#3">2.14.3</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.3-1.noarch.rpm">dCache 2.14.3 (rpm)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">00516ae685a1adaac360406976acc639</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.3-1.pkg">dCache 2.14.3 (Solaris package)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">34330dd5d2c3abb270a62838cf1ce904</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.3.tar.gz">dCache 2.14.3 (tgz)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">9c1fa0a2f268a651f25c8a764b4cf8a3</td>
</tr>
<tr id="2.14.2" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.2-1_all.deb">dCache 2.14.2 (Debian package)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">73cd6b39e55fd8d4fe81a01214cba61b</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#2">2.14.2</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.2-1.noarch.rpm">dCache 2.14.2 (rpm)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">bbce94b4e57287a1dbed1c1b318a55cd</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.2-1.pkg">dCache 2.14.2 (Solaris package)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">b09f17805f10d528e96164fab96918c3</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.2.tar.gz">dCache 2.14.2 (tgz)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">2e5cd9abed0104f422c183fea8b614a2</td>
</tr>
<tr id="2.14.1" class="even">
	<td class="link"><a href="repo/2.14/dcache_2.14.1-1_all.deb">dCache 2.14.1 (Debian package)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">4145ffe88124b08b16d7027c77ee6228</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.14.shtml#1">2.14.1</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.1-1.noarch.rpm">dCache 2.14.1 (rpm)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">045455383c74f0c55369e7ce2e1bf7ab</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.1-1.pkg">dCache 2.14.1 (Solaris package)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">e0d472a265759c8dc7c6464f0cf3acd7</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.14/dcache-2.14.1.tar.gz">dCache 2.14.1 (tgz)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">5d70cb02231d591beea75bf34d217686</td>
</tr>
<tr id="2.14.0" class="odd">
	<td class="link"><a href="repo/2.14/dcache_2.14.0-1_all.deb">dCache 2.14.0 (Debian package)</a></td>
	<td class="date">18.11.2015</td>
	<td class="hash">f6bd5d285a8412b8808a75bd4dd1bc9e</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.14.shtml#0">2.14.0</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.0-1.noarch.rpm">dCache 2.14.0 (rpm)</a></td>
	<td class="date">18.11.2015</td>
	<td class="hash">c15c9d3314e9295fafb9007487164693</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.14/dcache-2.14.0.tar.gz">dCache 2.14.0 (tgz)</a></td>
	<td class="date">18.11.2015</td>
	<td class="hash">cb08fcd5186cf3e71ed46f1b5f62ba66</td>
</tr>
</tbody>
</table>
<br xmlns=""> <a xmlns="" name="server-2.13"></a> <a name="server-2.13">server 2.13.x</a> <a href="rss-server-2.13-releases.xml" type="application/rss+xml"><img class="rss-icon" src="{{site.baseurl}}/images/rss-icon-14x14.png" alt="RSS" title="RSS feed for dCache server 2.13.x releases"></a>
	
	
In addition to the usual improvements and bug fixes, dCache
2.13 features the following highlights:
 
<ul xmlns="">
	  <li>major overhaul of admin interface,</li>
	  <li>robust internal delete and flush notification,</li>
	  <li>info-provider generates timestamps on published objects,</li>
	  <li>pool migration module maintains last-access-time,</li>
	  <li>pool implements strict LRU garbage collection,</li>
	  <li>improved shutdown in space-manager,</li>
	  <li>Reserving space from a linkgroup may be authorised by GID,</li>
	  <li>better scalability in FTP doors,</li>
	  <li>new admin commands for nfs service,</li>
	  <li>FTS-specific information recorded,</li>
	  <li>xrootd doors support the protocol's asynchronous open,</li>
	  <li>support for custom HTTP response headers.</li>
      </ul>
<p xmlns="">
	  dCache v2.13 requires a JVM supporting Java v8.
      </p>
<table xmlns="" class="releases">
<thead>
<tr>
	<th>Download</th>
	<th>Rel. Date</th>
	<th>md5 hash</th>
	<th>Release Notes</th>
</tr>
</thead>
<tbody>
<tr id="2.13.61" class="rec">
	<td class="link"><a href="repo/2.13/dcache_2.13.61-1_all.deb">dCache 2.13.61 (Debian package)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">0ed90b35c457ea58b64a6d435a073ce7</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml">2.13.61</a></td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.13/dcache-2.13.61-1.noarch.rpm">dCache 2.13.61 (rpm)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">e5dded2ff680943ad313c8c68418a3ea</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.13/dcache-2.13.61-1.pkg">dCache 2.13.61 (Solaris package)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">2d6e0e7f0d10c256de7d2bdead6f652c</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.13/dcache-2.13.61.tar.gz">dCache 2.13.61 (tgz)</a></td>
	<td class="date">2.8.2017</td>
	<td class="hash">a0d66f51e164280cd88291fd7c7ac343</td>
</tr>
<tr id="2.13.60" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.60-1_all.deb">dCache 2.13.60 (Debian package)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">c35c1b7f02e78e68b368fd04ec0fe7f2</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#60">2.13.60</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.60-1.noarch.rpm">dCache 2.13.60 (rpm)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">9ef06a14ac04203c1fd1dc52d420b373</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.60-1.pkg">dCache 2.13.60 (Solaris package)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">7efb714ee95a326933773bcc7adf6526</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.60.tar.gz">dCache 2.13.60 (tgz)</a></td>
	<td class="date">5.7.2017</td>
	<td class="hash">3a73d4db9af19915ddd23b70b42f3e9a</td>
</tr>
<tr id="2.13.59" class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.59-1.noarch.rpm">dCache 2.13.59 (rpm)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">e95139c56cd86922e2d290ab28249393</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#59">2.13.59</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.59-1.pkg">dCache 2.13.59 (Solaris package)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">8c5a8a94e3d0f1948f3a284d08f6483b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.59.tar.gz">dCache 2.13.59 (tgz)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">cfc1384c9f881a7810df46073e49cab7</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.59-1_all.deb">dCache 2.13.59 (Debian package)</a></td>
	<td class="date">14.6.2017</td>
	<td class="hash">fdfaa77480f93fec992ac33d6780d11d</td>
</tr>
<tr id="2.13.58" class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.58-1.noarch.rpm">dCache 2.13.58 (rpm)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">00603ab8e2b50e0de52255ae4f922fee</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#58">2.13.58</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.58-1.pkg">dCache 2.13.58 (Solaris package)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">1b6960d92666a555690d7222cffc6fd9</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.58.tar.gz">dCache 2.13.58 (tgz)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">2997121a55e35ecbeceb994ca618ca7e</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.58-1_all.deb">dCache 2.13.58 (Debian package)</a></td>
	<td class="date">9.5.2017</td>
	<td class="hash">4890dbbd1c7b94f019ce0109f17f84e2</td>
</tr>
<tr id="2.13.57" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.57-1_all.deb">dCache 2.13.57 (Debian package)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">f4b2c012c514674f56e6f13d8e68070f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#57">2.13.57</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.57-1.noarch.rpm">dCache 2.13.57 (rpm)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">74902accf8f18ec0277bf9feb71a337d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.57-1.pkg">dCache 2.13.57 (Solaris package)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">b886c7725c4f0e8cb31ccaa3842f94cd</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.57.tar.gz">dCache 2.13.57 (tgz)</a></td>
	<td class="date">30.3.2017</td>
	<td class="hash">ef4f0cd334ee50a02c31d3c0047c16e4</td>
</tr>
<tr id="2.13.56" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.56-1_all.deb">dCache 2.13.56 (Debian package)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">8c99ac4e5dd55eb1111af78444a13a9a</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#56">2.13.56</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.56-1.noarch.rpm">dCache 2.13.56 (rpm)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">b570d9c1878675183bcadc5e8442347d</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.56-1.pkg">dCache 2.13.56 (Solaris package)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">b38d35f509de5cc566e0e280477511ac</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.56.tar.gz">dCache 2.13.56 (tgz)</a></td>
	<td class="date">20.3.2017</td>
	<td class="hash">349c3e54e827fe7261918ff510a1b6a9</td>
</tr>
<tr id="2.13.55" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.55-1_all.deb">dCache 2.13.55 (Debian package)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">0e9cce6969d8b53356ed4e974ab04d6a</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#55">2.13.55</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.55-1.noarch.rpm">dCache 2.13.55 (rpm)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">83aeae21d37a170ae517e4f52a0e5131</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.55-1.pkg">dCache 2.13.55 (Solaris package)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">66bd74fa7ddc6e73ffc1ee5c790c6a64</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.55.tar.gz">dCache 2.13.55 (tgz)</a></td>
	<td class="date">7.3.2017</td>
	<td class="hash">5e031660a1d5b808aff645cac7a3da8b</td>
</tr>
<tr id="2.13.54" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.54-1_all.deb">dCache 2.13.54 (Debian package)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">49158787ddc6e86989e34fe82e76655f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#54">2.13.54</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.54-1.noarch.rpm">dCache 2.13.54 (rpm)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">cff64e66942e7cb285ae34211f3ceeb7</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.54-1.pkg">dCache 2.13.54 (Solaris package)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">bf70c119217499b1624457c3b4c997df</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.54.tar.gz">dCache 2.13.54 (tgz)</a></td>
	<td class="date">22.2.2017</td>
	<td class="hash">cabf0bca3775d53d6d4cdec2f6889948</td>
</tr>
<tr id="2.13.53" class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.53-1.noarch.rpm">dCache 2.13.53 (rpm)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">70076e3c25883a3254b2e36db10af465</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#53">2.13.53</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.53-1.pkg">dCache 2.13.53 (Solaris package)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">db5b111aa1705260fc665758faf7cef0</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.53.tar.gz">dCache 2.13.53 (tgz)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">b5f56082e85e10115fe4fbe327d246e8</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.53-1_all.deb">dCache 2.13.53 (Debian package)</a></td>
	<td class="date">16.2.2017</td>
	<td class="hash">dc3c2171a3dae8822ba820ab66e08f0e</td>
</tr>
<tr id="2.13.52" class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.52-1.noarch.rpm">dCache 2.13.52 (rpm)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">ccfa4c99aff818c1fb54c99041ec3fe7</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#52">2.13.52</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.52-1.pkg">dCache 2.13.52 (Solaris package)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">b9371a55abcbf460f2e3f4fd7a1da501</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.52.tar.gz">dCache 2.13.52 (tgz)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">436903825535673698d7bdb748f5c85f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.52-1_all.deb">dCache 2.13.52 (Debian package)</a></td>
	<td class="date">7.2.2017</td>
	<td class="hash">6ee16db5a3a7e81179b304c236ace718</td>
</tr>
<tr id="2.13.51" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.51-1_all.deb">dCache 2.13.51 (Debian package)</a></td>
	<td class="date">17.1.2017</td>
	<td class="hash">975f15e7bd31482f3993c08bcae37ccb</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#51">2.13.51</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.51-1.noarch.rpm">dCache 2.13.51 (rpm)</a></td>
	<td class="date">17.1.2017</td>
	<td class="hash">91f27bd724d6fac450a414dd3ff1b55f</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.51-1.pkg">dCache 2.13.51 (Solaris package)</a></td>
	<td class="date">17.1.2017</td>
	<td class="hash">3f6978fc36b34362235b654e9f59137d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.51.tar.gz">dCache 2.13.51 (tgz)</a></td>
	<td class="date">17.1.2017</td>
	<td class="hash">0cabacdcd49a819b2f8c9ecdef6c4819</td>
</tr>
<tr id="2.13.50" class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.50-1.noarch.rpm">dCache 2.13.50 (rpm)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">53fa1b2567c48e3747e0f3d5c0d8e5f1</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#50">2.13.50</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.50-1.pkg">dCache 2.13.50 (Solaris package)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">cea758837df9a368eb3a922a105fc598</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.50.tar.gz">dCache 2.13.50 (tgz)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">d43e85bda131ff16d8e731f02f0b7680</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.50-1_all.deb">dCache 2.13.50 (Debian package)</a></td>
	<td class="date">6.12.2016</td>
	<td class="hash">76bf0fd913d6f758fe6b96c9af963c34</td>
</tr>
<tr id="2.13.49" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.49-1_all.deb">dCache 2.13.49 (Debian package)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">586ae6ffe2ec2ba664e37c6cc5e25196</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#49">2.13.49</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.49-1.noarch.rpm">dCache 2.13.49 (rpm)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">f0cfae4b2cda54b989a272d7eb162c11</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.49-1.pkg">dCache 2.13.49 (Solaris package)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">7d28a4d00fbaf33d71b8540b7c55522e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.49.tar.gz">dCache 2.13.49 (tgz)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">348ff6daa47716e1afbf0114f2660069</td>
</tr>
<tr id="2.13.48" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.48-1_all.deb">dCache 2.13.48 (Debian package)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">15fb9cb1ce30041ed6af77290a980b5a</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#48">2.13.48</a></td>
</tr>
<tr class="odd">        
	<td class="link"><a href="repo/2.13/dcache-2.13.48-1.noarch.rpm">dCache 2.13.48 (rpm)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">50f2b5741a361e522d7bff17da18df58</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.48-1.pkg">dCache 2.13.48 (Solaris package)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">e9a9905f25b12398b2edc1d48bcc0f3a</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.48.tar.gz">dCache 2.13.48 (tgz)</a></td>
	<td class="date">28.10.2016</td>
	<td class="hash">e1ca71f5314a060775bba9076cd94260</td>
</tr>
<tr id="2.13.47" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.47-1_all.deb">dCache 2.13.47 (Debian package)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">19bddb8a6ed9210900dcc9cfeb77a0e4</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#47">2.13.47</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.47-1.noarch.rpm">dCache 2.13.47 (rpm)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">13f1524026541bd92aaf4f1601817a38</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.47-1.pkg">dCache 2.13.47 (Solaris package)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">1e79de12ded35f5311a0cc8563bffcc3</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.47.tar.gz">dCache 2.13.47 (tgz)</a></td>
	<td class="date">11.10.2016</td>
	<td class="hash">ae32910db687faad67806e414ce51dd8</td>
</tr>
<tr id="2.13.46" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.46-1_all.deb">dCache 2.13.46 (Debian package)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">e5e89130342f3b462dcef573bf248e82</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#46">2.13.46</a></td>
</tr>
<tr class="odd">        
	<td class="link"><a href="repo/2.13/dcache-2.13.46-1.noarch.rpm">dCache 2.13.46 (rpm)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">ead46a3ce0b5cb90eb1650ee180a59fc</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.46-1.pkg">dCache 2.13.46 (Solaris package)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">3459e481f0a72a59ba278e7526117e1f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.46.tar.gz">dCache 2.13.46 (tgz)</a></td>
	<td class="date">5.10.2016</td>
	<td class="hash">733b093650920c062589642b86ec52e8</td>
</tr>
<tr id="2.13.45" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.45-1_all.deb">dCache 2.13.45 (Debian package)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">8ddb340ee467f189f0888026d3c691c4</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#45">2.13.45</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.45-1.noarch.rpm">dCache 2.13.45 (rpm)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">759039c3df6663a8d068d00f813d9d83</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.45-1.pkg">dCache 2.13.45 (Solaris package)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">db45284078028e1eaddb7656960bc89c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.45.tar.gz">dCache 2.13.45 (tgz)</a></td>
	<td class="date">27.9.2016</td>
	<td class="hash">d40c08dec86bbe81b85f00bb6b62deea</td>
</tr>
<tr id="2.13.44" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.44-1_all.deb">dCache 2.13.44 (Debian package)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">5df1613f10b636ee3bad649d27470797</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#44">2.13.44</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.44-1.noarch.rpm">dCache 2.13.44 (rpm)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">1a363a10b0f0395389e80f623289661c</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.44-1.pkg">dCache 2.13.44 (Solaris package)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">78b73a929006251d982dc22ad004face</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.44.tar.gz">dCache 2.13.44 (tgz)</a></td>
	<td class="date">22.9.2016</td>
	<td class="hash">4abd68681bf4f30d6a4af2aa8a72865c</td>
</tr>
<tr id="2.13.43" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.43-1_all.deb">dCache 2.13.43 (Debian package)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">f0aae92addef7f417a507681171d8eb7</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#43">2.13.43</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.43-1.noarch.rpm">dCache 2.13.43 (rpm)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">1d2fbc6ee2e09ee04e3f87091c92dcac</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.43-1.pkg">dCache 2.13.43 (Solaris package)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">faeee0ef28744dcb63bb47a05e67e06b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.43.tar.gz">dCache 2.13.43 (tgz)</a></td>
	<td class="date">14.9.2016</td>
	<td class="hash">e44fb61c9a0765a00257f3c13fa5709b</td>
</tr>
<tr id="2.13.42" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.42-1_all.deb">dCache 2.13.42 (Debian package)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">67254a69508462f37132a421bd84518b</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#42">2.13.42</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.42-1.noarch.rpm">dCache 2.13.42 (rpm)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">65acb1abb5886dc5cb75bc431da72266</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.42-1.pkg">dCache 2.13.42 (Solaris package)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">347deb616e05d69792b6b1097a40d40b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.42.tar.gz">dCache 2.13.42 (tgz)</a></td>
	<td class="date">6.9.2016</td>
	<td class="hash">0f7b66f536ab95016a55e70152f159f0</td>
</tr>
<tr id="2.13.41" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.41-1_all.deb">dCache 2.13.41 (Debian package)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">f6af3e2b487516add112dc9a1a29a178</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#41">2.13.41</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.41-1.noarch.rpm">dCache 2.13.41 (rpm)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">89f515d7a0e8078d72be62747c212081</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.41-1.pkg">dCache 2.13.41 (Solaris package)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">67b857251e040e24737721cd6c8ffea8</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.41.tar.gz">dCache 2.13.41 (tgz)</a></td>
	<td class="date">30.8.2016</td>
	<td class="hash">6481fca65f17a4b1b5e24f306ceaad4d</td>
</tr>
<tr id="2.13.40" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.40-1_all.deb">dCache 2.13.40 (Debian package)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">55cd9e90e94f1622ac305ce3b330aa86</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#40">2.13.40</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.40-1.noarch.rpm">dCache 2.13.40 (rpm)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">0873c70821ba000cfb78290d19ea02c6</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.40-1.pkg">dCache 2.13.40 (Solaris package)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">66660243c4597df381a47f733e078960</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.40.tar.gz">dCache 2.13.40 (tgz)</a></td>
	<td class="date">23.8.2016</td>
	<td class="hash">ffc13f322bab3f3db48443b5a83306b1</td>
</tr>
<tr id="2.13.39" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.39-1_all.deb">dCache 2.13.39 (Debian package)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">be5dd5379ab562345783def46c53d09b</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#39">2.13.39</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.39-1.noarch.rpm">dCache 2.13.39 (rpm)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">a1d903158d108f3d972f9c2536439937</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.39-1.pkg">dCache 2.13.39 (Solaris package)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">628eaa1fd852f7e978a443ccabd9b636</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.39.tar.gz">dCache 2.13.39 (tgz)</a></td>
	<td class="date">16.8.2016</td>
	<td class="hash">1e94ed4d9951ebfa584a55f6324954fb</td>
</tr>
<tr id="2.13.38" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.38-1_all.deb">dCache 2.13.38 (Debian package)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">8308ab40abb6a3409a78d7113057b829</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#38">2.13.38</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.38-1.noarch.rpm">dCache 2.13.38 (rpm)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">b58a33dd81dadc12f1d7c9549ca9e21a</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.38-1.pkg">dCache 2.13.38 (Solaris package)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">b2d17313c06dd9bd63337da64ff5044e</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.38.tar.gz">dCache 2.13.38 (tgz)</a></td>
	<td class="date">9.8.2016</td>
	<td class="hash">2606c5494fe6f7b88faa8e897878cf4a</td>
</tr>
<tr id="2.13.37" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.37-1_all.deb">dCache 2.13.37 (Debian package)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">4b47c1ade521f2f4378ba8fb76896827</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#37">2.13.37</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.37-1.noarch.rpm">dCache 2.13.37 (rpm)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">7d88bf49706bcbeb37e04947ebc2276f</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.37.tar.gz">dCache 2.13.37 (tgz)</a></td>
	<td class="date">2.8.2016</td>
	<td class="hash">8d0d1c0a649bd6fbec76a4c0a4777eb5</td>
</tr>
<tr id="2.13.36" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.36-1_all.deb">dCache 2.13.36 (Debian package)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">de9f3ddd41be31376f2d529710be4c72</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#36">2.13.36</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.36-1.noarch.rpm">dCache 2.13.36 (rpm)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">ba87919579e7ee0e74c7f6970de16ff6</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.36-1.pkg">dCache 2.13.36 (Solaris package)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">51b016affabd0cc38520d03d6b704c9b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.36.tar.gz">dCache 2.13.36 (tgz)</a></td>
	<td class="date">20.7.2016</td>
	<td class="hash">16eb2cfdfe526048f5e85509f8cd704b</td>
</tr>
<tr id="2.13.35" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.35-1_all.deb">dCache 2.13.35 (Debian package)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">4741ddf0fa20dfe1e2dd7f4fdd6e31cf</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#35">2.13.35</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.35-1.noarch.rpm">dCache 2.13.35 (rpm)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">fc7f72d273950fcf6d7ed3defe65cdc1</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.35-1.pkg">dCache 2.13.35 (Solaris package)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">eaf14a61b6c9cdbf9cc5d14fe5524254</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.35.tar.gz">dCache 2.13.35 (tgz)</a></td>
	<td class="date">13.7.2016</td>
	<td class="hash">c7ea2d5a450e2820dcd1ff0bb229d02c</td>
</tr>
<tr id="2.13.34" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.34-1_all.deb">dCache 2.13.34 (Debian package)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">ad0181050ff3b74f7a1d1652e8f8f905</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#34">2.13.34</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.34-1.noarch.rpm">dCache 2.13.34 (rpm)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">0a7f3e3a2ed23ce411b6241662b896ca</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.34-1.pkg">dCache 2.13.34 (Solaris package)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">84dab5d7f3a6070fa40821209b36a3a4</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.34.tar.gz">dCache 2.13.34 (tgz)</a></td>
	<td class="date">21.6.2016</td>
	<td class="hash">2dc6d84a085fc91c2e0d5b915da836f6</td>
</tr>
<tr id="2.13.33" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.33-1_all.deb">dCache 2.13.33 (Debian package)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">74c5b8afb5439124c1158c0b62744145</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#33">2.13.33</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.33-1.noarch.rpm">dCache 2.13.33 (rpm)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">2c37a94a35607f5be9fc29d52c7572c1</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.33-1.pkg">dCache 2.13.33 (Solaris package)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">73e3966ef7418f4e6ff70b3140a6fa4b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.33.tar.gz">dCache 2.13.33 (tgz)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">62109125fcf9df08bbbe17a9b17623e1</td>
</tr>
<tr id="2.13.32" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.32-1_all.deb">dCache 2.13.32 (Debian package)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">29fa9e9ee5814115bb02984ca6edfa6c</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#32">2.13.32</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.32-1.noarch.rpm">dCache 2.13.32 (rpm)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">71d4d4339772010ef0c91749c46f17df</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.32-1.pkg">dCache 2.13.32 (Solaris package)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">0bcd9298b15acd5ac2e43cbcfe361125</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.32.tar.gz">dCache 2.13.32 (tgz)</a></td>
	<td class="date">7.6.2016</td>
	<td class="hash">4225cace943df785ea4de3c162d32f8a</td>
</tr>
<tr id="2.13.31" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.31-1_all.deb">dCache 2.13.31 (Debian package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">0762f039d6f1af4d60298d071e729caf</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#31">2.13.31</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.31-1.noarch.rpm">dCache 2.13.31 (rpm)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">b6609422f3f14cebb189040dae0b13bd</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.31-1.pkg">dCache 2.13.31 (Solaris package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">16b6a810fe4f97b9b9228f676dc29b74</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.31.tar.gz">dCache 2.13.31 (tgz)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">c2976067fa90cd781e82ccc94def52b3</td>
</tr>
<tr id="2.13.30" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.30-1_all.deb">dCache 2.13.30 (Debian package)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">008df51a185443e1a0a4087f6ce55ac3</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#30">2.13.30</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.30-1.noarch.rpm">dCache 2.13.30 (rpm)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">21891ec6f60ac249edac89dae143263b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.30-1.pkg">dCache 2.13.30 (Solaris package)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">910be6b82e152804e9e1530a755dd40f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.30.tar.gz">dCache 2.13.30 (tgz)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">c3175e08c91e12719507ebf5e802ae02</td>
</tr>
<tr id="2.13.29" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.29-1_all.deb">dCache 2.13.29 (Debian package)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">d6c6fdd41c494bb390547b90cc5bf863</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#29">2.13.29</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.29-1.noarch.rpm">dCache 2.13.29 (rpm)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">3d90fc02ea057ea5c2994a9f561977ce</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.29-1.pkg">dCache 2.13.29 (Solaris package)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">fd8769c96a48a583be0fdd55945fa7ad</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.29.tar.gz">dCache 2.13.29 (tgz)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">03470b350e54b6d82f6640463a1a9226</td>
</tr>
<tr id="2.13.28" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.28-1_all.deb">dCache 2.13.28 (Debian package)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">7b2d87eb02f11936ca7f3430b170ef00</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#28">2.13.28</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.28-1.noarch.rpm">dCache 2.13.28 (rpm)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">3d40043130ab96f52cc95b75cac4c217</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.28-1.pkg">dCache 2.13.28 (Solaris package)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">36c14cafd02a53795866ff54b4e0fdb7</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.28.tar.gz">dCache 2.13.28 (tgz)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">9fbec1c2d4ae7635f9fa6a91f0bc9b62</td>
</tr>
<tr id="2.13.27" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.27-1_all.deb">dCache 2.13.27 (Debian package)</a></td>
	<td class="date">15.3.2016</td>
	<td class="hash">82d7385d3f9ba7327feac70ac162d4b4</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#27">2.13.27</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.27-1.noarch.rpm">dCache 2.13.27 (rpm)</a></td>
	<td class="date">15.3.2016</td>
	<td class="hash">6642e148e2d04fb6796fe2b65a66364e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.27-1.pkg">dCache 2.13.27 (Solaris package)</a></td>
	<td class="date">15.3.2016</td>
	<td class="hash">15c261a3dd80d6e778473abe021cc94c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.27.tar.gz">dCache 2.13.27 (tgz)</a></td>
	<td class="date">15.3.2016</td>
	<td class="hash">879d1c6f3906f58d891245f17c984075</td>
</tr>
<tr id="2.13.26" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.26-1_all.deb">dCache 2.13.26 (Debian package)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">72d863aec1f6d28de7991bb0505b06f7</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#26">2.13.26</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.26-1.noarch.rpm">dCache 2.13.26 (rpm)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">4a960ec666b215240bb7de4c7ddb70ab</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.26-1.pkg">dCache 2.13.26 (Solaris package)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">3f55658baa60e83b53a6c35a016300f7</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.26.tar.gz">dCache 2.13.26 (tgz)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">74ac7a49d74edff3fd48104152d9eeac</td>
</tr>
<tr id="2.13.25" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.25-1_all.deb">dCache 2.13.25 (Debian package)</a></td>
	<td class="date">4.3.2016</td>
	<td class="hash">2eaf4c34f52145ce2602b9b7b35784a0</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#25">2.13.25</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.25-1.noarch.rpm">dCache 2.13.25 (rpm)</a></td>
	<td class="date">4.3.2016</td>
	<td class="hash">000e8e40116abaa41d70e28b262c33c1</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.25-1.pkg">dCache 2.13.25 (Solaris package)</a></td>
	<td class="date">4.3.2016</td>
	<td class="hash">cd0fd19188aa83ef0ec3136ebdb4baed</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.25.tar.gz">dCache 2.13.25 (tgz)</a></td>
	<td class="date">4.3.2016</td>
	<td class="hash">30eeec48aaf214a6d261d520d5d05729</td>
</tr>
<tr id="2.13.24" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.24-1_all.deb">dCache 2.13.24 (Debian package)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">c09b97452ecdc4e7adf1c4d2c783fccb</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#24">2.13.24</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.24-1.noarch.rpm">dCache 2.13.24 (rpm)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">4f0843d4ee323c64ae6905263fb0868f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.24-1.pkg">dCache 2.13.24 (Solaris package)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">25bde90e27083bd57fdd9b22832d8d88</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.24.tar.gz">dCache 2.13.24 (tgz)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">d75a6d9e88cb50c6c9494325af313fce</td>
</tr>
<tr id="2.13.23" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.23-1_all.deb">dCache 2.13.23 (Debian package)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">17bcd8a3088b10bbb9b365b07ec14586</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#23">2.13.23</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.23-1.noarch.rpm">dCache 2.13.23 (rpm)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">486d3a4e6c15b3209afa0da3af712a39</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.23-1.pkg">dCache 2.13.23 (Solaris package)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">ae3bc460eeb0d61141531b47813ac625</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.23.tar.gz">dCache 2.13.23 (tgz)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">998cd22227f38b294764e86fe1fa7099</td>
</tr>
<tr id="2.13.22" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.22-1_all.deb">dCache 2.13.22 (Debian package)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">b5ed577482d6075c053dfc5cb2ef8aa4</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#22">2.13.22</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.22-1.noarch.rpm">dCache 2.13.22 (rpm)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">c8e1f4c2cf6185c146cfc817c326870b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.22-1.pkg">dCache 2.13.22 (Solaris package)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">97b6420946621b43ec6d860a22f17aab</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.22.tar.gz">dCache 2.13.22 (tgz)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">71c897618067c5b6dbfd5681ada2e1ba</td>
</tr>
<tr id="2.13.21" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.21-1_all.deb">dCache 2.13.21 (Debian package)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">37d375a777319f1f61aee00d3fb1cc92</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#21">2.13.21</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.21-1.noarch.rpm">dCache 2.13.21 (rpm)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">baed99a2a8881655b735ad31d8d3636c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.21-1.pkg">dCache 2.13.21 (Solaris package)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">7f522c9e970d6b63e379cbecf90651d0</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.21.tar.gz">dCache 2.13.21 (tgz)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">f6d4327ec2e9860de7797e34fd703ea5</td>
</tr>
<tr id="2.13.20" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.20-1_all.deb">dCache 2.13.20 (Debian package)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">2eb07e67ed1fdefb9960367e3bb501d1</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#20">2.13.20</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.20-1.noarch.rpm">dCache 2.13.20 (rpm)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">894e4643b8545c12fd63fc3ceab86e7b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.20-1.pkg">dCache 2.13.20 (Solaris package)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">4c05e89974953454da140eb615be1569</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.20.tar.gz">dCache 2.13.20 (tgz)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">235c5ee52e23c9ca06c64acea4c5f361</td>
</tr>
<tr id="2.13.19" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.19-1_all.deb">dCache 2.13.19 (Debian package)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">e24599e49db8be758b74d8118c654adb</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#19">2.13.19</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.19-1.noarch.rpm">dCache 2.13.19 (rpm)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">795a535113d3ff2a596b133706b66eed</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.19-1.pkg">dCache 2.13.19 (Solaris package)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">2168408b92e9a8d26f896d5e36be4af6</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.19.tar.gz">dCache 2.13.19 (tgz)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">9bed1357b31a14df42bed1bd2da666a8</td>
</tr>
<tr id="2.13.18" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.18-1_all.deb">dCache 2.13.18 (Debian package)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">e0b8618fbb6cdd1f3ea9134d36c14974</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#18">2.13.18</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.18-1.noarch.rpm">dCache 2.13.18 (rpm)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">a731b375928446cf58dc4c88b67e7b00</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.18-1.pkg">dCache 2.13.18 (Solaris package)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">5c0d330a98ce9d575feb2b68ca3ba15a</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.18.tar.gz">dCache 2.13.18 (tgz)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">a04796c795b12da6934bbb70dea5497b</td>
</tr>
<tr id="2.13.17" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.17-1_all.deb">dCache 2.13.17 (Debian package)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">abd98ba90cdc31f46b3b6417ae081d6a</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#17">2.13.17</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.17-1.noarch.rpm">dCache 2.13.17 (rpm)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">6b8d50f18c721c6c000ce0d7c5902da9</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.17-1.pkg">dCache 2.13.17 (Solaris package)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">50a2f9f13db923a8f51f320cf5f27f43</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.17.tar.gz">dCache 2.13.17 (tgz)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">913f0d5540ef43382480fa2edf6fd63d</td>
</tr>
<tr id="2.13.16" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.16-1_all.deb">dCache 2.13.16 (Debian package)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">d63cb0fe61b85eaa0982a68d12f9a8d3</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#16">2.13.16</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.16-1.noarch.rpm">dCache 2.13.16 (rpm)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">8f060af77e1f861682816c99a1d9a11d</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.16-1.pkg">dCache 2.13.16 (Solaris package)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">bebf474207c563ec4c963ea7b67e9232</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.16.tar.gz">dCache 2.13.16 (tgz)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">4dbcf2f37ed300fd51513009f6f28c40</td>
</tr>
<tr id="2.13.15" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.15-1_all.deb">dCache 2.13.15 (Debian package)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">eab40d7ce35c93494518e3679ba836a2</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#15">2.13.15</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.15-1.noarch.rpm">dCache 2.13.15 (rpm)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">7d0ec08c289931948226c1aee011cf48</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.15-1.pkg">dCache 2.13.15 (Solaris package)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">4468598c8cb196f70bd712217b65db2a</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.15.tar.gz">dCache 2.13.15 (tgz)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">4ac087f06f702545359afb41bf747641</td>
</tr>
<tr id="2.13.14" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.14-1_all.deb">dCache 2.13.14 (Debian package)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">341343c45871ce228a868c29ef6669e1</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#14">2.13.14</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.14-1.noarch.rpm">dCache 2.13.14 (rpm)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">f1e69ab1d841761641324f516cbf0778</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.14-1.pkg">dCache 2.13.14 (Solaris package)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">f213397a684d91f595afa8f38a566d8b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.14.tar.gz">dCache 2.13.14 (tgz)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">f15a7664a06415565a8421594700ad82</td>
</tr>
<tr id="2.13.13" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.13-1_all.deb">dCache 2.13.13 (Debian package)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">edcb31f685abbc836b61b2c82dc787b2</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.13.shtml#13">2.13.13</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.13-1.noarch.rpm">dCache 2.13.13 (rpm)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">ae7ff76b78f2df01241f36001a626cce</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.13-1.pkg">dCache 2.13.13 (Solaris package)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">50c5fe6759621da5badce51b24203fda</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.13.tar.gz">dCache 2.13.13 (tgz)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">eb37d7088c58a26bd09b107ce1cad585</td>
</tr>
<tr id="2.13.12" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.12-1_all.deb">dCache 2.13.12 (Debian package)</a></td>
	<td class="date">2.11.2015</td>
	<td class="hash">4115d6ea767a31fa94391b17de95d2a9</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#12">2.13.12</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.12-1.noarch.rpm">dCache 2.13.12 (rpm)</a></td>
	<td class="date">2.11.2015</td>
	<td class="hash">c15c9d3314e9295fafb9007487164693</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.12.tar.gz">dCache 2.13.12 (tgz)</a></td>
	<td class="date">2.11.2015</td>
	<td class="hash">27bacb919c1b5b2f0bbce09060531cb1</td>
</tr>
<tr id="2.13.11" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.11-1_all.deb">dCache 2.13.11 (Debian package)</a></td>
	<td class="date">27.10.2015</td>
	<td class="hash">2d45090bad60126a061cf3e3d85123b3</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#11">2.13.11</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.11-1.noarch.rpm">dCache 2.13.11 (rpm)</a></td>
	<td class="date">27.10.2015</td>
	<td class="hash">ee045caad0ddf6d31df3096859d3ff2c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.11.tar.gz">dCache 2.13.11 (tgz)</a></td>
	<td class="date">27.10.2015</td>
	<td class="hash">4a3410cfb2ce9cc0b3f5a5e60d3f40cf</td>
</tr>
<tr id="2.13.10" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.10-1_all.deb">dCache 2.13.10 (Debian package)</a></td>
	<td class="date">14.10.2015</td>
	<td class="hash">d5903bb88f98cf48f055cad75e0414c4</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#10">2.13.10</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.10-1.noarch.rpm">dCache 2.13.10 (rpm)</a></td>
	<td class="date">14.10.2015</td>
	<td class="hash">52e16fa93e4c3465598a4f7a9f7fd97c</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.10.tar.gz">dCache 2.13.10 (tgz)</a></td>
	<td class="date">14.10.2015</td>
	<td class="hash">04238ced484c234f96acf004dc483321</td>
</tr>
<tr id="2.13.9" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.9-1_all.deb">dCache 2.13.9 (Debian package)</a></td>
	<td class="date">21.9.2015</td>
	<td class="hash">6f9b868d0d0c88feb3acfffca4a0cab0</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#9">2.13.9</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.9-1.noarch.rpm">dCache 2.13.9 (rpm)</a></td>
	<td class="date">21.9.2015</td>
	<td class="hash">cde323b86371a2c9c2c6e6a19fe69600</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.9.tar.gz">dCache 2.13.9 (tgz)</a></td>
	<td class="date">21.9.2015</td>
	<td class="hash">51c5a19cb87fa9ab2ff28d37fa1ca4cc</td>
</tr>
<tr id="2.13.8" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.8-1_all.deb">dCache 2.13.8 (Debian package)</a></td>
	<td class="date">9.9.2015</td>
	<td class="hash">4d47986871b326f93f22cc6a4d6f03ab</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#8">2.13.8</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.8-1.noarch.rpm">dCache 2.13.8 (rpm)</a></td>
	<td class="date">9.9.2015</td>
	<td class="hash">6cea6cb894ffd172dea11a250da90d22</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.8.tar.gz">dCache 2.13.8 (tgz)</a></td>
	<td class="date">9.9.2015</td>
	<td class="hash">abd2d7ea039b5b8b6871ba6636e1d2b0</td>
</tr>
<tr id="2.13.7" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.7-1_all.deb">dCache 2.13.7 (Debian package)</a></td>
	<td class="date">24.8.2015</td>
	<td class="hash">0af77e1e0a7093b8d55e4e8b4cccc1e2</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#7">2.13.7</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.7-2.noarch.rpm">dCache 2.13.7 (rpm)</a></td>
	<td class="date">24.8.2015</td>
	<td class="hash">c253f2cfe3321185e8fef832fb7b7f7a</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.7.tar.gz">dCache 2.13.7 (tgz)</a></td>
	<td class="date">24.8.2015</td>
	<td class="hash">fff7051aea8a4cd3a8df51720aca0562</td>
</tr>
<tr id="2.13.6" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.6-1_all.deb">dCache 2.13.6 (Debian package)</a></td>
	<td class="date">18.8.2015</td>
	<td class="hash">580c22de7aba847aba67f541c02a88c5</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#6">2.13.6</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.6-1.noarch.rpm">dCache 2.13.6 (rpm)</a></td>
	<td class="date">18.8.2015</td>
	<td class="hash">67eea2448a134e6370472283d9a998f8</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.6.tar.gz">dCache 2.13.6 (tgz)</a></td>
	<td class="date">18.8.2015</td>
	<td class="hash">cf63aecb1455b1633b4e650ab97e0cb9</td>
</tr>
<tr id="2.13.5" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.5-1_all.deb">dCache 2.13.5 (Debian package)</a></td>
	<td class="date">24.7.2015</td>
	<td class="hash">ab9893a2223e04990b9c4e6772ad10f9</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#5">2.13.5</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.5-1.noarch.rpm">dCache 2.13.5 (rpm)</a></td>
	<td class="date">24.7.2015</td>
	<td class="hash">60a12ee127a8219195a50d799c8b774c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.5.tar.gz">dCache 2.13.5 (tgz)</a></td>
	<td class="date">24.7.2015</td>
	<td class="hash">7f6942c8d3aa42d313423b268ddcb25f</td>
</tr>
<tr id="2.13.4" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.4-1_all.deb">dCache 2.13.4 (Debian package)</a></td>
	<td class="date">15.7.2015</td>
	<td class="hash">e0865ba0a529daeb642f227c63f68cc2</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#4">2.13.4</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.4-1.noarch.rpm">dCache 2.13.4 (rpm)</a></td>
	<td class="date">15.7.2015</td>
	<td class="hash">5df74aae8dbe73c30e08329d08e82c48</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.4.tar.gz">dCache 2.13.4 (tgz)</a></td>
	<td class="date">15.7.2015</td>
	<td class="hash">0a3242dee4ec72e06ca9512bec192750</td>
</tr>
<tr id="2.13.3" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.3-1_all.deb">dCache 2.13.3 (Debian package)</a></td>
	<td class="date">1.7.2015</td>
	<td class="hash">7153d26992205ef9624d18e68745fc17</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#3">2.13.3</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.3-1.noarch.rpm">dCache 2.13.3 (rpm)</a></td>
	<td class="date">1.7.2015</td>
	<td class="hash">d45aff87ba3d4439714b57a8a0d08d87</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.3.tar.gz">dCache 2.13.3 (tgz)</a></td>
	<td class="date">1.7.2015</td>
	<td class="hash">2c8339088e6bc75b046f3d917932cacd</td>
</tr>
<tr id="2.13.2" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.2-1_all.deb">dCache 2.13.2 (Debian package)</a></td>
	<td class="date">24.6.2015</td>
	<td class="hash">34f49fb7bfc47f8cde61b30a9c6e0567</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#2">2.13.2</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.2-1.noarch.rpm">dCache 2.13.2 (rpm)</a></td>
	<td class="date">24.6.2015</td>
	<td class="hash">8a6a40fb27529953ef44e2ed8dde02c7</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.2.tar.gz">dCache 2.13.2 (tgz)</a></td>
	<td class="date">24.6.2015</td>
	<td class="hash">8e4630d1d82c62a7ead20c4dd9f29ef3</td>
</tr>
<tr id="2.13.1" class="even">
	<td class="link"><a href="repo/2.13/dcache_2.13.1-1_all.deb">dCache 2.13.1 (Debian package)</a></td>
	<td class="date">16.6.2015</td>
	<td class="hash">56ff68e764c4b49f2e432970beb2073d</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#1">2.13.1</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.1-1.noarch.rpm">dCache 2.13.1 (rpm)</a></td>
	<td class="date">16.6.2015</td>
	<td class="hash">f9f9755fcf338b1f2d7f07000770852a</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.13/dcache-2.13.1.tar.gz">dCache 2.13.1 (tgz)</a></td>
	<td class="date">16.6.2015</td>
	<td class="hash">00d860e0b20841ca58f38a1209b737fc</td>
</tr>
<tr id="2.13.0" class="odd">
	<td class="link"><a href="repo/2.13/dcache_2.13.0-1_all.deb">dCache 2.13.0 (Debian package)</a></td>
	<td class="date">9.6.2015</td>
	<td class="hash">c9155fdc3498632442a78752d96b51d9</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.13.shtml#0">2.13.0</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.0-1.noarch.rpm">dCache 2.13.0 (rpm)</a></td>
	<td class="date">9.6.2015</td>
	<td class="hash">bd75ba8ebd506212aaba2509e6db9727</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.13/dcache-2.13.0.tar.gz">dCache 2.13.0 (tgz)</a></td>
	<td class="date">9.6.2015</td>
	<td class="hash">9d0d6641924f98769641ae6d38192c82</td>
</tr>
</tbody>
</table>

<br xmlns=""> <a xmlns="" name="server-2.12"></a> <a name="server-2.12">server 2.12.x</a> <a href="rss-server-2.12-releases.xml" type="application/rss+xml"><img class="rss-icon" src="{{site.baseurl}}/images/rss-icon-14x14.png" alt="RSS" title="RSS feed for dCache server 2.12.x releases"></a>
	
In addition to the usual improvements and bug fixes, dCache
2.12 features the following highlights:
     
<ul xmlns="">
        <li>New site description property to add local branding.</li>
        <li>Admin shell supports Ctrl-C to interrupt commands.</li>
        <li>Alarms service can share domains with other services.</li>
        <li>Improved attribute handling in Chimera.</li>
        <li>Shorter session identifiers.</li>
        <li>FTP and DCAP cell names are unique across restarts.</li>
        <li>Info provider publishes all global network interfaces.</li>
        <li>Improved login broker registration and SRM door selection, including
          improved IPv6 support.</li>
        <li>Improved and more robust NFS proxy mode.</li>
        <li>On the fly checksum calculation for NFS and xrootd.</li>
        <li>Improved nearline storage Service Provider Interface for more
          flexible drivers.</li>
        <li>Precomputed repository statistics in pools.</li>
        <li>HTTP and xrootd uploads block until post-processing completes.</li>
        <li>Reduced memory consumption in pools using Berkeley DB.</li>
        <li>Site specific srmPing attributes.</li>
        <li>Parameterized WebDAV templates.</li>
        <li>More uniform access logs.</li>
        <li>Localized timestamps in pinboard.</li>
        <li>Improved bash completion.</li>
      </ul>
<p xmlns="">
	  dCache v2.12 requires a JVM supporting Java v8.
      </p>
<table xmlns="" class="releases">
<thead>
<tr>
	<th>Download</th>
	<th>Rel. Date</th>
	<th>md5 hash</th>
	<th>Release Notes</th>
</tr>
</thead>
<tbody>
<tr id="2.12.41" class="rec">
	<td class="link"><a href="repo/2.12/dcache_2.12.41-1_all.deb">dCache 2.12.41 (Debian package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">c15dfb9d6a6e30182271c5f4b8a7c391</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml">2.12.41</a></td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.12/dcache-2.12.41-1.noarch.rpm">dCache 2.12.41 (rpm)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">eb7edf678e332c1057ee8a9c1ef6554c</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.12/dcache-2.12.41-1.pkg">dCache 2.12.41 (Solaris package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">fe16d8c3e6abe56660771b159516bfe8</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.12/dcache-2.12.41.tar.gz">dCache 2.12.41 (tgz)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">753fe217e5d805363765b06e5ed8c595</td>
</tr>
<tr id="2.12.40" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.40-1_all.deb">dCache 2.12.40 (Debian package)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">418e05a0e12f4c299e64b89d974fb644</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#40">2.12.40</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.40-1.noarch.rpm">dCache 2.12.40 (rpm)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">7e62f080a316a969c7efe0023b620502</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.40-1.pkg">dCache 2.12.40 (Solaris package)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">cf057982935b51d92728b737c58ee155</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.40.tar.gz">dCache 2.12.40 (tgz)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">8a89e99a89a272666c7f18c0164edf18</td>
</tr>
<tr id="2.12.39" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.39-1_all.deb">dCache 2.12.39 (Debian package)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">eb8d1ec643761d2bf11d764e65e8cbe6</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#39">2.12.39</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.39-1.noarch.rpm">dCache 2.12.39 (rpm)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">9267c86a69518fa6a5eb5d3ad59accf1</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.39-1.pkg">dCache 2.12.39 (Solaris package)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">814a5f717c937e10f1ba5ef33f9d9cee</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.39.tar.gz">dCache 2.12.39 (tgz)</a></td>
	<td class="date">5.4.2016</td>
	<td class="hash">904b85d0d1b380db6cff20bbf4d4c9a3</td>
</tr>
<tr id="2.12.38" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.38-1_all.deb">dCache 2.12.38 (Debian package)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">300f787a7bc0de246d814796a5f730ff</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#38">2.12.38</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.38-1.noarch.rpm">dCache 2.12.38 (rpm)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">4f2712845d88edd90a84a4275010fdfc</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.38-1.pkg">dCache 2.12.38 (Solaris package)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">aad041e5d873a91a17e115d9c6612a90</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.38.tar.gz">dCache 2.12.38 (tgz)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">ca2c75b2b324ee75b0d102fcbb924b0b</td>
</tr>
<tr id="2.12.37" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.37-1_all.deb">dCache 2.12.37 (Debian package)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">328f9d35b0a5ce1af12f0372382d2759</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#37">2.12.37</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.37-1.noarch.rpm">dCache 2.12.37 (rpm)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">90370518b34f3cbcd3825b6e372188fb</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.37-1.pkg">dCache 2.12.37 (Solaris package)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">36faa02346d2dd2b7e081658ab0ad69d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.37.tar.gz">dCache 2.12.37 (tgz)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">2b882b237fc4193db2bdcdaffa80be63</td>
</tr>
<tr id="2.12.36" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.36-1_all.deb">dCache 2.12.36 (Debian package)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">9e41bf43cfaf4780aaa85d8943fc9f4e</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#36">2.12.36</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.36-1.noarch.rpm">dCache 2.12.36 (rpm)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">2e72099606d934147165f05bdd10426e</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.36-1.pkg">dCache 2.12.36 (Solaris package)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">06e797a3b6f14fa8ae38bf42c061bfe4</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.36.tar.gz">dCache 2.12.36 (tgz)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">679e10b5830cfa6f0e99a32ab530ac85</td>
</tr>
<tr id="2.12.35" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.35-1_all.deb">dCache 2.12.35 (Debian package)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">30fdaf54358f718167dee7cfe343a6c2</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#35">2.12.35</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.35-1.noarch.rpm">dCache 2.12.35 (rpm)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">1d3c802a1fdf41e565a12153def02e7b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.35-1.pkg">dCache 2.12.35 (Solaris package)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">379a0fd4b9feecf65e438d7976d6dc6c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.35.tar.gz">dCache 2.12.35 (tgz)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">97a15004fae66cc79c2b5b5a11f39b18</td>
</tr>
<tr id="2.12.34" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.34-1_all.deb">dCache 2.12.34 (Debian package)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">11ec6cc0e7e1fe119210a365c7f50b3c</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#34">2.12.34</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.34-1.noarch.rpm">dCache 2.12.34 (rpm)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">007ff9ff2d7d0b2e18245ce62159acdb</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.34-1.pkg">dCache 2.12.34 (Solaris package)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">6c4c598bef1c4245a29f2a6b00fbc681</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.34.tar.gz">dCache 2.12.34 (tgz)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">710ebd5852a7bd211a6ea5abc53dfd85</td>
</tr>
<tr id="2.12.33" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.33-1_all.deb">dCache 2.12.33 (Debian package)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">806f433cb7d243b08efea3f7f541b74d</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#33">2.12.33</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.33-1.noarch.rpm">dCache 2.12.33 (rpm)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">00a1630d54aaa6f9e359976e824365c0</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.33-1.pkg">dCache 2.12.33 (Solaris package)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">df3d47fe9c2a0dbba706bc8c20ca93f3</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.33.tar.gz">dCache 2.12.33 (tgz)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">ee716e61869be6cbe6d81268421cce43</td>
</tr>
<tr id="2.12.32" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.32-1_all.deb">dCache 2.12.32 (Debian package)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">232de0ea7d0e88bf12bdd146d33c5abc</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#32">2.12.32</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.32-1.noarch.rpm">dCache 2.12.32 (rpm)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">dff233866154aad30379e7d4f072bf79</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.32-1.pkg">dCache 2.12.32 (Solaris package)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">c8aa02a1270588de16fe43dfc9d1f0e4</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.32.tar.gz">dCache 2.12.32 (tgz)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">ab281ffae657e1efd4644900956ac69b</td>
</tr>
<tr id="2.12.31" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.31-1_all.deb">dCache 2.12.31 (Debian package)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">4460ba7d59df36e8cd44f29746a14841</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#31">2.12.31</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.31-1.noarch.rpm">dCache 2.12.31 (rpm)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">21f206619db5e3161b353b934dfc4818</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.31-1.pkg">dCache 2.12.31 (Solaris package)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">10a54616d60c8a651df26109898bf0db</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.31.tar.gz">dCache 2.12.31 (tgz)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">7958fd7f2553e6e9e710b9a246c76c13</td>
</tr>
<tr id="2.12.30" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.30-1_all.deb">dCache 2.12.30 (Debian package)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">e6bf168ef198183b825a681651a2b097</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#30">2.12.30</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.30-1.noarch.rpm">dCache 2.12.30 (rpm)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">1b401eb52e703799332eca63358d3195</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.30-1.pkg">dCache 2.12.30 (Solaris package)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">3c62a8b1a70755219fa1efa71a539650</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.30.tar.gz">dCache 2.12.30 (tgz)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">f09d2a43f7ed9d050a8b244c3699e58e</td>
</tr>
<tr id="2.12.29" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.29-1_all.deb">dCache 2.12.29 (Debian package)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">c2b0d71498eccb863e20cbba6ed12f2a</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#29">2.12.29</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.29-1.noarch.rpm">dCache 2.12.29 (rpm)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">e781978ada8d88e2750020eb91f2ee41</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.29-1.pkg">dCache 2.12.29 (Solaris package)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">81701db10728964539e75bffce3b0d8e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.29.tar.gz">dCache 2.12.29 (tgz)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">19f47420dcc4d2cff6e31f8842dd7d69</td>
</tr>
<tr id="2.12.28" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.28-1_all.deb">dCache 2.12.28 (Debian package)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">a6f89b624ca75b815a740978711f6d90</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#28">2.12.28</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.28-1.noarch.rpm">dCache 2.12.28 (rpm)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">ae2e95a95bff32103b59786cb694514b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.28-1.pkg">dCache 2.12.28 (Solaris package)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">774e17f52a690e262ed8a3ca27d55ace</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.28.tar.gz">dCache 2.12.28 (tgz)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">a5cc48dfc9b5e3576e494a6c7a9560ea</td>
</tr>
<tr id="2.12.27" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.27-1_all.deb">dCache 2.12.27 (Debian package)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">df88c43016fefc813d5a97b9a542f451</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#27">2.12.27</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.27-1.noarch.rpm">dCache 2.12.27 (rpm)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">05ebf32f252879a7e851879e772b950d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.27-1.pkg">dCache 2.12.27 (Solaris package)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">e82535a78356bf965b9fead63aa7c096</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.27.tar.gz">dCache 2.12.27 (tgz)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">cc075ad711a7365e4afeae24b17752b4</td>
</tr>
<tr id="2.12.26" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.26-1_all.deb">dCache 2.12.26 (Debian package)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">8f6da1e262647348ede7338730a23a4f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#26">2.12.26</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.26-1.noarch.rpm">dCache 2.12.26 (rpm)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">5904c4605a30a69b7e6b572b491ba6df</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.26-1.pkg">dCache 2.12.26 (Solaris package)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">6dd95daa1610d736119c45e899fc0905</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.26.tar.gz">dCache 2.12.26 (tgz)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">425d18ed1a9fde901776ac8239ccb4fc</td>
</tr>
<tr id="2.12.25" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.25-1_all.deb">dCache 2.12.25 (Debian package)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">95bbb09c2c53d2f23107203232fb79c8</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.12.shtml#25">2.12.25</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.25-1.noarch.rpm">dCache 2.12.25 (rpm)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">dcccf8755347102f0dc519cd618268ed</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.25-1.pkg">dCache 2.12.25 (Solaris package)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">7b1bef325267d8d56ed8b25a2176db14</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.25.tar.gz">dCache 2.12.25 (tgz)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">93a0d78adb5b8921135bddccbbadc72b</td>
</tr>
<tr id="2.12.24" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.24-1_all.deb">dCache 2.12.24 (Debian package)</a></td>
	<td class="date">2.11.2015</td>
	<td class="hash">bb351d513811477ae662a3927f974e46</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#24">2.12.24</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.24-1.noarch.rpm">dCache 2.12.24 (rpm)</a></td>
	<td class="date">2.11.2015</td>
	<td class="hash">bb43a92a6e33232246ae427c5cbdc6ca</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.24.tar.gz">dCache 2.12.24 (tgz)</a></td>
	<td class="date">2.11.2015</td>
	<td class="hash">7490ee1316392a519c499577efe4f899</td>
</tr>
<tr id="2.12.23" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.23-1_all.deb">dCache 2.12.23 (Debian package)</a></td>
	<td class="date">27.10.2015</td>
	<td class="hash">a83e8806ec9a649aa893f2dc2d42a4c1</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#23">2.12.23</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.23-1.noarch.rpm">dCache 2.12.23 (rpm)</a></td>
	<td class="date">27.10.2015</td>
	<td class="hash">87eb3175cb2a656f31d009f31df91b9b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.23.tar.gz">dCache 2.12.23 (tgz)</a></td>
	<td class="date">27.10.2015</td>
	<td class="hash">992ebf627e6f554ba759a0983c9c49a8</td>
</tr>
<tr id="2.12.22" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.22-1_all.deb">dCache 2.12.22 (Debian package)</a></td>
	<td class="date">14.10.2015</td>
	<td class="hash">980c9332374a33806cfe778f53bf8de3</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#22">2.12.22</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.22-1.noarch.rpm">dCache 2.12.22 (rpm)</a></td>
	<td class="date">14.10.2015</td>
	<td class="hash">4d70ce1fe60b5e1723f1322e17359ad2</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.22.tar.gz">dCache 2.12.22 (tgz)</a></td>
	<td class="date">14.10.2015</td>
	<td class="hash">315b6cb237db1524e5b48f46768cf105</td>
</tr>
<tr id="2.12.21" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.21-1_all.deb">dCache 2.12.21 (Debian package)</a></td>
	<td class="date">21.9.2015</td>
	<td class="hash">45c105fc769af727ccb1c64e03338c9c</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#21">2.12.21</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.21-1.noarch.rpm">dCache 2.12.21 (rpm)</a></td>
	<td class="date">21.9.2015</td>
	<td class="hash">693d7ffe05d04d504358bf5dbf883908</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.21.tar.gz">dCache 2.12.21 (tgz)</a></td>
	<td class="date">21.9.2015</td>
	<td class="hash">de697b858f953809fcc8dcf43b29542e</td>
</tr>
<tr id="2.12.20" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.20-1_all.deb">dCache 2.12.20 (Debian package)</a></td>
	<td class="date">9.9.2015</td>
	<td class="hash">805b331b1f9fff13e8c1b7a557ec3a65</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#20">2.12.20</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.20-1.noarch.rpm">dCache 2.12.20 (rpm)</a></td>
	<td class="date">9.9.2015</td>
	<td class="hash">ac3c7da32ad882ae6786e8535decea04</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.20.tar.gz">dCache 2.12.20 (tgz)</a></td>
	<td class="date">9.9.2015</td>
	<td class="hash">e327fb6b22b7bbcba4d9eac8287f4b8d</td>
</tr>
<tr id="2.12.19" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.19-1_all.deb">dCache 2.12.19 (Debian package)</a></td>
	<td class="date">24.8.2015</td>
	<td class="hash">118205fe5fd4711cb496e93e8128f8da</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#19">2.12.19</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.19-2.noarch.rpm">dCache 2.12.19 (rpm)</a></td>
	<td class="date">24.8.2015</td>
	<td class="hash">73409ebadcf47a59d03b59406e387161</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.19.tar.gz">dCache 2.12.19 (tgz)</a></td>
	<td class="date">24.8.2015</td>
	<td class="hash">de64aab9c30e49be929a9c4efb7df6ac</td>
</tr>
<tr id="2.12.18" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.18-1_all.deb">dCache 2.12.18 (Debian package)</a></td>
	<td class="date">18.8.2015</td>
	<td class="hash">baf1d52457a3a7cef9227ddb4d549a04</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#18">2.12.18</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.18-1.noarch.rpm">dCache 2.12.18 (rpm)</a></td>
	<td class="date">18.8.2015</td>
	<td class="hash">acdf7afe15f314321e079fc986ed9a61</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.18.tar.gz">dCache 2.12.18 (tgz)</a></td>
	<td class="date">18.8.2015</td>
	<td class="hash">81aaba14064d4ce5bf47ceb6031f532e</td>
</tr>
<tr id="2.12.17" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.17-1_all.deb">dCache 2.12.17 (Debian package)</a></td>
	<td class="date">24.7.2015</td>
	<td class="hash">fdd089d67510e24406878203cdf59f25</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#17">2.12.17</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.17-1.noarch.rpm">dCache 2.12.17 (rpm)</a></td>
	<td class="date">24.7.2015</td>
	<td class="hash">25ec52f1da949d312ad10d04fe381f43</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.17.tar.gz">dCache 2.12.17 (tgz)</a></td>
	<td class="date">24.7.2015</td>
	<td class="hash">6ab6897439f16047ea9db197eee791ac</td>
</tr>
<tr id="2.12.16" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.16-1_all.deb">dCache 2.12.16 (Debian package)</a></td>
	<td class="date">15.7.2015</td>
	<td class="hash">8677dba5b4887e32c56bbd4358e69e93</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#16">2.12.16</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.16-1.noarch.rpm">dCache 2.12.16 (rpm)</a></td>
	<td class="date">15.7.2015</td>
	<td class="hash">b9dba6472bb04a11cab420a6035c5f33</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.16.tar.gz">dCache 2.12.16 (tgz)</a></td>
	<td class="date">15.7.2015</td>
	<td class="hash">8463d0b9f898e0d7f835fa80d6793fc6</td>
</tr>
<tr id="2.12.15" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.15-1_all.deb">dCache 2.12.15 (Debian package)</a></td>
	<td class="date">1.7.2015</td>
	<td class="hash">e4608cfd6f5cf69f40e9ea6238887fd8</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#15">2.12.15</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.15-1.noarch.rpm">dCache 2.12.15 (rpm)</a></td>
	<td class="date">1.7.2015</td>
	<td class="hash">77489d9b81b195d3aeae17e1f7b93912</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.15.tar.gz">dCache 2.12.15 (tgz)</a></td>
	<td class="date">1.7.2015</td>
	<td class="hash">d53cd7407475a310e92dc481a94863e8</td>
</tr>
<tr id="2.12.14" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.14-1_all.deb">dCache 2.12.14 (Debian package)</a></td>
	<td class="date">24.6.2015</td>
	<td class="hash">4792833e1a5e4dd3ce03804abfd621f2</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#14">2.12.14</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.14-1.noarch.rpm">dCache 2.12.14 (rpm)</a></td>
	<td class="date">24.6.2015</td>
	<td class="hash">137030068ea065668c7173b404bf5e27</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.14.tar.gz">dCache 2.12.14 (tgz)</a></td>
	<td class="date">24.6.2015</td>
	<td class="hash">7179b8d9276e142da17d04c2ab7f5384</td>
</tr>
<tr id="2.12.13" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.13-1_all.deb">dCache 2.12.13 (Debian package)</a></td>
	<td class="date">16.6.2015</td>
	<td class="hash">7e93865a3dce386171d86d21bf993f0f</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#13">2.12.13</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.13-1.noarch.rpm">dCache 2.12.13 (rpm)</a></td>
	<td class="date">16.6.2015</td>
	<td class="hash">c64630f5c6da73ca14cf99979ca27568</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.13.tar.gz">dCache 2.12.13 (tgz)</a></td>
	<td class="date">16.6.2015</td>
	<td class="hash">fb8ece663ba8bf80c30098612a48db85</td>
</tr>
<tr id="2.12.12" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.12-1_all.deb">dCache 2.12.12 (Debian package)</a></td>
	<td class="date">9.6.2015</td>
	<td class="hash">867a6b01aa38c0b896eed684a347c903</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#12">2.12.12</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.12-1.noarch.rpm">dCache 2.12.12 (rpm)</a></td>
	<td class="date">9.6.2015</td>
	<td class="hash">74da2b5b5c721e7b5f720a9410b1f146</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.12.tar.gz">dCache 2.12.12 (tgz)</a></td>
	<td class="date">9.6.2015</td>
	<td class="hash">5b8beedfd4c76ed57b1b939c251b7163</td>
</tr>
<tr id="2.12.11" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.11-1_all.deb">dCache 2.12.11 (Debian package)</a></td>
	<td class="date">2.6.2015</td>
	<td class="hash">98cdb56ceae316bb5881dca297d5499c</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#11">2.12.11</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.11-1.noarch.rpm">dCache 2.12.11 (rpm)</a></td>
	<td class="date">2.6.2015</td>
	<td class="hash">7893a884105e4448cfdb3e2eed19e180</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.11.tar.gz">dCache 2.12.11 (tgz)</a></td>
	<td class="date">2.6.2015</td>
	<td class="hash">e3fd223791eb8db74e4fbf31a41d5f43</td>
</tr>
<tr id="2.12.10" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.10-1_all.deb">dCache 2.12.10 (Debian package)</a></td>
	<td class="date">19.5.2015</td>
	<td class="hash">a2857368c7a3da14620c81da03747005</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#10">2.12.10</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.10-1.noarch.rpm">dCache 2.12.10 (rpm)</a></td>
	<td class="date">19.5.2015</td>
	<td class="hash">7bd1a941310cbb1056be0cddefb0ffc6</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.10.tar.gz">dCache 2.12.10 (tgz)</a></td>
	<td class="date">19.5.2015</td>
	<td class="hash">5fb86d24558da0f9a6fbd5c04b1050f3</td>
</tr>
<tr id="2.12.9" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.9-1_all.deb">dCache 2.12.9 (Debian package)</a></td>
	<td class="date">12.5.2015</td>
	<td class="hash">43f511849e76ddeba27adce699fe605b</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#9">2.12.9</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.9-1.noarch.rpm">dCache 2.12.9 (rpm)</a></td>
	<td class="date">12.5.2015</td>
	<td class="hash">b51d6b4bb72b380c19e4edc5f7d80686</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.9.tar.gz">dCache 2.12.9 (tgz)</a></td>
	<td class="date">12.5.2015</td>
	<td class="hash">5e27158d8854acb80e710d0f2824c34b</td>
</tr>
<tr id="2.12.8" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.8-1_all.deb">dCache 2.12.8 (Debian package)</a></td>
	<td class="date">5.5.2015</td>
	<td class="hash">fa631463a6219de38bc60f8ca9b3873e</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#8">2.12.8</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.8-1.noarch.rpm">dCache 2.12.8 (rpm)</a></td>
	<td class="date">5.5.2015</td>
	<td class="hash">6f6623d601678be04252b3cacbaebcbf</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.8.tar.gz">dCache 2.12.8 (tgz)</a></td>
	<td class="date">5.5.2015</td>
	<td class="hash">367a91b1ab9eff7a2bae13cc269e4817</td>
</tr>
<tr id="2.12.7" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.7-1_all.deb">dCache 2.12.7 (Debian package)</a></td>
	<td class="date">29.4.2015</td>
	<td class="hash">5df006ffc131f9a0f79d47b9caffe0d0</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#7">2.12.7</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.7-1.noarch.rpm">dCache 2.12.7 (rpm)</a></td>
	<td class="date">29.4.2015</td>
	<td class="hash">d8400da71e494cbfb6e8f3d19ae0070e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.7.tar.gz">dCache 2.12.7 (tgz)</a></td>
	<td class="date">29.4.2015</td>
	<td class="hash">9fee142ccb539c46ab0d911ef251b5e0</td>
</tr>
<tr id="2.12.5" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.5-1_all.deb">dCache 2.12.5 (Debian package)</a></td>
	<td class="date">21.4.2015</td>
	<td class="hash">1f3f6ad0f0b40b4eb00355108d7788bd</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#5">2.12.5</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.5-1.noarch.rpm">dCache 2.12.5 (rpm)</a></td>
	<td class="date">21.4.2015</td>
	<td class="hash">0946d5d13c1a7da1038423a2273166e0</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.5.tar.gz">dCache 2.12.5 (tgz)</a></td>
	<td class="date">21.4.2015</td>
	<td class="hash">9dcfb875dc27b47246f2e30612e87eb7</td>
</tr>
<tr id="2.12.4" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.4-1_all.deb">dCache 2.12.4 (Debian package)</a></td>
	<td class="date">31.3.2015</td>
	<td class="hash">c74acb39e13b400f312be749d67c262d</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#4">2.12.4</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.4-1.noarch.rpm">dCache 2.12.4 (rpm)</a></td>
	<td class="date">31.3.2015</td>
	<td class="hash">4b3c5ea775e912a89f22aa47da87fd55</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.4.tar.gz">dCache 2.12.4 (tgz)</a></td>
	<td class="date">31.3.2015</td>
	<td class="hash">b16729fbcd4ff51603bbc4345698b6d6</td>
</tr>
<tr id="2.12.3" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.3-1_all.deb">dCache 2.12.3 (Debian package)</a></td>
	<td class="date">24.3.2015</td>
	<td class="hash">327bbe74821932a9ebd83a0711fced74</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#3">2.12.3</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.3-1.noarch.rpm">dCache 2.12.3 (rpm)</a></td>
	<td class="date">24.3.2015</td>
	<td class="hash">f1e3867c6b7eb46bfd6dccd461d630bd</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.3.tar.gz">dCache 2.12.3 (tgz)</a></td>
	<td class="date">24.3.2015</td>
	<td class="hash">e2a8a739794b407855c9609687d08468</td>
</tr>
<tr id="2.12.2" class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.2-1_all.deb">dCache 2.12.2 (Debian package)</a></td>
	<td class="date">17.3.2015</td>
	<td class="hash">f660aa0b12b0e010ee687fd85967a6ea</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#2">2.12.2</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.2-1.noarch.rpm">dCache 2.12.2 (rpm)</a></td>
	<td class="date">17.3.2015</td>
	<td class="hash">b13153384b95d4da42abd09287ddb1ab</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.2.tar.gz">dCache 2.12.2 (tgz)</a></td>
	<td class="date">17.3.2015</td>
	<td class="hash">d2984cf476f9aebe5cb9746f9326a40a</td>
</tr>
<tr id="2.12.1" class="odd">
	<td class="link"><a href="repo/2.12/dcache_2.12.1-1_all.deb">dCache 2.12.1 (Debian package)</a></td>
	<td class="date">10.3.2015</td>
	<td class="hash">49c4fb5d0fe7110cbb20927d842e6363</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#1">2.12.1</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.1-1.noarch.rpm">dCache 2.12.1 (rpm)</a></td>
	<td class="date">10.3.2015</td>
	<td class="hash">f320ced46d61dd27c8ede0b7f4ca7fe1</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.12/dcache-2.12.1.tar.gz">dCache 2.12.1 (tgz)</a></td>
	<td class="date">10.3.2015</td>
	<td class="hash">8cf3514ee8ae4abe54aab449e4001755</td>
</tr>
<tr id="2.12.0" class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.0-1.noarch.rpm">dCache 2.12.0 (rpm)</a></td>
	<td class="date">06.03.2015</td>
	<td class="hash">21f5d462b55132b7c700a7ba63a5ad79</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.12.shtml#0">2.12.0</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache_2.12.0-1_all.deb">dCache 2.12.0 (Debian package)</a></td>
	<td class="date">06.03.2015</td>
	<td class="hash">25e3d645fab4100811aa5e34f140e82b</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.12/dcache-2.12.0.tar.gz">dCache 2.12.0 (tgz)</a></td>
	<td class="date">06.03.2015</td>
	<td class="hash">a19771477e2492610e5f44110a4a5342</td>
</tr>
</tbody>
</table>
<br xmlns="">
	<a xmlns="" name="server-2.11"></a>
	<h3 xmlns="">
	<a name="server-2.11">server 2.11.x</a>
	<a href="rss-server-2.11-releases.xml" type="application/rss+xml"><img class="rss-icon" src="{{site.baseurl}}/images/rss-icon-14x14.png" alt="RSS" title="RSS feed for dCache server 2.11.x releases"></a>
	</h3>
	<p xmlns="">
        In addition to the usual improvements and bug fixes, dCache
        2.11 features the following highlights:
      </p>
<ul xmlns="">
	  <li>Faster deletion speeds.</li>

          <li>Better integration of alarms service, easier configuration, and predefined alarms.</li>

          <li>Multiple GIDs in kpwd.</li>

          <li>Less clutter in GLUE 2 StorageShare.</li>

          <li>Improved pool response during HSM request bursts.</li>

          <li>Reduced latency on write.</li>

          <li>Automatic throttling of SRM request rate when database request queue is full.</li>

          <li>Decoupling of transfer managers from srm database.</li>
      </ul>
<p xmlns="">
	  dCache v2.11 requires a JVM supporting either Java v7 or Java v8.
      </p>
<table xmlns="" class="releases">
<thead>
<tr>
	<th>Download</th>
	<th>Rel. Date</th>
	<th>md5 hash</th>
	<th>Release Notes</th>
</tr>
</thead>
<tbody>
<tr id="2.11.51" class="rec">
	<td class="link"><a href="repo/2.11/dcache_2.11.51-1_all.deb">dCache 2.11.51 (Debian package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">778ad234187aa73367c731c8f05338e7</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml">2.11.51</a></td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.11/dcache-2.11.51-1.noarch.rpm">dCache 2.11.51 (rpm)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">81a3428f0f6c3cb6592ff1161a791706</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.11/dcache-2.11.51-1.pkg">dCache 2.11.51 (Solaris package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">c076f29bdd76311a590df775a4ea7dcc</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.11/dcache-2.11.51.tar.gz">dCache 2.11.51 (tgz)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">019bf2b10da12bf28d02e30575c1d591</td>
</tr>
<tr id="2.11.50" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.50-1_all.deb">dCache 2.11.50 (Debian package)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">4fab749d7770125cdd90081849e32195</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#50">2.11.50</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.50-1.noarch.rpm">dCache 2.11.50 (rpm)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">8c7d637cd475acf68c2a490eae87af01</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.50-1.pkg">dCache 2.11.50 (Solaris package)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">695e2cbbbd72dd72fba8ecc0eb1ea89d</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.50.tar.gz">dCache 2.11.50 (tgz)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">a56e741427aed8fe5e6f1e80f46561ed</td>
</tr>
<tr id="2.11.49" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.49-1_all.deb">dCache 2.11.49 (Debian package)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">db5f81a081754a496b0f4872f3d06b30</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#49">2.11.49</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.49-1.noarch.rpm">dCache 2.11.49 (rpm)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">848f24c2260f1f1b680040279be8af6a</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.49-1.pkg">dCache 2.11.49 (Solaris package)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">878d32189a21d533d3a8ce1389f94549</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.49.tar.gz">dCache 2.11.49 (tgz)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">751f1dbea0db2c998a4929a27c32ea37</td>
</tr>
<tr id="2.11.48" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.48-1_all.deb">dCache 2.11.48 (Debian package)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">c7d68b8fb85c444f9a515ef6e387cec4</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#48">2.11.48</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.48-1.noarch.rpm">dCache 2.11.48 (rpm)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">dbfb5baea818dacbdf56b38111bb609a</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.48-1.pkg">dCache 2.11.48 (Solaris package)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">15c5267428850833d5069c5b82583c42</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.48.tar.gz">dCache 2.11.48 (tgz)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">270477e178ad51038163b205acf8d8e2</td>
</tr>
<tr id="2.11.47" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.47-1_all.deb">dCache 2.11.47 (Debian package)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">28435912024acf6837a159d2d9b2cb12</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#47">2.11.47</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.47-1.noarch.rpm">dCache 2.11.47 (rpm)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">e5ffc42c37783d616defd98f72b487fa</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.47-1.pkg">dCache 2.11.47 (Solaris package)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">1287da5372eb5ffb694a5431e4ad77d6</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.47.tar.gz">dCache 2.11.47 (tgz)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">0beff28783fafe0493e6af3932381389</td>
</tr>
<tr id="2.11.46" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.46-1_all.deb">dCache 2.11.46 (Debian package)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">a11bc3b0982169c2592eacb3e410bdde</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#46">2.11.46</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.46-1.noarch.rpm">dCache 2.11.46 (rpm)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">8e5db6fb993720cbf8ae40b5446396bc</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.46-1.pkg">dCache 2.11.46 (Solaris package)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">72720ad0b1a719e437278b3190b8e5a9</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.46.tar.gz">dCache 2.11.46 (tgz)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">8b96edc7b2876fb8b2636489b146a96d</td>
</tr>
<tr id="2.11.45" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.45-1_all.deb">dCache 2.11.45 (Debian package)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">026a718db3c98b28085433537a6c4f38</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#45">2.11.45</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.45-1.noarch.rpm">dCache 2.11.45 (rpm)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">9691d4b545f620e98234dd095d7b2f52</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.45-1.pkg">dCache 2.11.45 (Solaris package)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">97b4cb70632e5294e803b945423095b5</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.45.tar.gz">dCache 2.11.45 (tgz)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">a94c92d0c7ce4a7222baf7ebe4e25d68</td>
</tr>
<tr id="2.11.44" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.44-1_all.deb">dCache 2.11.44 (Debian package)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">65c7a83f718d522c52e052434be4e5d9</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#44">2.11.44</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.44-1.noarch.rpm">dCache 2.11.44 (rpm)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">aa2d359ec14b74649c76883f347de26e</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.44-1.pkg">dCache 2.11.44 (Solaris package)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">260f295b5b0213be070261500ccb8686</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.44.tar.gz">dCache 2.11.44 (tgz)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">91bd232bfeab0c97dc3aa2e1ce7a4a15</td>
</tr>
<tr id="2.11.43" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.43-1_all.deb">dCache 2.11.43 (Debian package)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">6df5f2e4ff567dbfd73042529ad242c5</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#43">2.11.43</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.43-1.noarch.rpm">dCache 2.11.43 (rpm)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">0c81e288e703f38dca029ad5f496ace7</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.43-1.pkg">dCache 2.11.43 (Solaris package)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">6e1af19e8865082b229e4df077584c92</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.43.tar.gz">dCache 2.11.43 (tgz)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">871a96c79a7347b339de9691431ee1a0</td>
</tr>
<tr id="2.11.42" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.42-1_all.deb">dCache 2.11.42 (Debian package)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">e46f166f6b7d0c5a5d706a57cc2cfa09</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#42">2.11.42</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.42-1.noarch.rpm">dCache 2.11.42 (rpm)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">33a1694e292de6554fa833dce36c9cc6</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.42-1.pkg">dCache 2.11.42 (Solaris package)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">e02936730cc769bcb760b9f7b14ce107</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.42.tar.gz">dCache 2.11.42 (tgz)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">844d70dd17eed9e2f8864e14ba931549</td>
</tr>
<tr id="2.11.41" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.41-1_all.deb">dCache 2.11.41 (Debian package)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">9acba59fde58f5b62108268033b22f5d</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#41">2.11.41</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.41-1.noarch.rpm">dCache 2.11.41 (rpm)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">e2449f1b3d5cd23e0ff409aee3be806e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.41-1.pkg">dCache 2.11.41 (Solaris package)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">21ad81c29f918443b9dca0ef40932617</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.41.tar.gz">dCache 2.11.41 (tgz)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">a2d539a951c7ab9c5984945a9fbff16c</td>
</tr>
<tr id="2.11.40" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.40-1_all.deb">dCache 2.11.40 (Debian package)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">fa99077b351084ff63bec8477fb9375b</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#40">2.11.40</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.40-1.noarch.rpm">dCache 2.11.40 (rpm)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">e76025b878fa88b864814b831b0e5b77</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.40-1.pkg">dCache 2.11.40 (Solaris package)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">b26fab4730589939da42d09beadc0fb5</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.40.tar.gz">dCache 2.11.40 (tgz)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">09eb13360e75e2bc88117d404286ff12</td>
</tr>
<tr id="2.11.39" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.39-1_all.deb">dCache 2.11.39 (Debian package)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">cc34af296b2c875705705ab24702a38f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#39">2.11.39</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.39-1.noarch.rpm">dCache 2.11.39 (rpm)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">9a326c06bb4b1fafaa552d66a540fc50</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.39-1.pkg">dCache 2.11.39 (Solaris package)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">3faeb3c44de384ca2456578eee91d1dc</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.39.tar.gz">dCache 2.11.39 (tgz)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">9e00a6e3a1054429f2384b7e744f0926</td>
</tr>
<tr id="2.11.38" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.38-1_all.deb">dCache 2.11.38 (Debian package)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">89ef70670f9bd3a38f87672155a09c8b</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#38">2.11.38</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.38-1.noarch.rpm">dCache 2.11.38 (rpm)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">54146d3243406a166a1c23d8cb1ee650</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.38-1.pkg">dCache 2.11.38 (Solaris package)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">34cba9577c3bcf79e004faa109ec9bde</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.38.tar.gz">dCache 2.11.38 (tgz)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">7bdffb4913824a3b40b7589cdc98c117</td>
</tr>
<tr id="2.11.37" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.37-1_all.deb">dCache 2.11.37 (Debian package)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">74ceadffa96a7892df6e1474a2a9c4b7</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#37">2.11.37</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.37-1.noarch.rpm">dCache 2.11.37 (rpm)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">179e48c1129eddb7ae7d9f4e8adecd86</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.37-1.pkg">dCache 2.11.37 (Solaris package)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">8dae5aa6409df19252573f2f8ce79ac9</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.37.tar.gz">dCache 2.11.37 (tgz)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">e6c921c521ae60733f769fe4fbe73cd4</td>
</tr>
<tr id="2.11.36" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.36-1_all.deb">dCache 2.11.36 (Debian package)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">eb09ed088a3aed82b63bc89335a93668</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.11.shtml#36">2.11.36</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.36-1.noarch.rpm">dCache 2.11.36 (rpm)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">6cd35a5e64dc576c02ba5358a7e5a47c</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.36-1.pkg">dCache 2.11.36 (Solaris package)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">259497d0dff8ae7fd6b7ae957e637a6b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.36.tar.gz">dCache 2.11.36 (tgz)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">b0c313d1fd54888f6c5f0520dedd009b</td>
</tr>
<tr id="2.11.35" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.35-1_all.deb">dCache 2.11.35 (Debian package)</a></td>
	<td class="date">2.11.2015</td>
	<td class="hash">d09b8cae494d86f3f2fde977c59da036</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#35">2.11.35</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.35-1.noarch.rpm">dCache 2.11.35 (rpm)</a></td>
	<td class="date">2.11.2015</td>
	<td class="hash">74f1d36a44b469ff625cefa7eda08cdf</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.35.tar.gz">dCache 2.11.35 (tgz)</a></td>
	<td class="date">2.11.2015</td>
	<td class="hash">bb4a4658df13527d7195a058d46c8579</td>
</tr>
<tr id="2.11.34" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.34-1_all.deb">dCache 2.11.34 (Debian package)</a></td>
	<td class="date">27.10.2015</td>
	<td class="hash">aaebfccd108e8e71c5f066d17ca9761a</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#34">2.11.34</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.34-1.noarch.rpm">dCache 2.11.34 (rpm)</a></td>
	<td class="date">27.10.2015</td>
	<td class="hash">30f624b5d38fe7872fdac78a239add25</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.34.tar.gz">dCache 2.11.34 (tgz)</a></td>
	<td class="date">27.10.2015</td>
	<td class="hash">fa1e62d96db0bfbf329c95f46d337779</td>
</tr>
<tr id="2.11.33" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.33-1_all.deb">dCache 2.11.33 (Debian package)</a></td>
	<td class="date">14.10.2015</td>
	<td class="hash">391697b1c33c6d9e5b9c998aee246a0c</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#33">2.11.33</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.33-1.noarch.rpm">dCache 2.11.33 (rpm)</a></td>
	<td class="date">14.10.2015</td>
	<td class="hash">fdec56f432809cf053fe21c3878c4b78</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.33.tar.gz">dCache 2.11.33 (tgz)</a></td>
	<td class="date">14.10.2015</td>
	<td class="hash">e1547a91f30adb622e03b613fdce9e9c</td>
</tr>
<tr id="2.11.32" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.32-2_all.deb">dCache 2.11.32 (Debian package)</a></td>
	<td class="date">21.9.2015</td>
	<td class="hash">712f10bbadc37f5e31dc46aaad744116</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#32">2.11.32</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.32-2.noarch.rpm">dCache 2.11.32 (rpm)</a></td>
	<td class="date">21.9.2015</td>
	<td class="hash">052aaea1c3db03d04a171379c1a06b6c</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.32.tar.gz">dCache 2.11.32 (tgz)</a></td>
	<td class="date">21.9.2015</td>
	<td class="hash">d622849f8c6a829987052e71c0363980</td>
</tr>
<tr id="2.11.31" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.31-1_all.deb">dCache 2.11.31 (Debian package)</a></td>
	<td class="date">9.9.2015</td>
	<td class="hash">21a8e6fc7ee07f8f34f49e91d66ac150</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#31">2.11.31</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.31-1.noarch.rpm">dCache 2.11.31 (rpm)</a></td>
	<td class="date">9.9.2015</td>
	<td class="hash">a38777cd1d61376edd6ef47eb5578b13</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.31.tar.gz">dCache 2.11.31 (tgz)</a></td>
	<td class="date">9.9.2015</td>
	<td class="hash">4db4c7ed1be407cb2db86af36e3ca3d9</td>
</tr>
<tr id="2.11.30" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.30-1_all.deb">dCache 2.11.30 (Debian package)</a></td>
	<td class="date">24.8.2015</td>
	<td class="hash">ec382fefa339bcbbec00a7740c32e661</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#30">2.11.30</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.30-2.noarch.rpm">dCache 2.11.30 (rpm)</a></td>
	<td class="date">24.8.2015</td>
	<td class="hash">23ca3a2a86c15986eb1ad27ad6c69fc5</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.30.tar.gz">dCache 2.11.30 (tgz)</a></td>
	<td class="date">24.8.2015</td>
	<td class="hash">9b17392a8d32a9ce27ea2b8e77db3444</td>
</tr>
<tr id="2.11.29" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.29-1_all.deb">dCache 2.11.29 (Debian package)</a></td>
	<td class="date">18.8.2015</td>
	<td class="hash">cf9ac5fbfb6a988126f9870d5e59187c</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#29">2.11.29</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.29-2.noarch.rpm">dCache 2.11.29 (rpm)</a></td>
	<td class="date">18.8.2015</td>
	<td class="hash">86501d33264c4279f7108a723b085522</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.29.tar.gz">dCache 2.11.29 (tgz)</a></td>
	<td class="date">18.8.2015</td>
	<td class="hash">67dfab443ffd7e2a6970b54e744e5b10</td>
</tr>
<tr id="2.11.28" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.28-1_all.deb">dCache 2.11.28 (Debian package)</a></td>
	<td class="date">24.7.2015</td>
	<td class="hash">1abb10e5c66260c0ac8ab9f1e8983b7f</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#28">2.11.28</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.28-1.noarch.rpm">dCache 2.11.28 (rpm)</a></td>
	<td class="date">24.7.2015</td>
	<td class="hash">580e21afd64350b97811e427925ecccf</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.28.tar.gz">dCache 2.11.28 (tgz)</a></td>
	<td class="date">24.7.2015</td>
	<td class="hash">bce23bf35eef7fc950d7aa98caf02854</td>
</tr>
<tr id="2.11.27" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.27-1_all.deb">dCache 2.11.27 (Debian package)</a></td>
	<td class="date">15.7.2015</td>
	<td class="hash">3a2befbd9fd01f198287f8de3ebfc206</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#27">2.11.27</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.27-1.noarch.rpm">dCache 2.11.27 (rpm)</a></td>
	<td class="date">15.7.2015</td>
	<td class="hash">d43f7047fca67a74a9fa9146789ed63a</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.27.tar.gz">dCache 2.11.27 (tgz)</a></td>
	<td class="date">15.7.2015</td>
	<td class="hash">812ff826912d6bbe83106093e30e4d57</td>
</tr>
<tr id="2.11.26" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.26-1_all.deb">dCache 2.11.26 (Debian package)</a></td>
	<td class="date">1.7.2015</td>
	<td class="hash">f211f177b1869c6ea2f0a925810ed835</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#26">2.11.26</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.26-1.noarch.rpm">dCache 2.11.26 (rpm)</a></td>
	<td class="date">1.7.2015</td>
	<td class="hash">296c91b206707d679bd92aeccf71ecb1</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.26.tar.gz">dCache 2.11.26 (tgz)</a></td>
	<td class="date">1.7.2015</td>
	<td class="hash">bec2518779c01d1bdb69e139e08bb898</td>
</tr>
<tr id="2.11.25" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.25-1_all.deb">dCache 2.11.25 (Debian package)</a></td>
	<td class="date">24.6.2015</td>
	<td class="hash">c94717b37035fbb4006633e750f2914b</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#25">2.11.25</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.25-1.noarch.rpm">dCache 2.11.25 (rpm)</a></td>
	<td class="date">24.6.2015</td>
	<td class="hash">7bc39e3f8899be02b94959021b11e236</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.25.tar.gz">dCache 2.11.25 (tgz)</a></td>
	<td class="date">24.6.2015</td>
	<td class="hash">4a92801c6508be1a662c952e995eddd6</td>
</tr>
<tr id="2.11.24" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.24-1_all.deb">dCache 2.11.24 (Debian package)</a></td>
	<td class="date">16.6.2015</td>
	<td class="hash">ba71ebf9650b70724fb91555b90d090a</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#24">2.11.24</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.24-1.noarch.rpm">dCache 2.11.24 (rpm)</a></td>
	<td class="date">16.6.2015</td>
	<td class="hash">8195c548bb0a8b59c45748a1bf53120a</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.24.tar.gz">dCache 2.11.24 (tgz)</a></td>
	<td class="date">16.6.2015</td>
	<td class="hash">8bc3781a0f29faf62ef4483ba7fc8631</td>
</tr>
<tr id="2.11.23" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.23-1_all.deb">dCache 2.11.23 (Debian package)</a></td>
	<td class="date">9.6.2015</td>
	<td class="hash">6ebb869663c5cb9a0314890fd8697482</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#23">2.11.23</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.23-1.noarch.rpm">dCache 2.11.23 (rpm)</a></td>
	<td class="date">9.6.2015</td>
	<td class="hash">8f0f7cefabb8616d7b1ac186ea12ed64</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.23.tar.gz">dCache 2.11.23 (tgz)</a></td>
	<td class="date">9.6.2015</td>
	<td class="hash">2f1d166801b6f034ee3c0e87239c87d2</td>
</tr>
<tr id="2.11.22" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.22-1_all.deb">dCache 2.11.22 (Debian package)</a></td>
	<td class="date">2.6.2015</td>
	<td class="hash">6eb1aa3c01cb999b095a2355b3fa2b2a</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#22">2.11.22</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.22-1.noarch.rpm">dCache 2.11.22 (rpm)</a></td>
	<td class="date">2.6.2015</td>
	<td class="hash">8af03625f42990f2b20758b8208cf8ed</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.22.tar.gz">dCache 2.11.22 (tgz)</a></td>
	<td class="date">2.6.2015</td>
	<td class="hash">adf2049c5d6a4e2a813432c50828c8fa</td>
</tr>
<tr id="2.11.21" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.21-1_all.deb">dCache 2.11.21 (Debian package)</a></td>
	<td class="date">19.5.2015</td>
	<td class="hash">56bda015d2835b54028432da0092d94f</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#21">2.11.21</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.21-1.noarch.rpm">dCache 2.11.21 (rpm)</a></td>
	<td class="date">19.5.2015</td>
	<td class="hash">8449a10f3458ea98c548604b59880116</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.21.tar.gz">dCache 2.11.21 (tgz)</a></td>
	<td class="date">19.5.2015</td>
	<td class="hash">bb3af2ac284f124254f11ae411e636f3</td>
</tr>
<tr id="2.11.20" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.20-1_all.deb">dCache 2.11.20 (Debian package)</a></td>
	<td class="date">12.5.2015</td>
	<td class="hash">b5b39f97a7a3ca3196a096390503d676</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#20">2.11.20</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.20-1.noarch.rpm">dCache 2.11.20 (rpm)</a></td>
	<td class="date">12.5.2015</td>
	<td class="hash">40a3009b599c50729e5989a0e322810f</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.20.tar.gz">dCache 2.11.20 (tgz)</a></td>
	<td class="date">12.5.2015</td>
	<td class="hash">f6aad21f3e1972f43ae7bdcfe340f0fb</td>
</tr>
<tr id="2.11.19" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.19-1_all.deb">dCache 2.11.19 (Debian package)</a></td>
	<td class="date">5.5.2015</td>
	<td class="hash">24d8943db81488407925c1b49cc14d14</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#19">2.11.19</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.19-1.noarch.rpm">dCache 2.11.19 (rpm)</a></td>
	<td class="date">5.5.2015</td>
	<td class="hash">57ab04d020de4b24043253471c5c7b18</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.19.tar.gz">dCache 2.11.19 (tgz)</a></td>
	<td class="date">5.5.2015</td>
	<td class="hash">6d5da9eb26c4aca322d9cd8299efe4f2</td>
</tr>
<tr id="2.11.18" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.18-1_all.deb">dCache 2.11.18 (Debian package)</a></td>
	<td class="date">29.4.2015</td>
	<td class="hash">1d76a72e87f6d80366961f84694d6b06</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#18">2.11.18</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.18-1.noarch.rpm">dCache 2.11.18 (rpm)</a></td>
	<td class="date">29.4.2015</td>
	<td class="hash">827e1dc9867641c7ef3014bf61ed0054</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.18.tar.gz">dCache 2.11.18 (tgz)</a></td>
	<td class="date">29.4.2015</td>
	<td class="hash">1eb90e3375e151fa09a1ccf416f8ec57</td>
</tr>
<tr id="2.11.16" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.16-1_all.deb">dCache 2.11.16 (Debian package)</a></td>
	<td class="date">21.4.2015</td>
	<td class="hash">7a6d17476eb275ca3a956458fe5759a4</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#16">2.11.16</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.16-1.noarch.rpm">dCache 2.11.16 (rpm)</a></td>
	<td class="date">21.4.2015</td>
	<td class="hash">105d24b7852b7d4a3b05f6c245694dcc</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.16.tar.gz">dCache 2.11.16 (tgz)</a></td>
	<td class="date">21.4.2015</td>
	<td class="hash">8b21bb1bcfdf6e2e8e2542eb6d7ca04d</td>
</tr>
<tr id="2.11.15" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.15-1_all.deb">dCache 2.11.15 (Debian package)</a></td>
	<td class="date">31.3.2015</td>
	<td class="hash">e7ac099f935cb3f9a147e0a0c244ce9e</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#15">2.11.15</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.15-1.noarch.rpm">dCache 2.11.15 (rpm)</a></td>
	<td class="date">31.3.2015</td>
	<td class="hash">7486dd645536366fb8f9a9204305aa46</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.15.tar.gz">dCache 2.11.15 (tgz)</a></td>
	<td class="date">31.3.2015</td>
	<td class="hash">c570e1ece1b84d0a839762b82c428088</td>
</tr>
<tr id="2.11.14" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.14-1_all.deb">dCache 2.11.14 (Debian package)</a></td>
	<td class="date">24.3.2015</td>
	<td class="hash">0382dd1b0974cc7b32794f0450204a0b</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#14">2.11.14</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.14-1.noarch.rpm">dCache 2.11.14 (rpm)</a></td>
	<td class="date">24.3.2015</td>
	<td class="hash">d8d0e6d7b0c46dfabbbc39eb4adf1445</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.14.tar.gz">dCache 2.11.14 (tgz)</a></td>
	<td class="date">24.3.2015</td>
	<td class="hash">9dde39ef23dc7b077d3f00837ab7ddf5</td>
</tr>
<tr id="2.11.13" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.13-1_all.deb">dCache 2.11.13 (Debian package)</a></td>
	<td class="date">17.3.2015</td>
	<td class="hash">1544932125c18aed56aa353f8e45c2f1</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#13">2.11.13</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.13-1.noarch.rpm">dCache 2.11.13 (rpm)</a></td>
	<td class="date">17.3.2015</td>
	<td class="hash">a64f8b4990eb4fa27fd75fd2d7375dfd</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.13.tar.gz">dCache 2.11.13 (tgz)</a></td>
	<td class="date">17.3.2015</td>
	<td class="hash">4eb99395fee47b5c63f58a66f28e7871</td>
</tr>
<tr id="2.11.12" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.12-1_all.deb">dCache 2.11.12 (Debian package)</a></td>
	<td class="date">10.3.2015</td>
	<td class="hash">1ad3fe7cf946e187962528cc2410c53b</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#12">2.11.12</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.12-1.noarch.rpm">dCache 2.11.12 (rpm)</a></td>
	<td class="date">10.3.2015</td>
	<td class="hash">4a7d01b656cf4e4c3c91ed519f05a176</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.12.tar.gz">dCache 2.11.12 (tgz)</a></td>
	<td class="date">10.3.2015</td>
	<td class="hash">719a3024bb1d889396f2cf1e41aa52b8</td>
</tr>
<tr id="2.11.11" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.11-1_all.deb">dCache 2.11.11 (Debian package)</a></td>
	<td class="date">24.2.2015</td>
	<td class="hash">a5a05303bd3e8542d67dc75471bb2f08</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#11">2.11.11</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.11-1.noarch.rpm">dCache 2.11.11 (rpm)</a></td>
	<td class="date">24.2.2015</td>
	<td class="hash">b38b94579e91d5b08fcc5d8ec1d70e66</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.11.tar.gz">dCache 2.11.11 (tgz)</a></td>
	<td class="date">24.2.2015</td>
	<td class="hash">7160b563a607ab7a8d7fb54ad0761d96</td>
</tr>
<tr id="2.11.10" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.10-1_all.deb">dCache 2.11.10 (Debian package)</a></td>
	<td class="date">17.2.2015</td>
	<td class="hash">750b979a648ee6db74f9bc7784935a53</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#10">2.11.10</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.10-1.noarch.rpm">dCache 2.11.10 (rpm)</a></td>
	<td class="date">17.2.2015</td>
	<td class="hash">ea144ac01ac494f9cf74bdbc86de202d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.10.tar.gz">dCache 2.11.10 (tgz)</a></td>
	<td class="date">17.2.2015</td>
	<td class="hash">4743b9316afa1a35d47306293d7a65df</td>
</tr>
<tr id="2.11.9" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.9-1_all.deb">dCache 2.11.9 (Debian package)</a></td>
	<td class="date">9.2.2015</td>
	<td class="hash">bf605c6721b244f15bfd87b3aa4ce5a2</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#9">2.11.9</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.9-1.noarch.rpm">dCache 2.11.9 (rpm)</a></td>
	<td class="date">9.2.2015</td>
	<td class="hash">fed69f63340292bd02e379973f09543e</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.9.tar.gz">dCache 2.11.9 (tgz)</a></td>
	<td class="date">9.2.2015</td>
	<td class="hash">ec6dede8cee708f96fee53566bdb2986</td>
</tr>
<tr id="2.11.8" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.8-1_all.deb">dCache 2.11.8 (Debian package)</a></td>
	<td class="date">28.1.2015</td>
	<td class="hash">ee17e2ab569f9858019f3dd6e441743d</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#8">2.11.8</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.8-1.noarch.rpm">dCache 2.11.8 (rpm)</a></td>
	<td class="date">28.1.2015</td>
	<td class="hash">8c8f07bbdc55deccf8e690c47a3c92a1</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.8.tar.gz">dCache 2.11.8 (tgz)</a></td>
	<td class="date">28.1.2015</td>
	<td class="hash">16ae163eee36cc35a03ba89cef179c2c</td>
</tr>
<tr id="2.11.7" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.7-1_all.deb">dCache 2.11.7 (Debian package)</a></td>
	<td class="date">23.1.2015</td>
	<td class="hash">ac4e4a62c32222ec93a9d872c83dc421</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#7">2.11.7</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.7-1.noarch.rpm">dCache 2.11.7 (rpm)</a></td>
	<td class="date">23.1.2015</td>
	<td class="hash">121e55fbbdfffcf6f8dc5062abd4f8e9</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.7.tar.gz">dCache 2.11.7 (tgz)</a></td>
	<td class="date">23.1.2015</td>
	<td class="hash">30dd5fa69ced43f6269fcc3effb726a7</td>
</tr>
<tr id="2.11.5" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.5-1_all.deb">dCache 2.11.5 (Debian package)</a></td>
	<td class="date">19.12.2014</td>
	<td class="hash">121afa21fadb261fa2e36192f93d14c2</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#5">2.11.5</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.5-1.noarch.rpm">dCache 2.11.5 (rpm)</a></td>
	<td class="date">19.12.2014</td>
	<td class="hash">4d136f8188ddd0b2eaa7226672bc9e37</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.5.tar.gz">dCache 2.11.5 (tgz)</a></td>
	<td class="date">19.12.2014</td>
	<td class="hash">9a4de39a950f72f016aac31c78ab734b</td>
</tr>
<tr id="2.11.4" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.4-1_all.deb">dCache 2.11.4 (Debian package)</a></td>
	<td class="date">2.12.2014</td>
	<td class="hash">6dc8269de84045acecb1327348c4214b</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#4">2.11.4</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.4-1.noarch.rpm">dCache 2.11.4 (rpm)</a></td>
	<td class="date">2.12.2014</td>
	<td class="hash">98de657aa0326e1290d45cef6b16e4b8</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.4.tar.gz">dCache 2.11.4 (tgz)</a></td>
	<td class="date">2.12.2014</td>
	<td class="hash">9c1e24c60e64713d0ca624936b321ef2</td>
</tr>
<tr id="2.11.3" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.3-1_all.deb">dCache 2.11.3 (Debian package)</a></td>
	<td class="date">1.12.2014</td>
	<td class="hash">98fff4e787e087235491cb7fd181e8dc</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#3">2.11.3</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.3-1.noarch.rpm">dCache 2.11.3 (rpm)</a></td>
	<td class="date">1.12.2014</td>
	<td class="hash">6bfd4aa167e1efa16e29c3a8865c434f</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.3.tar.gz">dCache 2.11.3 (tgz)</a></td>
	<td class="date">1.12.2014</td>
	<td class="hash">476db4412c271af1d342b8c36feb0144</td>
</tr>
<tr id="2.11.2" class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.2-1_all.deb">dCache 2.11.2 (Debian package)</a></td>
	<td class="date">18.11.2014</td>
	<td class="hash">04c5d1d5feaad9eb91623a4e27369adb</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#2">2.11.2</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.2-1.noarch.rpm">dCache 2.11.2 (rpm)</a></td>
	<td class="date">18.11.2014</td>
	<td class="hash">d4bf88bec64fa57ba04cf0849cc15676</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.2.tar.gz">dCache 2.11.2 (tgz)</a></td>
	<td class="date">18.11.2014</td>
	<td class="hash">60399cbb0b8dace7ce025441be8cc6c6</td>
</tr>
<tr id="2.11.1" class="even">
	<td class="link"><a href="repo/2.11/dcache_2.11.1-1_all.deb">dCache 2.11.1 (Debian package)</a></td>
	<td class="date">12.11.2014</td>
	<td class="hash">5edec757f585103f3571f09e0dab6e73</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#1">2.11.1</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.1-1.noarch.rpm">dCache 2.11.1 (rpm)</a></td>
	<td class="date">12.11.2014</td>
	<td class="hash">346eb5cef24a24291737e56b732fa605</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.11/dcache-2.11.1.tar.gz">dCache 2.11.1 (tgz)</a></td>
	<td class="date">12.11.2014</td>
	<td class="hash">d6735229dfd4ca7e0b30073aa3d8ee18</td>
</tr>
<tr id="2.11.0" class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.0-1.noarch.rpm">dCache 2.11.0 (rpm)</a></td>
	<td class="date">6.11.2014</td>
	<td class="hash">f9cc2c9b330abe88183a636aa80ed6f5</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.11.shtml#0">2.11.0</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache_2.11.0-1_all.deb">dCache 2.11.0 (Debian package)</a></td>
	<td class="date">6.11.2014</td>
	<td class="hash">6dc6f404657f115a8200d53d5c8d07cf</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.11/dcache-2.11.0.tar.gz">dCache 2.11.0 (tgz)</a></td>
	<td class="date">6.11.2014</td>
	<td class="hash">9d3be2179affde6247f312e44663d002</td>
</tr>
</tbody>
</table>

<br xmlns=""> <a xmlns="" name="server-2.10"></a> <a name="server-2.10">server 2.10.x</a> <a href="rss-server-2.10-releases.xml" type="application/rss+xml"><img class="rss-icon" src="{{site.baseurl}}/images/rss-icon-14x14.png" alt="RSS" title="RSS feed for dCache server 2.10.x releases"></a>
		
In addition to the usual improvements and bug fixes, dCache
2.10 features the following highlights:
     
<ul xmlns="">
	  <li>Improved SRM scheduling and protection of other components.</li>

	  <li>Reimplemented webadmin active transfers page.</li>

	  <li>Improved support for HTTP and HTTPS 3rd-party transfers.</li>

	  <li>Added support for 3rd-party transfers through WebDAV.</li>

	  <li>Improved support for HTTP 3rd-party transfers through SRM.</li>

	  <li>Improved default HTML rendering in WebDAV.</li>

	  <li>Added JSON support for info.</li>
      </ul>
<p xmlns="">
	  dCache v2.10 requires a JVM supporting either Java v7 or Java v8.
      </p>
<table xmlns="" class="releases">
<thead>
<tr>
	<th>Download</th>
	<th>Rel. Date</th>
	<th>md5 hash</th>
	<th>Release Notes</th>
</tr>
</thead>
<tbody>
<tr id="2.10.62" class="rec">
	<td class="link"><a href="repo/2.10/dcache_2.10.62-1_all.deb">dCache 2.10.62 (Debian package)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">17707ac275f9d5e99dd89822de92e455</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml">2.10.62</a></td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.10/dcache-2.10.62-1.noarch.rpm">dCache 2.10.62 (rpm)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">1615418aa6745479035764ae311f64e6</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.10/dcache-2.10.62-1.pkg">dCache 2.10.62 (Solaris package)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">2877a9bf6508d5a7708df518290b566d</td>
</tr>
<tr class="rec">
	<td class="link"><a href="repo/2.10/dcache-2.10.62.tar.gz">dCache 2.10.62 (tgz)</a></td>
	<td class="date">22.11.2016</td>
	<td class="hash">1a112a7a091adbf42f1707385835639d</td>
</tr>
<tr id="2.10.61" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.61-1_all.deb">dCache 2.10.61 (Debian package)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">d51bf2098e502e7ab0f5fc1622bf0a7a</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#61">2.10.61</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.61-1.noarch.rpm">dCache 2.10.61 (rpm)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">d31532d003a562ce7adb2c096c0d1023</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.61-1.pkg">dCache 2.10.61 (Solaris package)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">9eb2b7a599b45a340de9289865b76fb2</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.61.tar.gz">dCache 2.10.61 (tgz)</a></td>
	<td class="date">14.6.2016</td>
	<td class="hash">7bd7f90cb7fd3a1133340ad9811290be</td>
</tr>
<tr id="2.10.60" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.60-1_all.deb">dCache 2.10.60 (Debian package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">042e7ec21e6df39f37b30e262dac5d0b</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#60">2.10.60</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.60-1.noarch.rpm">dCache 2.10.60 (rpm)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">a10921b50ca6d1d9dfbf39f07c041d2e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.60-1.pkg">dCache 2.10.60 (Solaris package)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">cacf05ed690f3acb69ccb4eb99198c95</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.60.tar.gz">dCache 2.10.60 (tgz)</a></td>
	<td class="date">2.6.2016</td>
	<td class="hash">5eeb6f43f3f68c5eded04c6ca4121785</td>
</tr>
<tr id="2.10.59" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.59-1_all.deb">dCache 2.10.59 (Debian package)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">844f7d86b2ef57c88c6a5d09652b8d64</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#59">2.10.59</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.59-1.noarch.rpm">dCache 2.10.59 (rpm)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">c9c9a6c0738f363392a0f6dd3ea3c222</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.59-1.pkg">dCache 2.10.59 (Solaris package)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">79697c1a5cf9d9785ca3fd51b68e7765</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.59.tar.gz">dCache 2.10.59 (tgz)</a></td>
	<td class="date">19.4.2016</td>
	<td class="hash">5c6df3e00c6f4636b9c4fb02b3e10564</td>
</tr>
<tr id="2.10.58" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.58-1_all.deb">dCache 2.10.58 (Debian package)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">12bf15a29bb4b74dbf9492762a222a74</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#58">2.10.58</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.58-1.noarch.rpm">dCache 2.10.58 (rpm)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">8f943f319ad1cba4104048c3d25efb7c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.58-1.pkg">dCache 2.10.58 (Solaris package)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">f213571415ff614a7d42d52085e4c3f6</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.58.tar.gz">dCache 2.10.58 (tgz)</a></td>
	<td class="date">22.3.2016</td>
	<td class="hash">65dce0fbd4a5dabaa45a760988b60bcd</td>
</tr>
<tr id="2.10.57" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.57-1_all.deb">dCache 2.10.57 (Debian package)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">2cc420c8a1224abe4472e6329ef525b5</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#57">2.10.57</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.57-1.noarch.rpm">dCache 2.10.57 (rpm)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">cb6afb46a551c5fac0cf7e0716401fa6</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.57-1.pkg">dCache 2.10.57 (Solaris package)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">428266fb78ffff791bb210c80058fa0e</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.57.tar.gz">dCache 2.10.57 (tgz)</a></td>
	<td class="date">8.3.2016</td>
	<td class="hash">bda57d998674cc3ff3da7a494b1465ff</td>
</tr>
<tr id="2.10.56" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.56-1_all.deb">dCache 2.10.56 (Debian package)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">b611425886d4a3dbacfa3a0ed42e70a9</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#56">2.10.56</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.56-1.noarch.rpm">dCache 2.10.56 (rpm)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">43a1f25f0fed2f90ee099afd74668eec</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.56-1.pkg">dCache 2.10.56 (Solaris package)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">eb444116bdb9a3852b4de67c1189c7c3</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.56.tar.gz">dCache 2.10.56 (tgz)</a></td>
	<td class="date">23.2.2016</td>
	<td class="hash">3b39172041c5a5d50b26218180ff8ec3</td>
</tr>
<tr id="2.10.55" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.55-1_all.deb">dCache 2.10.55 (Debian package)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">5b5ac2f3acc12e8c2cdcd6bd72fc707f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#55">2.10.55</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.55-1.noarch.rpm">dCache 2.10.55 (rpm)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">7b3f01ed1de398cf9efe0d9112d30f98</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.55-1.pkg">dCache 2.10.55 (Solaris package)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">de12467badf44206e526509e33b5d8b9</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.55.tar.gz">dCache 2.10.55 (tgz)</a></td>
	<td class="date">17.2.2016</td>
	<td class="hash">88b58e4ff793532a24950a568c6dc468</td>
</tr>
<tr id="2.10.54" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.54-1_all.deb">dCache 2.10.54 (Debian package)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">6c119f9eae6373002887135969be6ba4</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#54">2.10.54</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.54-1.noarch.rpm">dCache 2.10.54 (rpm)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">15c0bf21135bd3eaee30bede91f1ad48</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.54-1.pkg">dCache 2.10.54 (Solaris package)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">d726b2cd48ba741dbb62d8c17859b023</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.54.tar.gz">dCache 2.10.54 (tgz)</a></td>
	<td class="date">9.2.2016</td>
	<td class="hash">c708ff2c054b419e2490839d4fb1d225</td>
</tr>
<tr id="2.10.53" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.53-1_all.deb">dCache 2.10.53 (Debian package)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">cba81d4a8fe26346c5042bba28677506</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#53">2.10.53</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.53-1.noarch.rpm">dCache 2.10.53 (rpm)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">4a33dbf8d12180a929350c2ca4512e0e</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.53-1.pkg">dCache 2.10.53 (Solaris package)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">2c1fff5fa6a8b93507cd80573fb67cb8</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.53.tar.gz">dCache 2.10.53 (tgz)</a></td>
	<td class="date">2.2.2016</td>
	<td class="hash">eda35dfa6e584d85453dd7c251531389</td>
</tr>
<tr id="2.10.52" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.52-1_all.deb">dCache 2.10.52 (Debian package)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">c7765001f013b67a506400e461d74b53</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#52">2.10.52</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.52-1.noarch.rpm">dCache 2.10.52 (rpm)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">28fffb7f7aba396a9a19efcb139c0214</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.52-1.pkg">dCache 2.10.52 (Solaris package)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">e6ad036ec724fc5ea61f005bd848e93c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.52.tar.gz">dCache 2.10.52 (tgz)</a></td>
	<td class="date">27.1.2016</td>
	<td class="hash">84827a86bd67970fa4ea5b2c4c793a17</td>
</tr>
<tr id="2.10.51" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.51-1_all.deb">dCache 2.10.51 (Debian package)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">258d1556e79b3a33b7d938d2a6acf7f5</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#51">2.10.51</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.51-1.noarch.rpm">dCache 2.10.51 (rpm)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">cea25922bdc821d623d7fbf41a6074e2</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.51-1.pkg">dCache 2.10.51 (Solaris package)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">1b1af3c861f640a9ced7fbb212020227</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.51.tar.gz">dCache 2.10.51 (tgz)</a></td>
	<td class="date">20.1.2016</td>
	<td class="hash">3f6c34a8fcd6f7673e19b09ed54e12e7</td>
</tr>
<tr id="2.10.50" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.50-1_all.deb">dCache 2.10.50 (Debian package)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">a8e96d5686e1bfe9aed1bf5b9ea55fd0</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#50">2.10.50</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.50-1.noarch.rpm">dCache 2.10.50 (rpm)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">136683ec2172040e92ed09a7695f4d01</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.50-1.pkg">dCache 2.10.50 (Solaris package)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">cf0bfdfd6e9bae302489e609111bce59</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.50.tar.gz">dCache 2.10.50 (tgz)</a></td>
	<td class="date">12.1.2016</td>
	<td class="hash">d4204504514629b5ec3de0874591111f</td>
</tr>
<tr id="2.10.49" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.49-1_all.deb">dCache 2.10.49 (Debian package)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">95da720d4406a64432bc0c0c5163c93c</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#49">2.10.49</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.49-1.noarch.rpm">dCache 2.10.49 (rpm)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">e8a4dc87e2f4431ef134f9a5de18cd2d</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.49-1.pkg">dCache 2.10.49 (Solaris package)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">3de72d1722f42609007a490cd50e2311</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.49.tar.gz">dCache 2.10.49 (tgz)</a></td>
	<td class="date">7.1.2016</td>
	<td class="hash">2665277d0d0247f4458ecabc3433e256</td>
</tr>
<tr id="2.10.48" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.48-1_all.deb">dCache 2.10.48 (Debian package)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">c974887016c39fe4afb0f4357f6238fe</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#48">2.10.48</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.48-1.noarch.rpm">dCache 2.10.48 (rpm)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">5c3761e16f5f6fa48ff58ffcd34420b1</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.48-1.pkg">dCache 2.10.48 (Solaris package)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">a6ab00e9b229398eae6f3f22b93df71c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.48.tar.gz">dCache 2.10.48 (tgz)</a></td>
	<td class="date">17.12.2015</td>
	<td class="hash">6dad59b44608bc67f6f106ecd22d3eb0</td>
</tr>
<tr id="2.10.47" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.47-1_all.deb">dCache 2.10.47 (Debian package)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">bbd1bab9e0a41f2dab3c7fa5072f2a1f</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#47">2.10.47</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.47-1.noarch.rpm">dCache 2.10.47 (rpm)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">6feb1df9d48f68d6c03127d02aa2bd95</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.47-1.pkg">dCache 2.10.47 (Solaris package)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">76ec5370b9a6710c24f11a8e7ce57e61</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.47.tar.gz">dCache 2.10.47 (tgz)</a></td>
	<td class="date">8.12.2015</td>
	<td class="hash">282bba73758eb3dd417ed20caaaf57d6</td>
</tr>
<tr id="2.10.46" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.46-1_all.deb">dCache 2.10.46 (Debian package)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">2702916a7a05c47512d102a1788e5cc9</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#46">2.10.46</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.46-1.noarch.rpm">dCache 2.10.46 (rpm)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">b938f714bf1c8a0c5553137bc4de8b06</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.46-1.pkg">dCache 2.10.46 (Solaris package)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">abc3433acc98321ecde5665595cdd298</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.46.tar.gz">dCache 2.10.46 (tgz)</a></td>
	<td class="date">1.12.2015</td>
	<td class="hash">a0b9a13fad9653e9ce6ca06bc83989bd</td>
</tr>
<tr id="2.10.45" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.45-1_all.deb">dCache 2.10.45 (Debian package)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">ac1377c30188b66864c7bc216ef5550b</td>
	<td class="notes" rowspan="4"><a href="release-notes-2.10.shtml#45">2.10.45</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.45-1.noarch.rpm">dCache 2.10.45 (rpm)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">fea474268313ab915149fb56d5dd32c8</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.45-1.pkg">dCache 2.10.45 (Solaris package)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">5dd1e35389970d6ad1d9532933294699</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.45.tar.gz">dCache 2.10.45 (tgz)</a></td>
	<td class="date">24.11.2015</td>
	<td class="hash">3c82c6a5f543f9106a0f1bdd7705bd0f</td>
</tr>
<tr id="2.10.44" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.44-1_all.deb">dCache 2.10.44 (Debian package)</a></td>
	<td class="date">2.11.2015</td>
	<td class="hash">c6f693f4ac8519d79276c8a8424c750a</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#44">2.10.44</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.44-1.noarch.rpm">dCache 2.10.44 (rpm)</a></td>
	<td class="date">2.11.2015</td>
	<td class="hash">afcc5463c47f528b8319e62f4b644016</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.44.tar.gz">dCache 2.10.44 (tgz)</a></td>
	<td class="date">2.11.2015</td>
	<td class="hash">b362111e8bbce55b9b15b508312cf327</td>
</tr>
<tr id="2.10.43" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.43-1_all.deb">dCache 2.10.43 (Debian package)</a></td>
	<td class="date">27.10.2015</td>
	<td class="hash">2105da71bf4f8f44a0bba01f27e9d8ac</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#43">2.10.43</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.43-1.noarch.rpm">dCache 2.10.43 (rpm)</a></td>
	<td class="date">27.10.2015</td>
	<td class="hash">a960e82eb5d96a18983e18aa62c5286a</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.43.tar.gz">dCache 2.10.43 (tgz)</a></td>
	<td class="date">27.10.2015</td>
	<td class="hash">9ac09b8ecb5b4608e738ea9a29b97090</td>
</tr>
<tr id="2.10.42" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.42-1_all.deb">dCache 2.10.42 (Debian package)</a></td>
	<td class="date">14.10.2015</td>
	<td class="hash">1e1f1f9f5127f1c9a092f4bc68b63ce2</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#42">2.10.42</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.42-1.noarch.rpm">dCache 2.10.42 (rpm)</a></td>
	<td class="date">14.10.2015</td>
	<td class="hash">aa4e97fc836977311860cc2e34d88e07</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.42.tar.gz">dCache 2.10.42 (tgz)</a></td>
	<td class="date">14.10.2015</td>
	<td class="hash">58a0149f1b8bbe81246896fbcce47226</td>
</tr>
<tr id="2.10.41" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.41-2_all.deb">dCache 2.10.41 (Debian package)</a></td>
	<td class="date">21.9.2015</td>
	<td class="hash">327475712e238ffa8fe43cf4655dbd3b</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#41">2.10.41</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.41-2.noarch.rpm">dCache 2.10.41 (rpm)</a></td>
	<td class="date">21.9.2015</td>
	<td class="hash">60749171a77177b983f867b29f807abf</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.41.tar.gz">dCache 2.10.41 (tgz)</a></td>
	<td class="date">21.9.2015</td>
	<td class="hash">aef23b96bb8b654943298d07c2a3e379</td>
</tr>
<tr id="2.10.40" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.40-1_all.deb">dCache 2.10.40 (Debian package)</a></td>
	<td class="date">9.9.2015</td>
	<td class="hash">3395b7cc3297cb9e9cb6a4289ecf1bc6</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#40">2.10.40</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.40-1.noarch.rpm">dCache 2.10.40 (rpm)</a></td>
	<td class="date">9.9.2015</td>
	<td class="hash">bf19558818693a4a38e1a1e8b04ac569</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.40.tar.gz">dCache 2.10.40 (tgz)</a></td>
	<td class="date">9.9.2015</td>
	<td class="hash">8085b799b98f5ac6e970e2466e63069c</td>
</tr>
<tr id="2.10.39" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.39-1_all.deb">dCache 2.10.39 (Debian package)</a></td>
	<td class="date">24.8.2015</td>
	<td class="hash">c880fe54f9239b3f1b6314e44cb3d497</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#39">2.10.39</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.39-2.noarch.rpm">dCache 2.10.39 (rpm)</a></td>
	<td class="date">24.8.2015</td>
	<td class="hash">67226344c3f5f60f61cfcb7346988995</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.39.tar.gz">dCache 2.10.39 (tgz)</a></td>
	<td class="date">24.8.2015</td>
	<td class="hash">76036dbedfeec49365e53ceac22a136b</td>
</tr>
<tr id="2.10.38" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.38-1_all.deb">dCache 2.10.38 (Debian package)</a></td>
	<td class="date">18.8.2015</td>
	<td class="hash">1a79201cbccba3dffe59cc9301374ab5</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#38">2.10.38</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.38-2.noarch.rpm">dCache 2.10.38 (rpm)</a></td>
	<td class="date">18.8.2015</td>
	<td class="hash">14857ac39ffdaa276d08d4a19a047819</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.38.tar.gz">dCache 2.10.38 (tgz)</a></td>
	<td class="date">18.8.2015</td>
	<td class="hash">d0d7c85ffd300da600c7cf3257cabdbb</td>
</tr>
<tr id="2.10.37" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.37-1_all.deb">dCache 2.10.37 (Debian package)</a></td>
	<td class="date">24.7.2015</td>
	<td class="hash">1e662e23be72c934e9f37a6857c03226</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#37">2.10.37</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.37-1.noarch.rpm">dCache 2.10.37 (rpm)</a></td>
	<td class="date">24.7.2015</td>
	<td class="hash">caf015f9eb5a70f1b5cecc8dfa4bfd43</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.37.tar.gz">dCache 2.10.37 (tgz)</a></td>
	<td class="date">24.7.2015</td>
	<td class="hash">aeacbf4c33fcc7fa9d39ff43f77ee5a0</td>
</tr>
<tr id="2.10.36" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.36-1_all.deb">dCache 2.10.36 (Debian package)</a></td>
	<td class="date">15.7.2015</td>
	<td class="hash">234f42967c682c7da7226072fb1d479a</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#36">2.10.36</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.36-1.noarch.rpm">dCache 2.10.36 (rpm)</a></td>
	<td class="date">15.7.2015</td>
	<td class="hash">3e231a2cc148baa3f55e09200489a3cc</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.36.tar.gz">dCache 2.10.36 (tgz)</a></td>
	<td class="date">15.7.2015</td>
	<td class="hash">f4a9652724228958fd2d088a041ecd1f</td>
</tr>
<tr id="2.10.35" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.35-1_all.deb">dCache 2.10.35 (Debian package)</a></td>
	<td class="date">1.7.2015</td>
	<td class="hash">03420656fb040acf171cc66c065cf00a</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#35">2.10.35</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.35-1.noarch.rpm">dCache 2.10.35 (rpm)</a></td>
	<td class="date">1.7.2015</td>
	<td class="hash">559c7ec1ecb378a0e917ae3c3f01e340</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.35.tar.gz">dCache 2.10.35 (tgz)</a></td>
	<td class="date">1.7.2015</td>
	<td class="hash">d329cfc66d28f4083a4b0193f9f99a50</td>
</tr>
<tr id="2.10.34" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.34-1_all.deb">dCache 2.10.34 (Debian package)</a></td>
	<td class="date">24.6.2015</td>
	<td class="hash">5098965994fb36446d2bc5b063c9bf94</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#34">2.10.34</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.34-1.noarch.rpm">dCache 2.10.34 (rpm)</a></td>
	<td class="date">24.6.2015</td>
	<td class="hash">3b89beca003bd4f01b81c7ce62326265</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.34.tar.gz">dCache 2.10.34 (tgz)</a></td>
	<td class="date">24.6.2015</td>
	<td class="hash">99f1933cc29fd8f223fd6c1da7e66cf1</td>
</tr>
<tr id="2.10.33" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.33-1_all.deb">dCache 2.10.33 (Debian package)</a></td>
	<td class="date">16.6.2015</td>
	<td class="hash">f265954abff67bc82a6ec45637dd1693</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#33">2.10.33</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.33-1.noarch.rpm">dCache 2.10.33 (rpm)</a></td>
	<td class="date">16.6.2015</td>
	<td class="hash">313d2f90c62ebdb3bd39642d306e4ba8</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.33.tar.gz">dCache 2.10.33 (tgz)</a></td>
	<td class="date">16.6.2015</td>
	<td class="hash">fd69ca1bdfb186eb4a6a11155cacd23f</td>
</tr>
<tr id="2.10.32" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.32-1_all.deb">dCache 2.10.32 (Debian package)</a></td>
	<td class="date">9.6.2015</td>
	<td class="hash">4abb260ba49cb3986dae9fc39cb76bbe</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#32">2.10.32</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.32-1.noarch.rpm">dCache 2.10.32 (rpm)</a></td>
	<td class="date">9.6.2015</td>
	<td class="hash">8080bc4255c6befa6cede1698cbae79c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.32.tar.gz">dCache 2.10.32 (tgz)</a></td>
	<td class="date">9.6.2015</td>
	<td class="hash">58821bf845f3db23469395105beae6fd</td>
</tr>
<tr id="2.10.31" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.31-1_all.deb">dCache 2.10.31 (Debian package)</a></td>
	<td class="date">2.6.2015</td>
	<td class="hash">835d978c93ed9c136215ae1b28983380</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#31">2.10.31</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.31-1.noarch.rpm">dCache 2.10.31 (rpm)</a></td>
	<td class="date">2.6.2015</td>
	<td class="hash">534971f809c8449e8e54b88666cd10f6</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.31.tar.gz">dCache 2.10.31 (tgz)</a></td>
	<td class="date">2.6.2015</td>
	<td class="hash">286aca643de38b1444843f38d1591053</td>
</tr>
<tr id="2.10.30" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.30-1_all.deb">dCache 2.10.30 (Debian package)</a></td>
	<td class="date">19.5.2015</td>
	<td class="hash">419970866d152e3f441fda80e1b1b7a7</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#30">2.10.30</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.30-1.noarch.rpm">dCache 2.10.30 (rpm)</a></td>
	<td class="date">19.5.2015</td>
	<td class="hash">5c3f885a7aec62856247225d360f615c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.30.tar.gz">dCache 2.10.30 (tgz)</a></td>
	<td class="date">19.5.2015</td>
	<td class="hash">4cdc1758a03dfb2d408a4d514160a6d9</td>
</tr>
<tr id="2.10.29" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.29-1_all.deb">dCache 2.10.29 (Debian package)</a></td>
	<td class="date">12.5.2015</td>
	<td class="hash">1d748dd8cf7c2d85274c338cc86ed843</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#29">2.10.29</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.29-1.noarch.rpm">dCache 2.10.29 (rpm)</a></td>
	<td class="date">12.5.2015</td>
	<td class="hash">55950afeebdcbae4ed44d4116def0c5c</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.29.tar.gz">dCache 2.10.29 (tgz)</a></td>
	<td class="date">12.5.2015</td>
	<td class="hash">3577b96d309cea090f25793f3d5107f1</td>
</tr>
<tr id="2.10.28" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.28-1_all.deb">dCache 2.10.28 (Debian package)</a></td>
	<td class="date">5.5.2015</td>
	<td class="hash">32ec1b7d9b35abad835012a64d4d1f20</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#28">2.10.28</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.28-1.noarch.rpm">dCache 2.10.28 (rpm)</a></td>
	<td class="date">5.5.2015</td>
	<td class="hash">23c80313dd3df98062b9484a6bbf808a</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.28.tar.gz">dCache 2.10.28 (tgz)</a></td>
	<td class="date">5.5.2015</td>
	<td class="hash">ba4ffde733b678c6e6017bdb1ce14308</td>
</tr>
<tr id="2.10.27" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.27-1_all.deb">dCache 2.10.27 (Debian package)</a></td>
	<td class="date">29.4.2015</td>
	<td class="hash">c855dd3c3cdb44ff1d597ff605b26fc0</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#27">2.10.27</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.27-1.noarch.rpm">dCache 2.10.27 (rpm)</a></td>
	<td class="date">29.4.2015</td>
	<td class="hash">d081938fb50a7e1b5da7c2c6e3786d98</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.27.tar.gz">dCache 2.10.27 (tgz)</a></td>
	<td class="date">29.4.2015</td>
	<td class="hash">94c7bd6fa5de7b6ec34dd5b318126f5f</td>
</tr>
<tr id="2.10.25" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.25-1_all.deb">dCache 2.10.25 (Debian package)</a></td>
	<td class="date">21.4.2015</td>
	<td class="hash">9319b9b7be6ec11104f11fd6c2e5bc77</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#25">2.10.25</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.25-1.noarch.rpm">dCache 2.10.25 (rpm)</a></td>
	<td class="date">21.4.2015</td>
	<td class="hash">f19bc1f68341e74971034d6356db0eaf</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.25.tar.gz">dCache 2.10.25 (tgz)</a></td>
	<td class="date">21.4.2015</td>
	<td class="hash">440cc3505c3c2b814bbfecf378485db3</td>
</tr>
<tr id="2.10.24" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.24-1_all.deb">dCache 2.10.24 (Debian package)</a></td>
	<td class="date">31.3.2015</td>
	<td class="hash">dcd3d626ce332be89a40bcffacc59187</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#24">2.10.24</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.24-1.noarch.rpm">dCache 2.10.24 (rpm)</a></td>
	<td class="date">31.3.2015</td>
	<td class="hash">f56faba277718451c0c95c8a3c1b9ba7</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.24.tar.gz">dCache 2.10.24 (tgz)</a></td>
	<td class="date">31.3.2015</td>
	<td class="hash">d1eb3243664d6e258abbccb7ee1f96f8</td>
</tr>
<tr id="2.10.23" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.23-1_all.deb">dCache 2.10.23 (Debian package)</a></td>
	<td class="date">24.3.2015</td>
	<td class="hash">bf7e000c5b49d5ca128a007a2d20be5b</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#23">2.10.23</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.23-1.noarch.rpm">dCache 2.10.23 (rpm)</a></td>
	<td class="date">24.3.2015</td>
	<td class="hash">c6ef1964141b6121d04e87b13a6a5f0e</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.23.tar.gz">dCache 2.10.23 (tgz)</a></td>
	<td class="date">24.3.2015</td>
	<td class="hash">c634a133fada4b4d9987857c36f6a6eb</td>
</tr>
<tr id="2.10.22" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.22-1_all.deb">dCache 2.10.22 (Debian package)</a></td>
	<td class="date">17.3.2015</td>
	<td class="hash">531718220ab4113157d90b21851739a8</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#22">2.10.22</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.22-1.noarch.rpm">dCache 2.10.22 (rpm)</a></td>
	<td class="date">17.3.2015</td>
	<td class="hash">e255da0940ecfd96fcc9bc36d866c11e</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.22.tar.gz">dCache 2.10.22 (tgz)</a></td>
	<td class="date">17.3.2015</td>
	<td class="hash">961182d96f28bc8719e0ee83ff11d362</td>
</tr>
<tr id="2.10.21" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.21-1_all.deb">dCache 2.10.21 (Debian package)</a></td>
	<td class="date">10.3.2015</td>
	<td class="hash">15dfd125c41873775e406d5a0d238d69</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#21">2.10.21</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.21-1.noarch.rpm">dCache 2.10.21 (rpm)</a></td>
	<td class="date">10.3.2015</td>
	<td class="hash">f22f3c59563cf489f40e90f3660832f7</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.21.tar.gz">dCache 2.10.21 (tgz)</a></td>
	<td class="date">10.3.2015</td>
	<td class="hash">3942d96955f49fc8f01ff8e335cda53c</td>
</tr>
<tr id="2.10.20" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.20-1_all.deb">dCache 2.10.20 (Debian package)</a></td>
	<td class="date">24.2.2015</td>
	<td class="hash">a38a6b4a9f6c962d9446a39c4da1f515</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#20">2.10.20</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.20-1.noarch.rpm">dCache 2.10.20 (rpm)</a></td>
	<td class="date">24.2.2015</td>
	<td class="hash">5fa0335670e47487e773d39c9bf3012b</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.20.tar.gz">dCache 2.10.20 (tgz)</a></td>
	<td class="date">24.2.2015</td>
	<td class="hash">d1ab52722c4c995fb9842a54665a4ef1</td>
</tr>
<tr id="2.10.19" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.19-1_all.deb">dCache 2.10.19 (Debian package)</a></td>
	<td class="date">17.2.2015</td>
	<td class="hash">3fe2e7c1b2cf38af7f4b6bddae044b2d</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#19">2.10.19</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.19-1.noarch.rpm">dCache 2.10.19 (rpm)</a></td>
	<td class="date">17.2.2015</td>
	<td class="hash">1273698106e790ef67e230fb938a050c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.19.tar.gz">dCache 2.10.19 (tgz)</a></td>
	<td class="date">17.2.2015</td>
	<td class="hash">f08c49e9e8b620be0c31690aea38e446</td>
</tr>
<tr id="2.10.18" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.18-1_all.deb">dCache 2.10.18 (Debian package)</a></td>
	<td class="date">9.2.2015</td>
	<td class="hash">ca146451f1b566ff7602ca7a98672ae2</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#18">2.10.18</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.18-1.noarch.rpm">dCache 2.10.18 (rpm)</a></td>
	<td class="date">9.2.2015</td>
	<td class="hash">0ba5e86a3cd08102fb5632553044738e</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.18.tar.gz">dCache 2.10.18 (tgz)</a></td>
	<td class="date">9.2.2015</td>
	<td class="hash">9638662050eb2ead8fa341ab5ac8d494</td>
</tr>
<tr id="2.10.17" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.17-1_all.deb">dCache 2.10.17 (Debian package)</a></td>
	<td class="date">28.1.2015</td>
	<td class="hash">baf354dd7f995eae5088069faa270c06</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#17">2.10.17</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.17-1.noarch.rpm">dCache 2.10.17 (rpm)</a></td>
	<td class="date">28.1.2015</td>
	<td class="hash">0c0e2c0468d957e626251f19ac8ea7a4</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.17.tar.gz">dCache 2.10.17 (tgz)</a></td>
	<td class="date">28.1.2015</td>
	<td class="hash">8e95a5cd2e85e7b97d058cba92f99121</td>
</tr>
<tr id="2.10.16" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.16-1_all.deb">dCache 2.10.16 (Debian package)</a></td>
	<td class="date">23.1.2015</td>
	<td class="hash">af5051bf307899f7ac5fc0e29c1689a4</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#16">2.10.16</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.16-1.noarch.rpm">dCache 2.10.16 (rpm)</a></td>
	<td class="date">23.1.2015</td>
	<td class="hash">8f285d55e01afbe115e699a796edcda6</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.16.tar.gz">dCache 2.10.16 (tgz)</a></td>
	<td class="date">23.1.2015</td>
	<td class="hash">b06a2b2b428ead7dd5756f1fa578e938</td>
</tr>
<tr id="2.10.14" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.14-1_all.deb">dCache 2.10.14 (Debian package)</a></td>
	<td class="date">19.12.2014</td>
	<td class="hash">645fbf7d91ea606ea76e16f9b69527a5</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#14">2.10.14</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.14-1.noarch.rpm">dCache 2.10.14 (rpm)</a></td>
	<td class="date">19.12.2014</td>
	<td class="hash">f4c8d2f5bd3517f332ae5e672ab7030f</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.14.tar.gz">dCache 2.10.14 (tgz)</a></td>
	<td class="date">19.12.2014</td>
	<td class="hash">d4599227b7e49822f0c78edba95d24bc</td>
</tr>
<tr id="2.10.13" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.13-1_all.deb">dCache 2.10.13 (Debian package)</a></td>
	<td class="date">2.12.2014</td>
	<td class="hash">1e8eb5bbd7b2a2494a47e5dc576d7607</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#13">2.10.13</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.13-1.noarch.rpm">dCache 2.10.13 (rpm)</a></td>
	<td class="date">2.12.2014</td>
	<td class="hash">e327e0701dbad6ae0a20db3b3d72a826</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.13.tar.gz">dCache 2.10.13 (tgz)</a></td>
	<td class="date">2.12.2014</td>
	<td class="hash">174d495520f74f0386c057c3435091da</td>
</tr>
<tr id="2.10.12" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.12-1_all.deb">dCache 2.10.12 (Debian package)</a></td>
	<td class="date">1.12.2014</td>
	<td class="hash">0e52f092a9df902faec5dd5218aa20bd</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#12">2.10.12</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.12-1.noarch.rpm">dCache 2.10.12 (rpm)</a></td>
	<td class="date">1.12.2014</td>
	<td class="hash">4c9ac5cafd6986bf197f18d2958a51b8</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.12.tar.gz">dCache 2.10.12 (tgz)</a></td>
	<td class="date">1.12.2014</td>
	<td class="hash">6a6e231035d4d823a4486f4adf87321b</td>
</tr>
<tr id="2.10.11" class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.11-1_all.deb">dCache 2.10.11 (Debian package)</a></td>
	<td class="date">18.11.2014</td>
	<td class="hash">074a5beaa749c4a872eccf85794391fd</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#11">2.10.11</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.11-1.noarch.rpm">dCache 2.10.11 (rpm)</a></td>
	<td class="date">18.11.2014</td>
	<td class="hash">8f0e64881ba66eec09e6c698c0990285</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.11.tar.gz">dCache 2.10.11 (tgz)</a></td>
	<td class="date">18.11.2014</td>
	<td class="hash">e7525290afca0f850e3835f000cee5ad</td>
</tr>
<tr id="2.10.10" class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.10-1_all.deb">dCache 2.10.10 (Debian package)</a></td>
	<td class="date">12.11.2014</td>
	<td class="hash">082a28e36e72be0022440aa4f29b2a51</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#10">2.10.10</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.10-1.noarch.rpm">dCache 2.10.10 (rpm)</a></td>
	<td class="date">12.11.2014</td>
	<td class="hash">ac722f11a965c7350ead7b7105ab0339</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.10.tar.gz">dCache 2.10.10 (tgz)</a></td>
	<td class="date">12.11.2014</td>
	<td class="hash">bb74c693b60208dcbfb5914c4740084c</td>
</tr>
<tr id="2.10.9" class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.9-1.noarch.rpm">dCache 2.10.9 (rpm)</a></td>
	<td class="date">28.10.2014</td>
	<td class="hash">2e7186872520951453fec3aa75ac06ee</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#9">2.10.9</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.9-1_all.deb">dCache 2.10.9 (Debian package)</a></td>
	<td class="date">28.10.2014</td>
	<td class="hash">3262d5be5e94ced9a85c614cdd237fe1</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.9.tar.gz">dCache 2.10.9 (tgz)</a></td>
	<td class="date">28.10.2014</td>
	<td class="hash">30a991172941c72dfb8d5df335647ff1</td>
</tr>
<tr id="2.10.8" class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.8-1.noarch.rpm">dCache 2.10.8 (rpm)</a></td>
	<td class="date">21.10.2014</td>
	<td class="hash">a10d7e065c6ad9e5efde3f7525f5bc5c</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#8">2.10.8</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.8-1_all.deb">dCache 2.10.8 (Debian package)</a></td>
	<td class="date">21.10.2014</td>
	<td class="hash">6e77b2d0b165195e5a29f125f4a49a4d</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.8.tar.gz">dCache 2.10.8 (tgz)</a></td>
	<td class="date">21.10.2014</td>
	<td class="hash">b39b67347eb28d7cdf64932c5365a761</td>
</tr>
<tr id="2.10.7" class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.7-1.noarch.rpm">dCache 2.10.7 (rpm)</a></td>
	<td class="date">10.10.2014</td>
	<td class="hash">df72c66ee1169b8d2553900145213ca5</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#7">2.10.7</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.7-1_all.deb">dCache 2.10.7 (Debian package)</a></td>
	<td class="date">10.10.2014</td>
	<td class="hash">a383dacd3e5f5ca2a5e70589b49a47bc</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.7.tar.gz">dCache 2.10.7 (tgz)</a></td>
	<td class="date">10.10.2014</td>
	<td class="hash">5bfff2041d9390ba667ab3e767e9ae51</td>
</tr>
<tr id="2.10.4" class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.4-1.noarch.rpm">dCache 2.10.4 (rpm)</a></td>
	<td class="date">18.9.2014</td>
	<td class="hash">2683e6caacbf8865ace7198f71a1733b</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#4">2.10.4</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.4-1_all.deb">dCache 2.10.4 (Debian package)</a></td>
	<td class="date">18.9.2014</td>
	<td class="hash">ff76b831b5745450faeebf09fa4db753</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.4.tar.gz">dCache 2.10.4 (tgz)</a></td>
	<td class="date">18.9.2014</td>
	<td class="hash">66da493aac48c00df4d69a479a622b28</td>
</tr>
<tr id="2.10.3" class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.3-1.noarch.rpm">dCache 2.10.3 (rpm)</a></td>
	<td class="date">26.8.2014</td>
	<td class="hash">0224fc86ecf0c78e924699ee71bc86fc</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#3">2.10.3</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.3-1_all.deb">dCache 2.10.3 (Debian package)</a></td>
	<td class="date">26.8.2014</td>
	<td class="hash">e0cced63938ab184ddc9d2a5a7319f3d</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.3.tar.gz">dCache 2.10.3 (tgz)</a></td>
	<td class="date">26.8.2014</td>
	<td class="hash">bace0d9119f89cfd8b48ace8664ff596</td>
</tr>
<tr id="2.10.2" class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.2-1.noarch.rpm">dCache 2.10.2 (rpm)</a></td>
	<td class="date">12.8.2014</td>
	<td class="hash">830826d2f6e24ccb3d7e58bf55925509</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#2">2.10.2</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.2-1_all.deb">dCache 2.10.2 (Debian package)</a></td>
	<td class="date">12.8.2014</td>
	<td class="hash">9ce7f614ace646c9c5423708ea580f3c</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.2.tar.gz">dCache 2.10.2 (tgz)</a></td>
	<td class="date">12.8.2014</td>
	<td class="hash">5508c8b4752a08c9a255183a413c4f55</td>
</tr>
<tr id="2.10.1" class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.1-1.noarch.rpm">dCache 2.10.1 (rpm)</a></td>
	<td class="date">7.8.2014</td>
	<td class="hash">0174d719a1f954b2f4531187ac3e414a</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#1">2.10.1</a></td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache_2.10.1-1_all.deb">dCache 2.10.1 (Debian package)</a></td>
	<td class="date">7.8.2014</td>
	<td class="hash">c47aaa8227fac7ff7c85eebb876b45f0</td>
</tr>
<tr class="odd">
	<td class="link"><a href="repo/2.10/dcache-2.10.1.tar.gz">dCache 2.10.1 (tgz)</a></td>
	<td class="date">7.8.2014</td>
	<td class="hash">64d796d90d7e9d6f895ea95cf069d87c</td>
</tr>
<tr id="2.10.0" class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.0-1.noarch.rpm">dCache 2.10.0 (rpm)</a></td>
	<td class="date">11.7.2014</td>
	<td class="hash">700ac6bff1127430565155da3549079c</td>
	<td class="notes" rowspan="3"><a href="release-notes-2.10.shtml#0">2.10.0</a></td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache_2.10.0-1_all.deb">dCache 2.10.0 (Debian package)</a></td>
	<td class="date">11.7.2014</td>
	<td class="hash">2794caebd7a81c38c4ab907ebe588926</td>
</tr>
<tr class="even">
	<td class="link"><a href="repo/2.10/dcache-2.10.0.tar.gz">dCache 2.10.0 (tgz)</a></td>
	<td class="date">11.7.2014</td>
	<td class="hash">36a59d05f1d37f037fce61638c278a6d</td>
</tr>
</tbody>
</table>



#### Older dCache releases, which are no longer supported, are available from this link.
    
  	
