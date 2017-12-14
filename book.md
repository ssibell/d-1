---
layout: pages
title: Books
permalink: /book/
---

[release notes](/manuals/releasenotes.shtml) | Book: [1.9.5](/manuals/Book-1.9.5), 1.9.12 ([opt](/manuals/Book-1.9.12), [FHS](/manuals/Book-1.9.12/index-fhs.shtml)), <span class="activ">2.7</span> <span class="activ">(FHS)</span>, 2.8 ([FHS](/manuals/Book-2.8/index-fhs.shtml)), 2.9 ([FHS](/manuals/Book-2.9/index-fhs.shtml)), 2.10 ([FHS](/manuals/Book-2.10/index-fhs.shtml)), 2.11 ([FHS](/manuals/Book-2.11/index-fhs.shtml)), 2.12 ([FHS](/manuals/Book-2.12/index-fhs.shtml)), 2.13 ([FHS](/manuals/Book-2.13/index-fhs.shtml)), | [Wiki](http://trac.dcache.org/trac.cgi/wiki) | [Q&A](/manuals/FAQ.shtml) ![black_bg](/images/black_bg.png)

[Multi-page](/manuals/Book-2.7/index-fhs.shtml), [Single page](/manuals/Book-2.7/Book-fhs.shtml) | PDF: [A4-size](/manuals/Book-2.7/Book-fhs-a4.pdf), [Letter-size](/manuals/Book-2.7/Book-fhs-letter.pdf) | eBook: [epub](/manuals/Book-2.7/Book-fhs.epub) ![black_bg](/images/black_bg.png)


# The dCache Book



## for 2.7-series (FHS layout)


**Abstract**

The dCache Book is the guide for administrators of dCache systems. The first part describes the installation of a simple single-host <span class="productname">dCache</span> instance. The second part describes the components of <span class="productname">dCache</span> and in what ways they can be configured. This is the place for finding information about the role and functionality of components in <span class="productname">dCache</span> as needed by an administrator. The third part contains solutions for several problems and tasks which might occur during operating of a <span class="productname">dCache</span> system. Finally, the last two parts contain a glossary and a parameter and command reference.

</div>

</div>

</div>

* * *

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="preface">[Preface](#idp99776)</span></dt>

<dt><span class="part">[I. Getting started](#start)</span></dt>

<dd>

<dl>

<dt><span class="chapter">[1\. Introduction](#intro)</span></dt>

<dt><span class="chapter">[2\. Installing <span class="productname">dCache</span>](#in)</span></dt>

<dt><span class="chapter">[3\. Getting in Touch with <span class="productname">dCache</span>](#intouch)</span></dt>

</dl>

</dd>

<dt><span class="part">[II. Configuration of <span class="productname">dCache</span>](#cf)</span></dt>

<dd>

<dl>

<dt><span class="chapter">[4\. <span class="productname">Chimera</span>](#cf-chimera)</span></dt>

<dt><span class="chapter">[5\. The Cell Package](#cf-cellpackage)</span></dt>

<dt><span class="chapter">[6\. The `replica` Service (Replica Manager)](#cf-repman)</span></dt>

<dt><span class="chapter">[7\. The `poolmanager` Service](#cf-pm)</span></dt>

<dt><span class="chapter">[8\. The <span class="productname">dCache</span> Tertiary Storage System Interface](#cf-tss)</span></dt>

<dt><span class="chapter">[9\. File Hopping](#cf-hopping)</span></dt>

<dt><span class="chapter">[10\. Authorization in <span class="productname">dCache</span>](#cf-gplazma)</span></dt>

<dt><span class="chapter">[11\. dCache as xRootd-Server](#cf-xrootd)</span></dt>

<dt><span class="chapter">[12\. <span class="productname">dCache</span> as `NFSv4.1` Server](#cf-nfs4)</span></dt>

<dt><span class="chapter">[13\. <span class="productname">dCache</span> Storage Resource Manager](#cf-srm)</span></dt>

<dt><span class="chapter">[14\. The `statistics` Service](#cf-statistics)</span></dt>

<dt><span class="chapter">[15\. The `billing` Service](#cf-billing)</span></dt>

<dt><span class="chapter">[16\. The `alarms` Service](#cf-alarms)</span></dt>

<dt><span class="chapter">[17\. <span class="productname">dCache</span> Webadmin Interface](#cf-webadmin)</span></dt>

<dt><span class="chapter">[18\. <acronym class="acronym">ACL</acronym>s in <span class="productname">dCache</span>](#cf-acl)</span></dt>

<dt><span class="chapter">[19\. <acronym class="acronym">GLUE</acronym> Info Provider](#cf-glue)</span></dt>

<dt><span class="chapter">[20\. Stage Protection](#cf-stage-protection)</span></dt>

</dl>

</dd>

<dt><span class="part">[III. Cookbook](#cb)</span></dt>

<dd>

<dl>

<dt><span class="chapter">[21\. <span class="productname">dCache</span> Clients.](#cb-clients)</span></dt>

<dt><span class="chapter">[22\. Pool Operations](#cb-pool)</span></dt>

<dt><span class="chapter">[23\. <span class="productname">PostgreSQL</span> and <span class="productname">dCache</span>](#cb-postgres)</span></dt>

<dt><span class="chapter">[24\. Complex Network Configuration](#cb-net)</span></dt>

<dt><span class="chapter">[25\. Advanced Tuning](#cb-tuning)</span></dt>

</dl>

</dd>

<dt><span class="part">[IV. Reference](#rf)</span></dt>

<dd>

<dl>

<dt><span class="chapter">[26\. <span class="productname">dCache</span> Clients](#rf-clients)</span></dt>

<dt><span class="chapter">[27\. <span class="productname">dCache</span> Cell Commands](#rf-cc)</span></dt>

<dt><span class="chapter">[28\. <span class="productname">dCache</span> Default Port Values](#rf-ports)</span></dt>

<dt><span class="chapter">[29\. Glossary](#rf-glossary)</span></dt>

</dl>

</dd>

</dl>

</div>

<div class="list-of-figures">

**List of Figures**

<dl>

<dt>1.1\. [The <span class="productname">dCache</span> Layer Model](#fig-intro-layer-model)</dt>

<dt>6.1\. [Pool State Diagram](#resilient_poolstate)</dt>

</dl>

</div>

<div class="list-of-tables">

**List of Tables**

<dl>

<dt>23.1\. [Protocol Overview](#idp6442256)</dt>

<dt>25.1\. [Property Overview](#idp6674032)</dt>

<dt>25.2\. [Property Overview](#idp6693584)</dt>

<dt>25.3\. [Property Overview](#idp6731776)</dt>

</dl>

</div>

<div class="list-of-examples">

**List of Examples**

<dl>

<dt>18.1\. [<acronym class="acronym">ACL</acronym> allowing specific user to delete files in a directory](#cf-acl-eg-delete)</dt>

<dt>18.2\. [<acronym class="acronym">ACL</acronym> to deny a group](#idp5418400)</dt>

<dt>18.3\. [<acronym class="acronym">ACL</acronym> to allow a user to delete all files and subdirectories](#idp5428016)</dt>

<dt>18.4\. [Obtain <acronym class="acronym">ACL</acronym> information by absolute path](#idp5465040)</dt>

<dt>21.1\. [surveying the space tokens available in a directory.](#idp5981488)</dt>

<dt>21.2\. [Listing the space tokens for a `SRM`:](#idp5985440)</dt>

<dt>21.3\. [Using `srmls -l`:](#idp6022896)</dt>

<dt>21.4\. [Using `srmls -l`:](#idp6028768)</dt>

<dt>21.5\. [Limited directory listing](#idp6039408)</dt>

</dl>

</div>

<div class="preface" title="Preface">

<div class="titlepage">

<div>

<div>

## <a name="idp99776"></a>Preface

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Who should read this book?](#idp136560)</span></dt>

<dt><span class="section">[Minimum System Requirements?](#idp137840)</span></dt>

<dt><span class="section">[What is inside?](#idp142608)</span></dt>

<dt><span class="section">[Looking for help?](#idp151264)</span></dt>

</dl>

</div>

Welcome to the <span class="productname">dCache</span>. <span class="productname">dCache</span> is a distributed storage solution for storing huge amounts of data without a hard limit, used to provide storage in the petabyte range. Therefore it qualifies as the storage system supporting data intensive experiments.

<span class="productname">dCache</span> is a joined effort between the Deutsches Elektronen-Synchrotron (DESY) in Hamburg, Nordic Data Grid Facility (NDGF based in Copenhagen), the Fermi National Accelerator Laboratory near Chicago with significant distributions and support from the University of California, San Diego, INFN, Bari as well as Rutherford Appleton Laboratory, UK and CERN in Geneva.

<span class="productname">dCache</span> can use hierarchical storage management (e.g., hard disk and tape), provides mechanisms to automatically increase performance and balance loads, increase resilience and availability. It also supplies advanced control systems to manage data as well as data flows. Normal filesystem (btrfs, ext4, XFS, ZFS) is used to store data on storage nodes. There are several ways of accessing data stored in <span class="productname">dCache</span>:

<div class="itemizedlist">

*   `NFS` 4.1 (<span class="productname">Chimera</span>)

*   `HTTP` and `WebDAV`

*   `GridFTP` (`GSI-FTP`)

*   xrootd

*   `SRM` (versions 1.1 and 2.2)

*   `dCap` and `GSIdCap`

</div>

<span class="productname">dCache</span> supports certificate based authentication through the Grid Security Infrastructure used in `GSI-FTP`, `GSIdCap` transfer protocols and the `SRM` management protocol. Certificate authentication is also available for `HTTP` and `WebDAV`. <span class="productname">dCache</span> also supports fine-grain authorization with support for POSIX file permissions and `NFS`-style access control lists. Other features of <span class="productname">dCache</span> are:

<div class="itemizedlist">

*   Resilience and high availability can be implemented in different ways by having multiple replicas of the same files.

*   Easy migration of data via the migration module.

*   A powerful cost calculation system that allows to control the data flow (reading and writing from/to pools, between pools and also between pools and tape).

*   Load balancing and performance tuning by hot pool replication (via cost calculation and replicas created by pool-to-pool-transfers).

*   Space management and support for space tokens.

*   Garbage collection of replicas, depending on their flags, age, et cetera.

*   Detailed logging and debugging as well as accounting and statistics.

*   <abbr class="abbrev">XML</abbr> information provider with detailed live information about the cluster.

*   Scriptable adminstration interface with a terminal-based front-end.

*   Web-interface with live information of the most important information.

*   Ensuring data integrity through checksumming.

</div>

<span class="productname">dCache</span> / `SRM` can transparently manage data distributed among dozens of disk storage nodes (sometimes distributed over several countries). The system has shown to significantly improve the efficiency of connected tape storage systems, by caching, gather and flush and scheduled staging techniques. Furthermore, it optimizes the throughput to and from data clients by dynamically replicating datasets on the detection of load hot spots. The system is tolerant against failures of its data servers, which allows administrators to deploy commodity disk storage components.

Access to the data is provided by various standard protocols. Furthermore the software comes with an implementation of the Storage Resource Manager protocol (`SRM`), which is an open standard for grid middleware to communicate with site specific storage fabrics.

<div class="section" title="Who should read this book?">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="idp136560"></a>Who should read this book?

</div>

</div>

</div>

This book is primerally targeted at system administrators.

</div>

<div class="section" title="Minimum System Requirements?">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="idp137840"></a>Minimum System Requirements?

</div>

</div>

</div>

For minimal test installation:

<div class="itemizedlist">

*   Hardware: contemporary CPU , 1 GiB of RAM , 100 MiB free harddisk space

*   Software: Oracle/Sun Java, Postgres SQL Server

</div>

For a high performance Grid scenario the hardware requirements highly differ, which makes it impossible to provide such parameters here. However, if you wish to setup a <span class="productname">dCache</span>-based storage system, just let us know and we will help you with your system specifications. Just contact us: `<[support@dcache.org](mailto:support@dcache.org)>`.

</div>

<div class="section" title="What is inside?">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="idp142608"></a>What is inside?

</div>

</div>

</div>

This book shall introduce you to <span class="productname">dCache</span> and provide you with the details of the installation. It describes configuration, customization of <span class="productname">dCache</span> as well as the usage of several protocols that <span class="productname">dCache</span> supports. Additionally, it provides cookbooks for standard tasks.

Here is an overview part by part:

Part 1, Getting started: This part introduces you to the cells and domain concept in <span class="productname">dCache</span>. It provides a detailed description of installing, the basic configuration, and upgrading <span class="productname">dCache</span>.

Part 2, Configuration of dCache: Within this part the configuration of several additional features of <span class="productname">dCache</span> is described. They are not necessary to run <span class="productname">dCache</span> but will be needed by some users depending on their requirements.

Part 3, Cookbook: This part comprises guides for specific tasks a system administrator might want to perform.

</div>

<div class="section" title="Looking for help?">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="idp151264"></a>Looking for help?

</div>

</div>

</div>

This part gets you all the help that you might need:

<div class="itemizedlist">

*   For acquiring resources:

    <div class="itemizedlist">

    *   The [download page](http://www.dcache.org/downloads).

    *   The [YUM repositories](http://trac.dcache.org/projects/dcache/wiki/manuals/Yum).

    </div>

*   For getting help during installation:

    <div class="itemizedlist">

    *   Developers `<[support@dcache.org](mailto:support@dcache.org)>`

    *   Additional Support:

        <div class="itemizedlist">

        *   German support:`<[german-support@dcache.org](mailto:german-support@dcache.org)>`

        *   UK support:`<[GRIDPP-STORAGE@JISCMAIL.AC.UK](mailto:GRIDPP-STORAGE@JISCMAIL.AC.UK)>`

        *   USA support:`<[osg-storage@opensciencegrid.org](mailto:osg-storage@opensciencegrid.org)>`

        *   User Forum: `<[user-forum@dcache.org](mailto:user-forum@dcache.org)>`

        </div>

    </div>

*   For features that you would like to see in <span class="productname">dCache</span> or bugs that should be fixed: Just write an e-mail to `<[support@dcache.org](mailto:support@dcache.org)>`

*   If you like to stay up-to-date about new releases you can use the RSS feeds available from [our downloads page](http://www.dcache.org/downloads).

*   For EMI releases of <span class="productname">dCache</span> please visit the [EMI <span class="productname">dCache</span> download page](http://www.eu-emi.eu/releases).

</div>

</div>

</div>

<div class="part" title="Part I. Getting started">

<div class="titlepage">

<div>

<div>

# <a name="start"></a>Part I. Getting started

</div>

</div>

</div>

<div class="partintro" title="Getting started">

This part is intended for people who are new to <span class="productname">dCache</span>. It gives an introduction to <span class="productname">dCache</span>, including how to configure a simple setup, and details some simple and routine administrative operations.

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="chapter">[1\. Introduction](#intro)</span></dt>

<dd>

<dl>

<dt><span class="section">[Cells and Domains](#intro-cells-domains)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[2\. Installing <span class="productname">dCache</span>](#in)</span></dt>

<dd>

<dl>

<dt><span class="section">[Installing a <span class="productname">dCache</span> instance](#in-install)</span></dt>

<dd>

<dl>

<dt><span class="section">[Prerequisites](#in-install-prerequisites)</span></dt>

<dt><span class="section">[Installation of the <span class="productname">dCache</span> Software](#in-install-installation)</span></dt>

<dt><span class="section">[Readying the <span class="productname">PostgreSQL</span> server for the use with <span class="productname">dCache</span>](#in-install-postgres)</span></dt>

<dt><span class="section">[Configuring <span class="productname">Chimera</span>](#in-install-chimera)</span></dt>

<dt><span class="section">[Configuring <span class="productname">dCache</span>](#in-install-configure)</span></dt>

<dt><span class="section">[Installing <span class="productname">dCache</span> on several nodes](#in-install-multinode)</span></dt>

</dl>

</dd>

<dt><span class="section">[Upgrading a <span class="productname">dCache</span> Instance](#in-upgrade)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[3\. Getting in Touch with <span class="productname">dCache</span>](#intouch)</span></dt>

<dd>

<dl>

<dt><span class="section">[Checking the Functionality](#intouch-client)</span></dt>

<dd>

<dl>

<dt><span class="section">[<span class="productname">dCache</span> without mounted namespace](#dcache-unmounted)</span></dt>

<dt><span class="section">[`WebDAV`](#intouch-client-webdav)</span></dt>

<dt><span class="section">[`dCap`](#intouch-client-dcap)</span></dt>

</dl>

</dd>

<dt><span class="section">[The Web Interface for Monitoring <span class="productname">dCache</span>](#intouch-web)</span></dt>

<dt><span class="section">[The Admin Interface](#intouch-admin)</span></dt>

<dd>

<dl>

<dt><span class="section">[First steps](#intouch-admin-first-steps)</span></dt>

<dt><span class="section">[Access with `ssh2`](#intouch-admin-ssh2)</span></dt>

<dt><span class="section">[Access with `ssh1`](#intouch-admin-ssh1)</span></dt>

<dt><span class="section">[How to use the Admin Interface](#idp693968)</span></dt>

<dt><span class="section">[Create a new user](#intouch-admin-new-user)</span></dt>

<dt><span class="section">[Use of the `ssh` Admin Interface by scripts](#idp838000)</span></dt>

</dl>

</dd>

<dt><span class="section">[Authentication and Authorization in <span class="productname">dCache</span>](#intouch-certificates)</span></dt>

<dt><span class="section">[How to work with secured <span class="productname">dCache</span>](#intouch-sec-dcache)</span></dt>

<dd>

<dl>

<dt><span class="section">[`GSIdCap`](#intouch-client-gsidcap)</span></dt>

<dt><span class="section">[`SRM`](#intouch-client-srm)</span></dt>

<dt><span class="section">[`WebDAV` with certificates](#intouch-client-https)</span></dt>

</dl>

</dd>

<dt><span class="section">[Files](#intouch-files)</span></dt>

</dl>

</dd>

</dl>

</div>

</div>

<div class="chapter" title="Chapter 1\. Introduction">

<div class="titlepage">

<div>

<div>

## <a name="intro"></a>Chapter 1\. Introduction

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Cells and Domains](#intro-cells-domains)</span></dt>

</dl>

</div>

<span class="productname">dCache</span> is a distributed storage solution. It organises storage across computers so the combined storage can be used without the end-users being aware of where their data is stored. They simply see a large amount of storage.

Because end-users do not need to know on which computer their data is stored, it can be migrated from one computer to another without any interruption of service. As a consequence, (new) servers may be added to or taken away from the <span class="productname">dCache</span> storage cluster at any time.

<span class="productname">dCache</span> supports requesting data from a tertiary storage system. Such systems typically store data on magnetic tapes instead of disks, which must be loaded and unloaded using a tape robot. The main reason for using tertiary storage is the better cost-efficiency, archiving a very large amount of data on rather inexpensive hardware. In turn the access latency for archived data is significantly higher.

<span class="productname">dCache</span> also supports many transfer protocols (allowing users to read and write to data). These have a modular deployment, allowing <span class="productname">dCache</span> to support expanded capacity by providing additional front-end machines.

Another performance feature of <span class="productname">dCache</span> is hot-spot data migration. In this process, <span class="productname">dCache</span> will detect when files are requested very often. If this happens, <span class="productname">dCache</span> can generate duplicates of the popular files on other computers. This allows the load to be spread across multiple machines, so increasing throughput.

The flow of data within <span class="productname">dCache</span> can also be carefully controlled. This is especially important for large sites as chaotic movement of data may lead to suboptimal usage. Instead, incoming and outgoing data can be marshaled so they use designated resources guaranteeing better throughput and improving end-user experience.

<span class="productname">dCache</span> provides a comprehensive administrative interface for configuring the <span class="productname">dCache</span> instance. This is described in the later sections of this book.

<div class="section" title="Cells and Domains">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="intro-cells-domains"></a>Cells and Domains

</div>

</div>

</div>

<span class="productname">dCache</span>, as distributed storage software, can provide a coherent service using multiple computers or _nodes_ (the two terms are used interchangeable). Although <span class="productname">dCache</span> can provide a complete storage solution on a single computer, one of its strengths is the ability to scale by spreading the work over multiple nodes.

A _cell_ is <span class="productname">dCache</span>’s most fundamental executable building block. Even a small <span class="productname">dCache</span> deployment will have many cells running. Each cell has a specific task to perform and most will interact with other cells to achieve it.

Cells can be grouped into common types; for example, pools, doors. Cells of the same type behave in a similar fashion and have higher-level behaviour (such as storing files, making files available). Later chapters will describe these different cell types and how they interact in more detail.

There are only a few cells where (at most) only a single instance is required. The majority of cells within a <span class="productname">dCache</span> instance can have multiple instances and <span class="productname">dCache</span> is designed to allow load-balancing over these cells.

A _domain_ is a container for running cells. Each domain runs in its own Java Virtual Machine (JVM) instance, which it cannot share with any other domain. In essence, a domain <span class="emphasis">_is_</span> a JVM with the additional functionality necessary to run cells (such as system administration and inter-cell communication). This also implies, that a node’s resources, such as memory, available CPU and network bandwidth, are shared among several domains running on the same node.

<span class="productname">dCache</span> comes with a set of domain definitions, each specifying a useful set of cells to run within that domain to achieve a certain goal. These goals include storing data, providing a front-end to the storage, recording file names, and so on. The list of cells to run within these domains are recommended deployments: the vast majority of <span class="productname">dCache</span> deployments do not need to alter these lists.

A node is free to run multiple domains, provided there’s no conflicting requirement from the domains for exclusive access to hardware. A node may run a single domain; but, typically a node will run multiple domains. The choice of which domains to run on which nodes will depend on expected load of the <span class="productname">dCache</span> instance and on the available hardware. If this sounds daunting, don’t worry: starting and stopping a domain is easy and migrating a domain from one node to another is often as easy as stopping the domain on one node and starting it on another.

<span class="productname">dCache</span> is scalable storage software. This means that (in most cases) the performance of <span class="productname">dCache</span> can be improved by introducing new hardware. Depending on the performance issue, the new hardware may be used by hosting a domain migrated from a overloaded node, or by running an additional instance of a domain to allow load-balancing.

Most cells communicate in such a way that they don’t rely on in which domain they are running. This allows a site to move cells from one domain to another or to create new domain definitions with some subset of available cells. Although this is possible, it is rare that redefining domains or defining new domains is necessary. Starting or stopping domains is usually sufficient for managing load.

</div>

<div class="figure"><a name="fig-intro-layer-model"></a>

**Figure 1.1\. The <span class="productname">dCache</span> Layer Model**

<div class="figure-contents">

<div class="mediaobject" align="center">![The dCache Layer Model](/images/test.png)</div>

</div>

</div>

The layer model shown in [Figure 1.1, “The <span class="productname">dCache</span> Layer Model”](#fig-intro-layer-model "Figure 1.1\. The dCache Layer Model") gives an overview of the architecture of the <span class="productname">dCache</span> system.

</div>

<div class="chapter" title="Chapter 2\. Installing dCache">

<div class="titlepage">

<div>

<div>

## <a name="in"></a>Chapter 2\. Installing <span class="productname">dCache</span>

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Installing a <span class="productname">dCache</span> instance](#in-install)</span></dt>

<dd>

<dl>

<dt><span class="section">[Prerequisites](#in-install-prerequisites)</span></dt>

<dt><span class="section">[Installation of the <span class="productname">dCache</span> Software](#in-install-installation)</span></dt>

<dt><span class="section">[Readying the <span class="productname">PostgreSQL</span> server for the use with <span class="productname">dCache</span>](#in-install-postgres)</span></dt>

<dt><span class="section">[Configuring <span class="productname">Chimera</span>](#in-install-chimera)</span></dt>

<dt><span class="section">[Configuring <span class="productname">dCache</span>](#in-install-configure)</span></dt>

<dt><span class="section">[Installing <span class="productname">dCache</span> on several nodes](#in-install-multinode)</span></dt>

</dl>

</dd>

<dt><span class="section">[Upgrading a <span class="productname">dCache</span> Instance](#in-upgrade)</span></dt>

</dl>

</div>

The first section describes the installation of a fresh <span class="productname">dCache</span> instance using RPM files downloaded from [the <span class="productname">dCache</span> home-page](http://www.dcache.org). It is followed by a guide to upgrading an existing installation. In both cases we assume standard requirements of a small to medium sized <span class="productname">dCache</span> instance without an attached [_tertiary storage system_](#gl-tss). The third section contains some pointers on extended features.

<div class="section" title="Installing a dCache instance">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="in-install"></a>Installing a <span class="productname">dCache</span> instance

</div>

</div>

</div>

In the following the installation of a <span class="productname">dCache</span> instance will be described. The <span class="productname">Chimera</span> name space provider, some management components, and the `SRM` need a <span class="productname">PostgreSQL</span> server installed. We recommend running this <span class="productname">PostgreSQL</span> on the local node. The first section describes the configuration of a <span class="productname">PostgreSQL</span> server. After that the installation of <span class="productname">Chimera</span> and of the <span class="productname">dCache</span> components will follow. During the whole installation process root access is required.

<div class="section" title="Prerequisites">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="in-install-prerequisites"></a>Prerequisites

</div>

</div>

</div>

In order to install <span class="productname">dCache</span> the following requirements must be met:

<div class="itemizedlist">

*   An RPM-based Linux distribution is required for the following procedure. For Debian derived systems we provide Debian packages and for Solaris the Solaris packages or the tarball.

*   <span class="productname">dCache</span> requires Java 1.7 JRE. Please use the latest patch-level and check for upgrades frequently. It is recommended to use JDK as <span class="productname">dCache</span> scripts can make use of some extra features that JDK provides to gather more diagnostic information (heap-dump, etc). This helps when tracking down bugs.

*   <span class="productname">PostgreSQL</span> must be installed and running. We recommend the use of <span class="productname">PostgreSQL</span> version 9.2 (at least <span class="productname">PostgreSQL</span> version 8.3 is required).

    <div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

    ### Important

    For good performance it is necessary to maintain and tune your <span class="productname">PostgreSQL</span> server. There are several good books on this topic, one of which is [_PostgreSQL 9.0 High Performance_](http://www.2ndquadrant.com/books/postgresql-9-0-high-performance).

    </div>

</div>

</div>

<div class="section" title="Installation of the dCache Software">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="in-install-installation"></a>Installation of the <span class="productname">dCache</span> Software

</div>

</div>

</div>

The RPM packages may be installed right away, for example using the command:

    [root] #

The actual sources lie at [http://www.dcache.org/downloads/IAgree.shtml](http://www.dcache.org/downloads/IAgree.shtml). To install for example Version 2.7.0-1 you would use this:

    [root] #

The client can be found in the download-section of the above url, too.

</div>

<div class="section" title="Readying the PostgreSQL server for the use with dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="in-install-postgres"></a>Readying the <span class="productname">PostgreSQL</span> server for the use with <span class="productname">dCache</span>

</div>

</div>

</div>

Using a <span class="productname">PostgreSQL</span> server with <span class="productname">dCache</span> places a number of requirements on the database. You must configure <span class="productname">PostgreSQL</span> for use by <span class="productname">dCache</span> and create the necessary <span class="productname">PostgreSQL</span> user accounts and database structure. This section describes how to do this.

<div class="section" title="Starting PostgreSQL">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="in-install-postgres-start"></a>Starting <span class="productname">PostgreSQL</span>

</div>

</div>

</div>

Install the <span class="productname">PostgreSQL</span> server with the tools of the operating system.

Initialize the database directory (for <span class="productname">PostgreSQL</span> version 9.2 this is `/var/lib/pgsql/9.2/data/`) , start the database server, and make sure that it is started at system start-up.

    [root] #

</div>

<div class="section" title="Enabling local trust">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="in-install-postgres-trust"></a>Enabling local trust

</div>

</div>

</div>

Perhaps the simplest configuration is to allow password-less access to the database and the following documentation assumes this is so.

To allow local users to access <span class="productname">PostgreSQL</span> without requiring a password, ensure the file `pg_hba.conf`, which (for <span class="productname">PostgreSQL</span> version 9.2) is located in `/var/lib/pgsql/9.2/data`, contains the following lines.

<pre class="programlisting"># TYPE  DATABASE        USER            ADDRESS                 METHOD

# "local" is for Unix domain socket connections only
local   all             all                                     trust
# IPv4 local connections:
host    all             all             127.0.0.1/32            trust
# IPv6 local connections:
host    all             all             ::1/128                 trust</pre>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Please note it is also possible to run <span class="productname">dCache</span> with all <span class="productname">PostgreSQL</span> accounts requiring passwords. See [the section called “Configuring Access to <span class="productname">PostgreSQL</span>”](#cb-postgres-configure "Configuring Access to PostgreSQL") for more advice on the configuration of <span class="productname">PostgreSQL</span>.

</div>

<div class="important" title="Restarting PostgreSQL" style="margin-left: 0.5in; margin-right: 0.5in;">

### Restarting <span class="productname">PostgreSQL</span>

If you have edited <span class="productname">PostgreSQL</span> configuration files, you <span class="emphasis">_must_</span> restart <span class="productname">PostgreSQL</span> for those changes to take effect. On many systems, this can be done with the following command:

    [root] #

</div>

</div>

</div>

<div class="section" title="Configuring Chimera">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="in-install-chimera"></a>Configuring <span class="productname">Chimera</span>

</div>

</div>

</div>

<span class="productname">Chimera</span> is a library providing a hierarchical name space with associated meta data. Where pools in <span class="productname">dCache</span> store the content of files, <span class="productname">Chimera</span> stores the names and meta data of those files. <span class="productname">Chimera</span> itself stores the data in a relational database. We will use <span class="productname">PostgreSQL</span> in this tutorial. The properties of <span class="productname">Chimera</span> are defined in `<span>/usr/share/dcache</span>/defaults/chimera.properties`. See [Chapter 4, _<span class="productname">Chimera</span>_](#cf-chimera "Chapter 4\. Chimera") for more information.

<div class="section" title="Creating users and databases for dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="in-install-chimera-initDB"></a>Creating users and databases for <span class="productname">dCache</span>

</div>

</div>

</div>

Create the <span class="database">Chimera</span> database and user.

    [root] #

The <span class="productname">dCache</span> components will access the database server with the user <span class="database">srmdcache</span>.

    [root] #

Several management components running on the head node as well as the `SRM` will use the database <span class="database">dcache</span> for storing their state information:

    [root] #

There might be several of these on several hosts. Each is used by the <span class="productname">dCache</span> components running on the respective host.

Create the database used for the billing plots.

    [root] #

And run the command <span class="command">**dcache database update**</span>.

    [root] #

Now the configuration of <span class="productname">Chimera</span> is done.

</div>

Before the first start of <span class="productname">dCache</span> replace the file `<span>/etc/dcache</span>/gplazma.conf` with an empty file.

    [root] #

<span class="productname">dCache</span> can be started now.

    [root] #

So far, no configuration of <span class="productname">dCache</span> is done, so only the predefined domain is started.

</div>

<div class="section" title="Configuring dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="in-install-configure"></a>Configuring <span class="productname">dCache</span>

</div>

</div>

</div>

<div class="section" title="Terminology">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="in-install-configure-terminology"></a>Terminology

</div>

</div>

</div>

<span class="productname">dCache</span> consists of one or more _domains_. A domain in <span class="productname">dCache</span> is a Java Virtual Machine hosting one or more <span class="productname">dCache</span> _cells_. Each domain must have a name which is unique throughout the <span class="productname">dCache</span> instance and a cell must have a unique name within the domain hosting the cell.

A _service_ is an abstraction used in the <span class="productname">dCache</span> configuration to describe atomic units to add to a domain. It is typically implemented through one or more cells. <span class="productname">dCache</span> keeps lists of the domains and the services that are to be run within these domains in the _layout files_. The layout file may contain domain- and service- specific configuration values. A _pool_ is a cell providing physical data storage services.

</div>

<div class="section" title="Configuration files">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="in-install-configure-files"></a>Configuration files

</div>

</div>

</div>

In the setup of <span class="productname">dCache</span>, there are three main places for configuration files:

<div class="itemizedlist">

*   `<span>/usr/share/dcache</span>/defaults`
*   `<span>/etc/dcache</span>/dcache.conf`
*   `<span>/etc/dcache</span>/layouts`

</div>

The folder `<span>/usr/share/dcache</span>/defaults` contains the default settings of the <span class="productname">dCache</span>. If one of the default configuration values needs to be changed, copy the default setting of this value from one of the files in `<span>/usr/share/dcache</span>/defaults` to the file `<span>/etc/dcache</span>/dcache.conf`, which initially is empty and update the value.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

In this first installation of <span class="productname">dCache</span> your <span class="productname">dCache</span> will not be connected to a tape sytem. Therefore please change the values for `pnfsmanager.default-retention-policy` and `pnfsmanager.default-access-latency` in the file `<span>/etc/dcache</span>/dcache.conf`.

<pre class="programlisting">pnfsmanager.default-retention-policy=REPLICA
pnfsmanager.default-access-latency=ONLINE</pre>

</div>

Layouts describe which domains to run on a host and which services to run in each domain. For the customized configuration of your <span class="productname">dCache</span> you will have to create a layout file in `<span>/etc/dcache</span>/layouts`. In this tutorial we will call it the `mylayout.conf` file.

</div>

<div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

### Important

Do not update configuration values in the files in the defaults folder, since changes to these files will be overwritten by updates.

</div>

As the files in `<span>/usr/share/dcache</span>/defaults/` do serve as succinct documentation for all available configuration parameters and their default values it is quite useful to have a look at them.

<div class="section" title="Defining domains and services">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="in-install-layout"></a>Defining domains and services

</div>

</div>

</div>

Domains and services are defined in the layout files. Depending on your site, you may have requirements upon the doors that you want to configure and domains within which you want to organise them.

A domain must be defined if services are to run in that domain. Services will be started in the order in which they are defined.

Every domain is a Java Virtual Machine that can be started and stopped separately. You might want to define several domains for the different services depending on the necessity of restarting the services separately.

The layout files define which domains to start and which services to put in which domain. Configuration can be done per domain and per service.

A name in square brackets, <span class="emphasis">_without_</span> a forward-slash (`/`) defines a domain. A name in square brackets <span class="emphasis">_with_</span> a forward slash defines a service that is to run in a domain. Lines starting with a hash-symbol (`#`) are comments and will be ignored by <span class="productname">dCache</span>.

There may be several layout files in the layout directory, but only one of them is read by <span class="productname">dCache</span> when starting up. By default it is the `single.conf`. If the <span class="productname">dCache</span> should be started with another layout file you will have to make this configuration in `<span>/etc/dcache</span>/dcache.conf`.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">dcache.layout=mylayout</pre>

This entry in `<span>/etc/dcache</span>/dcache.conf` will instruct <span class="productname">dCache</span> to read the layout file `<span>/etc/dcache</span>/layouts/mylayout.conf` when starting up.</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

These are the first lines of `<span>/etc/dcache</span>/layouts/single.conf`:

<pre class="programlisting">dcache.broker.scheme=none

[dCacheDomain]
[dCacheDomain/admin]
[dCacheDomain/broadcast]
[dCacheDomain/poolmanager]</pre>

`[`dCacheDomain`]` defines a domain called `dCacheDomain`. In this example only one domain is defined. All the services are running in that domain. Therefore no messagebroker is needed, which is the meaning of the entry `messageBroker=none`.

`[`dCacheDomain`/`admin`]` declares that the `admin` service is to be run in the `dCacheDomain` domain.

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

This is an example for the `mylayout.conf` file of a single node <span class="productname">dCache</span> with several domains.

<pre class="programlisting">[dCacheDomain]
[dCacheDomain/broadcast]
[dCacheDomain/loginbroker]
[dCacheDomain/topo]
[dCacheDomain/info]

[namespaceDomain]
[namespaceDomain/pnfsmanager]
[namespaceDomain/cleaner]
[namespaceDomain/dir]

[poolmanagerDomain]
[poolmanagerDomain/poolmanager]

[adminDoorDomain]
[adminDoorDomain/admin]

[httpdDomain]
[httpdDomain/httpd]
[httpdDomain/billing]
[httpdDomain/srm-loginbroker]

[gPlazmaDomain]
[gPlazmaDomain/gplazma]</pre>

</div>

</div>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

If you defined more than one domain, a messagebroker is needed, because the defined domains need to be able to communicate with each other. This means that if you use the file `single.conf` as a template for a <span class="productname">dCache</span> with more than one domain you need to delete the line `messageBroker=none`. Then the default value will be used which is `messageBroker=cells`, as defined in the defaults `<span>/usr/share/dcache</span>/defaults/dcache.properties`.

</div>

</div>

<div class="section" title="Creating and configuring pools">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="in-install-configure-pools"></a>Creating and configuring pools

</div>

</div>

</div>

<span class="productname">dCache</span> will need to write the files it keeps in pools. These pools are defined as services within <span class="productname">dCache</span>. Hence, they are added to the layout file of your <span class="productname">dCache</span> instance, like all other services.

The best way to create a pool, is to use the `dcache` script and restart the domain the pool runs in. The pool will be added to your layout file.

<pre class="programlisting">[_<tt><domainname></tt>_/pool]
name=_<tt><poolname></tt>_
path=/path/to/pool
pool.wait-for-files=${path}/data</pre>

The property `pool.wait-for-files` instructs the pool not to start up until the specified file or directory is available. This prevents problems should the underlying storage be unavailable (e.g., if a RAID device is offline).

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Please restart <span class="productname">dCache</span> if your pool is created in a domain that did not exist before.

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [root] #

In this example we create a pool called pool1 in the directory `/srv/dcache/p1`. The created pool will be running in the domain `poolDomain`.

</div>

</div>

<div class="note" title="Mind the Gap!" style="margin-left: 0.5in; margin-right: 0.5in;">

### Mind the Gap!

The default gap for poolsizes is 4GiB. This means you should make a bigger pool than 4GiB otherwise you would have to change this gap in the <span class="productname">dCache</span> admin tool. See the example below. See also [the section called “The Admin Interface”](#intouch-admin "The Admin Interface").

    (local) admin >

</div>

Adding a pool to a configuration does not modify the pool or the data in it and can thus safely be undone or repeated.

</div>

<div class="section" title="Starting dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="in-install-configure-starting"></a>Starting <span class="productname">dCache</span>

</div>

</div>

</div>

Restart <span class="productname">dCache</span> to start the newly configured components **`dcache restart`** and check the status of <span class="productname">dCache</span> with **`dcache status`**.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [root] #

</div>

</div>

</div>

Now you can have a look at your <span class="productname">dCache</span> via The Web Interface, see [the section called “The Web Interface for Monitoring <span class="productname">dCache</span>”](#intouch-web "The Web Interface for Monitoring dCache"): `http://_<tt><httpd.example.org></tt>_:2288/`, where _<tt><httpd.example.org></tt>_ is the node on which your `httpd` service is running. For a single node <span class="productname">dCache</span> this is the machine on which your <span class="productname">dCache</span> is running.

<div class="section" title="Java heap size">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="in-install-configure-java"></a><span class="productname">Java</span> heap size

</div>

</div>

</div>

By default the <span class="productname">Java</span> heap size and the maximum direct buffer size are defined as

<pre class="programlisting">dcache.java.memory.heap=512m
dcache.java.memory.direct=512m</pre>

Again, these values can be changed in `<span>/etc/dcache</span>/dcache.conf`.

For optimization of your <span class="productname">dCache</span> you can define the <span class="productname">Java</span> heap size in the layout file separately for every domain.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">[dCacheDomain]
dcache.java.memory.heap=2048m
dcache.java.memory.direct=0m
...
[utilityDomain]
dcache.java.memory.heap=384m
dcache.java.memory.direct=16m</pre>

</div>

</div>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

<span class="productname">dCache</span> uses <span class="productname">Java</span> to parse the configuration files and will search for <span class="productname">Java</span> on the system path first; if it is found there, no further action is needed. If <span class="productname">Java</span> is not on the system path, the environment variable `JAVA_HOME` defines the location of the <span class="productname">Java</span> installation directory. Alternatively, the environment variable `JAVA` can be used to point to the <span class="productname">Java</span> executable directly.

If `JAVA_HOME` or `JAVA` cannot be defined as global environment variables in the operating system, then they can be defined in either `/etc/default/dcache` or `/etc/dcache.env`. These two files are sourced by the init script and allow `JAVA_HOME`, `JAVA` and `DCACHE_HOME` to be defined.

</div>

</div>

</div>

<div class="section" title="Installing dCache on several nodes">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="in-install-multinode"></a>Installing <span class="productname">dCache</span> on several nodes

</div>

</div>

</div>

Installing <span class="productname">dCache</span> on several nodes is not much more complicated than installing it on a single node. Think about how <span class="productname">dCache</span> should be organised regarding services and domains. Then adapt the layout files, as described in [the section called “Defining domains and services”](#in-install-layout "Defining domains and services"), to the layout that you have in mind. The files `<span>/etc/dcache</span>/layouts/head.conf` and `<span>/etc/dcache</span>/layouts/pool.conf` contain examples for a <span class="productname">dCache</span> head-node and a <span class="productname">dCache</span> pool respectively.

<div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

### Important

You must configure a domain called `dCacheDomain` but the other domain names can be chosen freely.

Please make sure that the domain names that you choose are unique. Having the same domain names in different layout files on different nodes may result in an error.

</div>

On any other nodes than the head node, the property `dcache.broker.host` has to be added to the file `<span>/etc/dcache</span>/dcache.conf`. This property should point to the host containing the special domain `dCacheDomain`, because that domain acts implicitly as a broker.

<div class="tip" title="Tip" style="margin-left: 0.5in; margin-right: 0.5in;">

### Tip

On <span class="productname">dCache</span> nodes running only pool services you do not need to install <span class="productname">PostgreSQL</span>. If your current node hosts only these services, the installation of <span class="productname">PostgreSQL</span> can be skipped.

</div>

</div>

</div>

<div class="section" title="Upgrading a dCache Instance">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="in-upgrade"></a>Upgrading a <span class="productname">dCache</span> Instance

</div>

</div>

</div>

<div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

### Important

Always read the release notes carefully before upgrading!

</div>

Upgrading to bugfix releases within one supported branch (e.g. from 2.7.0 to 2.7.1) may be done by upgrading the packages with

    [root] #

Now <span class="productname">dCache</span> needs to be started again.

For major upgrades please

<div class="itemizedlist">

*   use [The Ultimate Golden Release Upgrade Guide I](http://www.dcache.org/manuals/2011/goettingen/upgradeguide/upgrade-guide.html) to upgrade from 1.9.5 to 1.9.12.
*   use the [The Ultimate Golden Release Upgrade Guide II](http://www.dcache.org/manuals/upgrade-1.9.12-to-2.2.shtml) to upgrade from 1.9.12 to 2.2.
*   use the [The Ultimate Golden Release Upgrade Guide III](http://www.dcache.org/manuals/upgrade/upgrade-2.2-to-2.6.html) to upgrade from 2.2 to 2.6\.
*   use the [/opt to /usr](http://trac.dcache.org/wiki/optToUsr) migration guide to migrate from the /opt layout to the fhs-compliant layout.

</div>

</div>

</div>

<div class="chapter" title="Chapter 3\. Getting in Touch with dCache">

<div class="titlepage">

<div>

<div>

## <a name="intouch"></a>Chapter 3\. Getting in Touch with <span class="productname">dCache</span>

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Checking the Functionality](#intouch-client)</span></dt>

<dd>

<dl>

<dt><span class="section">[<span class="productname">dCache</span> without mounted namespace](#dcache-unmounted)</span></dt>

<dt><span class="section">[`WebDAV`](#intouch-client-webdav)</span></dt>

<dt><span class="section">[`dCap`](#intouch-client-dcap)</span></dt>

</dl>

</dd>

<dt><span class="section">[The Web Interface for Monitoring <span class="productname">dCache</span>](#intouch-web)</span></dt>

<dt><span class="section">[The Admin Interface](#intouch-admin)</span></dt>

<dd>

<dl>

<dt><span class="section">[First steps](#intouch-admin-first-steps)</span></dt>

<dt><span class="section">[Access with `ssh2`](#intouch-admin-ssh2)</span></dt>

<dt><span class="section">[Access with `ssh1`](#intouch-admin-ssh1)</span></dt>

<dt><span class="section">[How to use the Admin Interface](#idp693968)</span></dt>

<dt><span class="section">[Create a new user](#intouch-admin-new-user)</span></dt>

<dt><span class="section">[Use of the `ssh` Admin Interface by scripts](#idp838000)</span></dt>

</dl>

</dd>

<dt><span class="section">[Authentication and Authorization in <span class="productname">dCache</span>](#intouch-certificates)</span></dt>

<dt><span class="section">[How to work with secured <span class="productname">dCache</span>](#intouch-sec-dcache)</span></dt>

<dd>

<dl>

<dt><span class="section">[`GSIdCap`](#intouch-client-gsidcap)</span></dt>

<dt><span class="section">[`SRM`](#intouch-client-srm)</span></dt>

<dt><span class="section">[`WebDAV` with certificates](#intouch-client-https)</span></dt>

</dl>

</dd>

<dt><span class="section">[Files](#intouch-files)</span></dt>

</dl>

</div>

This section is a guide for exploring a newly installed <span class="productname">dCache</span> system. The confidence obtained by this exploration will prove very helpful when encountering problems in the running system. This forms the basis for the more detailed stuff in the later parts of this book. The starting point is a fresh installation according to the [the section called “Installing a <span class="productname">dCache</span> instance”](#in-install "Installing a dCache instance").

<div class="section" title="Checking the Functionality">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="intouch-client"></a>Checking the Functionality

</div>

</div>

</div>

Reading and writing data to and from a <span class="productname">dCache</span> instance can be done with a number of protocols. After a standard installation, these protocols are `dCap`, `GSIdCap`, and `GridFTP`. In addition <span class="productname">dCache</span> comes with an implementation of the `SRM` protocol which negotiates the actual data transfer protocol.

<div class="section" title="dCache without mounted namespace">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="dcache-unmounted"></a><span class="productname">dCache</span> without mounted namespace

</div>

</div>

</div>

Create the root of the <span class="productname">Chimera</span> namespace and a world-writable directory by

    [root] #

</div>

<div class="section" title="WebDAV">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="intouch-client-webdav"></a>`WebDAV`

</div>

</div>

</div>

To use `WebDAV` you need to define a `WebDAV` service in your layout file. You can define this service in an extra domain, e.g. `[webdavDomain]` or add it to another domain.

<pre class="programlisting">[webdavDomain]
[webdavDomain/webdav]
webdav.authz.anonymous-operations=FULL</pre>

to the file `<span>/etc/dcache</span>/layouts/mylayout.conf`.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Depending on the client you might need to set `webdav.redirect.on-read=false` and/or `webdav.redirect.on-write=false`.

<pre class="programlisting">#  ---- Whether to redirect GET requests to a pool
#
#   If true, WebDAV doors will respond with a 302 redirect pointing to
#   a pool holding the file. This requires that a pool can accept
#   incoming TCP connections and that the client follows the
#   redirect. If false, data is relayed through the door. The door
#   will establish a TCP connection to the pool.
#
(one-of?true|false)webdav.redirect.on-read=true

#  ---- Whether to redirect PUT requests to a pool
#
#   If true, WebDAV doors will respond with a 307 redirect pointing to
#   a pool to which to upload the file. This requires that a pool can
#   accept incoming TCP connections and that the client follows the
#   redirect. If false, data is relayed through the door. The door
#   will establish a TCP connection to the pool. Only clients that send
#   a Expect: 100-Continue header will be redirected - other requests
#   will always be proxied through the door.
#
(one-of?true|false)webdav.redirect.on-write=true</pre>

</div>

Now you can start the `WebDAV` domain

    [root] #

and access your files via `http://_<tt><webdav-door.example.org></tt>_:2880` with your browser.

You can connect the webdav server to your file manager and copy a file into your <span class="productname">dCache</span>.

To use `curl` to copy a file into your <span class="productname">dCache</span> you will need to set `webdav.redirect.on-write=false`.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Write the file `test.txt`

    [root] #

and read it

    [root] #

</div>

</div>

</div>

<div class="section" title="dCap">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="intouch-client-dcap"></a>`dCap`

</div>

</div>

</div>

To be able to use `dCap` you need to have the `dCap` door running in a domain.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">[dCacheDomain]
[dCacheDomain/dcap]</pre>

</div>

</div>

For this tutorial install `dCap` on your worker node. This can be the machine where your <span class="productname">dCache</span> is running.

Get the <span class="productname">gLite</span> repository (which contains `dCap`) and install `dCap` using <span class="command">**yum**</span>.

    [root] #

Create the root of the <span class="productname">Chimera</span> namespace and a world-writable directory for `dCap` to write into as described [above](#dcache-unmounted "dCache without mounted namespace").

Copy the data (here `/bin/sh` is used as example data) using the <span class="command">**dccp**</span> command and the `dCap` protocol describing the location of the file using a URL, where _<tt><dcache.example.org></tt>_ is the host on which the <span class="productname">dCache</span> is running

    [root] #

and copy the file back.

    [root] #

To remove the file you will need to mount the namespace.

</div>

</div>

<div class="section" title="The Web Interface for Monitoring dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="intouch-web"></a>The Web Interface for Monitoring <span class="productname">dCache</span>

</div>

</div>

</div>

In the standard configuration the <span class="productname">dCache</span> web interface is started on the head node (meaning that the domain hosting the `httpd` service is running on the head node) and can be reached via port `2288`. Point a web browser to `http://_<tt><head-node.example.org></tt>_:2288/` to get to the main menu of the <span class="productname">dCache</span> web interface. The contents of the web interface are self-explanatory and are the primary source for most monitoring and trouble-shooting tasks.

The <span class="quote">“<span class="quote">Cell Services</span>”</span> page displays the status of some important [_cells_](#gl-cell) of the <span class="productname">dCache</span> instance.

The <span class="quote">“<span class="quote">Pool Usage</span>”</span> page gives a good overview of the current space usage of the whole <span class="productname">dCache</span> instance. In the graphs, free space is marked yellow, space occupied by [_cached files_](#gl-cached) (which may be deleted when space is needed) is marked green, and space occupied by [_precious files_](#gl-precious), which cannot be deleted is marked red. Other states (e.g., files which are currently written) are marked purple.

The page <span class="quote">“<span class="quote">Pool Request Queues</span>”</span> (or <span class="quote">“<span class="quote">Pool Transfer Queues</span>”</span>) gives information about the number of current requests handled by each pool. <span class="quote">“<span class="quote">Actions Log</span>”</span> keeps track of all the transfers performed by the pools up to now.

The remaining pages are only relevant with more advanced configurations: The page <span class="quote">“<span class="quote">Pools</span>”</span> (or <span class="quote">“<span class="quote">Pool Attraction Configuration</span>”</span>) can be used to analyze the current configuration of the [_pool selection unit_](#gl-pm-comp-psu) in the pool manager. The remaining pages are relevant only if a [_tertiary storage system (HSM)_](#gl-tss) is connected to the <span class="productname">dCache</span> instance.

</div>

<div class="section" title="The Admin Interface">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="intouch-admin"></a>The Admin Interface

</div>

</div>

</div>

<div class="important" title="Just use commands that are documented here" style="margin-left: 0.5in; margin-right: 0.5in;">

### Just use commands that are documented here

Only commands described in this documentation should be used for the administration of a <span class="productname">dCache</span> system.

</div>

<div class="section" title="First steps">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="intouch-admin-first-steps"></a>First steps

</div>

</div>

</div>

<span class="productname">dCache</span> has a powerful administration interface. It can be accessed with the `ssh1` or with the `ssh2` protocol. The server is part of the `adminDoor` domain.

It is useful to define the `admin` service in a seperate domain. This allowes to restart the `admin` service seperatly from other services. In the example in [the section called “Installing a <span class="productname">dCache</span> instance”](#in-install "Installing a dCache instance") this domain was called `adminDoorDomain`.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">[adminDoorDomain]
[adminDoorDomain/admin]</pre>

</div>

</div>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

The admin interface is using `ssh2`. It used to be available using `ssh1`, which is insecure and therefore discouraged. If you want to run the admin service with `ssh1` you need to define the `ssh1` service.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">[adminDoorDomain]
[adminDoorDomain/ssh1]</pre>

</div>

</div>

</div>

</div>

<div class="section" title="Access with ssh2">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="intouch-admin-ssh2"></a>Access with `ssh2`

</div>

</div>

</div>

There are two ways of authorizing administrators to access the <span class="productname">dCache</span> `ssh2` admin interface. The preferred method authorizes users through their public key. The second method employs `gPlazma2` and the `dcache.kpwd` file. Thereby authorization mechanisms can be added later by deploying another `gPlazma2` plugin. The configuration of both authorization mechanisms is described in the following.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

All configurable values of the `ssh2` admin interface can be found in the `<span>/usr/share/dcache</span>/defaults/admin.properties` file. Please do NOT change any value in this file. Instead enter the key value combination in the `<span>/etc/dcache</span>/dcache.conf`.

</div>

<div class="section" title="Public Key Authorization">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp627632"></a>Public Key Authorization

</div>

</div>

</div>

To authorize administrators through their public key just insert it into the file `authorized_keys2` which should by default be in the directory `<span>/etc/dcache/admin</span>` as specified in the file `<span>/usr/share/dcache</span>/defaults/admin.properties` under `admin.paths.authorized-keys=`. Keys have to be in one line and should have a standard format, such as:

<pre class="screen">ssh-dss AAAAB3....GWvM= /Users/JohnDoe/.ssh/id_dsa</pre>

<div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

### Important

Please make sure that the copied key is still in one line. Any line-break will prevent the key from being read.

</div>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

You may omit the part behind the equal sign as it is just a comment and not used by <span class="productname">dCache</span>.

</div>

Key-based authorization will always be the default. In case the user key can not be found in the file `authorized_keys2` or the file does not exist, ssh2Admin will fall back to authorizing the user via `gPlazma2` and the `dcache.kpwd` file.

Now you can login to the admin interface by

    [user] $

</div>

<div class="section" title="Access via gPlazma2 and the dcache.kpwd File">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp641632"></a>Access via `gPlazma2` and the `dcache.kpwd` File

</div>

</div>

</div>

To use `gPlazma` make sure that you defined a `gPlazmaDomain` in your layout file.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">Part of the layout file in `<span>/etc/dcache</span>/layouts`:

<pre class="programlisting">[_<tt><gplazma-${host.name}></tt>_Domain]
[_<tt><gplazma-${host.name}></tt>_Domain/gplazma]</pre>

</div>

</div>

To use `gPlazma2` you need to specify it in the `<span>/etc/dcache</span>/dcache.conf` file:

<pre class="programlisting"># This is the main configuration file of dCache.
#
...
#
# use gPlazma2
gplazma.version=2</pre>

Moreover, you need to create the file `<span>/etc/dcache</span>/gplazma.conf` with the content

<pre class="programlisting">auth optional kpwd "kpwd=<span>/etc/dcache</span>/dcache.kpwd"
map optional kpwd "kpwd=<span>/etc/dcache</span>/dcache.kpwd"
session optional kpwd "kpwd=<span>/etc/dcache</span>/dcache.kpwd"</pre>

and add the user `admin` to the `<span>/etc/dcache</span>/dcache.kpwd` file using the `dcache` script.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

adds this to the `<span>/etc/dcache</span>/dcache.kpwd` file:

<pre class="programlisting"># set pwd
passwd admin 4091aba7 read-write 12345 1000 / /</pre>

</div>

</div>

Edit the file `<span>/etc/dcache</span>/dcachesrm-gplazma.policy` to switch on the `kpwd-plugin`. For more information about `gPlazma` see [Chapter 10, _Authorization in <span class="productname">dCache</span>_](#cf-gplazma "Chapter 10\. Authorization in dCache").

Now the user `admin` can login to the admin interface with his password `password` by:

    [user] $

To allow other users access to the admin interface add them to the `<span>/etc/dcache</span>/dcache.kpwd` file as described above.

Just adding a user in the `dcache.kpwd` file is not sufficient. The generated user also needs access rights that can only be set within the admin interface itself.

See [the section called “Create a new user”](#intouch-admin-new-user "Create a new user") to learn how to create the user in the admin interface and set the rights.

</div>

</div>

<div class="section" title="Access with ssh1">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="intouch-admin-ssh1"></a>Access with `ssh1`

</div>

</div>

</div>

Connect to the server using `ssh1` with:

    [user] $

The initial password is <span class="quote">“<span class="quote">`dickerelch`</span>”</span> (which is German for <span class="quote">“<span class="quote">fat elk</span>”</span>) and you will be greeted by the prompt

<pre class="screen">   dCache Admin (VII) (user=admin)

`(local) admin >`</pre>

The password can now be changed with

    (local) admin >

</div>

<div class="section" title="How to use the Admin Interface">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp693968"></a>How to use the Admin Interface

</div>

</div>

</div>

The command <span class="command">**help**</span> lists all commands the cell knows and their parameters. However, many of the commands are only used for debugging and development purposes.

<div class="warning" title="Warning" style="margin-left: 0.5in; margin-right: 0.5in;">

### Warning

Some commands are dangerous. Executing them without understanding what they do may lead to data loss.

</div>

Starting from the local prompt (`(local) admin >`) the command <span class="command">**cd**</span> takes you to the specified [_cell_](#gl-cell). In general the address of a cell is a concatenation of cell name `@` symbol and the domain name. <span class="command">**cd**</span> to a cell by:

    (local) admin >

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

If the cells are _well-known_, they can be accessed without adding the domain-scope. See [Chapter 5, _The Cell Package_](#cf-cellpackage "Chapter 5\. The Cell Package") for more information.

</div>

The domains that are running on the <span class="productname">dCache</span>-instance, can be viewed in the layout-configuration (see [Chapter 2, _Installing <span class="productname">dCache</span>_](#in "Chapter 2\. Installing dCache")). Additionally, there is the `topo` cell, which keeps track of the instance’s domain topology. If it is running, it can be used to obtain the list of domains the following way:

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

The `topo` cell rescans every five minutes which domains are running, so it can take some time until <span class="command">**ls**</span> displays the full domain list.

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

As the `topo` cell is a `well-known` cell you can <span class="command">**cd**</span> to it directly by `<span class="command">**cd**</span> topo`.

Use the command <span class="command">**ls**</span> to see which domains are running.

    (local) admin >

</div>

</div>

The escape sequence <span class="command">**..**</span> takes you back to the local prompt.

The command <span class="command">**logoff**</span> exits the admin shell.

If you want to find out which cells are running on a certain domain, you can issue the command <span class="command">**ps**</span> in the `System` cell of the domain.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

For example, if you want to list the cells running on the `poolDomain`, <span class="command">**cd**</span> to its `System` cell and issue the <span class="command">**ps**</span> command.

    (local) admin >

</div>

</div>

The cells in the domain can be accessed using <span class="command">**cd**</span> together with the cell-name scoped by the domain-name. So first, one has to get back to the local prompt, as the <span class="command">**cd**</span> command will not work otherwise.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Note that <span class="command">**cd**</span> only works from the local prompt. If the cell you are trying to access does not exist, the <span class="command">**cd**</span> command will complain.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    (local) admin >

</div>

</div>

Type <span class="command">**..**</span> to return to the `(local) admin >` prompt.

</div>

Login to the routing manager of the `dCacheDomain` to get a list of all well-known cells you can directly <span class="command">**cd**</span> to without having to add the domain.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    (System@poolDomain) admin >

</div>

</div>

All cells know the commands <span class="command">**info**</span> for general information about the cell and <span class="command">**show pinboard**</span> for listing the last lines of the [_pinboard_](#gl-pinboard) of the cell. The output of these commands contains useful information for solving problems.

It is a good idea to get aquainted with the normal output in the following cells: `PoolManager`, `PnfsManager`, and the pool cells (e.g., `_<tt><poolHostname></tt>__1`).

The most useful command of the pool cells is [<span class="refentrytitle"><span class="command">**rep ls**</span></span>](#cmd-rep_ls "rep ls"). To execute this command <span class="command">**cd**</span> into the pool. It lists the files which are stored in the pool by their <span class="productname">`pnfs`</span> IDs:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    (RoutingMgr@dCacheDoorDomain) admin >

Each file in a pool has one of the 4 primary states: <span class="quote">“<span class="quote">cached</span>”</span> (`<C---`), <span class="quote">“<span class="quote">precious</span>”</span> (`<-P--`), <span class="quote">“<span class="quote">from client</span>”</span> (`<--C-`), and <span class="quote">“<span class="quote">from store</span>”</span> (`<---S`).

</div>

</div>

See [the section called “How to Store-/Restore files via the Admin Interface”](#cf-tss-pools-admin "How to Store-/Restore files via the Admin Interface") for more information about <span class="command">**rep ls**</span>.

The most important commands in the `PoolManager` are: [<span class="refentrytitle"><span class="command">**rc ls**</span></span>](#cmd-rc_ls "rc ls") and <span class="command">**cm ls -r**</span>.

<span class="command">**rc ls**</span> lists the requests currently handled by the `PoolManager`. A typical line of output for a read request with an error condition is (all in one line):

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    (pool_1) admin >

As the error message at the end of the line indicates, no pool was found containing the file and no pool could be used for staging the file from a tertiary storage system.

</div>

</div>

See [the section called “Obtain information via the <span class="productname">dCache</span> Command Line Admin Interface”](#cf-tss-monitor-clAdmin "Obtain information via the dCache Command Line Admin Interface") for more information about the command <span class="command">**rc ls**</span>

Finally, [<span class="refentrytitle"><span class="command">**cm ls**</span></span>](#cmd-cm_ls "cm ls") with the option `-r` gives the information about the pools currently stored in the cost module of the pool manager. A typical output is:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    (PoolManager) admin >

</div>

</div>

While the first line for each pool gives the information stored in the cache of the cost module, the second line gives the costs (SC: [_space cost_](#gl-space_cost), CC: [_performance cost_](#gl-performance_cost)) calculated for a (hypothetical) file of zero size. For details on how these are calculated and their meaning, see [the section called “Classic Partitions”](#cf-pm-classic "Classic Partitions").

</div>

<div class="section" title="Create a new user">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="intouch-admin-new-user"></a>Create a new user

</div>

</div>

</div>

To create a new user, `_<tt><new-user></tt>_` and set a new password for the user <span class="command">**cd**</span> from the local prompt (`(local) admin >`) to the `acm`, the access control manager, and run following command sequence:

    (local) admin >

For the new created users there will be an entry in the directory `<span>/etc/dcache/admin</span>/users/meta`.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

As the initial user `admin` has not been created with the above command you will not find him in the directory `<span>/etc/dcache/admin</span>/users/meta`.

</div>

Give the new user access to a particular cell:

    (acm) admin >

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Give the new user access to the `PnfsManager`.

    (acm) admin >

Now you can check the permissions by:

    (acm) admin >

</div>

</div>

The following commands allow access to every cell for a user _<tt><new-user></tt>_:

    (acm) admin >

The following command makes a user as powerful as `admin` (<span class="productname">dCache</span>’s equivalent to the `root` user):

    (acm) admin >

</div>

<div class="section" title="Use of the ssh Admin Interface by scripts">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp838000"></a>Use of the `ssh` Admin Interface by scripts

</div>

</div>

</div>

The `ssh` admin interface can be used non-interactively by scripts. For this the <span class="productname">dCache</span>-internal `ssh` server uses public/private key pairs.

The file ``<span>/etc/dcache</span>/authorized_keys`` contains one line per user. The file has the same format as `~/.ssh/authorized_keys` which is used by <span class="command">**sshd**</span>. The keys in ``<span>/etc/dcache</span>/authorized_keys`` have to be of type RSA1 as <span class="productname">dCache</span> only supports SSH protocol 1\. Such a key is generated with

    [user] $

The passphrase is used to encrypt the private key (now stored in `/home/_<tt><user></tt>_/.ssh/identity`). If you do not want to enter the passphrase every time the private key is used, you can use <span class="command">**ssh-add**</span> to add it to a running <span class="command">**ssh-agent**</span>. If no agent is running start it with

    [user] $

and add the key to it with

    [user] $

Now, insert the public key `~/.ssh/identity.pub` as a separate line into ``<span>/etc/dcache</span>/authorized_keys``. The comment field in this line <span class="quote">“<span class="quote">SSH1 key of _<tt><user></tt>_</span>”</span> has to be changed to the <span class="productname">dCache</span> user name. An example file is:

<pre class="programlisting">1024 35 141939124_<span class="lineannotation">(... many more numbers ...)</span>_15331 admin</pre>

Using ssh-add -L >> `<span>/etc/dcache</span>/authorized_keys` will not work, because the line added is not correct. The key manager within <span class="productname">dCache</span> will read this file every minute.

Now, the `ssh` program should not ask for a password anymore. This is still quite secure, since the unencrypted private key is only held in the memory of the <span class="command">**ssh-agent**</span>. It can be removed from it with

    [user] $

In scripts, one can use a <span class="quote">“<span class="quote">Here Document</span>”</span> to list the commands, or supply them to <span class="command">**ssh**</span> as standard-input (stdin). The following demonstrates using a Here Document:

<pre class="programlisting">#!/bin/sh
#
#  Script to automate dCache administrative activity

outfile=/tmp/$(basename $0).$.out

ssh -c blowfish -p 22223 admin@_<tt><adminNode></tt>_ > $outfile << EOF
cd PoolManager
cm ls -r
_<span class="lineannotation">(more commands here)</span>_
logoff
EOF</pre>

or, the equivalent as stdin.

<pre class="programlisting">#!/bin/bash
#
#   Script to automate dCache administrative activity.

echo -e 'cd _<tt><pool_1></tt>_\nrep ls\n_<span class="lineannotation">(more commands here)</span>_\nlogoff' \
  | ssh -c blowfish -p 22223 admin@_<tt><adminNode></tt>_ \
  | tr -d '\r' > rep_ls.out</pre>

</div>

</div>

<div class="section" title="Authentication and Authorization in dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="intouch-certificates"></a>Authentication and Authorization in <span class="productname">dCache</span>

</div>

</div>

</div>

In <span class="productname">dCache</span> digital certificates are used for authentication and authorisation. To be able to verify the chain of trust when using the non-commercial grid-certificates you should install the list of certificates of grid Certification Authorities (CAs). In case you are using commercial certificates you will find the list of CAs in your browser.

    [root] #

You will need a server certificate for the host on which your <span class="productname">dCache</span> is running and a user certificate. The host certificate needs to be copied to the directory `/etc/grid-security/` on your server and converted to `hostcert.pem` and `hostkey.pem` as described in [Using X.509 Certificates](#cf-gplazma-certificates "Using X.509 Certificates"). Your user certificate is usually located in `.globus`. If it is not there you should copy it from your browser to `.globus` and convert the `*.p12` file to `usercert.pem` and `userkey.pem`.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

If you have the clients installed on the machine on which your <span class="productname">dCache</span> is running you will need to add a user to that machine in order to be able to execute the <span class="command">**voms-proxy-init**</span> command and execute <span class="command">**voms-proxy-init**</span> as this user.

    [root] #

Change the password of the new user in order to be able to copy files to this account.

    [root] #

Copy your key files from your local machine to the new user on the machine where the <span class="productname">dCache</span> is running.

    [user] $

</div>

</div>

Install glite-security-voms-clients (contained in the <span class="productname">gLite</span>-UI).

    [root] #

Generate a proxy certificate using the command <span class="command">**voms-proxy-init**</span>.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

</div>

</div>

With <span class="command">**voms-proxy-init -voms _<tt><yourVO></tt>_**</span> you can add VOMS attributes to the proxy. A user’s roles (Fully Qualified Attribute Names) are read from the certificate chain found within the proxy. These attributes are signed by the user’s VOMS server when the proxy is created. For the <span class="command">**voms-proxy-init -voms** </span>command you need to have the file `/etc/vomses` which contains entries about the VOMS servers like

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">"desy" "grid-voms.desy.de" "15104" "/C=DE/O=GermanGrid/OU=DESY/CN=host/grid-voms.desy.de" "desy" "24"
"atlas" "voms.cern.ch" "15001" "/DC=ch/DC=cern/OU=computers/CN=voms.cern.ch" "atlas" "24"
"dteam" "lcg-voms.cern.ch" "15004" "/DC=ch/DC=cern/OU=computers/CN=lcg-voms.cern.ch" "dteam" "24"
"dteam" "voms.cern.ch" "15004" "/DC=ch/DC=cern/OU=computers/CN=voms.cern.ch" "dteam" "24"
      </pre>

</div>

</div>

Now you can generate your voms proxy containing your VO.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

</div>

</div>

Authentication and authorization in <span class="productname">dCache</span> is done by the `gplazma` service. Define this service in the layout file.

<pre class="programlisting">[gPlazmaDomain]
[gPlazmaDomain/gplazma]</pre>

In this tutorial we will use the [gplazmalite-vorole-mapping plugin](#cf-gplazma-plug-inconfig-vorolemap "The gplazmalite-vorole-mapping plug-in"). To this end you need to edit the `/etc/grid-security/grid-vorolemap` and the `/etc/grid-security/storage-authzdb` as well as the `<span>/etc/dcache</span>/dcachesrm-gplazma.policy`.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

The `/etc/grid-security/grid-vorolemap`:

<pre class="programlisting">"/C=DE/O=GermanGrid/OU=DESY/CN=John Doe" "/desy" doegroup</pre>

The `/etc/grid-security/storage-authzdb`:

<pre class="programlisting">version 2.1

authorize  doegroup read-write 12345 1234 / / /</pre>

The `<span>/etc/dcache</span>/dcachesrm-gplazma.policy`:

<pre class="programlisting"># Switches
xacml-vo-mapping="OFF"
saml-vo-mapping="OFF"
kpwd="OFF"
grid-mapfile="OFF"
gplazmalite-vorole-mapping="ON"

# Priorities
xacml-vo-mapping-priority="5"
saml-vo-mapping-priority="2"
kpwd-priority="3"
grid-mapfile-priority="4"
gplazmalite-vorole-mapping-priority="1"
      </pre>

</div>

</div>

</div>

<div class="section" title="How to work with secured dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="intouch-sec-dcache"></a>How to work with secured <span class="productname">dCache</span>

</div>

</div>

</div>

If you want to copy files into <span class="productname">dCache</span> with `GSIdCap`, `SRM` or `WebDAV` with certificates you need to follow the instructions in the section [above](#intouch-certificates "Authentication and Authorization in dCache").

<div class="section" title="GSIdCap">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="intouch-client-gsidcap"></a>`GSIdCap`

</div>

</div>

</div>

To use `GSIdCap` you must run a `GSIdCap` door. This is achieved by including the `gsidcap` service in your layout file on the machine you wish to host the door.

<pre class="programlisting">[gsidcapDomain]
[gsidcapDomain/dcap]
dcap.authn.protocol=gsi</pre>

In addition, you need to have <span class="package">libdcap-tunnel-gsi</span> installed on your worker node, which is contained in the <span class="productname">gLite</span>-UI.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

As ScientificLinux 5 32bit is not supported by <span class="productname">gLite</span> there is no <span class="package">libdcap-tunnel-gsi</span> for SL5 32bit.

</div>

    [root] #

It is also available on the [`dCap` downloads page](http://www.dcache.org/downloads/dcap/).

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [root] #

</div>

</div>

The machine running the `GSIdCap` door needs to have a host certificate and you need to have a valid user certificate. In addition, you should have created a [voms proxy](#cf-gplazma-certificates-voms-proxy-init "Creating a VOMS proxy") as mentioned [above](#intouch-certificates "Authentication and Authorization in dCache").

Now you can copy a file into your <span class="productname">dCache</span> using `GSIdCap`

    [user] $

and copy it back

    [user] $

</div>

<div class="section" title="SRM">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="intouch-client-srm"></a>`SRM`

</div>

</div>

</div>

To use the `SRM` you need to define the `srm` service in your layout file.

<pre class="programlisting">[srmDomain]
[srmDomain/srm]</pre>

In addition, the user needs to install an `SRM` client for example the `dcache-srmclient`, which is contained in the <span class="productname">gLite</span>-UI, on the worker node and set the `PATH` environment variable.

    [root] #

You can now copy a file into your <span class="productname">dCache</span> using the `SRM`,

    [user] $

copy it back

    [user] $

and delete it

    [user] $

If the grid functionality is not required the file can be deleted with the `NFS` mount of the <span class="productname">Chimera</span> namespace:

    [user] $

</div>

<div class="section" title="WebDAV with certificates">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="intouch-client-https"></a>`WebDAV` with certificates

</div>

</div>

</div>

To use `WebDAV` with certificates you change the entry in `<span>/etc/dcache</span>/layouts/mylayout.conf` from

<pre class="programlisting">[webdavDomain]
[webdavDomain/webdav]
webdav.authz.anonymous-operations=FULL
webdav.root=/data/world-writable</pre>

to

<pre class="programlisting">[webdavDomain]
[webdavDomain/webdav]
webdav.authz.anonymous-operations=NONE
webdav.root=/data/world-writable
webdav.authn.protocol=https</pre>

Then you will need to import the host certificate into the <span class="productname">dCache</span> keystore using the command

    [root] #

and initialise your truststore by

    [root] #

Now you need to restart the `WebDAV` domain

    [root] #

and access your files via `https://_<tt><dcache.example.org></tt>_:2880` with your browser.

<div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

### Important

If the host certificate contains an extended key usage extension, it must include the extended usage for server authentication. Therefore you have to make sure that your host certificate is either unrestricted or it is explicitly allowed as a certificate for `TLS Web Server Authentication`.

</div>

<div class="section" title="Allowing authenticated and non-authenticated access with WebDAV">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp1017040"></a>Allowing authenticated and non-authenticated access with `WebDAV`

</div>

</div>

</div>

You can also choose to have secure and insecure access to your files at the same time. You might for example allow access without authentication for reading and access with authentication for reading and writing.

<pre class="programlisting">[webdavDomain]
[webdavDomain/webdav]
webdav.root=/data/world-writable
webdav.authz.anonymous-operations=READONLY
port=2880
webdav.authn.protocol=https</pre>

You can access your files via `https://_<tt><dcache.example.org></tt>_:2880` with your browser.

</div>

</div>

</div>

<div class="section" title="Files">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="intouch-files"></a>Files

</div>

</div>

</div>

In this section we will have a look at the configuration and log files of <span class="productname">dCache</span>.

The <span class="productname">dCache</span> software is installed in various directories according to the Filesystem Hierarchy Standard. All configuration files can be found in `/etc/dcache`.

Log files of domains are by default stored in `<span>/var/log/dcache</span>/_<tt><domainName></tt>_.log`.

More details about domains and cells can be found in [Chapter 5, _The Cell Package_](#cf-cellpackage "Chapter 5\. The Cell Package").

The most central component of a <span class="productname">dCache</span> instance is the `PoolManager` cell. It reads additional configuration information from the file `<span>/var/lib/dcache/config/poolmanager.conf</span>` at start-up. However, it is not necessary to restart the domain when changing the file. We will see an example of this below.

</div>

</div>

</div>

<div class="part" title="Part II. Configuration of dCache">

<div class="titlepage">

<div>

<div>

# <a name="cf"></a>Part II. Configuration of <span class="productname">dCache</span>

</div>

</div>

</div>

<div class="partintro" title="Configuration of dCache">

This part contains descriptions of the components of <span class="productname">dCache</span>, their role, functionality within the framework. In short, all information necessary for configuring them.

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="chapter">[4\. <span class="productname">Chimera</span>](#cf-chimera)</span></dt>

<dd>

<dl>

<dt><span class="section">[Mounting <span class="productname">Chimera</span> through `NFS`](#chimera-mount)</span></dt>

<dd>

<dl>

<dt><span class="section">[Using `dCap` with a mounted file system](#chimera-useDcap)</span></dt>

</dl>

</dd>

<dt><span class="section">[Communicating with <span class="productname">Chimera</span>](#chimera-commands)</span></dt>

<dt><span class="section">[IDs](#cf-chimera-ids)</span></dt>

<dt><span class="section">[Directory Tags](#chimera-tags)</span></dt>

<dd>

<dl>

<dt><span class="section">[Create, List and Read Directory Tags if the Namespace is not Mounted](#idp1220352)</span></dt>

<dt><span class="section">[Create, List and Read Directory Tags if the Namespace is Mounted](#idp1245968)</span></dt>

<dt><span class="section">[Directory Tags and Command Files](#idp1284256)</span></dt>

<dt><span class="section">[Directory Tags for <span class="productname">dCache</span>](#idp1297248)</span></dt>

<dt><span class="section">[Storage Class and Directory Tags](#chimera-tags-storageClass)</span></dt>

</dl>

</dd>

</dl>

</dd>

<dt><span class="chapter">[5\. The Cell Package](#cf-cellpackage)</span></dt>

<dt><span class="chapter">[6\. The `replica` Service (Replica Manager)](#cf-repman)</span></dt>

<dd>

<dl>

<dt><span class="section">[The Basic Setup](#cf-repman-basics)</span></dt>

<dd>

<dl>

<dt><span class="section">[Define a poolgroup for resilient pools](#idp1474720)</span></dt>

</dl>

</dd>

<dt><span class="section">[Operation](#cf-repman-op)</span></dt>

<dd>

<dl>

<dt><span class="section">[Pool States](#cf-repman-op-pool-states)</span></dt>

<dt><span class="section">[Startup](#cf-repman-op-start)</span></dt>

<dt><span class="section">[Avoid replicas on the same host](#cf-repman-op-same-host)</span></dt>

<dt><span class="section">[Hybrid <span class="productname">dCache</span>](#cf-repman-op-hybrid)</span></dt>

<dt><span class="section">[Commands for the admin interface](#cf-repman-op-cmds)</span></dt>

</dl>

</dd>

<dt><span class="section">[Properties of the `replica` service](#cf-repman-op-args)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[7\. The `poolmanager` Service](#cf-pm)</span></dt>

<dd>

<dl>

<dt><span class="section">[The Pool Selection Mechanism](#cf-pm-psu)</span></dt>

<dd>

<dl>

<dt><span class="section">[Links](#cf-pm-links)</span></dt>

<dt><span class="section">[Examples](#idp1899280)</span></dt>

</dl>

</dd>

<dt><span class="section">[The Partition Manager](#cf-pm-pm)</span></dt>

<dd>

<dl>

<dt><span class="section">[Overview](#cf-pm-pm-overview)</span></dt>

<dt><span class="section">[Managing Partitions](#cf-pm-pm-commands)</span></dt>

<dt><span class="section">[Using Partitions](#cf-pm-pm-usingPartitions)</span></dt>

<dt><span class="section">[Classic Partitions](#cf-pm-classic)</span></dt>

</dl>

</dd>

<dt><span class="section">[Link Groups](#cf-pm-linkgroups)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[8\. The <span class="productname">dCache</span> Tertiary Storage System Interface](#cf-tss)</span></dt>

<dd>

<dl>

<dt><span class="section">[Introduction](#idp2428816)</span></dt>

<dt><span class="section">[Scope of this chapter](#idp2434560)</span></dt>

<dt><span class="section">[Requirements for a Tertiary Storage System](#cf-tss-hsm-requirements)</span></dt>

<dd>

<dl>

<dt><span class="section">[Migrating Tertiary Storage Systems with a file system interface.](#idp2446528)</span></dt>

<dt><span class="section">[Tertiary Storage Systems with a minimalistic `PUT`, `GET` and `REMOVE` interface](#idp2450656)</span></dt>

</dl>

</dd>

<dt><span class="section">[How <span class="productname">dCache</span> interacts with a Tertiary Storage System](#idp2459904)</span></dt>

<dt><span class="section">[Details on the <abbr class="abbrev">TSS</abbr>-support `executable`](#cf-tss-support)</span></dt>

<dd>

<dl>

<dt><span class="section">[Summary of command line options](#cf-tss-support-clo)</span></dt>

<dt><span class="section">[Summary of return codes](#cf-tss-support-return-codes)</span></dt>

<dt><span class="section">[The `executable` and the `STORE FILE` operation](#idp2584224)</span></dt>

<dt><span class="section">[The `executable` and the `FETCH FILE` operation](#idp2617184)</span></dt>

<dt><span class="section">[The `executable` and the `REMOVE FILE` operation](#idp2635248)</span></dt>

</dl>

</dd>

<dt><span class="section">[Configuring pools to interact with a Tertiary Storage System](#cf-tss-pools)</span></dt>

<dd>

<dl>

<dt><span class="section">[The <span class="productname">dCache</span> layout files](#cf-tss-pools-layout)</span></dt>

<dt><span class="section">[What happens next](#idp2720384)</span></dt>

</dl>

</dd>

<dt><span class="section">[How to Store-/Restore files via the Admin Interface](#cf-tss-pools-admin)</span></dt>

<dt><span class="section">[How to monitor what’s going on](#cf-tss-monitor)</span></dt>

<dd>

<dl>

<dt><span class="section">[Log Files](#cf-tss-monitor-log)</span></dt>

<dt><span class="section">[Obtain information via the <span class="productname">dCache</span> Command Line Admin Interface](#cf-tss-monitor-clAdmin)</span></dt>

</dl>

</dd>

<dt><span class="section">[Example of an `executable` to simulate a tape backend](#tss-executable)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[9\. File Hopping](#cf-hopping)</span></dt>

<dd>

<dl>

<dt><span class="section">[_File Hopping on arrival_ from outside <span class="productname">dCache</span>](#cf-hopping-onarrival)</span></dt>

<dd>

<dl>

<dt><span class="section">[File mode of replicated files](#cf-hopping-onarrival-file-mode)</span></dt>

<dt><span class="section">[File Hopping managed by the `PoolManager`](#idp2899136)</span></dt>

<dt><span class="section">[File Hopping managed by the `HoppingManager`](#idp2934624)</span></dt>

</dl>

</dd>

</dl>

</dd>

<dt><span class="chapter">[10\. Authorization in <span class="productname">dCache</span>](#cf-gplazma)</span></dt>

<dd>

<dl>

<dt><span class="section">[Basics](#cf-gplazma-basics)</span></dt>

<dt><span class="section">[Configuration](#cf-gplazma-gp2-configuration)</span></dt>

<dd>

<dl>

<dt><span class="section">[Plug-ins](#cf-gplazma-gp2-configuration-plug-ins)</span></dt>

</dl>

</dd>

<dt><span class="section">[Using `X.509` Certificates](#cf-gplazma-certificates)</span></dt>

<dd>

<dl>

<dt><span class="section">[CA Certificates](#cf-gplazma-certificates-cacerts)</span></dt>

<dt><span class="section">[User Certificate](#cf-gplazma-certificates-usercert)</span></dt>

<dt><span class="section">[Host Certificate](#cf-gplazma-certificates-hostcert)</span></dt>

<dt><span class="section">[<span class="productname">VOMS</span> Proxy Certificate](#cb-voms-proxy-glite)</span></dt>

</dl>

</dd>

<dt><span class="section">[Configuration files](#cf-gplazma-plug-inconfig)</span></dt>

<dd>

<dl>

<dt><span class="section">[`storage-authzdb`](#cf-gplazma-plug-inconfig-authzdb)</span></dt>

<dt><span class="section">[The gplazmalite-vorole-mapping plug-in](#cf-gplazma-plug-inconfig-vorolemap)</span></dt>

<dt><span class="section">[Authorizing a VO](#cf-gplazma-plug-inconfig-voauth)</span></dt>

<dt><span class="section">[The kpwd plug-in](#cf-gplazma-kpwd)</span></dt>

<dt><span class="section">[The `gridmap` plug-in](#cf-gplazma-gridmap)</span></dt>

</dl>

</dd>

<dt><span class="section">[`gPlazma` specific <span class="productname">dCache</span> configuration](#cf-gplazma-setup)</span></dt>

<dd>

<dl>

<dt><span class="section">[Enabling Username/Password Access for `WebDAV`](#cf-gplazma-username-password-webdav-example)</span></dt>

<dt><span class="section">[`gPlazma` config example to work with authenticated webadmin](#cf-gplazma-webadmin-example)</span></dt>

</dl>

</dd>

</dl>

</dd>

<dt><span class="chapter">[11\. dCache as xRootd-Server](#cf-xrootd)</span></dt>

<dd>

<dl>

<dt><span class="section">[Setting up](#cf-xrootd-setup)</span></dt>

<dd>

<dl>

<dt><span class="section">[Parameters](#cf-xrootd-setup-params)</span></dt>

</dl>

</dd>

<dt><span class="section">[Quick tests](#cf-xrootd-tests)</span></dt>

<dd>

<dl>

<dt><span class="section">[Copying files with xrdcp](#cf-xrootd-tests-xrdcp)</span></dt>

<dt><span class="section">[Accessing files from within ROOT](#cf-xrootd-tests-ROOT)</span></dt>

</dl>

</dd>

<dt><span class="section">[`xrootd` security](#cf-xrootd-sec)</span></dt>

<dd>

<dl>

<dt><span class="section">[Read-Write access](#cf-xrootd-sec-ro)</span></dt>

<dt><span class="section">[Permitting read/write access on selected directories](#cf-xrootd-sec-selected)</span></dt>

<dt><span class="section">[Token-based authorization](#cf-xrootd-sec-authz)</span></dt>

<dt><span class="section">[Strong authentication](#cf-xrootd-sec-authn)</span></dt>

<dt><span class="section">[Precedence of security mechanisms](#cf-xrootd-sec-precedence)</span></dt>

<dt><span class="section">[Other configuration options](#cf-xrootd-other-configuration)</span></dt>

</dl>

</dd>

</dl>

</dd>

<dt><span class="chapter">[12\. <span class="productname">dCache</span> as `NFSv4.1` Server](#cf-nfs4)</span></dt>

<dd>

<dl>

<dt><span class="section">[Setting up](#cf-nfs4-setup)</span></dt>

<dt><span class="section">[Configuring ``NFSv4.1` door` with GSS-API support](#cf-nfs4-gss)</span></dt>

<dt><span class="section">[Configuring principal-id mapping for NFS access](#cf-idmap)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[13\. <span class="productname">dCache</span> Storage Resource Manager](#cf-srm)</span></dt>

<dd>

<dl>

<dt><span class="section">[Introduction](#cf-srm-intro)</span></dt>

<dt><span class="section">[Configuring the `srm` service](#cf-srm-srm)</span></dt>

<dd>

<dl>

<dt><span class="section">[The Basic Setup](#idp3868496)</span></dt>

<dt><span class="section">[Important `srm` configuration options](#idp3893328)</span></dt>

</dl>

</dd>

<dt><span class="section">[Utilization of Space Reservations for Data Storage](#idp3913392)</span></dt>

<dd>

<dl>

<dt><span class="section">[Properties of Space Reservation](#cf-srm-intro-spaceReservation)</span></dt>

</dl>

</dd>

<dt><span class="section">[<span class="productname">dCache</span> specific concepts](#idp3967952)</span></dt>

<dd>

<dl>

<dt><span class="section">[Activating `SRM` `SpaceManager`](#idp3969184)</span></dt>

<dt><span class="section">[Explicit and Implicit Space Reservations for Data Storage in <span class="productname">dCache</span>](#idp3978640)</span></dt>

</dl>

</dd>

<dt><span class="section">[`SpaceManager` configuration for Explicit Space Reservations](#cf-srm-space)</span></dt>

<dd>

<dl>

<dt><span class="section">[`SRM` `SpaceManager` and Link Groups](#cf-srm-space-linkgroups)</span></dt>

<dt><span class="section">[Making a Space Reservation](#idp4032304)</span></dt>

<dt><span class="section">[`SRM` configuration for experts](#cf-srm-expert-config)</span></dt>

</dl>

</dd>

<dt><span class="section">[Configuring the <span class="productname">PostgreSQL</span> Database](#cf-srm-psql)</span></dt>

<dd>

<dl>

<dt><span class="section">[`SRM` or srm monitoring on a separate node](#idp4425056)</span></dt>

</dl>

</dd>

<dt><span class="section">[General `SRM` Concepts (for developers)](#idp4433440)</span></dt>

<dd>

<dl>

<dt><span class="section">[The `SRM` service](#idp4435088)</span></dt>

<dt><span class="section">[Space Management Functions](#cf-srm-intro-spaceManagementFunct)</span></dt>

<dt><span class="section">[Data Transfer Functions](#cf-srm-intro-dataTransferFunct)</span></dt>

<dt><span class="section">[Request Status Functions](#cf-srm-intro-requestStatusFunct)</span></dt>

<dt><span class="section">[Directory Functions](#cf-srm-intro-directoryFunct)</span></dt>

<dt><span class="section">[Permission functions](#cf-srm-intro-permissionFunct)</span></dt>

</dl>

</dd>

</dl>

</dd>

<dt><span class="chapter">[14\. The `statistics` Service](#cf-statistics)</span></dt>

<dd>

<dl>

<dt><span class="section">[The Basic Setup](#cf-statistics-basic)</span></dt>

<dt><span class="section">[The Statistics Web Page](#cf-statistics-webPage)</span></dt>

<dt><span class="section">[Explanation of the File Format of the `xxx.raw` Files](#cf-statistics-raw)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[15\. The `billing` Service](#cf-billing)</span></dt>

<dd>

<dl>

<dt><span class="section">[The billing log files](#cf-billing-log-files)</span></dt>

<dt><span class="section">[The <span class="database">billing</span> database](#cf-billing-db)</span></dt>

<dd>

<dl>

<dt><span class="section">[Customizing the database](#billing-customize)</span></dt>

</dl>

</dd>

<dt><span class="section">[Generating and Displaying Billing Plots](#config-billing-plots)</span></dt>

<dt><span class="section">[Upgrading a Previous Installation](#cf-billing-upgrade)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[16\. The `alarms` Service](#cf-alarms)</span></dt>

<dd>

<dl>

<dt><span class="section">[The Basic Setup](#cf-alarms-basic)</span></dt>

<dd>

<dl>

<dt><span class="section">[Configure where the `alarms` service is Running](#cf-alarms-basic-remoteServer)</span></dt>

<dt><span class="section">[The Defined Alarms](#cf-alarms-basic-definedAlarms)</span></dt>

</dl>

</dd>

<dt><span class="section">[Using the Alarms Web Page](#cf-alarms-webPage)</span></dt>

<dt><span class="section">[Alarms Database](#cf-alarms-db)</span></dt>

<dt><span class="section">[Advanced](#cf-alarms-advanced)</span></dt>

<dd>

<dl>

<dt><span class="section">[Email on Alarm](#cf-alarms-advanced-email)</span></dt>

<dt><span class="section">[Defining an Alarm](#cf-alarms-advanced-defineAlarm)</span></dt>

<dt><span class="section">[Run the Logback Server Independently from <span class="productname">dCache</span>](#cf-alarms-advanced-logbackServer)</span></dt>

</dl>

</dd>

<dt><span class="section">[Properties of the `alarms` Service](#cf-alarms-prop)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[17\. <span class="productname">dCache</span> Webadmin Interface](#cf-webadmin)</span></dt>

<dd>

<dl>

<dt><span class="section">[Installation](#cf-webadmin-install)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[18\. <acronym class="acronym">ACL</acronym>s in <span class="productname">dCache</span>](#cf-acl)</span></dt>

<dd>

<dl>

<dt><span class="section">[Introduction](#cf-acl-introduction)</span></dt>

<dt><span class="section">[Database configuration](#cf-acl-db-install)</span></dt>

<dt><span class="section">[Configuring <acronym class="acronym">ACL</acronym> support](#cf-acl-dcachesetup)</span></dt>

<dd>

<dl>

<dt><span class="section">[Enabling <acronym class="acronym">ACL</acronym> support](#cf-acl-config-enable)</span></dt>

</dl>

</dd>

<dt><span class="section">[Administrating <acronym class="acronym">ACL</acronym>s](#cf-acl-admin)</span></dt>

<dd>

<dl>

<dt><span class="section">[How to set <acronym class="acronym">ACL</acronym>s](#idp5159312)</span></dt>

<dt><span class="section">[Viewing configured <acronym class="acronym">ACL</acronym>s](#cf-acl-view)</span></dt>

</dl>

</dd>

</dl>

</dd>

<dt><span class="chapter">[19\. <acronym class="acronym">GLUE</acronym> Info Provider](#cf-glue)</span></dt>

<dd>

<dl>

<dt><span class="section">[Internal collection of information](#cf-glue-info)</span></dt>

<dt><span class="section">[Configuring the info provider](#cf-glue-cf-info-provider)</span></dt>

<dt><span class="section">[Testing the info provider](#cf-glue-testing-info-provider)</span></dt>

<dt><span class="section">[Decommissioning the old info provider](#cf-glue-decommission)</span></dt>

<dt><span class="section">[Publishing <span class="productname">dCache</span> information](#cf-glue-publishing)</span></dt>

<dt><span class="section">[Troubleshooting <acronym class="acronym">BDII</acronym> problems](#cf-glue-troubleshooting)</span></dt>

<dt><span class="section">[Updating information](#cf-glue-updating)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[20\. Stage Protection](#cf-stage-protection)</span></dt>

<dd>

<dl>

<dt><span class="section">[Configuration of Stage Protection](#cf-stage-protection-configuration)</span></dt>

<dt><span class="section">[Definition of the White List](#cf-stage-protection-whiteList)</span></dt>

</dl>

</dd>

</dl>

</div>

</div>

<div class="chapter" title="Chapter 4\. Chimera">

<div class="titlepage">

<div>

<div>

## <a name="cf-chimera"></a>Chapter 4\. <span class="productname">Chimera</span>

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Mounting <span class="productname">Chimera</span> through `NFS`](#chimera-mount)</span></dt>

<dd>

<dl>

<dt><span class="section">[Using `dCap` with a mounted file system](#chimera-useDcap)</span></dt>

</dl>

</dd>

<dt><span class="section">[Communicating with <span class="productname">Chimera</span>](#chimera-commands)</span></dt>

<dt><span class="section">[IDs](#cf-chimera-ids)</span></dt>

<dt><span class="section">[Directory Tags](#chimera-tags)</span></dt>

<dd>

<dl>

<dt><span class="section">[Create, List and Read Directory Tags if the Namespace is not Mounted](#idp1220352)</span></dt>

<dt><span class="section">[Create, List and Read Directory Tags if the Namespace is Mounted](#idp1245968)</span></dt>

<dt><span class="section">[Directory Tags and Command Files](#idp1284256)</span></dt>

<dt><span class="section">[Directory Tags for <span class="productname">dCache</span>](#idp1297248)</span></dt>

<dt><span class="section">[Storage Class and Directory Tags](#chimera-tags-storageClass)</span></dt>

</dl>

</dd>

</dl>

</div>

<span class="productname">dCache</span> is a distributed storage system, nevertheless it provides a single-rooted file system view. While <span class="productname">dCache</span> supports multiple namespace providers, <span class="productname">Chimera</span> is the recommended provider and is used by default.

The inner <span class="productname">dCache</span> components talk to the namespace via a module called `PnfsManager`, which in turn communicates with the <span class="productname">Chimera</span> database using a thin <span class="productname">Java</span> layer, which in turn communicates directly with the <span class="productname">Chimera</span> database. <span class="productname">Chimera</span> allows direct access to the namespace by providing an `NFSv3` and `NFSv4.1` server. Clients can `NFS`-mount the namespace locally. This offers the opportunity to use OS-level tools like <span class="command">**ls**</span>, <span class="command">**mkdir**</span>, <span class="command">**mv**</span> for <span class="productname">Chimera</span>. Direct I/O-operations like <span class="command">**cp**</span> and <span class="command">**cat**</span> are possible with the `NFSv4.1` door.

The properties of <span class="productname">Chimera</span> are defined in `<span>/usr/share/dcache</span>/defaults/chimera.properties`. For customisation the files `<span>/etc/dcache</span>/layouts/mylayout.conf` or `<span>/etc/dcache</span>/dcache.conf` should be modified (see [the section called “Defining domains and services”](#in-install-layout "Defining domains and services")).

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

This example shows an extract of the `<span>/etc/dcache</span>/layouts/mylayout.conf` file in order to run <span class="productname">dCache</span> with `NFSv3`.

<pre class="programlisting">[namespaceDomain]
[namespaceDomain/pnfsmanager]
[namespaceDomain/nfs]
nfs.version=3</pre>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

If you want to run the `NFSv4.1` server you need to add the corresponding `nfs` service to a domain in the `<span>/etc/dcache</span>/layouts/mylayout.conf` file and start this domain.

<pre class="programlisting">[namespaceDomain]
[namespaceDomain/pnfsmanager]
[namespaceDomain/nfs]
nfs.version = 4.1</pre>

</div>

</div>

If you wish <span class="productname">dCache</span> to access your <span class="productname">Chimera</span> with a <span class="productname">PostgreSQL</span> user other than <span class="database">chimera</span> then you must specify the username and password in `<span>/etc/dcache</span>/dcache.conf`.

<pre class="programlisting">chimera.db.user=myuser
chimera.db.password=secret</pre>

<div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

### Important

Do not update configuration values in `<span>/usr/share/dcache</span>/defaults/chimera.properties`, since changes to this file will be overwritten by updates.

</div>

<div class="section" title="Mounting Chimera through NFS">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="chimera-mount"></a>Mounting <span class="productname">Chimera</span> through `NFS`

</div>

</div>

</div>

<span class="productname">dCache</span> does not need the <span class="productname">Chimera</span> filesystem to be mounted but a mounted file system is convenient for administrative access. This offers the opportunity to use OS-level tools like <span class="command">**ls**</span> and <span class="command">**mkdir**</span> for <span class="productname">Chimera</span>. However, direct I/O-operations like <span class="command">**cp**</span> are not possible, since the `NFSv3` interface provides the namespace part only. This section describes how to start the <span class="productname">Chimera</span> `NFSv3` server and mount the name space.

If you want to mount <span class="productname">Chimera</span> for easier administrative access, you need to edit the `/etc/exports` file as the <span class="productname">Chimera</span> `NFS` server uses it to manage exports. If this file doesn’t exist it must be created. The typical `exports` file looks like this:

<pre class="programlisting">/ localhost(rw)
/data
# or
# /data *.my.domain(rw)</pre>

As any RPC service <span class="productname">Chimera</span> `NFS` requires `rpcbind` service to run on the host. Nevertheless `rpcbind` has to be configured to accept requests from <span class="productname">Chimera</span> `NFS`.

On RHEL6 based systems you need to add

<pre class="programlisting">RPCBIND_ARGS="-i"</pre>

into `/etc/sysconfig/rpcbind` and restart `rpcbind`. Check your OS manual for details.

    [root] #

If your OS does not provide `rpcbind` <span class="productname">Chimera</span> `NFS` can use an embedded `rpcbind`. This requires to disable the `portmap` service if it exists.

    [root] #

and restart the domain in which the `NFS` server is running.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [root] #

</div>

</div>

Now you can mount <span class="productname">Chimera</span> by

    [root] #

and create the root of the <span class="productname">Chimera</span> namespace which you can call `data`:

    [root] #

If you don’t want to mount chimera you can create the root of the <span class="productname">Chimera</span> namespace by

    [root] #

You can now add directory tags. For more information on tags see [the section called “Directory Tags”](#chimera-tags "Directory Tags").

    [root] #

<div class="section" title="Using dCap with a mounted file system">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="chimera-useDcap"></a>Using `dCap` with a mounted file system

</div>

</div>

</div>

If you plan to use `dCap` with a mounted file system instead of the <acronym class="acronym">URL</acronym>-syntax (e.g. <span class="command">**dccp**</span> `/data/file1` `/tmp/file1`), you need to mount the root of <span class="productname">Chimera</span> locally (remote mounts are not allowed yet). This will allow us to establish wormhole files so `dCap` clients can discover the `dCap` doors.

    [root] #

The default values for ports can be found in [Chapter 28, _<span class="productname">dCache</span> Default Port Values_](#rf-ports "Chapter 28\. dCache Default Port Values") (for `dCap` the default port is `22125`) and in the file `<span>/usr/share/dcache</span>/defaults/dcache.properties`. They can be altered in `<span>/etc/dcache</span>/dcache.conf`

Create the directory in which the users are going to store their data and change to this directory.

    [root] #

Now you can copy a file into your <span class="productname">dCache</span>

    [root] #

and copy the data back using the <span class="command">**dccp**</span> command.

    [root] #

The file has been transferred succesfully.

Now remove the file from the <span class="productname">dCache</span>.

    [root] #

When the configuration is complete you can unmount <span class="productname">Chimera</span>:

    [root] #

</div>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Please note that whenever you need to change the configuration, you have to remount the root `localhost:/` to a temporary location like `/mnt`.

</div>

</div>

<div class="section" title="Communicating with Chimera">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="chimera-commands"></a>Communicating with <span class="productname">Chimera</span>

</div>

</div>

</div>

Many configuration parameters of <span class="productname">Chimera</span> and the application specific meta data is accessed by reading, writing, or creating files of the form `.(_<tt><command></tt>_)(_<tt><para></tt>_)`. For example, the following prints the <span class="productname">Chimera</span>ID of the file `/data/some/dir/file.dat`:

    [user] $

From the point of view of the `NFS` protocol, the file `.(id)(file.dat)` in the directory `/data/some/dir/` is read. However, <span class="productname">Chimera</span> interprets it as the command `id` with the parameter `file.dat` executed in the directory `/data/some/dir/`. The quotes are important, because the shell would otherwise try to interpret the parentheses.

Some of these command files have a second parameter in a third pair of parentheses. Note, that files of the form `.(_<tt><command></tt>_)(_<tt><para></tt>_)` are not really files. They are not shown when listing directories with <span class="command">**ls**</span>. However, the command files are listed when they appear in the argument list of <span class="command">**ls**</span> as in

    [user] $

Only a subset of file operations are allowed on these special command files. Any other operation will result in an appropriate error. Beware, that files with names of this form might accidentally be created by typos. They will then be shown when listing the directory.

</div>

<div class="section" title="IDs">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-chimera-ids"></a>IDs

</div>

</div>

</div>

Each file in <span class="productname">Chimera</span> has a unique 18 byte long ID. It is referred to as ChimeraID or as pnfsID. This is comparable to the inode number in other filesystems. The ID used for a file will never be reused, even if the file is deleted. <span class="productname">dCache</span> uses the ID for all internal references to a file.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

The ID of the file `example.org/data/examplefile` can be obtained by reading the command-file `.(id)(examplefile)` in the directory of the file.

    [user] $

</div>

</div>

A file in <span class="productname">Chimera</span> can be referred to by the ID for most operations.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

The name of a file can be obtained from the ID with the command `nameof` as follows:

    [user] $

And the ID of the directory it resides in is obtained by:

    [user] $

</div>

</div>

This way, the complete path of a file may be obtained starting from the ID.

</div>

<div class="section" title="Directory Tags">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="chimera-tags"></a>Directory Tags

</div>

</div>

</div>

In the <span class="productname">Chimera</span> namespace, each directory can have a number of tags. These directory tags may be used within <span class="productname">dCache</span> to control the file placement policy in the pools (see [the section called “The Pool Selection Mechanism”](#cf-pm-psu "The Pool Selection Mechanism")). They might also be used by a [tertiary storage system](#cf-tss "Chapter 8\. The dCache Tertiary Storage System Interface") for similar purposes (e.g. controlling the set of tapes used for the files in the directory).

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Directory tags are not needed to control the behaviour of <span class="productname">dCache</span>. <span class="productname">dCache</span> works well without directory tags.

</div>

<div class="section" title="Create, List and Read Directory Tags if the Namespace is not Mounted">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp1220352"></a>Create, List and Read Directory Tags if the Namespace is not Mounted

</div>

</div>

</div>

You can create tags with

    [user] $

list tags with

    [user] $

and read tags with

    [user] $

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Create tags for the directory `data` with

    [user] $

list the existing tags with

    [user] $

and their content with

    [user] $

</div>

</div>

</div>

<div class="section" title="Create, List and Read Directory Tags if the Namespace is Mounted">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp1245968"></a>Create, List and Read Directory Tags if the Namespace is Mounted

</div>

</div>

</div>

If the namespace is mounted, change to the directory for which the tag should be set and create a tag with

    [user] $

Then the existing tags may be listed with

    [user] $

and the content of a tag can be read with

    [user] $

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Create tags for the directory `data` with

    [user] $

list the existing tags with

    [user] $

and their content with

    [user] $

A nice trick to list all tags with their contents is

    [user] $

</div>

</div>

</div>

<div class="section" title="Directory Tags and Command Files">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp1284256"></a>Directory Tags and Command Files

</div>

</div>

</div>

When creating or changing directory tags by writing to the command file as in

    [user] $

one has to take care not to treat the command files in the same way as regular files, because tags are different from files in the following aspects:

<div class="orderedlist">

1.  The _<tt><tagName></tt>_ is limited to 62 characters and the _<tt><content></tt>_ to 512 bytes. Writing more to the command file, will be silently ignored.

2.  If a tag which does not exist in a directory is created by writing to it, it is called a <span class="emphasis">_primary_</span> tag.

3.  Tags are <span class="emphasis">_inherited_</span> from the parent directory by a newly created directory. Changing a primary tag in one directory will change the tags inherited from it in the same way. Creating a new primary tag in a directory will not create an inherited tag in its subdirectories.

    Moving a directory within the <span class="productname">Chimera</span> namespace will not change the inheritance. Therefore, a directory does not necessarily inherit tags from its parent directory. Removing an inherited tag does not have any effect.

4.  Empty tags are ignored.

</div>

</div>

<div class="section" title="Directory Tags for dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp1297248"></a>Directory Tags for <span class="productname">dCache</span>

</div>

</div>

</div>

The following directory tags appear in the <span class="productname">dCache</span> context:

<div class="variablelist">

<dl>

<dt><span class="term">OSMTemplate</span></dt>

<dd>

Must contain a line of the form <span class="quote">“<span class="quote">`StoreName` _<tt><storeName></tt>_</span>”</span> and specifies the name of the store that is used by <span class="productname">dCache</span> to construct the [storage class](#chimera-tags-storageClass "Storage Class and Directory Tags") if the [_HSM Type_](#gl-hsm_type) is `osm`.

</dd>

<dt><span class="term">HSMType</span></dt>

<dd>

The [_`HSMType`_](#gl-hsm_type) tag is normally determined from the other existing tags. E.g., if the tag `OSMTemplate` exists, `HSMType`=`osm` is assumed. With this tag it can be set explicitly. A class implementing that <abbr class="abbrev">HSM</abbr> type has to exist. Currently the only implementations are `osm` and `enstore`.

</dd>

<dt><span class="term">sGroup</span></dt>

<dd>

The storage group is also used to construct the [storage class](#chimera-tags-storageClass "Storage Class and Directory Tags") if the [_`HSMType`_](#gl-hsm_type) is `osm`.

</dd>

<dt><span class="term">cacheClass</span></dt>

<dd>

The cache class is only used to control on which pools the files in a directory may be stored, while the storage class (constructed from the two above tags) might also be used by the <abbr class="abbrev">HSM</abbr>. The cache class is only needed if the above two tags are already fixed by <abbr class="abbrev">HSM</abbr> usage and more flexibility is needed.

</dd>

<dt><span class="term">hsmInstance</span></dt>

<dd>

If not set, the `hsmInstance` tag will be the same as the `HSMType` tag. Setting this tag will only change the name as used in the [storage class](#chimera-tags-storageClass "Storage Class and Directory Tags") and in the pool commands.

</dd>

<dt><span class="term">WriteToken</span></dt>

<dd>

Assign a `WriteToken` tag to a directory in order to be able to write to a space token without using the `SRM`.

</dd>

</dl>

</div>

</div>

<div class="section" title="Storage Class and Directory Tags">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="chimera-tags-storageClass"></a>Storage Class and Directory Tags

</div>

</div>

</div>

The [storage class](#secStorageClass "Storage Classes") is a string of the form _<tt><StoreName></tt>_:_<tt><StorageGroup></tt>_@_<tt><hsm-type></tt>_, where _<tt><StoreName></tt>_ is given by the `OSMTemplate` tag, _<tt><StorageGroup></tt>_ by the `sGroup` tag and _<tt><hsm-type></tt>_ by the `HSMType` tag. As mentioned above the `HSMType` tag is assumed to be `osm` if the tag `OSMTemplate` exists.

In the examples above two tags have been created.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

As the tag `OSMTemplate` was created the tag `HSMType` is assumed to be `osm`.

The storage class of the files which are copied into the directory `/data` after the tags have been set will be `myStore:myGroup@osm`.

</div>

</div>

If directory tags are used to control the behaviour of <span class="productname">dCache</span> and/or a tertiary storage system, it is a good idea to plan the directory structure in advance, thereby considering the necessary tags and how they should be set up. Moving directories should be done with great care or even not at all. Inherited tags can only be created by creating a new directory.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Assume that data of two experiments, `experiment-a` and `experiment-b` is written into a namespace tree with subdirectories `/data/experiment-a` and `/data/experiment-b`. As some pools of the <span class="productname">dCache</span> are financed by `experiment-a` and others by `experiment-b` they probably do not like it if they are also used by the other group. To avoid this the directories of `experiment-a` and `experiment-b` can be tagged.

    [user] $

Data from `experiment-a` taken in 2010 shall be written into the directory `/data/experiment-a/2010` and data from `experiment-a` taken in 2011 shall be written into `/data/experiment-a/2011`. Data from `experiment-b` shall be written into `/data/experiment-b`. Tag the directories correspondingly.

    [user] $

List the content of the tags by

    [user] $

As the tag `OSMTemplate` was created the `HSMType` is assumed to be `osm`.

The storage classes of the files which are copied into these directories after the tags have been set will be

<div class="itemizedlist">

*   `exp-a:run2010@osm` for the files in `/data/experiment-a/2010`
*   `exp-a:run2011@osm` for the files in `/data/experiment-a/2011`
*   `exp-b:alldata@osm` for the files in `/data/experiment-b`

</div>

To see how storage classes are used for pool selection have a look at the example ’Reserving Pools for Storage and Cache Classes’ in the PoolManager chapter.

</div>

</div>

There are more tags used by <span class="productname">dCache</span> if the `HSMType` is `enstore`.

</div>

</div>

</div>

<div class="chapter" title="Chapter 5\. The Cell Package">

<div class="titlepage">

<div>

<div>

## <a name="cf-cellpackage"></a>Chapter 5\. The Cell Package

</div>

</div>

</div>

All of <span class="productname">dCache</span> makes use of the cell package. It is a framework for a distributed and scalable server system in Java. The <span class="productname">dCache</span> system is divided into cells which communicate with each other via messages. Several cells run simultaneously in one domain.

Each domain runs in a separate Java virtual machine and each cell is run as a separate thread therein. Domain names have to be unique. The domains communicate with each other via `TCP` using connections that are established at start-up. The topology is controlled by the location manager service. In the standard configuration, all domains connect with the `dCacheDomain`, which routes all messages to the appropriate domains. This forms a star topology.

<div class="note" title="Only for message communication" style="margin-left: 0.5in; margin-right: 0.5in;">

### Only for message communication

The `TCP` communication controlled by the location manager service is for the short control messages sent between cells. Any transfer of the data stored within <span class="productname">dCache</span> does not use these connections; instead, dedicated `TCP` connections are established as needed.

</div>

A single node provides the location-manager service. For a single-host <span class="productname">dCache</span> instance, this is `localhost`; for multi-host <span class="productname">dCache</span> instances, the hostname of the node providing this service must be configured using the `serviceLocatorHost` property.

The domain that hosts the location manager service is also configurable. By default, the service runs within the `dCacheDomain` domain; however, this may be changed by setting the `dcache.broker.domain` property. The port that the location manager listens on is also configurable, using the `dcache.broker.port` property; however, most sites may leave this property unaltered and use the default value.

Within this framework, cells send messages to other cells addressing them in the form `_<tt><cellName></tt>_@_<tt><domainName></tt>_`. This way, cells can communicate without knowledge about the host they run on. Some cells are [_well known_](#gl-well-known-cell), i.e. they can be addressed just by their name without `@_<tt><domainName></tt>_`. Evidently, this can only work properly if the name of the cell is unique throughout the whole system. If two well known cells with the same name are present, the system will behave in an undefined way. Therefore it is wise to take care when starting, naming, or renaming the well known cells. In particular this is true for pools, which are well known cells.

A domain is started with a shell script `bin/dcache start _<tt><domainName></tt>_`. The routing manager and location manager cells are started in each domain and are part of the underlying cell package structure. Each domain will contain at least one cell in addition to them.

</div>

<div class="chapter" title="Chapter 6\. The replica Service (Replica Manager)">

<div class="titlepage">

<div>

<div>

## <a name="cf-repman"></a>Chapter 6\. The `replica` Service (Replica Manager)

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[The Basic Setup](#cf-repman-basics)</span></dt>

<dd>

<dl>

<dt><span class="section">[Define a poolgroup for resilient pools](#idp1474720)</span></dt>

</dl>

</dd>

<dt><span class="section">[Operation](#cf-repman-op)</span></dt>

<dd>

<dl>

<dt><span class="section">[Pool States](#cf-repman-op-pool-states)</span></dt>

<dt><span class="section">[Startup](#cf-repman-op-start)</span></dt>

<dt><span class="section">[Avoid replicas on the same host](#cf-repman-op-same-host)</span></dt>

<dt><span class="section">[Hybrid <span class="productname">dCache</span>](#cf-repman-op-hybrid)</span></dt>

<dt><span class="section">[Commands for the admin interface](#cf-repman-op-cmds)</span></dt>

</dl>

</dd>

<dt><span class="section">[Properties of the `replica` service](#cf-repman-op-args)</span></dt>

</dl>

</div>

The `replica` service (which is also referred to as Replica Manager) controls the number of replicas of a file on the pools. If no [_tertiary storage system_](#gl-tss) is connected to a <span class="productname">dCache</span> instance (i.e., it is configured as a [_large file store_](#gl-lfs)), there might be only one copy of each file on disk. (At least the [_precious replica_](#gl-precious).) If a higher security and/or availability is required, the resilience feature of <span class="productname">dCache</span> can be used: If running in the default configuration, the `replica` service will make sure that the number of [_replicas_](#gl-replica) of a file will be at least 2 and not more than 3\. If only one replica is present it will be copied to another pool by a [_pool to pool transfer_](#gl-p2p). If four or more replicas exist, some of them will be deleted.

<div class="section" title="The Basic Setup">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-repman-basics"></a>The Basic Setup

</div>

</div>

</div>

The standard configuration assumes that the database server is installed on the same machine as the `replica` service — usually the admin node of the <span class="productname">dCache</span> instance. If this is not the case you need to set the property `replica.db.host`.

To create and configure the database _replicas_ used by the `replica` service in the database server do:

    [root] #

To activate the `replica` service you need to

<div class="orderedlist">

1.  Enable the `replica` service in a layout file.

    <pre class="programlisting">[_<tt><someDomain></tt>_]
    ...

    [_<tt><someDomain></tt>_/replica]</pre>

2.  Configure the service in the `<span>/etc/dcache</span>/dcache.conf` file on the node with the `dCacheDomain` and on the node on which the `pnfsmanager` is running.

    <pre class="programlisting">dcache.enable.replica=true</pre>

    <div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

    ### Note

    It will not work properly if you defined the `replica` service in one of the layout files and set this property to `no` on the node with the `dCacheDomain` or on the node on which the `pnfsmanager` is running.

    </div>

3.  Define a pool group for the resilient pools if necessary.

4.  Start the `replica` service.

</div>

In the default configuration, all pools of the <span class="productname">dCache</span> instance which have been created with the command <span class="command">**dcache pool create**</span> will be managed. These pools are in the pool group named `default` which does exist by default. The `replica` service will keep the number of replicas between 2 and 3 (including). At each restart of the `replica` service the pool configuration in the database will be recreated.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<div class="orderedlist">

This is a simple example to get started with. All your pools are assumed to be in the pool group `default`.

1.  In your layout file in the directory `<span>/etc/dcache</span>/layouts` define the `replica` service.

    <pre class="programlisting">[dCacheDomain]
    ...

    [replicaDomain]
    [replicaDomain/replica]</pre>

2.  In the file `<span>/etc/dcache</span>/dcache.conf` set the value for the property `replicaManager` to `true` and the `replica.poolgroup` to `default`.

    <pre class="programlisting">dcache.enable.replica=true
    replica.poolgroup=default</pre>

3.  The pool group `default` exists by default and does not need to be defined.

4.  To start the `replica` service restart <span class="productname">dCache</span>.

        [root] #

</div>

</div>

</div>

<div class="section" title="Define a poolgroup for resilient pools">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp1474720"></a>Define a poolgroup for resilient pools

</div>

</div>

</div>

For more complex installations of <span class="productname">dCache</span> you might want to define a pool group for the resilient pools.

Define the resilient pool group in the `<span>/var/lib/dcache/config/poolmanager.conf</span>` file on the host running the `poolmanager` service. Only pools defined in the resilient pool group will be managed by the `replica` service.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Login to the admin interface and cd to the `PoolManager`. Define a poolgroup for resilient pools and add pools to that poolgroup.

    (local) admin >

By default the pool group named `ResilientPools` is used for replication.

</div>

</div>

To use another pool group defined in `<span>/var/lib/dcache/config/poolmanager.conf</span>` for replication, please specify the group name in the `etc/dcache.conf` file.

<pre class="programlisting">replica.poolgroup=_<tt><NameOfResilientPoolGroup></tt>_.</pre>

</div>

</div>

<div class="section" title="Operation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-repman-op"></a>Operation

</div>

</div>

</div>

When a file is transfered into <span class="productname">dCache</span> its replica is copied into one of the pools. Since this is the only replica and normally the required range is higher (e.g., by default at least 2 and at most 3), this file will be replicated to other pools.

When some pools go down, the replica count for the files in these pools may fall below the valid range and these files will be replicated. Replicas of the file with replica count below the valid range and which need replication are called _deficient replicas_.

Later on some of the failed pools can come up and bring online more valid replicas. If there are too many replicas for some file these extra replicas are called _redundant replicas_ and they will be <span class="quote">“<span class="quote">reduced</span>”</span>. Extra replicas will be deleted from pools.

The `replica` service counts the number of replicas for each file in the pools which can be used online (see Pool States below) and keeps the number of replicas within the valid range (`replica.limits.replicas.min`, `replica.limits.replicas.max`).

<div class="section" title="Pool States">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-repman-op-pool-states"></a>Pool States

</div>

</div>

</div>

The possible states of a pool are `online`, `down`, `offline`, `offline-prepare` and `drainoff`. They can be set by the admin through the admin interface. (See [the section called “Commands for the admin interface”](#cf-repman-op-cmds "Commands for the admin interface").)

<div class="figure"><a name="resilient_poolstate"></a>

**Figure 6.1\. Pool State Diagram**

<div class="figure-contents">

<div class="mediaobject" align="center">![Pool State Diagram](/images/resilient_poolstate_v1-0.png)</div>

</div>

</div>

<div class="variablelist">

<dl>

<dt><span class="term">online</span></dt>

<dd>

Normal operation.

Replicas in this state are readable and can be counted. Files can be written (copied) to this pool.

</dd>

<dt><span class="term">down</span></dt>

<dd>

A pool can be `down` because

<div class="itemizedlist">

*   the admin stopped the domain in which the pool was running.
*   the admin set the state value via the admin interface.
*   the pool crashed

</div>

To confirm that it is safe to turn pool down there is the command <span class="command">**ls unique**</span> in the admin interface to check number of files which can be locked in this pool. (See [the section called “Commands for the admin interface”](#cf-repman-op-cmds "Commands for the admin interface").)

Replicas in pools which are `down` are not counted, so when a pool crashes the number of `online` replicas for some files is reduced. The crash of a pool (pool departure) may trigger replication of multiple files.

On startup, the pool comes briefly to the `online` state, and then it goes `down` to do pool <span class="quote">“<span class="quote">Inventory</span>”</span> to cleanup files which broke when the pool crashed during transfer. When the pool comes online again, the `replica` service will update the list of replicas in the pool and store it in the database.

Pool recovery (arrival) may trigger massive deletion of file replicas, not necessarily in this pool.

</dd>

<dt><span class="term">offline</span></dt>

<dd>

The admin can set the pool state to be `offline`. This state was introduced to avoid unnecessary massive replication if the operator wants to bring the pool down briefly without triggering massive replication.

Replicas in this pool are counted, therefore it does not matter for replication purpose if an `offline` pool goes down or up.

When a pool comes `online` from an `offline` state replicas in the pool will be inventoried to make sure we know the real list of replicas in the pool.

</dd>

<dt><span class="term">offline-prepare</span></dt>

<dd>

This is a transient state betweeen `online` and `offline`.

The admin will set the pool state to be `offline-prepare` if he wants to change the pool state and does not want to trigger massive replication.

Unique files will be evacuated — at least one replica for each unique file will be copied out. It is unlikely that a file will be locked out when a single pool goes down as normally a few replicas are online. But when several pools go down or set drainoff or offline file lockout might happen.

Now the admin can set the pool state `offline` and then `down` and no file replication will be triggered.

</dd>

<dt><span class="term">drainoff</span></dt>

<dd>

This is a transient state betweeen `online` and `down`.

The admin will set the pool state to be `drainoff` if he needs to set a pool or a set of pools permanently out of operation and wants to make sure that there are no replicas <span class="quote">“<span class="quote">locked out</span>”</span>.

Unique files will be evacuated — at least one replica for each unique file will be copied out. It is unlikely that a file will be locked out when a single pool goes down as normally a few replicas are online. But when several pools go down or set drainoff or offline file lockout might happen.

Now the admin can set the pool state down. Files from other pools might be replicated now, depending on the values of `replica.limits.replicas.min` and `replica.limits.replicas.max`.

</dd>

</dl>

</div>

</div>

<div class="section" title="Startup">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-repman-op-start"></a>Startup

</div>

</div>

</div>

When the `replica` service starts it cleans up the database. Then it waits for some time to give a chance to most of the pools in the system to connect. Otherwise unnecessary massive replication would start. Currently this is implemented by some delay to start adjustments to give the pools a chance to connect.

<div class="section" title="Cold Start">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp1552480"></a>Cold Start

</div>

</div>

</div>

Normally (during Cold Start) all information in the database is cleaned up and recreated again by polling pools which are `online` shortly after some minimum delay after the `replica` service starts. The `replica` service starts to track the pools’ state (pool up/down messages and polling list of online pools) and updates the list of replicas in the pools which came online. This process lasts for about 10-15 minutes to make sure all pools came up online and/or got connected. Pools which once get connected to the `replica` service are in online or down state.

It can be annoying to wait for some large period of time until all known <span class="quote">“<span class="quote">good</span>”</span> pools get connected. There is a <span class="quote">“<span class="quote">Hot Restart</span>”</span> option to accelerate the restart of the system after the crash of the head node.

</div>

<div class="section" title="Hot Restart">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp1558528"></a>Hot Restart

</div>

</div>

</div>

On Hot Restart the `replica` service retrieves information about the pools’ states before the crash from the database and saves the pools’ states to some internal structure. When a pool gets connected the `replica` service checks the old pool state and registers the old pool’s state in the database again if the state was `offline`, `offline-prepare` or `drainoff` state. The `replica` service also checks if the pool was `online` before the crash. When all pools which were `online` get connected once, the `replica` service supposes it recovered its old configuration and the `replica` service starts adjustments. If some pools went down during the connection process they were already accounted and adjustment would take care of it.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Suppose we have ten pools in the system, where eight pools were `online` and two were `offline` before a crash. The `replica` service does not care about the two `offline` pools to get connected to start adjustments. For the other eight pools which were `online`, suppose one pool gets connected and then it goes down while the other pools try to connect. The `replica` service considers this pool in known state, and when the other seven pools get connected it can start adjustments and does not wait any more.

If the system was in equilibrium state before the crash, the `replica` service may find some deficient replicas because of the crashed pool and start replication right away.

</div>

</div>

</div>

</div>

<div class="section" title="Avoid replicas on the same host">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-repman-op-same-host"></a>Avoid replicas on the same host

</div>

</div>

</div>

For security reasons you might want to spread your replicas such that they are not on the same host, or in the same building or even in the same town. To configure this you need to set the `tag.hostname` label for your pools and check the properties `replica.enable.check-pool-host` and `replica.enable.same-host-replica`.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

We assume that some pools of your <span class="productname">dCache</span> are in Hamburg and some are in Berlin. In the layout files where the respective pools are defined you can set

<pre class="programlisting">[poolDomain]
[poolDomain/pool1]
name=pool1
path=/srv/dcache/p1
pool.size=500G
pool.wait-for-files=${path}/data
tag.hostname=Hamburg</pre>

and

<pre class="programlisting">[poolDomain]
[poolDomain/pool2]
name=pool2
path=/srv/dcache/p2
pool.size=500G
pool.wait-for-files=${path}/data
tag.hostname=Berlin</pre>

</div>

</div>

By default the property `replica.enable.check-pool-host` is `true` and `replica.enable.same-host-replica` is `false`. This means that the `tag.hostname` will be checked and the replication to a pool with the same `tag.hostname` is not allowed.

</div>

<div class="section" title="Hybrid dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-repman-op-hybrid"></a>Hybrid <span class="productname">dCache</span>

</div>

</div>

</div>

A _hybrid <span class="productname">dCache</span>_ operates on a combination of pools (maybe connected to tape) which are not in a resilient pool group and the set of resilient pools. The `replica` service takes care only of the subset of pools configured in the pool group for resilient pools and ignores all other pools.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

If a file in a resilient pool is marked precious and the pool were connected to a tape system, then it would be flushed to tape. Therefore, the pools in the resilient pool group are not allowed to be connected to tape.

</div>

</div>

<div class="section" title="Commands for the admin interface">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-repman-op-cmds"></a>Commands for the admin interface

</div>

</div>

</div>

If you are an advanced user, have proper privileges and you know how to issue a command to the admin interface you may connect to the `ReplicaManager` cell and issue the following commands. You may find more commands in online help which are for debug only — do not use them as they can stop `replica` service operating properly.

<div class="variablelist">

<dl>

<dt><span class="term"><span class="command">**set pool**</span> _<tt><pool></tt>__<tt><state></tt>_</span></dt>

<dd>

set pool state

</dd>

<dt><span class="term"><span class="command">**show pool**</span> _<tt><pool></tt>_</span></dt>

<dd>

show pool state

</dd>

<dt><span class="term"><span class="command">**ls unique**</span> _<tt><pool></tt>_</span></dt>

<dd>

Reports number of unique replicas in this pool.

</dd>

<dt><span class="term"><span class="command">**exclude**</span> _<tt><pnfsId></tt>_</span></dt>

<dd>

exclude _<tt><pnfsId></tt>_ from adjustments

</dd>

<dt><span class="term"><span class="command">**release**</span> _<tt><pnfsId></tt>_</span></dt>

<dd>

removes transaction/`BAD` status for _<tt><pnfsId></tt>_

</dd>

<dt><span class="term"><span class="command">**debug true | false**</span></span></dt>

<dd>

enable/disable DEBUG messages in the log file

</dd>

</dl>

</div>

</div>

</div>

<div class="section" title="Properties of the replica service">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-repman-op-args"></a>Properties of the `replica` service

</div>

</div>

</div>

<div class="variablelist">

<dl>

<dt><span class="term">replica.cell.name</span></dt>

<dd>

Default: `dcache.enable.replica`

Cell name of the `replica` service

</dd>

<dt><span class="term">dcache.enable.replica</span></dt>

<dd>

Default: `false`

Set this value to `true` if you want to use the `replica` service.

</dd>

<dt><span class="term">replica.poolgroup</span></dt>

<dd>

Default: `ResilientPools`

If you want to use another pool group for the resilient pools set this value to the name of the resilient pool group.

</dd>

<dt><span class="term">replica.db.host</span></dt>

<dd>

Default: `localhost`

Set this value to the name of host of the `replica` service database.

</dd>

<dt><span class="term">replica.db.name</span></dt>

<dd>

Default: `replicas`

Name of the replica database table.

</dd>

<dt><span class="term">replica.db.user</span></dt>

<dd>

Default: `srmdcache`

Change if the `replicas` database was created with a user other than `srmdcache`.

</dd>

<dt><span class="term">replica.db.password.file</span></dt>

<dd>

Default: no password

</dd>

<dt><span class="term">replica.db.driver</span></dt>

<dd>

Default: `org.postgresql.Driver`

`replica` service was tested with <span class="productname">PostgreSQL</span> only.

</dd>

<dt><span class="term">replica.limits.pool-watchdog-period</span></dt>

<dd>

Default: `600` (10 min)

Pools Watch Dog poll period. Poll the pools with this period to find if some pool went south without sending a notice (messages). Can not be too short because a pool can have a high load and not send pings for some time. Can not be less than pool ping period.

</dd>

<dt><span class="term">replica.limits.excluded-files-expiration-timeout</span></dt>

<dd>

Default: `43200` (12 hours)

</dd>

<dt><span class="term">replica.limits.delay-db-start-timeout</span></dt>

<dd>

Default: `1200` (20 min)

On first start it might take some time for the pools to get connected. If replication started right away, it would lead to massive replications when not all pools were connected yet. Therefore the database init thread sleeps some time to give a chance to the pools to get connected.

</dd>

<dt><span class="term">replica.limits.adjust-start-timeout</span></dt>

<dd>

Default: `1200` (20 min)

Normally Adjuster waits for database init thread to finish. If by some abnormal reason it cannot find a database thread then it will sleep for this delay.

</dd>

<dt><span class="term">replica.limits.wait-replicate-timeout</span></dt>

<dd>

Default: `43200` (12 hours)

Timeout for pool-to-pool replica copy transfer.

</dd>

<dt><span class="term">replica.limits.wait-reduce-timeout</span></dt>

<dd>

Default: `43200` (12 hours)

Timeout to delete replica from the pool.

</dd>

<dt><span class="term">replica.limits.workers</span></dt>

<dd>

Default: `6`

Number of worker threads to do the replication. The same number of worker threads is used for reduction. Must be more for larger systems but avoid situation when requests get queued in the pool.

</dd>

<dt><span class="term">replica.limits.replicas.min</span></dt>

<dd>

Default: `2`

Minimum number of replicas in pools which are `online` or `offline`.

</dd>

<dt><span class="term">replica.limits.replicas.max</span></dt>

<dd>

Default: `3`

Maximum number of replicas in pools which are `online` or `offline`.

</dd>

<dt><span class="term">replica.enable.check-pool-host</span></dt>

<dd>

Default: `true`

Checks `tag.hostname` which can be specified in the layout file for each pool.

Set this property to `false` if you do not want to perform this check.

</dd>

<dt><span class="term">replica.enable.same-host-replica</span></dt>

<dd>

Default: `false`

If set to `true` you allow files to be copied to a pool, which has the same `tag.hostname` as the source pool.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

The property `replica.enable.check-pool-host` needs to be set to `true` if `replica.enable.same-host-replica` is set to false.</div>

</dd>

</dl>

</div>

</div>

</div>

<div class="chapter" title="Chapter 7\. The poolmanager Service">

<div class="titlepage">

<div>

<div>

## <a name="cf-pm"></a>Chapter 7\. The `poolmanager` Service

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[The Pool Selection Mechanism](#cf-pm-psu)</span></dt>

<dd>

<dl>

<dt><span class="section">[Links](#cf-pm-links)</span></dt>

<dt><span class="section">[Examples](#idp1899280)</span></dt>

</dl>

</dd>

<dt><span class="section">[The Partition Manager](#cf-pm-pm)</span></dt>

<dd>

<dl>

<dt><span class="section">[Overview](#cf-pm-pm-overview)</span></dt>

<dt><span class="section">[Managing Partitions](#cf-pm-pm-commands)</span></dt>

<dt><span class="section">[Using Partitions](#cf-pm-pm-usingPartitions)</span></dt>

<dt><span class="section">[Classic Partitions](#cf-pm-classic)</span></dt>

</dl>

</dd>

<dt><span class="section">[Link Groups](#cf-pm-linkgroups)</span></dt>

</dl>

</div>

The heart of a <span class="productname">dCache</span> system is the `poolmanager`. When a user performs an action on a file - reading or writing - a _transfer request_ is sent to the <span class="productname">dCache</span> system. The `poolmanager` then decides how to handle this request.

If a file the user wishes to read resides on one of the storage-pools within the <span class="productname">dCache</span> system, it will be transferred from that pool to the user. If it resides on several pools, the file will be retrieved from one of the pools determined by a configurable load balancing policy. If all pools the file is stored on are busy, a new copy of the file on an idle pool will be created and this pool will answer the request.

A new copy can either be created by a _pool to pool transfer_ (<abbr class="abbrev">p2p</abbr>) or by fetching it from a connected _tertiary storage system_ (sometimes called <abbr class="abbrev">HSM</abbr> - hierarchical storage manager). Fetching a file from a tertiary storage system is called _staging_. It is also performed if the file is not present on any of the pools in the <span class="productname">dCache</span> system. The pool manager has to decide on which pool the new copy will be created, i.e. staged or p2p-copied.

The behaviour of the `poolmanager` service is highly configurable. In order to exploit the full potential of the software it is essential to understand the mechanisms used and how they are configured. The `poolmanager` service creates the `PoolManager` cell, which is a unique cell in <span class="productname">dCache</span> and consists of several sub-modules: The important ones are the _pool selection unit_ (<abbr class="abbrev"><abbr class="abbrev">PSU</abbr></abbr>) and the load balancing policy as defined by the _partition manager_ (<abbr class="abbrev">PM</abbr>).

The `poolmanager` can be configured by either directly editing the file `<span>/var/lib/dcache/config/poolmanager.conf</span>` or via the [Admin Interface](#intouch-admin "The Admin Interface"). Changes made via the Admin Interface will be saved in the file `<span>/var/lib/dcache/config/poolmanager.conf</span>` by the <span class="command">**save**</span> command. This file will be parsed, whenever the <span class="productname">dCache</span> starts up. It is a simple text file containing the corresponding Admin Interface commands. It can therefore also be edited before the system is started. It can also be loaded into a running system with the <span class="command">**reload**</span> command. In this chapter we will describe the commands allowed in this file.

<div class="section" title="The Pool Selection Mechanism">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-pm-psu"></a>The Pool Selection Mechanism

</div>

</div>

</div>

The <abbr class="abbrev">PSU</abbr> is responsible for finding the set of pools which can be used for a specific transfer-request. By telling the <abbr class="abbrev">PSU</abbr> which pools are permitted for which type of transfer-request, the administrator of the <span class="productname">dCache</span> system can adjust the system to any kind of scenario: Separate organizations served by separate pools, special pools for writing the data to a tertiary storage system, pools in a DMZ which serves only a certain kind of data (e.g., for the grid). This section explains the mechanism employed by the <abbr class="abbrev">PSU</abbr> and shows how to configure it with several examples.

The <abbr class="abbrev">PSU</abbr> generates a list of allowed storage-pools for each incoming transfer-request. The <abbr class="abbrev">PSU</abbr> configuration described below tells the <abbr class="abbrev">PSU</abbr> which combinations of transfer-request and storage-pool are allowed. Imagine a two-dimensional table with a row for each possible transfer-request and a column for each pool - each field in the table containing either <span class="quote">“<span class="quote">yes</span>”</span> or <span class="quote">“<span class="quote">no</span>”</span>. For an incoming transfer-request the <abbr class="abbrev">PSU</abbr> will return a list of all pools with <span class="quote">“<span class="quote">yes</span>”</span> in the corresponding row.

Instead of <span class="quote">“<span class="quote">yes</span>”</span> and <span class="quote">“<span class="quote">no</span>”</span> the table really contains a _preference_ - a non-negative integer. However, the <abbr class="abbrev">PSU</abbr> configuration is easier to understand if this is ignored.

Actually maintaining such a table in memory (and as user in a configuration file) would be quite inefficient, because there are many possibilities for the transfer-requests. Instead, the <abbr class="abbrev">PSU</abbr> consults a set of rules in order to generate the list of allowed pools. Each such rule is called a _link_ because it links a set of transfer-requests to a group of pools.

<div class="section" title="Links">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-pm-links"></a>Links

</div>

</div>

</div>

A link consists of a set of unit groups and a list of pools. If all the unit groups are matched, the pools belonging to the link are added to the list of allowable pools.

A link is defined in the file `<span>/var/lib/dcache/config/poolmanager.conf</span>` by

<div class="cmdsynopsis">

`psu create link` _<tt><link></tt>_ _<tt><unitgroup></tt>_  
`psu set link` _<tt><link></tt>_ _`-readpref`_=_<tt><rpref></tt>_ _`-writepref`_=_<tt><wpref></tt>_ _`-cachepref`_=_<tt><cpref></tt>_ _`-p2ppref`_=_<tt><ppref></tt>_  
`psu add link` _<tt><link></tt>_ _<tt><poolgroup></tt>_

</div>

For the preference values see [the section called “Preference Values for Type of Transfer”](#cf-pm-psu-pref "Preference Values for Type of Transfer").

The main task is to understand how the unit groups in a link are defined. After we have dealt with that, the preference values will be discussed and a few examples will follow.

The four properties of a transfer request, which are relevant for the <abbr class="abbrev">PSU</abbr>, are the following:

<div class="variablelist">

<dl>

<dt><span class="term">Location of the File</span></dt>

<dd>

The location of the file in the file system is not used directly. Each file has the following two properties which can be set per directory:

<div class="itemizedlist">

*   **Storage Class.** The storage class is a string. It is used by a tertiary storage system to decide where to store the file (i.e. on which set of tapes) and <span class="productname">dCache</span> can use the storage class for a similar purpose (i.e. on which pools the file can be stored.). A detailed description of the syntax and how to set the storage class of a directory in the namespace is given in [the section called “Storage Classes”](#secStorageClass "Storage Classes").

*   **Cache Class.** The cache class is a string with essentially the same functionality as the storage class, except that it is not used by a tertiary storage system. It is used in cases, where the storage class does not provide enough flexibility. It should only be used, if an existing configuration using storage classes does not provide sufficient flexibility.

</div>

</dd>

<dt><span class="term">IP Address</span></dt>

<dd>

The IP address of the requesting host.

</dd>

<dt><span class="term">Protocol / Type of Door</span></dt>

<dd>

The protocol respectively the type of door used by the transfer.

</dd>

<dt><span class="term">Type of Transfer</span></dt>

<dd>

The type of transfer is either `read`, `write`, `p2p` request or `cache`.

A request for reading a file which is not on a read pool will trigger a `p2p` request and a subsequent `read` request. These will be treated as two separate requests.

A request for reading a file which is not stored on disk, but has to be staged from a connected tertiary storage system will trigger a `cache` request to fetch the file from the tertiary storage system and a subsequent `read` request. These will be treated as two separate requests.

</dd>

</dl>

</div>

Each link contains one or more _unit groups_, all of which have to be matched by the transfer request. Each unit group in turn contains several _units_. The unit group is matched if at least one of the units is matched.

<div class="section" title="Types of Units">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-pm-links-units"></a>Types of Units

</div>

</div>

</div>

There are four types of units: network (`-net`), protocol (`-protocol`), storage class (`-store`) and cache class (`-dcache`) units. Each type imposes a condition on the IP address, the protocol, the storage class and the cache class respectively.

For each transfer at most one of each of the four unit types will match. If more than one unit of the same type could match the request then the most restrictive unit matches.

The unit that matches is selected from all units defined in <span class="productname">dCache</span>, not just those for a particular unit group. This means that, if a unit group has a unit that could match a request but this request also matches a more restrictive unit defined elsewhere then the less restrictive unit will not match.

<div class="variablelist">

<dl>

<dt><span class="term">Network Unit</span></dt>

<dd>

A <span class="emphasis">_network unit_</span> consists of an IP address and a net mask written as `_<tt><IP-address></tt>_/_<tt><net mask></tt>_`, say `111.111.111.0/255.255.255.0`. It is satisfied, if the request is coming from a host with IP address within the subnet given by the address/netmask pair.

<pre class="screen"><span class="command">**psu create ugroup**</span> _<tt><name-of-unitgroup></tt>_
<span class="command">**psu create unit**</span>_ `-net`_ _<tt><IP-address></tt>_/_<tt><net mask></tt>_
<span class="command">**psu addto ugroup**</span> _<tt><name-of-unitgroup></tt>_ _<tt><IP-address></tt>_/_<tt><net mask></tt>_</pre>

</dd>

<dt><span class="term">Protocol Unit</span></dt>

<dd>

A <span class="emphasis">_protocol unit_</span> consists of the name of the protocol and the version number written as _<tt><protocol-name></tt>_/_<tt><version-number></tt>_, e.g., `xrootd/3`.

<pre class="screen"><span class="command">**psu create ugroup**</span> _<tt><name-of-unitgroup></tt>_
<span class="command">**psu create unit**</span>_ `-protocol`_ _<tt><protocol-name></tt>_/_<tt><version-number></tt>_
<span class="command">**psu addto ugroup**</span> _<tt><name-of-unitgroup></tt>_ _<tt><protocol-name></tt>_/_<tt><version-number></tt>_</pre>

</dd>

<dt><span class="term">Storage Class Unit</span></dt>

<dd>

A <span class="emphasis">_storage class unit_</span> is given by a storage class. It is satisfied if the requested file has this storage class. Simple wild cards are allowed: for this it is important to know that a storage class must always contain exactly one `@`-symbol as will be explained in [the section called “Storage Classes”](#secStorageClass "Storage Classes"). In a storage class unit, either the part before the `@`-symbol or both parts may be replaced by a `*`-symbol; for example, `*@osm` and `*@*` are both valid storage class units whereas `something@*` is invalid. The `*`-symbol represents a limited wildcard: any string that doesn’t contain an `@`-symbol will match.

<pre class="screen"><span class="command">**psu create ugroup**</span> _<tt><name-of-unitgroup></tt>_
<span class="command">**psu create unit**</span> _`-store`_ _<tt><StoreName></tt>_:_<tt><StorageGroup></tt>_@_<tt><type-of-storage-system></tt>_
<span class="command">**psu addto ugroup**</span> _<tt><name-of-unitgroup></tt>_ _<tt><StoreName></tt>_:_<tt><StorageGroup></tt>_@_<tt><type-of-storage-system></tt>_</pre>

</dd>

<dt><span class="term">Cache Class Unit</span></dt>

<dd>

A <span class="emphasis">_cache class unit_</span> is given by a cache class. It is satisfied, if the cache class of the requested file agrees with it.

<pre class="screen"><span class="command">**psu create ugroup**</span> _<tt><name-of-unitgroup></tt>_
<span class="command">**psu create unit**</span> _`-dcache`_ _<tt><name-of-cache-class></tt>_
<span class="command">**psu addto ugroup**</span> _<tt><name-of-unitgroup></tt>_ _<tt><name-of-cache-class></tt>_</pre>

</dd>

</dl>

</div>

</div>

<div class="section" title="Preference Values for Type of Transfer">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-pm-psu-pref"></a>Preference Values for Type of Transfer

</div>

</div>

</div>

The conditions for the <span class="emphasis">_type of transfer_</span> are not specified with units. Instead, each link contains four attributes `-readpref`, `-writepref`, `-p2ppref` and `-cachepref`, which specify a preference value for the respective types of transfer. If all the unit groups in the link are matched, the corresponding preference is assigned to each pool the link points to. Since we are ignoring different preference values at the moment, a preference of `0` stands for `no` and a non-zero preference stands for `yes`. A negative value for `-p2ppref` means, that the value for `-p2ppref` should equal the one for the `-readpref`.

<div class="section" title="Multiple non-zero Preference Values">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="idp1811600"></a>Multiple non-zero Preference Values

</div>

</div>

</div>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

This explanation of the preference values can be skipped at first reading. It will not be relevant, if all non-zero preference values are the same. If you want to try configuring the pool manager right now without bothering about the preferences, you should only use `0` (for `no`) and, say, `10` (for `yes`) as preferences. You can choose `-p2ppref=-1` if it should match the value for `-readpref`. The first examples below are of this type.

</div>

If several different non-zero preference values are used, the <abbr class="abbrev">PSU</abbr> will not generate a single list but a set of lists, each containing pools with the same preference. The Pool Manager will use the list of pools with highest preference and select a pool according to the load balancing policy for the transfer. Only if all pools with the highest preference are offline, the next list will be considered by the Pool Manager. This can be used to configure a set of fall-back pools which are used if none of the other pools are available.

</div>

</div>

<div class="section" title="Pool Groups">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp1819296"></a>Pool Groups

</div>

</div>

</div>

Pools can be grouped together to pool groups.

<pre class="screen"><span class="command">**psu create pgroup**</span> _<tt><name-of-poolgroup></tt>_
<span class="command">**psu create pool**</span> _<tt><name-of-pool></tt>_
<span class="command">**psu addto pgroup**</span> _<tt><name-of-poolgroup></tt>_ _<tt><name-of-pool></tt>_</pre>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Consider a host `pool1` with two pools, `pool1_1` and `pool1_2`, and a host `pool2` with one pool `pool2_1`. If you want to treat them in the same way, you would create a pool group and put all of them in it:

<pre class="programlisting"><span class="command">**psu create pgroup**</span> normal-pools
<span class="command">**psu create pool**</span> pool1_1
<span class="command">**psu addto pgroup**</span> normal-pools pool1_1
<span class="command">**psu create pool**</span> pool1_2
<span class="command">**psu addto pgroup**</span> normal-pools pool1_2
<span class="command">**psu create pool**</span> pool2_1
<span class="command">**psu addto pgroup**</span> normal-pools pool2_1</pre>

If you later want to treat `pool1_2` differently from the others, you would remove it from this pool group and add it to a new one:

<pre class="programlisting"><span class="command">**psu removefrom pgroup**</span> normal-pools pool1_2
<span class="command">**psu create pgroup**</span> special-pools
<span class="command">**psu addto pgroup**</span> special-pools pool1_2</pre>

</div>

</div>

In the following, we will assume that the necessary pool groups already exist. All names ending with `-pools` will denote pool groups.

Note that a pool-node will register itself with the `PoolManager`: The pool will be created within the <abbr class="abbrev">PSU</abbr> and added to the pool group `default`, if that exists. This is why the <span class="productname">dCache</span> system will automatically use any new pool-nodes in the standard configuration: All pools are in `default` and can therefore handle any request.

</div>

<div class="section" title="Storage Classes">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="secStorageClass"></a>Storage Classes

</div>

</div>

</div>

The storage class is a string of the form `_<tt><StoreName></tt>_:_<tt><StorageGroup></tt>_@_<tt><type-of-storage-system></tt>_`, where `_<tt><type-of-storage-system></tt>_` denotes the type of storage system in use, and `_<tt><StoreName></tt>_`:`_<tt><StorageGroup></tt>_` is a string describing the storage class in a syntax which depends on the storage system. In general use `_<tt><type-of-storage-system></tt>_=osm`.

Consider for example the following setup:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [root] #

This is the setup after a fresh installation and it will lead to the storage class `myStore:STRING@osm`. An adjustment to more sensible values will look like

    [root] #

and will result in the storage class `exp-a:run2010@osm` for any data stored in the `/data/experiment-a` directory.

</div>

</div>

To summarize: The storage class depends on the directory the data is stored in and is configurable.

</div>

<div class="section" title="Cache Class">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="secCacheClass"></a>Cache Class

</div>

</div>

</div>

Storage classes might already be in use for the configuration of a tertiary storage system. In most cases they should be flexible enough to configure the <abbr class="abbrev">PSU</abbr>. However, in rare cases the existing configuration and convention for storage classes might not be flexible enough.

Consider for example a situation, where data produced by an experiment always has the same storage class `exp-a:alldata@osm`. This is good for the tertiary storage system, since all data is supposed to go to the same tape set sequentially. However, the data also contains a relatively small amount of meta-data, which is accessed much more often by analysis jobs than the rest of the data. You would like to keep the meta-data on a dedicated set of <span class="productname">dCache</span> pools. However, the storage class does not provide means to accomplish that.

The cache class of a directory is set by the tag `cacheClass` as follows:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [root] #

In this example the meta-data is stored in directories which are tagged in this way.

</div>

</div>

Check the existing tags of a directory and their content by:

    [root] #

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

A new directory will inherit the tags from the parent directory. But updating a tag will <span class="emphasis">_not_</span> update the tags of any child directories.

</div>

</div>

<div class="section" title="Define a link">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp1881312"></a>Define a link

</div>

</div>

</div>

Now we have everything we need to define a link.

<pre class="screen"><span class="command">**psu create ugroup**</span> _<tt><name-of-unitgroup></tt>_
<span class="command">**psu create unit**</span>_ `- _<tt><type></tt>_`_ _<tt><unit></tt>_
<span class="command">**psu addto ugroup**</span> _<tt><name-of-unitgroup></tt>_ _<tt><lt;unit></tt>_

<span class="command">**psu create pgroup**</span> _<tt><poolgroup></tt>_
<span class="command">**psu create pool**</span> _<tt><pool></tt>_
<span class="command">**psu addto pgroup**</span> _<tt><poolgroup></tt>_ _<tt><pool></tt>_

<span class="command">**psu create link**</span> _<tt><link></tt>_ _<tt><name-of-unitgroup></tt>_
<span class="command">**psu set link**</span> _<tt><link></tt>_ _`-readpref=`__<tt><10></tt>_ _`-writepref=`__<tt><0></tt>_ _`-cachepref=`__<tt><10></tt>__`-p2ppref=`__<tt><-1></tt>_
<span class="command">**psu add link**</span> _<tt><link></tt>_  _<tt><poolgroup></tt>_
</pre>

</div>

</div>

<div class="section" title="Examples">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp1899280"></a>Examples

</div>

</div>

</div>

Find some examples for the configuration of the <abbr class="abbrev">PSU</abbr> below.

<div class="section" title="Separate Write and Read Pools">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="secExReadWrite"></a>Separate Write and Read Pools

</div>

</div>

</div>

The <span class="productname">dCache</span> we are going to configure receives data from a running experiment, stores the data onto a tertiary storage system, and serves as a read cache for users who want to analyze the data. While the new data from the experiment should be stored on highly reliable and therefore expensive systems, the cache functionality may be provided by inexpensive hardware. It is therefore desirable to have a set of pools dedicated for writing the new data and a separate set for reading.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

The simplest configuration for such a setup would consist of two links <span class="quote">“<span class="quote">write-link</span>”</span> and <span class="quote">“<span class="quote">read-link</span>”</span>. The configuration is as follows:

<pre class="programlisting"><span class="command">**psu create pgroup**</span> read-pools
<span class="command">**psu create pool**</span> pool1
<span class="command">**psu addto pgroup**</span> read-pools pool1
<span class="command">**psu create pgroup**</span> write-pools
<span class="command">**psu create pool**</span> pool2
<span class="command">**psu addto pgroup**</span> write-pools pool2

<span class="command">**psu create unit**</span>_ `-net`_ 0.0.0.0/0.0.0.0
<span class="command">**psu create ugroup**</span> allnet-cond
<span class="command">**psu addto ugroup**</span> allnet-cond 0.0.0.0/0.0.0.0

<span class="command">**psu create link**</span> read-link allnet-cond
<span class="command">**psu set link**</span> read-link _`-readpref=`_10 _`-writepref=`_0 _`-cachepref=`_10
<span class="command">**psu add link**</span> read-link read-pools

<span class="command">**psu create link**</span> write-link allnet-cond
<span class="command">**psu set link**</span> write-link _`-readpref=`_0 _`-writepref=`_10 _`-cachepref=`_0
<span class="command">**psu add link**</span> write-link write-pools</pre>

Why is the unit group `allnet-cond` necessary? It is used as a condition which is always true in both links. This is needed, because each link must contain at least one unit group.

</div>

</div>

</div>

<div class="section" title="Restricted Access by IP Address">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp1922688"></a>Restricted Access by IP Address

</div>

</div>

</div>

You might not want to give access to the pools for the whole network, as in the previous example ([the section called “Separate Write and Read Pools”](#secExReadWrite "Separate Write and Read Pools")), though.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Assume, the experiment data is copied into the cache from the hosts with IP `111.111.111.201`, `111.111.111.202`, and `111.111.111.203`. As you might guess, the subnet of the site is `111.111.111.0/255.255.255.0`. Access from outside should be denied. Then you would modify the above configuration as follows:

<pre class="programlisting"><span class="command">**psu create pgroup**</span> read-pools
<span class="command">**psu create pool**</span> pool1
<span class="command">**psu addto pgroup**</span> read-pools pool1
<span class="command">**psu create pgroup**</span> write-pools
<span class="command">**psu create pool**</span> pool2
<span class="command">**psu addto pgroup**</span> write-pools pool2

<span class="command">**psu create unit**</span> _`-store`_ *@*

<span class="command">**psu create unit**</span> _`-net`_ 111.111.111.0/255.255.255.0
<span class="command">**psu create unit**</span> _`-net`_ 111.111.111.201/255.255.255.255
<span class="command">**psu create unit**</span> _`-net`_ 111.111.111.202/255.255.255.255
<span class="command">**psu create unit**</span> _`-net`_ 111.111.111.203/255.255.255.255

<span class="command">**psu create ugroup**</span> write-cond
<span class="command">**psu addto ugroup**</span> write-cond 111.111.111.201/255.255.255.255
<span class="command">**psu addto ugroup**</span> write-cond 111.111.111.202/255.255.255.255
<span class="command">**psu addto ugroup**</span> write-cond 111.111.111.203/255.255.255.255

<span class="command">**psu create ugroup**</span> read-cond
<span class="command">**psu addto ugroup**</span> read-cond 111.111.111.0/255.255.255.0
<span class="command">**psu addto ugroup**</span> read-cond 111.111.111.201/255.255.255.255
<span class="command">**psu addto ugroup**</span> read-cond 111.111.111.202/255.255.255.255
<span class="command">**psu addto ugroup**</span> read-cond 111.111.111.203/255.255.255.255

<span class="command">**psu create link**</span> read-link read-cond
<span class="command">**psu set link**</span> read-link _`-readpref=`_10 _`-writepref=`_0 _`-cachepref=`_10
<span class="command">**psu add link**</span> read-link read-pools

<span class="command">**psu create link**</span> write-link write-cond
<span class="command">**psu set link**</span> write-link _`-readpref=`_0 _`-writepref=`_10 _`-cachepref=`_0
<span class="command">**psu add link**</span> write-link write-pools</pre>

<div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

### Important

For a given transfer exactly zero or one storage class unit, cache class unit, net unit and protocol unit will match. As always the most restrictive one will match, the IP `111.111.111.201` will match the `111.111.111.201/255.255.255.255` unit and not the `111.111.111.0/255.255.255.0` unit. Therefore if you only add `111.111.111.0/255.255.255.0` to the unit group <span class="quote">“<span class="quote">read-cond</span>”</span>, the transfer request coming from the IP `111.111.111.201` will only be allowed to write and not to read. The same is true for transfer requests from `111.111.111.202` and `111.111.111.203`.

</div>

</div>

</div>

</div>

<div class="section" title="Reserving Pools for Storage and Cache Classes">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp1962240"></a>Reserving Pools for Storage and Cache Classes

</div>

</div>

</div>

If pools are financed by one experimental group, they probably do not like it if they are also used by another group. The best way to restrict data belonging to one experiment to a set of pools is with the help of storage class conditions. If more flexibility is needed, cache class conditions can be used for the same purpose.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Assume, data of experiment A obtained in 2010 is written into subdirectories in the namespace tree which are tagged with the storage class `exp-a:run2010@osm`, and similarly for the other years. (How this is done is described in [the section called “Storage Classes”](#secStorageClass "Storage Classes").) Experiment B uses the storage class `exp-b:alldata@osm` for all its data. Especially important data is tagged with the cache class `important`. (This is described in [the section called “Cache Class”](#secCacheClass "Cache Class").) A suitable setup would be

<pre class="programlisting"><span class="command">**psu create pgroup**</span> exp-a-pools
<span class="command">**psu create pool**</span> pool1
<span class="command">**psu addto pgroup**</span> exp-a-pools pool1

<span class="command">**psu create pgroup**</span> exp-b-pools
<span class="command">**psu create pool**</span> pool2
<span class="command">**psu addto pgroup**</span> exp-b-pools pool2

<span class="command">**psu create pgroup**</span> exp-b-imp-pools
<span class="command">**psu create pool**</span> pool3
<span class="command">**psu addto pgroup**</span> exp-b-imp-pools pool3

<span class="command">**psu create unit**</span> _`-net`_ 111.111.111.0/255.255.255.0
<span class="command">**psu create ugroup**</span> allnet-cond
<span class="command">**psu addto ugroup**</span> allnet-cond 111.111.111.0/255.255.255.0

<span class="command">**psu create ugroup**</span> exp-a-cond
<span class="command">**psu create unit**</span> -store exp-a:run2011@osm
<span class="command">**psu addto ugroup**</span> exp-a-cond exp-a:run2011@osm
<span class="command">**psu create unit**</span> -store exp-a:run2010@osm
<span class="command">**psu addto ugroup**</span> exp-a-cond exp-a:run2010@osm

<span class="command">**psu create link**</span> exp-a-link allnet-cond exp-a-cond
<span class="command">**psu set link**</span> exp-a-link _`-readpref=`_10 _`-writepref=`_10 _`-cachepref=`_10
<span class="command">**psu add link**</span> exp-a-link exp-a-pools

<span class="command">**psu create ugroup**</span> exp-b-cond
<span class="command">**psu create unit**</span> _`-store`_ exp-b:alldata@osm
<span class="command">**psu addto ugroup**</span> exp-b-cond exp-b:alldata@osm

<span class="command">**psu create ugroup**</span> imp-cond
<span class="command">**psu create unit**</span> _`-dcache`_ important
<span class="command">**psu addto ugroup**</span> imp-cond important

<span class="command">**psu create link**</span> exp-b-link allnet-cond exp-b-cond
<span class="command">**psu set link**</span> exp-b-link _`-readpref=`_10 _`-writepref=`_10 _`-cachepref=`_10
<span class="command">**psu add link**</span> exp-b-link exp-b-pools

<span class="command">**psu create link**</span> exp-b-imp-link allnet-cond exp-b-cond imp-cond
<span class="command">**psu set link**</span> exp-b-imp-link _`-readpref=`_20 _`-writepref=`_20 _`-cachepref=`_20
<span class="command">**psu add link**</span> exp-b-link exp-b-imp-pools</pre>

Data tagged with cache class <span class="quote">“<span class="quote">`important`</span>”</span> will always be written and read from pools in the pool group `exp-b-imp-pools`, except when all pools in this group cannot be reached. Then the pools in `exp-a-pools` will be used.

Note again that these will never be used otherwise. Not even, if all pools in `exp-b-imp-pools` are very busy and some pools in `exp-a-pools` have nothing to do and lots of free space.

</div>

</div>

The central IT department might also want to set up a few pools, which are used as fall-back, if none of the pools of the experiments are functioning. These will also be used for internal testing. The following would have to be added to the previous setup:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting"><span class="command">**psu create pgroup**</span> it-pools
<span class="command">**psu create pool**</span> pool_it
<span class="command">**psu addto pgroup**</span> it-pools pool_it

<span class="command">**psu create link**</span> fallback-link allnet-cond
<span class="command">**psu set link**</span> fallback-link _`-readpref=`_5 _`-writepref=`_5 _`-cachepref=`_5
<span class="command">**psu add link**</span> fallback-link it-pools</pre>

Note again that these will only be used, if none of the experiments pools can be reached, or if the storage class is not of the form `exp-a:run2009@osm`, `exp-a:run2010@osm`, or `exp-b:alldata@osm`. If the administrator fails to create the unit `exp-a:run2005@osm` and add it to the unit group `exp-a-cond`, the fall-back pools will be used eventually.

</div>

</div>

</div>

</div>

</div>

<div class="section" title="The Partition Manager">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-pm-pm"></a>The Partition Manager

</div>

</div>

</div>

The partition manager defines one or more load balancing policies. Whereas the <abbr class="abbrev">PSU</abbr> produces a prioritized set of candidate pools using a collection of rules defined by the administrator, the load balancing policy determines the specific pool to use. It is also the load balancing policy that determines when to fall back to lesser prirority links, or when to trigger creation of additional copies of a file.

Since the load balancing policy and parameters are defined per partition, understanding the partition manager is essential to tuning load balancing. This does not imply that one has to partition the <span class="productname">dCache</span> instance. It is perfectly valid to use a single partition for the complete instance.

This section documents the use of the partition manager, how to create partitions, set parameters and how to associate links with partitions. In the following sections the available partition types and their configuration parameters are described.

<div class="section" title="Overview">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-pm-pm-overview"></a>Overview

</div>

</div>

</div>

There are various parameters that affect the load balancing policy. Some of them are generic and apply to any load balancing policy, but many are specific to a particular policy. To avoid limiting the complete <span class="productname">dCache</span> instance to a single configuration, the choice of load balancing policy and the various parameters apply to _partitions_ of the instance. The load balancing algorithm and the available parameters is determined by the _partition type_.

Each <abbr class="abbrev">PSU</abbr> link can be associated with a different partion and the policy and parameters of that partition will be used to choose a pool from the set of candidate pools. The only partition that exists without being explicitly created is the partition called `default`. This partition is used by all links that do not explicitly identify a partition. Other partitions can be created or modified as needed.

The `default` partition has a hard-coded partition type called `classic`. This type implements the one load balancing policy that was available in <span class="productname">dCache</span> before version 2.0\. The `classic` partition type is described later. Other partitions have one of a number of available types. The system is pluggable, meaning that third party plugins can be loaded at runtime and add additional partition types, thus providing the ultimate control over load balancing in <span class="productname">dCache</span>. Documentation on how to develop plugins is beyond the scope of this chapter.

To ease the management of partition parameters, a common set of shared parameters can be defined outside all partitions. Any parameter not explicitly set on a partition inherits the value from the common set. If not defined in the common set, a default value determined by the partition type is used. Currently, the common set of parameters happens to be the same as the parameters of the `default` partition, however this is only due to compatibility constraints and may change in future versions.

</div>

<div class="section" title="Managing Partitions">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-pm-pm-commands"></a>Managing Partitions

</div>

</div>

</div>

For each partition you can choose the load balancing policy. You do this by chosing the type of the partition.

Currently four different partition types are supported:

<div class="variablelist">

<dl>

<dt><span class="term">`classic`:</span></dt>

<dd>

This is the pool selection algorithm used in the versions of <span class="productname">dCache</span> prior to version `2.0`. See [the section called “Classic Partitions”](#cf-pm-classic "Classic Partitions") for a detailed description.

</dd>

<dt><span class="term">`random`:</span></dt>

<dd>

This pool selection algorithm selects a pool randomly from the set of available pools.

</dd>

<dt><span class="term">`lru`:</span></dt>

<dd>

This pool selection algorithm selects the pool that has not been used the longest.

</dd>

<dt><span class="term">`wass`:</span></dt>

<dd>

This pool selection algorithm selects pools randomly weighted by available space, while incorporating age and amount of garbage collectible files and information about load.

This is the partition type of the default partition. See [How to Pick a Pool](http://www.dcache.org/articles/wass.html) for more details.

</dd>

<dt><span class="term">`wrandom`:</span></dt>

<dd>

This pool selection algorithm selects read pools randomly and write pools with a weighted probability (based on (free+removable/total) per pool.

The `wrandom` partition type is a special case of the `wass` partition type: by choosing the correct parameters, `wass` can be made to perform like `wrandom`.

The advantage of `wass` over `wrandom` is that it is more flexible and tries to take into account a file’s age. This is something like a distributed LRU cache: the system tries to delete older removable files to keep newer removable files. This is advantageous if files read recently are more likely to be re-read than older files.

</dd>

</dl>

</div>

Commands related to <span class="productname">dCache</span> partitioning:

<div class="itemizedlist">

*   <div class="cmdsynopsis">

    `pm types`

    </div>

    Lists available partition types. New partition types can be added through plugins.

*   <div class="cmdsynopsis">

    `pm create` [-type=_<tt><partitionType></tt>_] _<tt><partitionName></tt>_

    </div>

    Creates a new partition. If no partition type is specified, then a `wass` partition is created.

*   <div class="cmdsynopsis">

    `pm set` [_<tt><partitionName></tt>_] -_<tt><parameterName></tt>_ =_<tt><value></tt>_|off

    </div>

    Sets a parameter _<tt><parameterName></tt>_ to a new value.

    If _<tt><partitionName></tt>_ is omitted, the common shared set of parameters is updated. The value is used by any partition for which the parameter is not explicitly set.

    If a parameter is set to `off` then this parameter is no longer defined and is inherited from the common shared set of parameters, or a partition type specific default value is used if the parameter is not defined in the common set.

*   <div class="cmdsynopsis">

    `pm ls` [-l] [_<tt><partitionName></tt>_]

    </div>

    Lists a single or all partitions, including the type of each partition. If a partition name or the `-l` option are used, then the partition parameters are shown too. Inherited and default values are identified as such.

*   <div class="cmdsynopsis">

    `pm destroy` _<tt><partitionName></tt>_

    </div>

    Removes a partition from <span class="productname">dCache</span>. Any links configured to use this partition will fall back to the `default` partition.

</div>

</div>

<div class="section" title="Using Partitions">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-pm-pm-usingPartitions"></a>Using Partitions

</div>

</div>

</div>

A partition, so far, is just a set of parameters which may or may not differ from the default set. To let a partition relate to a part of the <span class="productname">dCache</span>, links are used. Each link may be assigned to exactly one partition. If not set, or the assigned partition doesn’t exist, the link defaults to the `default` partition.

<div class="cmdsynopsis">

`psu set link` [_<tt><linkName></tt>_] -section=_<tt><partitionName></tt>_ [_<tt><other-options></tt>_...]

</div>

Whenever this link is chosen for pool selection, the associated parameters of the assigned partition will become active for further processing.

<div class="warning" title="Warning" style="margin-left: 0.5in; margin-right: 0.5in;">

### Warning

Depending on the way links are setup it may very well happen that more than just one link is triggered for a particular <span class="productname">dCache</span> request. This is not illegal but leads to an ambiguity in selecting an appropriate <span class="productname">dCache</span> partition. If only one of the selected links has a partition assigned, this partition is chosen. Otherwise, if different links point to different partitions, the result is indeterminate. This issue is not yet solved and we recommend to clean up the `poolmanager` configuration to eliminate links with the same preferences for the same type of requests.

</div>

In the [Web Interface](#intouch-web "The Web Interface for Monitoring dCache") you can find a web page listing partitions and more information. You will find a page summarizing the partition status of the system. This is essentially the output of the command <span class="command">**pm ls -l**</span>.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

For your <span class="productname">dCache</span> on `dcache.example.org` the address is

`http://dcache.example.org:2288/poolInfo/parameterHandler/set/matrix/*`

</div>

</div>

<div class="section" title="Examples">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-pm-pm-examples"></a>Examples

</div>

</div>

</div>

For the subsequent examples we assume a basic `poolmanager` setup :

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">#
# define the units
#
psu create unit -protocol   */*
psu create unit -protocol   xrootd/*
psu create unit -net        0.0.0.0/0.0.0.0
psu create unit -net        131.169.0.0/255.255.0.0
psu create unit -store      *@*
#
#  define unit groups
#
psu create ugroup  any-protocol
psu create ugroup  any-store
psu create ugroup  world-net
psu create ugroup  xrootd
#
psu addto ugroup any-protocol */*
psu addto ugroup any-store    *@*
psu addto ugroup world-net    0.0.0.0/0.0.0.0
psu addto ugroup desy-net     131.169.0.0/255.255.0.0
psu addto ugroup xrootd       xrootd/*
#
#  define the pools
#
psu create pool pool1
psu create pool pool2
psu create pool pool3
psu create pool pool4

#
#  define the pool groups
#
psu create pgroup default-pools
psu create pgroup special-pools
#
psu addto pgroup default-pools pool1
psu addto pgroup default-pools pool2
#
psu addto pgroup special-pools pool3
psu addto pgroup special-pools pool4
#</pre>

</div>

</div>

<div class="section" title="Disallowing pool to pool transfers for special pool groups based on the access protocol">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="idp2104880"></a>Disallowing pool to pool transfers for special pool groups based on the access protocol

</div>

</div>

</div>

For a special set of pools, where we only allow the `xrootd` protocol, we don’t want the datasets to be replicated on high load while for the rest of the pools we allow replication on hot spot detection.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">#
pm create xrootd-section
#
pm set default        -p2p=0.4
pm set xrootd-section -p2p=0.0
#
psu create link default-link any-protocol any-store world-net
psu add    link default-link default-pools
psu set    link default-link -readpref=10 -cachepref=10 -writepref=0
#
psu create link xrootd-link xrootd any-store world-net
psu add    link xrootd-link special-pools
psu set    link xrootd-link -readpref=10 -cachepref=10 -writepref=0
psu set    link xrootd-link -section=xrootd-section
#        </pre>

</div>

</div>

</div>

<div class="section" title="Choosing pools randomly for incoming traffic only">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="idp2108960"></a>Choosing pools randomly for incoming traffic only

</div>

</div>

</div>

For a set of pools we select pools following the default setting of cpu and space related cost factors. For incoming traffic from outside, though, we select the same pools, but in a randomly distributed fashion. Please note that this is not really a physical partitioning of the <span class="productname">dCache</span> system, but rather a virtual one, applied to the same set of pools.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">#
pm create incoming-section
#
pm set default          -cpucostfactor=0.2 -spacecostfactor=1.0
pm set incoming-section -cpucostfactor=0.0 -spacecostfactor=0.0
#
psu create link default-link any-protocol any-store desy-net
psu add    link default-link default-pools
psu set    link default-link -readpref=10 -cachepref=10 -writepref=10
#
psu create link default-link any-protocol any-store world-net
psu add    link default-link default-pools
psu set    link default-link -readpref=10 -cachepref=10 -writepref=0
#
psu create link incoming-link any-protocol any-store world-net
psu add    link incoming-link default-pools
psu set    link incoming-link -readpref=10 -cachepref=10 -writepref=10
psu set    link incoming-link -section=incoming-section
#</pre>

</div>

</div>

</div>

</div>

</div>

<div class="section" title="Classic Partitions">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-pm-classic"></a>Classic Partitions

</div>

</div>

</div>

The `classic` partition type implements the load balancing policy known from <span class="productname">dCache</span> releases before version 2.0\. This partition type is still the default. This section describes this load balancing policy and the available configuration parameters.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

To create a classic partition use the command: <span class="command">**pm create**</span> -type=classic _<tt><partitionName></tt>_

</div>

</div>

<div class="section" title="Load Balancing Policy">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-pm-classic-policy"></a>Load Balancing Policy

</div>

</div>

</div>

From the allowable pools as determined by the [_pool selection unit_](#gl-pm-comp-psu), the pool manager determines the pool used for storing or reading a file by calculating a [_cost_](#gl-cost) value for each pool. The pool with the lowest cost is used.

If a client requests to read a file which is stored on more than one allowable pool, the [_performance costs_](#gl-performance_cost) are calculated for these pools. In short, this cost value describes how much the pool is currently occupied with transfers.

If a pool has to be selected for storing a file, which is either written by a client or [_restored_](#gl-restore) from a [_tape backend_](#gl-tape_backend), this performance cost is combined with a [_space cost_](#gl-space_cost) value to a [_total cost_](#gl-cost) value for the decision. The space cost describes how much it <span class="quote">“<span class="quote">hurts</span>”</span> to free space on the pool for the file.

The [_cost module_](#gl-pm-comp-cm) is responsible for calculating the cost values for all pools. The pools regularly send all necessary information about space usage and request queue lengths to the cost module. It can be regarded as a cache for all this information. This way it is not necessary to send <span class="quote">“<span class="quote">get cost</span>”</span> requests to the pools for each client request. The cost module interpolates the expected costs until a new precise information package is coming from the pools. This mechanism prevents clumping of requests.

Calculating the cost for a data transfer is done in two steps. First, the cost module merges all information about space and transfer queues of the pools to calculate the performance and space costs separately. Second, in the case of a write or stage request, these two numbers are merged to build the total cost for each pool. The first step is isolated within a separate loadable class. The second step is done by the partition.

</div>

<div class="section" title="The Performance Cost">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-pm-classic-perf"></a>The Performance Cost

</div>

</div>

</div>

The load of a pool is determined by comparing the current number of active and waiting _transfers_ to the maximum number of concurrent transfers allowed. This is done separately for each of the transfer types ([_store_](#gl-store), [_restore_](#gl-restore), pool-to-pool client, pool-to-pool server, and client request) with the following equation:

perfCost(per Type) = ( activeTransfers + waitingTransfers ) / maxAllowed .

The maximum number of concurrent transfers (<span class="symbol">maxAllowed</span>) can be configured with the commands [<span class="refentrytitle"><span class="command">**st set max active**</span></span>](#cmd-st_set_max_active "st set max active") (store), [<span class="refentrytitle"><span class="command">**rh set max active**</span></span>](#cmd-rh_set_max_active "rh set max active") (restore), [<span class="refentrytitle"><span class="command">**mover set max active**</span></span>](#cmd-mover_set_max_active "mover set max active") (client request), [<span class="refentrytitle"><span class="command">**mover set max active -queue=p2p**</span></span>](#cmd-p2p_set_max_active "mover set max active -queue=p2p") (pool-to-pool server), and [<span class="refentrytitle"><span class="command">**pp set max active**</span></span>](#cmd-pp_set_max_active "pp set max active") (pool-to-pool client).

Then the average is taken for each mover type where <span class="symbol">maxAllowed</span> is not zero. For a pool where store, restore and client transfers are allowed, e.g.,

perfCost(total) = ( perfCost(store) + perfCost(restore) + perfCost(client) ) / 3 ,

and for a read only pool:

perfCost(total) = ( perfCost(restore) + perfCost(client) ) / 2 .

For a well balanced system, the performance cost should not exceed 1.0.

</div>

<div class="section" title="The Space Cost">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-pm-classic-space"></a>The Space Cost

</div>

</div>

</div>

In this section only the new scheme for calculating the space cost will be described. Be aware, that the old scheme will be used if the [_breakeven parameter_](#gl-breakeven) of a pool is larger or equal 1.0.

The cost value used for determining a pool for storing a file depends either on the free space on the pool or on the age of the [_least recently used (LRU) file_](#gl-lru), which whould have to be deleted.

The space cost is calculated as follows:

<div class="informaltable">

<table border="0"><colgroup><col align="left" class="if"><col align="left" class="formula"><col align="left" class="and"><col align="left" class="formula"><col align="left" class="then"><col align="left" class="formula"></colgroup>

<tbody>

<tr>

<td align="left">If</td>

<td align="left">_freeSpace > gapPara_</td>

<td align="left">then</td>

<td align="left">_spaceCost = 3 * newFileSize / freeSpace_</td>

</tr>

<tr>

<td align="left">If</td>

<td align="left">_freeSpace <= gapPara_</td>

<td align="left">and</td>

<td align="left">_lruAge < 60_</td>

<td align="left">then</td>

<td align="left">_spaceCost = 1 + costForMinute_</td>

</tr>

<tr>

<td align="left">If</td>

<td align="left">_freeSpace <= gapPara_</td>

<td align="left">and</td>

<td align="left">_lruAge >= 60_</td>

<td align="left">then</td>

<td align="left">_spaceCost = 1 + costForMinute * 60 / lruAge_</td>

</tr>

</tbody>

</table>

</div>

where the variable names have the following meanings:

<div class="variablelist">

<dl>

<dt><span class="term">_freeSpace_</span></dt>

<dd>

The free space left on the pool

</dd>

<dt><span class="term">_newFileSize_</span></dt>

<dd>

The size of the file to be written to one of the pools, and at least 50MB.

</dd>

<dt><span class="term">_lruAge_</span></dt>

<dd>

The age of the [_least recently used file_](#gl-lru) on the pool.

</dd>

<dt><span class="term">_gapPara_</span></dt>

<dd>

The gap parameter. Default is 4 GiB. The size of free space below which it will be assumed that the pool is full and consequently the least recently used file has to be removed. If, on the other hand, the free space is greater than `gapPara`, it will be expensive to store a file on the pool which exceeds the free space.

It can be set per pool with the [<span class="refentrytitle"><span class="command">**set gap**</span></span>](#cmd-set_gap "set gap") command. This has to be done in the pool cell and not in the pool manager cell. Nevertheless it only influences the cost calculation scheme within the pool manager and not the bahaviour of the pool itself.

</dd>

<dt><span class="term">_costForMinute_</span></dt>

<dd>

A parameter which fixes the space cost of a one-minute-old LRU file to _(1 + costForMinute)_. It can be set with the [<span class="refentrytitle"><span class="command">**set breakeven**</span></span>](#cmd-set_breakeven "set breakeven"), where

costForMinute = breakeven * 7 * 24 * 60.

I.e. the the space cost of a one-week-old LRU file will be _(1 + breakeven)_. Note again, that all this only applies if _breakeven < 1.0_

</dd>

</dl>

</div>

The prescription above can be stated a little differently as follows:

<div class="informaltable">

<table border="0"><colgroup><col class="if"><col class="formula"><col class="then"><col class="formula2"></colgroup>

<tbody>

<tr>

<td>If</td>

<td>freeSpace > gapPara</td>

<td>then</td>

<td>spaceCost = 3 * newFileSize / freeSpace</td>

</tr>

<tr>

<td>If</td>

<td>freeSpace <= gapPara</td>

<td>then</td>

<td>spaceCost = 1 + breakeven * 7 * 24 * 60 * 60 / lruAge ,</td>

</tr>

</tbody>

</table>

</div>

where `newFileSize` is at least 50MB and `lruAge` at least one minute.

<div class="section" title="Rationale">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="idp2199184"></a>Rationale

</div>

</div>

</div>

As the last version of the formula suggests, a pool can be in two states: Either _freeSpace > gapPara_ or _freeSpace <= gapPara_ - either there is free space left to store files without deleting cached files or there isn’t.

Therefore, `gapPara` should be around the size of the smallest files which frequently might be written to the pool. If files smaller than `gapPara` appear very seldom or never, the pool might get stuck in the first of the two cases with a high cost.

If the LRU file is smaller than the new file, other files might have to be deleted. If these are much younger than the LRU file, this space cost calculation scheme might not lead to a selection of the optimal pool. However, in pratice this happens very seldomly and this scheme turns out to be very efficient.

</div>

</div>

<div class="section" title="The Total Cost">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-pm-classic-total"></a>The Total Cost

</div>

</div>

</div>

The total cost is a linear combination of the [_performance_](#gl-performance_cost) and [_space cost_](#gl-space_cost). I.e. totalCost = ccf * perfCost + scf * spaceCost , where `ccf` and `scf` are configurable with the command [<span class="refentrytitle"><span class="command">**set pool decision**</span></span>](#cmd-set_pool_decision "set pool decision"). E.g.,

    (PoolManager) admin >

will give the [_space cost_](#gl-space_cost) three times the weight of the [_performance cost_](#gl-performance_cost).

</div>

<div class="section" title="Parameters of Classic Partitions">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-pm-classic-parameters"></a>Parameters of Classic Partitions

</div>

</div>

</div>

Classic partitions have a large number of tunable parameters. These parameters are set using the <span class="command">**pm set**</span> command.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

To set the space cost factor on the `default` partition to `0.3`, use the following command:

<pre class="programlisting">                  <span class="command">**pm set**</span> default -spacecostfactor=0.3
              </pre>

</div>

</div>

<div class="informaltable">

<table border="1"><colgroup><col align="left"><col align="left"><col align="left"></colgroup>

<thead>

<tr>

<th align="left">Command</th>

<th align="left">Meaning</th>

<th align="left">Type</th>

</tr>

</thead>

<tbody>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -spacecostfactor=_<tt><scf></tt>_

</div>

</td>

<td align="left">

Sets the `space cost factor` for the partition.

The default value is `1.0`.

</td>

<td align="left">float</td>

</tr>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -cpucostfactor=_<tt><ccf></tt>_

</div>

</td>

<td align="left">

Sets the cpu cost factor for the partition.

The default value is `1.0`.

</td>

<td align="left">float</td>

</tr>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -idle=_<tt><idle-value></tt>_

</div>

</td>

<td align="left">

The concept of the _idle value_ will be turned on if _<tt><idle-value></tt>_ > `0.0`.

A pool is idle if its performance cost is smaller than the _<tt><idle-value></tt>_. Otherwise it is not idle.

If one or more pools that satisfy the read request are idle then only one of them is chosen for a particular file irrespective of total cost. I.e. if the same file is requested more than once it will always be taken from the same pool. This allowes the copies on the other pools to age and be garbage collected.

The default value is `0.0`, which disables this feature.

</td>

<td align="left">float</td>

</tr>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -p2p=_<tt><p2p-value></tt>_

</div>

</td>

<td align="left">

Sets the static replication threshold for the partition.

If the performance cost on the best pool exceeds _<tt><p2p-value></tt>_ and the value for [_<tt><slope></tt>_](#slope) = `0.0` then this pool is called _hot_ and a pool to pool replication may be triggered.

The default value is `0.0`, which disables this feature.

</td>

<td align="left">float</td>

</tr>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -alert=_<tt><value></tt>_

</div>

</td>

<td align="left">

Sets the _alert value_ for the partition.

If the best pool’s performance cost exceeds the p2p value and the alert value then no pool to pool copy is triggered and a message will be logged stating that no pool to pool copy will be made.

The default value is `0.0`, which disables this feature.

</td>

<td align="left">float</td>

</tr>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -panic=_<tt><value></tt>_

</div>

</td>

<td align="left">

Sets the _panic cost cut level_ for the partition.

If the performance cost of the best pool exceeds the panic cost cut level the request will fail.

The default value is `0.0`, which disables this feature.

</td>

<td align="left">float</td>

</tr>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -fallback=_<tt><value></tt>_

</div>

</td>

<td align="left">

Sets the fallback cost cut level for the partition.

If the best pool’s performance cost exceeds the fallback cost cut level then a pool of the next _level_ will be chosen. This means for example that instead of choosing a pool with `readpref` = 20 a pool with `readpref` < 20 will be chosen.

The default value is `0.0`, which disables this feature.

</td>

<td align="left">float</td>

</tr>

<tr>

<td align="left"><a name="slope"></a>

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -slope=_<tt><slope></tt>_

</div>

</td>

<td align="left">

Sets the dynamic replication threshold value for the partition.

If _<tt><slope></tt>_> `0.01` then the product of best pool’s performance cost and _<tt><slope></tt>_ is used as threshold for pool to pool replication.

If the performance cost on the best pool exceeds this threshold then this pool is called hot.

The default value is `0.0`, which disables this feature.

</td>

<td align="left">float</td>

</tr>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -p2p-allowed=_<tt><value></tt>_

</div>

</td>

<td align="left">

This value can be specified if an <abbr class="abbrev">HSM</abbr> is attached to the <span class="productname">dCache</span>.

If a partition has no <abbr class="abbrev">HSM</abbr> connected, then this option is overridden. This means that no matter which value is set for `p2p-allowed` the pool to pool replication will always be allowed.

By setting _<tt><value></tt>_ = `off` the values for `p2p-allowed`, `p2p-oncost` and `p2p-fortransfer` will take over the value of the default partition.

If _<tt><value></tt>_ = `yes` then pool to pool replication is allowed.

As a side effect of setting _<tt><value></tt>_ = `no` the values for `p2p-oncost` and `p2p-fortransfer` will also be set to `no`.

The default value is `yes`.

</td>

<td align="left">boolean</td>

</tr>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -p2p-oncost=_<tt><value></tt>_

</div>

</td>

<td align="left">

Determines whether pool to pool replication is allowed if the best pool for a read request is hot.

The default value is `no`.

</td>

<td align="left">boolean</td>

</tr>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -p2p-fortransfer=_<tt><value></tt>_

</div>

</td>

<td align="left">

If the best pool is hot and the requested file will be copied either from the hot pool or from tape to another pool, then the requested file will be read from the pool where it just had been copied to if _<tt><value></tt>_ = `yes`. If _<tt><value></tt>_ = `no` then the requested file will be read from the hot pool.

The default value is `no`.

</td>

<td align="left">boolean</td>

</tr>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -stage-allowed=_<tt><value></tt>_

</div>

</td>

<td align="left">

Set the _stage allowed value_ to `yes` if a tape system is connected and to `no` otherwise.

As a side effect, setting the value for `stage-allowed` to `no` changes the value for `stage-oncost` to `no`.

The default value is `no`.

</td>

<td align="left">boolean</td>

</tr>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -stage-oncost=_<tt><value></tt>_

</div>

</td>

<td align="left">

If the best pool is hot, p2p-oncost is disabled and an <abbr class="abbrev">HSM</abbr> is connected to a pool then this parameter determines whether to stage the requested file to a different pool.

The default value is `no`.

</td>

<td align="left">boolean</td>

</tr>

<tr>

<td align="left">

<div class="cmdsynopsis">

`pm set` [_<tt><partitionName></tt>_] -max-copies=_<tt><copies></tt>_

</div>

</td>

<td align="left">

Sets the maximal number of replicas of one file. If the maximum is reached no more replicas will be created.

The default value is `500`.

</td>

<td align="left">integer</td>

</tr>

</tbody>

</table>

</div>

</div>

</div>

</div>

<div class="section" title="Link Groups">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-pm-linkgroups"></a>Link Groups

</div>

</div>

</div>

The `PoolManager` supports a type of objects called _link groups_. These link groups are used by the [`SRM` `SpaceManager`](#cf-srm-space "SpaceManager configuration for Explicit Space Reservations") to make reservations against space. Each link group corresponds to a number of <span class="productname">dCache</span> pools in the following way: A link group is a collection of [links](#cf-pm-links "Links") and each link points to a set of pools. Each link group knows about the size of its available space, which is the sum of all sizes of available space in all the pools included in this link group.

To create a new link group login to the [Admin Interface](#intouch-admin "The Admin Interface") and <span class="command">**cd**</span> to the `PoolManager`.

    (local) admin >

With <span class="command">**save**</span> the changes will be saved to the file `<span>/var/lib/dcache/config/poolmanager.conf</span>`.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

You can also edit the file `<span>/var/lib/dcache/config/poolmanager.conf</span>` to create a new link group. Please make sure that it already exists. Otherwise you will have to create it first via the Admin Interface by

    (PoolManager) admin >

Edit the file `<span>/var/lib/dcache/config/poolmanager.conf</span>`

<pre class="screen"><span class="command">**psu create linkGroup**</span> _<tt><linkgroup></tt>_
<span class="command">**psu addto linkGroup**</span> _<tt><linkgroup></tt>_ _<tt><link></tt>_</pre>

After editing this file you will have to restart the domain which contains the `PoolManager` cell to apply the changes.

</div>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Administrators will have to take care, that no pool is present in more than one link group.

</div>

**Properties of [space reservation](#cf-srm-intro-spaceReservation "Properties of Space Reservation").** The <span class="productname">dCache</span> administrator can specify a _`RetentionPolicy`_ and an _`AccessLatency`_ for the space reservation, where `RetentionPolicy` describes the quality of the storage service that will be provided for the data (files) stored in this space reservation and `AccessLatency` describes the availability of this data.

A link group has five boolean properties called `replicaAllowed`, `outputAllowed`, `custodialAllowed`, `onlineAllowed` and `nearlineAllowed`. The values of these properties (`true` or `false`) can be configured via the Admin Interface or directly in the file `<span>/var/lib/dcache/config/poolmanager.conf</span>`.

The link groups contained in a space reservation match the `RetentionPolicy` and the `AccessLatency` of the space reservation.

    (PoolManager) admin >

Moreover an attribute can be assigned to a link group.

    (PoolManager) admin >

<div class="informalexample">

**Example:**

<div class="informalexamplebody">Possible assignments for attributes are:

    (PoolManager) admin >

</div>

</div>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Please note that that it is up to administrators that the link groups’ attributes are specified correctly.

For example <span class="productname">dCache</span> will not complain if the link group that does not support tape backend will be declared as one that supports `custodial`.

</div>

</div>

</div>

<div class="chapter" title="Chapter 8\. The dCache Tertiary Storage System Interface">

<div class="titlepage">

<div>

<div>

## <a name="cf-tss"></a>Chapter 8\. The <span class="productname">dCache</span> Tertiary Storage System Interface

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Introduction](#idp2428816)</span></dt>

<dt><span class="section">[Scope of this chapter](#idp2434560)</span></dt>

<dt><span class="section">[Requirements for a Tertiary Storage System](#cf-tss-hsm-requirements)</span></dt>

<dd>

<dl>

<dt><span class="section">[Migrating Tertiary Storage Systems with a file system interface.](#idp2446528)</span></dt>

<dt><span class="section">[Tertiary Storage Systems with a minimalistic `PUT`, `GET` and `REMOVE` interface](#idp2450656)</span></dt>

</dl>

</dd>

<dt><span class="section">[How <span class="productname">dCache</span> interacts with a Tertiary Storage System](#idp2459904)</span></dt>

<dt><span class="section">[Details on the <abbr class="abbrev">TSS</abbr>-support `executable`](#cf-tss-support)</span></dt>

<dd>

<dl>

<dt><span class="section">[Summary of command line options](#cf-tss-support-clo)</span></dt>

<dt><span class="section">[Summary of return codes](#cf-tss-support-return-codes)</span></dt>

<dt><span class="section">[The `executable` and the `STORE FILE` operation](#idp2584224)</span></dt>

<dt><span class="section">[The `executable` and the `FETCH FILE` operation](#idp2617184)</span></dt>

<dt><span class="section">[The `executable` and the `REMOVE FILE` operation](#idp2635248)</span></dt>

</dl>

</dd>

<dt><span class="section">[Configuring pools to interact with a Tertiary Storage System](#cf-tss-pools)</span></dt>

<dd>

<dl>

<dt><span class="section">[The <span class="productname">dCache</span> layout files](#cf-tss-pools-layout)</span></dt>

<dt><span class="section">[What happens next](#idp2720384)</span></dt>

</dl>

</dd>

<dt><span class="section">[How to Store-/Restore files via the Admin Interface](#cf-tss-pools-admin)</span></dt>

<dt><span class="section">[How to monitor what’s going on](#cf-tss-monitor)</span></dt>

<dd>

<dl>

<dt><span class="section">[Log Files](#cf-tss-monitor-log)</span></dt>

<dt><span class="section">[Obtain information via the <span class="productname">dCache</span> Command Line Admin Interface](#cf-tss-monitor-clAdmin)</span></dt>

</dl>

</dd>

<dt><span class="section">[Example of an `executable` to simulate a tape backend](#tss-executable)</span></dt>

</dl>

</div>

<div class="section" title="Introduction">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="idp2428816"></a>Introduction

</div>

</div>

</div>

One of the features <span class="productname">dCache</span> provides is the ability to migrate files from its disk repository to one or more connected Tertiary Storage Systems (<abbr class="abbrev">TSS</abbr>) and to move them back to disk when necessary. Although the interface between <span class="productname">dCache</span> and the <abbr class="abbrev">TSS</abbr> is kept simple, <span class="productname">dCache</span> assumes to interact with an intelligent <abbr class="abbrev">TSS</abbr>. <span class="productname">dCache</span> does not drive tape robots or tape drives by itself. More detailed requirements to the storage system are described in one of the subsequent paragraphs.

</div>

<div class="section" title="Scope of this chapter">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="idp2434560"></a>Scope of this chapter

</div>

</div>

</div>

This document describes how to enable a standard <span class="productname">dCache</span> installation to interact with a Tertiary Storage System. In this description we assume that

<div class="itemizedlist">

*   every <span class="productname">dCache</span> disk pool is connected to only one <abbr class="abbrev">TSS</abbr> instance.
*   all <span class="productname">dCache</span> disk pools are connected to the same <abbr class="abbrev">TSS</abbr> instance.
*   the <span class="productname">dCache</span> instance has not yet been populated with data, or only with a negligible amount of files.

</div>

In general, not all pools need to be configured to interact with the same Tertiary Storage System or with a storage system at all. Furthermore pools can be configured to have more than one Tertiary Storage System attached, but all those cases are not in the scope of the document.

</div>

<div class="section" title="Requirements for a Tertiary Storage System">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-tss-hsm-requirements"></a>Requirements for a Tertiary Storage System

</div>

</div>

</div>

<span class="productname">dCache</span> can only drive intelligent Tertiary Storage Systems. This essentially means that tape robot and tape drive operations must be done by the <abbr class="abbrev">TSS</abbr> itself and that there is some simple way to abstract the file `PUT`, `GET` and `REMOVE` operation.

<div class="section" title="Migrating Tertiary Storage Systems with a file system interface.">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp2446528"></a>Migrating Tertiary Storage Systems with a file system interface.

</div>

</div>

</div>

Most migrating storage systems provide a regular POSIX file system interface. Based on rules, data is migrated from primary to tertiary storage (mostly tape systems). Examples for migrating storage systems are:

<div class="itemizedlist">

*   [HPSS](http://www.hpss-collaboration.org/) (High Performance Storage System)
*   [DMF](http://www.sgi.com/products/storage/software/dmf.html) (Data Migration Facility)

</div>

</div>

<div class="section" title="Tertiary Storage Systems with a minimalistic PUT, GET and REMOVE interface">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp2450656"></a>Tertiary Storage Systems with a minimalistic `PUT`, `GET` and `REMOVE` interface

</div>

</div>

</div>

Some tape systems provide a simple `PUT`, `GET`, `REMOVE` interface. Typically, a copy-like application writes a disk file into the <abbr class="abbrev">TSS</abbr> and returns an identifier which uniquely identifies the written file within the Tertiary Storage System. The identifier is sufficient to get the file back to disk or to remove the file from the <abbr class="abbrev">TSS</abbr>. Examples are:

<div class="itemizedlist">

*   [OSM](http://www.qstar.com/qstar-products/qstar-object-storage-manager) (Object Storage Manager)
*   [Enstore](http://www-ccf.fnal.gov/enstore/) (FERMIlab)

</div>

</div>

</div>

<div class="section" title="How dCache interacts with a Tertiary Storage System">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="idp2459904"></a>How <span class="productname">dCache</span> interacts with a Tertiary Storage System

</div>

</div>

</div>

Whenever <span class="productname">dCache</span> decides to copy a file from disk to tertiary storage a user-provided [`executable`](#tss-executable "Example of an executable to simulate a tape backend") which can be either a script or a binary is automatically started on the pool where the file is located. That `executable` is expected to write the file into the Backend Storage System and to return a URI, uniquely identifying the file within that storage system. The format of the URI as well as the arguments to the `executable`, are described later in this document. The unique part of the URI can either be provided by the storage element, in return of the `STORE FILE` operation, or can be taken from <span class="productname">dCache</span>. A non-error return code from the `executable` lets <span class="productname">dCache</span> assume that the file has been successfully stored and, depending on the properties of the file, <span class="productname">dCache</span> can decide to remove the disk copy if space is running short on that pool. On a non-zero return from the `executable`, the file doesn’t change its state and the operation is retried or an error flag is set on the file, depending on the error [return code](#cf-tss-support-return-codes "Summary of return codes") from the `executable`.

If <span class="productname">dCache</span> needs to restore a file to disk the same `executable` is launched with a different set of arguments, including the URI, provided when the file was written to tape. It is in the responsibility of the `executable` to fetch the file back from tape based on the provided URI and to return `0` if the `FETCH FILE` operation was successful or non-zero otherwise. In case of a failure the pool retries the operation or <span class="productname">dCache</span> decides to fetch the file from tape using a different pool.

</div>

<div class="section" title="Details on the TSS-support executable">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-tss-support"></a>Details on the <abbr class="abbrev">TSS</abbr>-support `executable`

</div>

</div>

</div>

<div class="section" title="Summary of command line options">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-tss-support-clo"></a>Summary of command line options

</div>

</div>

</div>

This part explains the syntax of calling the `executable` that supports `STORE FILE`, `FETCH FILE` and `REMOVE FILE` operations.

<div class="cmdsynopsis">

`put` _<tt><pnfsID></tt>_ _<tt><filename></tt>_ -si=_<tt><storage-information></tt>_ [_<tt><other-options></tt>_...]

</div>

<div class="cmdsynopsis">

`get` _<tt><pnfsID></tt>_ _<tt><filename></tt>_ -si=_<tt><storage-information></tt>_ -uri=_<tt><storage-uri></tt>_ [_<tt><other-options></tt>_...]

</div>

<div class="cmdsynopsis">

`remove` -uri=_<tt><storage-uri></tt>_ [_<tt><other-options></tt>_...]

</div>

<div class="itemizedlist">

*   <span class="command">**put**</span> / <span class="command">**get**</span> / <span class="command">**remove**</span>: these keywords indicate the operation to be performed.

    <div class="itemizedlist">

    *   <span class="command">**put**</span>: copy file from disk to <abbr class="abbrev">TSS</abbr>.
    *   <span class="command">**get**</span>: copy file back from <abbr class="abbrev">TSS</abbr> to disk.
    *   <span class="command">**remove**</span>: remove the file from <abbr class="abbrev">TSS</abbr>.

    </div>

*   _<tt><[pnfsID](#cf-chimera-ids "IDs")></tt>_: The internal identifier (i-node) of the file within <span class="productname">dCache</span>. The _<tt><pnfsID></tt>_ is unique within a single <span class="productname">dCache</span> instance and globally unique with a very high probability.
*   _<tt><filename></tt>_: is the full path of the local file to be copied to the <abbr class="abbrev">TSS</abbr> (for <span class="command">**put**</span>) and respectively into which the file from the <abbr class="abbrev">TSS</abbr> should be copied (for <span class="command">**get**</span>).
*   _<tt><storage-information></tt>_: the storage information of the file, as explained [below](#cf-tss-support-storage-info "Storage Information").
*   [_<tt><storage-uri></tt>_](#cf-tss-support-storage-uri "Storage URI"): the URI, which was returned by the `executable`, after the file was written to tertiary storage. In order to get the file back from the <abbr class="abbrev">TSS</abbr> the information of the URI is preferred over the information in the _<tt><storage-information></tt>_.
*   _<tt><other-options></tt>_: -_<tt><key></tt>_ = _<tt><value></tt>_ pairs taken from the <abbr class="abbrev">TSS</abbr> configuration commands of the pool 'setup' file. One of the options, always provided is the option -command=_<tt><full path of this `executable`></tt>_.

</div>

<div class="section" title="Storage Information">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-tss-support-storage-info"></a>Storage Information

</div>

</div>

</div>

The _<tt><storage-information></tt>_ is a string in the format

<pre class="programlisting">-si=size=_<tt><bytes></tt>_;new=_<tt><true/false></tt>_;stored=_<tt><true/false></tt>_;sClass=_<tt><StorageClass></tt>_;\
cClass0_<tt><CacheClass></tt>_;hsm=_<tt><StorageType></tt>_;_<tt><key></tt>_=_<tt><value></tt>_;[_<tt><key></tt>_=_<tt><value></tt>_;[...]]</pre>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">-si=size=1048576000;new=true;stored=false;sClass=desy:cms-sc3;cClass=-;hsm=osm;Host=desy;</pre>

</div>

</div>

<div class="itemizedlist" title="Mandatory storage information’s keys">

**Mandatory storage information’s keys**

*   _<tt><size></tt>_: Size of the file in bytes
*   _<tt><new></tt>_: <span class="emphasis">_False_</span> if file already in the <span class="productname">dCache</span>; <span class="emphasis">_True_</span> otherwise
*   _<tt><stored></tt>_: <span class="emphasis">_True_</span> if file already stored in the <abbr class="abbrev">TSS</abbr>; <span class="emphasis">_False_</span> otherwise
*   _<tt><sClass></tt>_: <abbr class="abbrev">HSM</abbr> depended, is used by the `poolmanager` for pool attraction.
*   _<tt><cClass></tt>_: Parent directory tag (cacheClass). Used by the `poolmanager` for pool attraction. May be '-'.
*   _<tt><hsm></tt>_: Storage manager name (enstore/osm). Can be overwritten by the parent directory tag (hsmType).

</div>

<div class="itemizedlist" title="OSM specific storage information’s keys">

**OSM specific storage information’s keys**

*   _<tt><group></tt>_: The storage group of the file to be stored as specified in the ".(tag)(sGroup)" tag of the parent directory of the file to be stored.
*   _<tt><store></tt>_: The store name of the file to be stored as specified in the ".(tag)(OSMTemplate)" tag of the parent directory of the file to be stored.
*   _<tt><bfid></tt>_: Bitfile ID (get and remove only) (e.g. 000451243.2542452542.25424524)

</div>

<div class="itemizedlist" title="Enstore specific storage information’s keys">

**Enstore specific storage information’s keys**

*   _<tt><group></tt>_: The storage group (e.g. cdf, cms ...)
*   _<tt><family></tt>_: The file family (e.g. sgi2test, h6nxl8, ...)
*   _<tt><bfid></tt>_: Bitfile ID (get only) (e.g. B0MS105746894100000)
*   _<tt><volume></tt>_: Tape Volume (get only) (e.g. IA6912)
*   _<tt><location></tt>_: Location on tape (get only) (e.g. : 0000_000000000_0000117)

</div>

There might be more key values pairs which are used by the <span class="productname">dCache</span> internally and which should not affect the behaviour of the `executable`.

</div>

<div class="section" title="Storage URI">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-tss-support-storage-uri"></a>Storage URI

</div>

</div>

</div>

The _<tt><storage-uri></tt>_ is formatted as follows:

    hsmType://hsmInstance/?store=<storename>&group=<groupname>&bfid=<bfid>

<div class="itemizedlist">

*   _<tt><hsmType></tt>_: The type of the Tertiary Storage System
*   _<tt><hsmInstance></tt>_: The name of the instance
*   _<tt><storename></tt>_ and _<tt><groupname></tt>_ : The store and group name of the file as provided by the arguments to this `executable`.
*   _<tt><bfid></tt>_: The unique identifier needed to restore or remove the file if necessary.

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

A storage-uri:

    osm://osm/?store=sql&group=chimera&bfid=3434.0.994.1188400818542

</div>

</div>

</div>

</div>

<div class="section" title="Summary of return codes">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-tss-support-return-codes"></a>Summary of return codes

</div>

</div>

</div>

<div class="informaltable">

<table border="1"><colgroup><col align="left"><col align="left"><col align="left"><col align="left"></colgroup>

<thead>

<tr>

<th align="left">Return Code</th>

<th align="left">Meaning</th>

<th align="left">Behaviour for PUT FILE</th>

<th align="left">Behaviour for GET FILE</th>

</tr>

</thead>

<tbody>

<tr>

<td align="left">30 <= rc < 40</td>

<td align="left">User defined</td>

<td align="left">Deactivates request</td>

<td align="left">Reports problem to `poolmanager`</td>

</tr>

<tr>

<td align="left">41</td>

<td align="left">No space left on device</td>

<td align="left">Pool retries</td>

<td align="left">Disables pool and reports problem to `poolmanager`</td>

</tr>

<tr>

<td align="left">42</td>

<td align="left">Disk read I/O error</td>

<td align="left">Pool retries</td>

<td align="left">Disables pool and reports problem to `poolmanager`</td>

</tr>

<tr>

<td align="left">43</td>

<td align="left">Disk write I/O error</td>

<td align="left">Pool retries</td>

<td align="left">Disables pool and reports problem to `poolmanager`</td>

</tr>

<tr>

<td align="left">other</td>

<td align="left">-</td>

<td align="left">Pool retries</td>

<td align="left">Reports problem to `poolmanager`</td>

</tr>

</tbody>

</table>

</div>

</div>

<div class="section" title="The executable and the STORE FILE operation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp2584224"></a>The `executable` and the `STORE FILE` operation

</div>

</div>

</div>

Whenever a disk file needs to be copied to a Tertiary Storage System <span class="productname">dCache</span> automatically launches an `executable` on the pool containing the file to be copied. Exactly one instance of the `executable` is started for each file. Multiple instances of the `executable` may run concurrently for different files. The maximum number of concurrent instances of the ``executable`s` per pool as well as the full path of the `executable` can be configured in the ’setup’ file of the pool as described in [the section called “The pool ’setup’ file”](#cf-tss-pools-layout-setup "The pool ’setup’ file").

The following arguments are given to the `executable` of a `STORE FILE` operation on startup.

<div class="cmdsynopsis">

`put` _<tt><pnfsID></tt>_ _<tt><filename></tt>_ -si=_<tt><storage-information></tt>_ _<tt><more options></tt>_

</div>

Details on the meaning of certain arguments are described in [the section called “Summary of command line options”](#cf-tss-support-clo "Summary of command line options").

With the arguments provided the `executable` is supposed to copy the file into the Tertiary Storage System. The `executable` must not terminate before the transfer of the file was either successful or failed.

Success must be indicated by a `0` return of the `executable`. All non-zero values are interpreted as a failure which means, <span class="productname">dCache</span> assumes that the file has not been copied to tape.

In case of a `0` return code the `executable` has to return a valid storage URI to <span class="productname">dCache</span> in formate:

    hsmType://hsmInstance/?store=<storename>&group=<groupname>&bfid=<bfid>

Details on the meaning of certain parameters are described [above](#cf-tss-support-storage-uri "Storage URI").

The _<tt><bfid></tt>_ can either be provided by the <abbr class="abbrev">TSS</abbr> as result of the `STORE FILE` operation or the `pnfsID` may be used. The latter assumes that the file has to be stored with exactly that `pnfsID` within the <abbr class="abbrev">TSS</abbr>. Whatever URI is chosen, it must allow to uniquely identify the file within the Tertiary Storage System.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Only the URI must be printed to stdout by the `executable`. Additional information printed either before or after the URI will result in an error. stderr can be used for additional debug information or error messages.

</div>

</div>

<div class="section" title="The executable and the FETCH FILE operation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp2617184"></a>The `executable` and the `FETCH FILE` operation

</div>

</div>

</div>

Whenever a disk file needs to be restored from a Tertiary Storage System <span class="productname">dCache</span> automatically launches an `executable` on the pool containing the file to be copied. Exactly one instance of the `executable` is started for each file. Multiple instances of the `executable` may run concurrently for different files. The maximum number of concurrent instances of the `executable` per pool as well as the full path of the `executable` can be configured in the ’setup’ file of the pool as described in [the section called “The pool ’setup’ file”](#cf-tss-pools-layout-setup "The pool ’setup’ file").

The following arguments are given to the `executable` of a `FETCH FILE` operation on startup:

<div class="cmdsynopsis">

`get` _<tt><pnfsID></tt>_ _<tt><filename></tt>_ -si=_<tt><storage-information></tt>_ -uri=_<tt><storage-uri></tt>_ _<tt><more options></tt>_

</div>

Details on the meaning of certain arguments are described in [the section called “Summary of command line options”](#cf-tss-support-clo "Summary of command line options"). For return codes see [the section called “Summary of return codes”](#cf-tss-support-return-codes "Summary of return codes").

</div>

<div class="section" title="The executable and the REMOVE FILE operation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp2635248"></a>The `executable` and the `REMOVE FILE` operation

</div>

</div>

</div>

Whenever a file is removed from the <span class="productname">dCache</span> namespace (file system) a process inside <span class="productname">dCache</span> makes sure that all copies of the file are removed from all internal and external media. The pool which is connected to the <abbr class="abbrev">TSS</abbr> which stores the file is activating the `executable` with the following command line options:

<div class="cmdsynopsis">

`remove` -uri=_<tt><storage-uri></tt>_ _<tt><more options></tt>_

</div>

Details on the meaning of certain arguments are described in [the section called “Summary of command line options”](#cf-tss-support-clo "Summary of command line options"). For return codes see [the section called “Summary of return codes”](#cf-tss-support-return-codes "Summary of return codes").

The `executable` is supposed to remove the file from the <abbr class="abbrev">TSS</abbr> and report a zero return code. If a non-zero error code is returned, the <span class="productname">dCache</span> will call the script again at a later point in time.

</div>

</div>

<div class="section" title="Configuring pools to interact with a Tertiary Storage System">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-tss-pools"></a>Configuring pools to interact with a Tertiary Storage System

</div>

</div>

</div>

The `executable` interacting with the Tertiary Storage System (<abbr class="abbrev">TSS</abbr>), as described in the chapter above, has to be provided to <span class="productname">dCache</span> on all pools connected to the <abbr class="abbrev">TSS</abbr>. The `executable`, either a script or a binary, has to be made <span class="quote">“<span class="quote">executable</span>”</span> for the user, <span class="productname">dCache</span> is running as, on that host.

The following files have to be modified to allow <span class="productname">dCache</span> to interact with the <abbr class="abbrev">TSS</abbr>.

<div class="itemizedlist">

*   The `<span>/var/lib/dcache/config/poolmanager.conf</span>` file (one per system)
*   The pool layout file (one per pool host)
*   The pool 'setup' file (one per pool)
*   The namespaceDomain layout file (one per system)

</div>

After the layout files and the various ’setup’ files have been corrected, the following domains have to be restarted :

<div class="itemizedlist">

*   pool services
*   dCacheDomain
*   namespaceDomain

</div>

<div class="section" title="The dCache layout files">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-tss-pools-layout"></a>The <span class="productname">dCache</span> layout files

</div>

</div>

</div>

<div class="section" title="The /var/lib/dcache/config/poolmanager.conf file">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp2662592"></a>The `<span>/var/lib/dcache/config/poolmanager.conf</span>` file

</div>

</div>

</div>

To be able to read a file from the tape in case the cached file has been deleted from all pools, enable the restore-option. The best way to do this is to log in to the Admin Interface and run the following commands:

<pre class="programlisting">[example.dcache.org] `(local) admin >` cd `PoolManager`
[example.dcache.org] `(PoolManager) admin >` pm set -stage-allowed=yes
[example.dcache.org] `(PoolManager) admin >` save</pre>

A restart of the `dCacheDomain` is not necessary in this case.

Alternatively, if the file `<span>/var/lib/dcache/config/poolmanager.conf</span>` already exists then you can add the entry

<pre class="programlisting">pm set -stage allowed=yes</pre>

and restart the `dCacheDomain`.

<div class="warning" title="Warning" style="margin-left: 0.5in; margin-right: 0.5in;">

### Warning

Do not create the file `<span>/var/lib/dcache/config/poolmanager.conf</span>` with this single entry! This will result in an error.</div>

</div>

<div class="section" title="The pool layout">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp2675008"></a>The pool layout

</div>

</div>

</div>

The <span class="productname">dCache</span> layout file must be modified for each pool node connected to a <abbr class="abbrev">TSS</abbr>. If your pool nodes have been configured correctly to work without <abbr class="abbrev">TSS</abbr>, you will find the entry `lfs=precious` in the layout file (that is located in `<span>/etc/dcache</span>/layouts` and in the file `<span>/etc/dcache</span>/dcache.conf` respectively) for each pool service. This entry is a disk-only-option and has to be removed for each pool which should be connected to a <abbr class="abbrev">TSS</abbr>. This will default the `lfs` parameter to `hsm` which is exactly what we need.

</div>

<div class="section" title="The pool ’setup’ file">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-tss-pools-layout-setup"></a>The pool ’setup’ file

</div>

</div>

</div>

The pool ’setup’ file is the file `$poolHomeDir/$poolName/setup`. It mainly defines 3 details related to <abbr class="abbrev">TSS</abbr> connectivity.

<div class="itemizedlist">

*   Pointer to the `executable` which is launched on storing and fetching files.
*   The maximum number of concurrent `STORE FILE` requests allowed per pool.
*   The maximum number of concurrent `FETCH FILE` requests allowed per pool.

</div>

Define the `executable` and Set the maximum number of concurrent `PUT` and `GET` operations:

<pre class="programlisting">hsm set _<tt><hsmType></tt>_ [_<tt><hsmInstanceName></tt>_] [-command=_<tt></path/to/executable></tt>_] [-key=_<tt><value></tt>_]

#
#  PUT operations
# set the maximum number of active PUT operations >= 1
#
st set max active _<tt><numberOfConcurrentPUTS></tt>_

#
# GET operations
# set the maximum number of active GET operations >= 1
#
rh set max active _<tt><numberOfConcurrentGETs></tt>_</pre>

<div class="itemizedlist">

*   _<tt><hsmType></tt>_: the type ot the <abbr class="abbrev">TSS</abbr> system. Must be set to <span class="quote">“<span class="quote">osm</span>”</span> for basic setups.
*   _<tt><hsmInstanceName></tt>_: the instance name of the <abbr class="abbrev">TSS</abbr> system. Must be set to <span class="quote">“<span class="quote">osm</span>”</span> for basic setups.
*   _<tt></path/to/executable></tt>_: the full path to the `executable` which should be launched for each <abbr class="abbrev">TSS</abbr> operation.

</div>

Setting the maximum number of concurrent `PUT` and `GET` operations.

Both numbers must be non zero to allow the pool to perform transfers.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

We provide a [script](#tss-executable "Example of an executable to simulate a tape backend") to simulate a connection to a <abbr class="abbrev">TSS</abbr>. To use this script place it in the directory `<span>/usr/share/dcache/lib</span>`, and create a directory to simulate the base of the <abbr class="abbrev">TSS</abbr>.

    [root] #

Login to the Admin Interface to change the entry of the pool ’setup’ file for a pool named pool_1.

    (local) admin >

</div>

</div>

</div>

<div class="section" title="The namespace layout">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp2716560"></a>The namespace layout

</div>

</div>

</div>

In order to allow <span class="productname">dCache</span> to remove files from attached <abbr class="abbrev">TSS</abbr>es, the <span class="quote">“<span class="quote">cleaner.enable.hsm = true</span>”</span> must be added immediately underneath the [namespaceDomain/cleaner] service declaration:

<pre class="programlisting">[namespaceDomain]
 ... other services ...
[namespaceDomain/cleaner]
cleaner.enable.hsm = true
.. more ...</pre>

</div>

</div>

<div class="section" title="What happens next">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp2720384"></a>What happens next

</div>

</div>

</div>

After restarting the necessary <span class="productname">dCache</span> domains, pools, already containing files, will start transferring them into the <abbr class="abbrev">TSS</abbr> as those files only have a disk copy so far. The number of transfers is determined by the configuration in the pool ’setup’ file as described above in [the section called “The pool ’setup’ file”](#cf-tss-pools-layout-setup "The pool ’setup’ file").

</div>

</div>

<div class="section" title="How to Store-/Restore files via the Admin Interface">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-tss-pools-admin"></a>How to Store-/Restore files via the Admin Interface

</div>

</div>

</div>

In order to see the state of files within a pool, login into the pool in the admin interface and run the command <span class="command">**rep ls**</span>.

<pre class="programlisting">[example.dcache.org] `(_<tt><poolname></tt>_) admin >` rep ls</pre>

The output will have the following format:

<pre class="programlisting">PNFSID <MODE-BITS(LOCK-TIME)[OPEN-COUNT]> SIZE si={STORAGE-CLASS}</pre>

<div class="itemizedlist">

*   PNFSID: The <span class="productname">`pnfs`</span>ID of the file
*   MODE-BITS:

    <pre class="programlisting">   CPCScsRDXEL
       |||||||||||
       ||||||||||+--  (L) File is locked (currently in use)
       |||||||||+---  (E) File is in error state
       ||||||||+----  (X) File is pinned (aka "sticky")
       |||||||+-----  (D) File is in process of being destroyed
       ||||||+------  (R) File is in process of being removed
       |||||+-------  (s) File sends data to back end store
       ||||+--------  (c) File sends data to client (`dCap`,`FTP`...)
       |||+---------  (S) File receives data from back end store
       ||+----------  (C) File receives data from client (`dCap`,`FTP`)
       |+-----------  (P) File is precious, i.e., it is only on disk
       +------------  (C) File is on tape and only cached on disk.</pre>

*   LOCK-TIME: The number of milli-seconds this file will still be locked. Please note that this is an internal lock and not the pin-time (`SRM`).
*   OPEN-COUNT: Number of clients currently reading this file.
*   SIZE: File size
*   STORAGE-CLASS: The storage class of this file.

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">[example.dcache.org] `(pool_1) admin >` rep ls
00008F276A952099472FAD619548F47EF972 <-P---------L(0)[0]> 291910 si={dteam:STATIC}
00002A9282C2D7A147C68A327208173B81A6 <-P---------L(0)[0]> 2011264 si={dteam:STATIC}
0000EE298D5BF6BB4867968B88AE16BA86B0 <C----------L(0)[0]> 1976 si={dteam:STATIC}</pre>

</div>

</div>

In order to `flush` a file to the tape run the command <span class="command">**flush pnfsid**</span>.

<pre class="programlisting">[example.dcache.org] `(_<tt><poolname></tt>_) admin >` flush pnfsid _<tt><pnfsid></tt>_</pre>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">[example.dcache.org] `(pool_1) admin >` flush pnfsid 00002A9282C2D7A147C68A327208173B81A6
Flush Initiated</pre>

</div>

</div>

A file that has been flushed to tape gets the flag ’C’.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">[example.dcache.org] `(pool_1) admin >` rep ls
00008F276A952099472FAD619548F47EF972 <-P---------L(0)[0]> 291910 si={dteam:STATIC}
00002A9282C2D7A147C68A327208173B81A6 <C----------L(0)[0]> 2011264 si={dteam:STATIC}
0000EE298D5BF6BB4867968B88AE16BA86B0 <C----------L(0)[0]> 1976 si={dteam:STATIC}</pre>

</div>

</div>

To remove such a file from the repository run the command <span class="command">**rep rm**</span>.

<pre class="programlisting">[example.dcache.org] `(_<tt><poolname></tt>_) admin >` rep rm _<tt><pnfsid></tt>_</pre>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">[example.dcache.org] `(pool_1) admin >` rep rm  00002A9282C2D7A147C68A327208173B81A6
Removed 00002A9282C2D7A147C68A327208173B81A6</pre>

</div>

</div>

In this case the file will be restored when requested.

To `restore` a file from the tape you can simply request it by initializing a reading transfer or you can fetch it by running the command <span class="command">**rh restore**</span>.

<pre class="programlisting">[example.dcache.org] `(_<tt><poolname></tt>_) admin >` rh restore [-block] _<tt><pnfsid></tt>_</pre>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">[example.dcache.org] `(pool_1) admin >` rh restore 00002A9282C2D7A147C68A327208173B81A6
Fetch request queued</pre>

</div>

</div>

</div>

<div class="section" title="How to monitor what’s going on">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-tss-monitor"></a>How to monitor what’s going on

</div>

</div>

</div>

This section briefly describes the commands and mechanisms to monitor the <abbr class="abbrev">TSS</abbr> `PUT`, `GET` and `REMOVE` operations. <span class="productname">dCache</span> provides a configurable logging facility and a Command Line Admin Interface to query and manipulate transfer and waiting queues.

<div class="section" title="Log Files">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-tss-monitor-log"></a>Log Files

</div>

</div>

</div>

By default <span class="productname">dCache</span> is configured to only log information if something unexpected happens. However, to get familiar with Tertiary Storage System interactions you might be interested in more details. This section provides advice on how to obtain this kind of information.

<div class="section" title="The executable log file">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp2768576"></a>The `executable` log file

</div>

</div>

</div>

Since you provide the `executable`, interfacing <span class="productname">dCache</span> and the <abbr class="abbrev">TSS</abbr>, it is in your responsibility to ensure sufficient logging information to be able to trace possible problems with either <span class="productname">dCache</span> or the <abbr class="abbrev">TSS</abbr>. Each request should be printed with the full set of parameters it receives, together with a timestamp. Furthermore information returned to <span class="productname">dCache</span> should be reported.

</div>

<div class="section" title="dCache log files in general">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp2774480"></a><span class="productname">dCache</span> log files in general

</div>

</div>

</div>

In <span class="productname">dCache</span>, each domain (e.g. `dCacheDomain`, `_<tt><pool></tt>_Domain` etc) prints logging information into its own log file named after the domain. The location of those log files it typically the `/var/log` or `/var/log/dCache` directory depending on the individual configuration. In the default logging setup only errors are reported. This behavior can be changed by either modifying `<span>/etc/dcache</span>/logback.xml` or using the <span class="productname">dCache</span> CLI to increase the log level of particular components as described [below](#cf-tss-monitor-log-cli "Increase the dCache log level via the Command Line Admin Interface").

<div class="section" title="Increase the dCache log level by changes in /etc/dcache/logback.xml">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="idp2783552"></a>Increase the <span class="productname">dCache</span> log level by changes in `<span>/etc/dcache</span>/logback.xml`

</div>

</div>

</div>

If you intend to increase the log level of all components on a particular host you would need to change the `<span>/etc/dcache</span>/logback.xml` file as described below. <span class="productname">dCache</span> components need to be restarted to activate the changes.

<pre class="programlisting"><threshold>
     <appender>stdout</appender>
     <logger>root</logger>
     <level>warn</level>
   </threshold>
</pre>

needs to be changed to

<pre class="programlisting"><threshold>
     <appender>stdout</appender>
     <logger>root</logger>
     <level>info</level>
   </threshold></pre>

<div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

### Important

The change might result in a significant increase in log messages. So don’t forget to change back before starting production operation. The next section describes how to change the log level in a running system.

</div>

</div>

<div class="section" title="Increase the dCache log level via the Command Line Admin Interface">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-tss-monitor-log-cli"></a>Increase the <span class="productname">dCache</span> log level via the Command Line Admin Interface

</div>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Login into the <span class="productname">dCache</span> Command Line Admin Interface and increase the log level of a particular service, for instance for the `poolmanager` service:

<pre class="programlisting">[example.dcache.org] `(local) admin >` cd PoolManager
[example.dcache.org] `(PoolManager) admin >` log set stdout ROOT INFO
[example.dcache.org] `(PoolManager) admin >` log ls
stdout:
  ROOT=INFO
  dmg.cells.nucleus=WARN*
  logger.org.dcache.cells.messages=ERROR*
.....</pre>

</div>

</div>

</div>

</div>

</div>

<div class="section" title="Obtain information via the dCache Command Line Admin Interface">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-tss-monitor-clAdmin"></a>Obtain information via the <span class="productname">dCache</span> Command Line Admin Interface

</div>

</div>

</div>

The <span class="productname">dCache</span> Command Line Admin Interface gives access to information describing the process of storing and fetching files to and from the <abbr class="abbrev">TSS</abbr>, as there are:

<div class="itemizedlist">

*   The _Pool Manager Restore Queue_. A list of all requests which have been issued to all pools for a `FETCH FILE` operation from the <abbr class="abbrev">TSS</abbr> (rc ls)
*   The _Pool Collector Queue_. A list of files, per pool and storage group, which will be scheduled for a `STORE FILE` operation as soon as the configured trigger criteria match.
*   The _Pool `STORE FILE` Queue_. A list of files per pool, scheduled for the `STORE FILE` operation. A configurable amount of requests within this queue are active, which is equivalent to the number of concurrent store processes, the rest is inactive, waiting to become active.
*   The _Pool `FETCH FILE` Queue_. A list of files per pool, scheduled for the `FETCH FILE` operation. A configurable amount of requests within this queue are active, which is equivalent to the number of concurrent fetch processes, the rest is inactive, waiting to become active.

</div>

For evaluation purposes, the _pinboard_ of each component can be used to track down <span class="productname">dCache</span> behavior. The pinboard only keeps the most recent 200 lines of log information but reports not only errors but informational messages as well.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Check the pinboard of a service, here the `poolmanager` service.

<pre class="programlisting">[example.dcache.org] `(local) admin >` cd PoolManager
[example.dcache.org] `(PoolManager) admin >` show pinboard 100
08.30.45  [Thread-7] [pool_1 PoolManagerPoolUp] sendPoolStatusRelay: ...
08.30.59  [writeHandler] [NFSv41-dcachetogo PoolMgrSelectWritePool ...
....</pre>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

**The `PoolManager` Restore Queue.** Remove the file `test.root` with the <span class="productname">`pnfs`</span>-ID 00002A9282C2D7A147C68A327208173B81A6.

    [example.dcache.org] (pool_1) admin >

Request the file `test.root`

    [user] $

Check the `PoolManager` Restore Queue:

<pre class="programlisting">[example.dcache.org] `(local) admin >` cd PoolManager
[example.dcache.org] `(PoolManager) admin >` rc ls
0000AB1260F474554142BA976D0ADAF78C6C@0.0.0.0/0.0.0.0-*/* m=1 r=0 [pool_1] [Staging 08.15 17:52:16] {0,}</pre>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

**The Pool Collector Queue.**

<pre class="programlisting">[example.dcache.org] `(local) admin >` cd pool_1
[example.dcache.org] `(pool_1) admin >` queue ls -l queue
                   Name: chimera:alpha
              Class@Hsm: chimera:alpha@osm
 Expiration rest/defined: -39 / 0   seconds
 Pending   rest/defined: 1 / 0
 Size      rest/defined: 877480 / 0
 Active Store Procs.   :  0
  00001BC6D76570A74534969FD72220C31D5D

[example.dcache.org] `(pool_1) admin >` flush ls
Class                 Active   Error  Last/min  Requests    Failed
dteam:STATIC@osm           0       0         0         1         0</pre>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

**The pool `STORE FILE` Queue.**

<pre class="programlisting">[example.dcache.org] `(local) admin >` cd pool_1
[example.dcache.org] `(pool_1) admin >` st ls
0000EC3A4BFCA8E14755AE4E3B5639B155F9  1   Fri Aug 12 15:35:58 CEST 2011</pre>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

**The pool `FETCH FILE` Queue.**

<pre class="programlisting">[example.dcache.org] `(local) admin >` cd pool_1
[example.dcache.org] `(pool_1) admin >`  rh ls
0000B56B7AFE71C14BDA9426BBF1384CA4B0  0   Fri Aug 12 15:38:33 CEST 2011</pre>

</div>

</div>

To check the repository on the pools run the command <span class="command">**rep ls**</span> that is described in the beginning of [the section called “How to Store-/Restore files via the Admin Interface”](#cf-tss-pools-admin "How to Store-/Restore files via the Admin Interface").

</div>

</div>

<div class="section" title="Example of an executable to simulate a tape backend">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="tss-executable"></a>Example of an `executable` to simulate a tape backend

</div>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">#!/bin/sh
#
#set -x
#
logFile=/tmp/hsm.log
#
################################################################
#
#  Some helper functions
#
##.........................................
#
# print usage
#
usage() {
   echo "Usage : put|get <pnfsId> <filePath> [-si=<storageInfo>] [-key[=value] ...]" 1>&2
}
##.........................................
#
#
printout() {
#---------
   echo "$pnfsid : $1" >>${logFile}
   return 0
}
##.........................................
#
#  print error into log file and to stdout.
#
printerror() {
#---------

   if [ -z "$pnfsid" ] ; then
#      pp="000000000000000000000000000000000000"
      pp="------------------------------------"
   else
      pp=$pnfsid
   fi

   echo "$pp : (E) : $*" >>${logFile}
   echo "$pp : $*" 1>&2

}
##.........................................
#
#  find a key in the storage info
#
findKeyInStorageInfo() {
#-------------------

   result=`echo $si  | awk  -v hallo=$1 -F\; '{ for(i=1;i<=NF;i++){ split($i,a,"=") ; if( a[1] == hallo )print a[2]} }'`
   if [ -z "$result" ] ; then return 1 ; fi
   echo $result
   exit 0

}
##.........................................
#
#  find a key in the storage info
#
printStorageInfo() {
#-------------------
   printout "storageinfo.StoreName : $storeName"
   printout "storageinfo.store : $store"
   printout "storageinfo.group : $group"
   printout "storageinfo.hsm   : $hsmName"
   printout "storageinfo.accessLatency   : $accessLatency"
   printout "storageinfo.retentionPolicy : $retentionPolicy"
   return 0
}
##.........................................
#
#  assign storage info the keywords
#
assignStorageInfo() {
#-------------------

    store=`findKeyInStorageInfo "store"`
    group=`findKeyInStorageInfo "group"`
    storeName=`findKeyInStorageInfo "StoreName"`
    hsmName=`findKeyInStorageInfo "hsm"`
    accessLatency=`findKeyInStorageInfo "accessLatency"`
    retentionPolicy=`findKeyInStorageInfo "retentionPolicy"`
    return 0
}
##.........................................
#
# split the arguments into the options -<key>=<value> and the
# positional arguments.
#
splitArguments() {
#----------------
#
  args=""
  while [ $# -gt 0 ] ; do
    if expr "$1" : "-.*" >/dev/null ; then
       a=`expr "$1" : "-\(.*\)" 2>/dev/null`
       key=`echo "$a" | awk -F= '{print $1}' 2>/dev/null`
         value=`echo "$a" | awk -F= '{for(i=2;i<NF;i++)x=x $i "=" ; x=x $NF ; print x }' 2>/dev/null`
       if [ -z "$value" ] ; then a="${key}=" ; fi
       eval "${key}=\"${value}\""
       a="export ${key}"
       eval "$a"
    else
       args="${args} $1"
    fi
    shift 1
  done
  if [ ! -z "$args" ] ; then
     set `echo "$args" | awk '{ for(i=1;i<=NF;i++)print $i }'`
  fi
  return 0
}
#
#
##.........................................
#
splitUri() {
#----------------
#
  uri_hsmName=`expr "$1" : "\(.*\)\:.*"`
  uri_hsmInstance=`expr "$1" : ".*\:\/\/\(.*\)\/.*"`
  uri_store=`expr "$1" : ".*\/\?store=\(.*\)&group.*"`
  uri_group=`expr "$1" : ".*group=\(.*\)&bfid.*"`
  uri_bfid=`expr "$1" : ".*bfid=\(.*\)"`
#
  if [  \( -z "${uri_store}" \) -o \( -z "${uri_group}" \) -o \(  -z "${uri_bfid}" \) \
     -o \( -z "${uri_hsmName}" \) -o \( -z "${uri_hsmInstance}" \) ] ; then
     printerror "Illegal URI formal : $1"
     return 1
  fi
  return 0

}
#########################################################
#
echo "--------- $* `date`" >>${logFile}
#
#########################################################
#
createEnvironment() {

   if [ -z "${hsmBase}" ] ; then
      printerror "hsmBase not set, can't continue"
      return 1
   fi
   BASE=${hsmBase}/data
   if [ ! -d ${BASE} ] ; then
      printerror "${BASE} is not a directory or doesn't exist"
      return 1
   fi
}
##
#----------------------------------------------------------
doTheGetFile() {

   splitUri $1
   [ $? -ne 0 ] && return 1

   createEnvironment
   [ $? -ne 0 ] && return 1

   pnfsdir=${BASE}/$uri_hsmName/${uri_store}/${uri_group}
   pnfsfile=${pnfsdir}/$pnfsid

   cp $pnfsfile $filename 2>/dev/null
   if [ $? -ne 0 ] ; then
      printerror "Couldn't copy file $pnfsfile to $filename"
      return 1
   fi

   return 0
}
##
#----------------------------------------------------------
doTheStoreFile() {

   splitUri $1
   [ $? -ne 0 ] && return 1

   createEnvironment
   [ $? -ne 0 ] && return 1

   pnfsdir=${BASE}/$hsmName/${store}/${group}
   mkdir -p ${pnfsdir} 2>/dev/null
   if [ $? -ne 0 ] ; then
      printerror "Couldn't create $pnfsdir"
      return 1
   fi
   pnfsfile=${pnfsdir}/$pnfsid

   cp $filename $pnfsfile 2>/dev/null
   if [ $? -ne 0 ] ; then
      printerror "Couldn't copy file $filename to $pnfsfile"
      return 1
   fi

   return 0

}
##
#----------------------------------------------------------
doTheRemoveFile() {

   splitUri $1
   [ $? -ne 0 ] && return 1

   createEnvironment
   [ $? -ne 0 ] && return 1

   pnfsdir=${BASE}/$uri_hsmName/${uri_store}/${uri_group}
   pnfsfile=${pnfsdir}/$uri_bfid

   rm $pnfsfile 2>/dev/null
   if [ $? -ne 0 ] ; then
      printerror "Couldn't remove file $pnfsfile"
      return 1
   fi

   return 0
}
#########################################################
#
#  split arguments
#
  args=""
  while [ $# -gt 0 ] ; do
    if expr "$1" : "-.*" >/dev/null ; then
       a=`expr "$1" : "-\(.*\)" 2>/dev/null`
       key=`echo "$a" | awk -F= '{print $1}' 2>/dev/null`
         value=`echo "$a" | awk -F= '{for(i=2;i<NF;i++)x=x $i "=" ; x=x $NF ; print x }' 2>/dev/null`
       if [ -z "$value" ] ; then a="${key}=" ; fi
       eval "${key}=\"${value}\""
       a="export ${key}"
       eval "$a"
    else
       args="${args} $1"
    fi
    shift 1
  done
  if [ ! -z "$args" ] ; then
     set `echo "$args" | awk '{ for(i=1;i<=NF;i++)print $i }'`
  fi
#
#
if [ $# -lt 1 ] ; then
    printerror "Not enough arguments : ... put/get/remove ..."
    exit 1
fi
#
command=$1
pnfsid=$2
#
# !!!!!!  Hides a bug in the dCache HSM remove
#
if [ "$command" = "remove" ] ; then pnfsid="000000000000000000000000000000000000" ; fi
#
#
printout "Request for $command started `date`"
#
################################################################
#
if [ "$command" = "put" ] ; then
#
################################################################
#
  filename=$3
#
  if [ -z "$si" ] ; then
     printerror "StorageInfo (si) not found in put command"
     exit 5
  fi
#
  assignStorageInfo
#
  printStorageInfo
#
  if [ \( -z "${store}" \) -o \( -z "${group}" \) -o \( -z "${hsmName}" \) ] ; then
     printerror "Didn't get enough information to flush : hsmName = $hsmName store=$store group=$group pnfsid=$pnfsid "
     exit 3
  fi
#
  uri="$hsmName://$hsmName/?store=${store}&group=${group}&bfid=${pnfsid}"

  printout "Created identifier : $uri"

  doTheStoreFile $uri
  rc=$?
  if [ $rc -eq 0 ] ; then echo $uri ; fi

  printout "Request 'put' finished at `date` with return code $rc"
  exit $rc
#
#
################################################################
#
elif [ "$command" = "get"  ] ; then
#
################################################################
#
  filename=$3
  if [ -z "$uri" ] ; then
     printerror "Uri not found in arguments"
     exit 3
  fi
#
  printout "Got identifier : $uri"
#
  doTheGetFile $uri
  rc=$?
  printout "Request 'get' finished at `date` with return code $rc"
  exit $rc
#
################################################################
#
elif [ "$command" = "remove" ] ; then
#
################################################################
#
   if [ -z "$uri" ] ; then
      printerror "Illegal Argument error : URI not specified"
      exit 4
   fi
#
   printout "Remove uri = $uri"
   doTheRemoveFile $uri
   rc=$?
#
   printout "Request 'remove' finished at `date` with return code $rc"
   exit $rc
#
else
#
   printerror "Expected command : put/get/remove , found : $command"
   exit 1
#
fi</pre>

</div>

</div>

</div>

</div>

<div class="chapter" title="Chapter 9\. File Hopping">

<div class="titlepage">

<div>

<div>

## <a name="cf-hopping"></a>Chapter 9\. File Hopping

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[_File Hopping on arrival_ from outside <span class="productname">dCache</span>](#cf-hopping-onarrival)</span></dt>

<dd>

<dl>

<dt><span class="section">[File mode of replicated files](#cf-hopping-onarrival-file-mode)</span></dt>

<dt><span class="section">[File Hopping managed by the `PoolManager`](#idp2899136)</span></dt>

<dt><span class="section">[File Hopping managed by the `HoppingManager`](#idp2934624)</span></dt>

</dl>

</dd>

</dl>

</div>

File hopping is a collective term in <span class="productname">dCache</span>, summarizing the possibility of having files being transferred between <span class="productname">dCache</span> pools triggered by a variety of conditions. The most prominent examples are:

<div class="itemizedlist">

*   If a file is requested by a client but the file resides on a pool from which this client, by configuration, is not allowed to read data, the dataset is transferred to an <span class="quote">“<span class="quote">allowed</span>”</span> pool first.

*   If a pool encounters a steady high load, the system may, if configured, decide to replicate files to other pools to achieve an equal load distribution.

*   <abbr class="abbrev">HSM</abbr> restore operations may be split into two steps. The first one reads data from tertiary storage to an <span class="quote">“<span class="quote">HSM connected</span>”</span> pool and the second step takes care that the file is replicated to a general read pool. Under some conditions this separation of <abbr class="abbrev">HSM</abbr> and non-<abbr class="abbrev">HSM</abbr> pools might become necessary for performance reasons.

*   If a dataset has been written into <span class="productname">dCache</span> it might become necessary to have this file replicated instantly. The reasons can be, to either have a second, safe copy, or to make sure that clients don’t access the file for reading on the write pools.

</div>

<div class="section" title="File Hopping on arrival from outside dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-hopping-onarrival"></a>_File Hopping on arrival_ from outside <span class="productname">dCache</span>

</div>

</div>

</div>

_File Hopping on arrival_ is a term, denoting the possibility of initiating a pool to pool transfer as the result of a file successfully arriving on a pool from some external client. Files restored from <abbr class="abbrev">HSM</abbr> or arriving on a pool as the result of a pool to pool transfer will not yet be forwarded.

Forwarding of incoming files can be enabled by setting the `pool.destination.replicate` property in the `<span>/etc/dcache</span>/dcache.conf` file or per pool in the layout file. It can be set to `on`, `PoolManager` or `HoppingManager`, where `on` does the same as `PoolManager`.

The pool is requested to send a `replicateFile` message to either the `PoolManager` or to the `HoppingManager`, if available. The different approaches are briefly described below and in more detail in the subsequent sections.

<div class="itemizedlist">

*   The `replicateFile` message is sent to the `PoolManager`. This happens for all files arriving at that pool from outside (no restore or p2p). No intermediate `HoppingManager` is needed. The restrictions are

    <div class="itemizedlist">

    *   All files are replicated. No pre-selection, e.g. on the storage class can be done.

    *   The mode of the replicated file is determined by the destination pool and cannot be overwritten. See [the section called “File mode of replicated files”](#cf-hopping-onarrival-file-mode "File mode of replicated files")

    </div>

*   The `replicateFile` message is sent to the `HoppingManager`. The `HoppingManager` can be configured to replicate certain storage classes only and to set the mode of the replicated file according to rules. The file mode of the source file cannot be modified.

</div>

<div class="section" title="File mode of replicated files">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-hopping-onarrival-file-mode"></a>File mode of replicated files

</div>

</div>

</div>

The mode of a replicated file can either be determined by settings in the destination pool or by the `HoppingManager`. It can be `cached` or `precious`.

<div class="itemizedlist">

*   If the `PoolManager` is used for replication, the mode of the replicated file is determined by the destination pool. The default setting is `cached`.

*   If a `HoppingManager` is used for file replication, the mode of the replicated file is determined by the `HoppingManager` rule responsible for this particular replication. If the destination mode is set to `keep` in the rule, the mode of the destination pool determines the final mode of the replicated file.

</div>

</div>

<div class="section" title="File Hopping managed by the PoolManager">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp2899136"></a>File Hopping managed by the `PoolManager`

</div>

</div>

</div>

To enable replication on arrival by the `PoolManager` set the property `pool.destination.replicate` to `PoolManager` for the particular pool

<pre class="programlisting">[_<tt><exampleDomain></tt>_]
[_<tt><exampleDomain></tt>_/pool]
...
pool.destination.replicate=PoolManager</pre>

or for several pools in the `<span>/etc/dcache</span>/dcache.conf` file.

<pre class="programlisting">...
pool.destination.replicate=PoolManager</pre>

File hopping configuration instructs a pool to send a `replicateFile` request to the `PoolManager` as the result of a file arriving on that pool from some external client. All arriving files will be treated the same. The `PoolManager` will process this transfer request by trying to find a matching link (Please find detailed information at [Chapter 7, _The `poolmanager` Service_](#cf-pm "Chapter 7\. The poolmanager Service").

It is possible to configure the `PoolManager` such that files are replicated from this pool to a special set of destination pools.

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Assume that we want to have all files, arriving on pool `ocean` to be immediately replicated to a subset of read pools. This subset of pools is described by the poolgroup `ocean-copies`. No other pool is member of the poolgroup `ocean-copies`.

Other than that, files arriving at the pool `mountain` should be replicated to all read pools from which farm nodes on the `131.169.10.0/24` subnet are allowed to read.

The layout file defining the pools `ocean` and `mountain` should read like this:

<pre class="programlisting">[exampleDomain]
[exampleDomain/pool]

name=ocean
path=/path/to/pool-ocean
pool.wait-for-files=${path}/data
pool.destination.replicate=PoolManager

name=mountain
path=/path/to/pool-mountain
pool.wait-for-files=${path}/data
pool.destination.replicate=PoolManager</pre>

In the layout file it is defined that all files arriving on the pools `ocean` or `mountain` should be replicated immediately. The following `PoolManager.conf` file contains instructions for the `PoolManager` how to replicate these files. Files arriving at the `ocean` pool will be replicated to the `ocean-copies` subset of the read pools and files arriving at the pool `mountain` will be replicated to all read pools from which farm nodes on the `131.169.10.0/24` subnet are allowed to read.

<pre class="programlisting">#
# define the units
#
psu create unit -protocol   */*
psu create unit -net        0.0.0.0/0.0.0.0
psu create unit -net        131.169.10.0/255.255.255.0
# create the faked net unit
psu create unit -net        192.1.1.1/255.255.255.255
psu create unit -store      *@*
psu create unit -store      ocean:raw@osm
#
#
#  define unit groups
#
psu create ugroup  any-protocol
psu create ugroup  any-store
psu create ugroup  ocean-copy-store
psu create ugroup farm-network
psu create ugroup ocean-copy-network
#
psu addto ugroup any-protocol */*
psu addto ugroup any-store    *@*
psu addto ugroup ocean-copy-store ocean:raw@osm
psu addto ugroup farm-network  131.169.10.0/255.255.255.0
psu addto ugroup ocean-copy-network  192.1.1.1/255.255.255.255
psu addto ugroup allnet-cond 0.0.0.0/0.0.0.0
psu addto ugroup allnet-cond 131.169.10.0/255.255.255.0
psu addto ugroup allnet-cond 192.1.1.1/255.255.255.255
#
#
#  define the write-pools
#
psu create pool ocean
psu create pool mountain
#
#
#  define the write-pools poolgroup
#
psu create pgroup write-pools
psu addto pgroup write-pools ocean
psu addto pgroup write-pools mountain
#
#
#  define the write-pools-link, add write pools and set transfer preferences
#
psu create link write-pools-link any-store any-protocol allnet-cond
psu addto link write-pools-link write-pools
psu set link farm-read-link -readpref=0 -writepref=10 -cachepref=0 -p2ppref=-1
#
#
#  define the read-pools
#
psu create pool read-pool-1
psu create pool read-pool-2
psu create pool read-pool-3
psu create pool read-pool-4
#
#
#  define the farm-read-pools poolgroup and add pool members
#
psu create pgroup farm-read-pools
psu addto pgroup farm-read-pools read-pool-1
psu addto pgroup farm-read-pools read-pool-2
psu addto pgroup farm-read-pools read-pool-3
psu addto pgroup farm-read-pools read-pool-4
#
#
#  define the ocean-copy-pools poolgroup and add a pool
#
psu create pgroup ocean-copy-pools
psu addto pgroup ocean-copy-pools  read-pool-1
#
#
# define the farm-read-link, add farm-read-pools and set transfer preferences
#
psu create link farm-read-link any-store any-protocol farm-network
psu addto link farm-read-link farm-read-pools
psu set link farm-read-link -readpref=10 -writepref=0 -cachepref=10 -p2ppref=-1
#
#
# define the ocean-copy-link, add ocean-copy-pools and set transfer preferences
#
psu create link ocean-copy-link ocean-copy-store any-protocol ocean-copy-network
psu addto link ocean-copy-link ocean-copy-pools
psu set link ocean-copy-link -readpref=10 -writepref=0 -cachepref=10 -p2ppref=-1
#
#</pre>

While `131.169.10.1` is a legal IP address e.g. of one of your farm nodes, the `192.1.1.1` IP address must not exist anywhere at your site.

</div>

</div>

<div class="section" title="File Hopping managed by the HoppingManager">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp2934624"></a>File Hopping managed by the `HoppingManager`

</div>

</div>

</div>

With the `HoppingManager` you have several configuration options for `file hopping on arrival`, e.g.:

<div class="itemizedlist">

*   With the `HoppingManager` you can define a rule such that only the files with a specific storage class should be replicated.
*   You can specify the protocol the replicated files can be accessed with.
*   You can specify from which ip-adresses it should be possible to access the files.

</div>

<div class="section" title="Starting the FileHopping Manager service">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp2940352"></a>Starting the FileHopping Manager service

</div>

</div>

</div>

Add the `hoppingmanager` service to a domain in your layout file and restart the domain.

<pre class="programlisting">[_<tt><DomainName></tt>_]
[_<tt><DomainName></tt>_/hoppingmanager]</pre>

Initially no rules are configured for the `HoppingManager`. You may add rules by either edit the file `<span>/var/lib/dcache</span>/config/HoppingManager.conf` and restart the `hoppingmanager` service, or use the admin interface and save the modifications by the <span class="command">**save**</span> command into the `HoppingManager.conf`

</div>

<div class="section" title="Configuring pools to use the HoppingManager">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp2948544"></a>Configuring pools to use the `HoppingManager`

</div>

</div>

</div>

To enable replication on arrival by the `HoppingManager` set the property `pool.destination.replicate` to `HoppingManager` for the particular pool

<pre class="programlisting">[_<tt><exampleDomain></tt>_]
[_<tt><exampleDomain></tt>_/pool]
...
pool.destination.replicate=HoppingManager</pre>

or for several pools in the `<span>/etc/dcache</span>/dcache.conf` file.

<pre class="programlisting">...
pool.destination.replicate=HoppingManager</pre>

</div>

<div class="section" title="HoppingManager Configuration Introduction">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp2956240"></a>`HoppingManager` Configuration Introduction

</div>

</div>

</div>

<div class="itemizedlist">

*   The `HoppingManager` essentially receives `replicateFile` messages from pools, configured to support file hopping, and either discards or modifies and forwards them to the `PoolManager`, depending on rules described below.

*   The `HoppingManager` decides on the action to perform, based on a set of configurable rules. Each rule has a name. Rules are checked in alphabetic order concerning their names.

*   A rule it triggered if the storage class matches the storage class pattern assigned to that rule. If a rule is triggered, it is processed and no further rule checking is performed. If no rule is found for this request the file is not replicated.

*   If for whatever reason, a file cannot be replicated, NO RETRY is being performed.

*   Processing a triggered rule can be :

    <div class="itemizedlist">

    *   The message is discarded. No replication is done for this particular storage class.

    *   The rule modifies the `replicateFile` message, before it is forwarded to the `PoolManager`.

        An ip-number of a farm-node of the farm that should be allowed to read the file can be added to the `replicateFile` message.

        The mode of the replicated file can be specified. This can either be `precious`, `cached` or `keep`. `keep` means that the pool mode of the source pool determines the replicated file mode.

        The requested protocol can be specified.

    </div>

</div>

</div>

<div class="section" title="HoppingManager Configuration Reference">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp2974272"></a>`HoppingManager` Configuration Reference

</div>

</div>

</div>

<pre class="screen">         define hop OPTIONS _<tt><name></tt>_ _<tt><pattern></tt>_ precious|cached|keep
            OPTIONS
              -destination=_<tt><cellDestination></tt>_ # default : PoolManager
              -overwrite
              -continue
              -source=write|restore|*   #  !!!! for experts only      StorageInfoOptions
              -host=_<tt><destinationHostIp></tt>_
              -protType=dCap|ftp...
              -protMinor=_<tt><minorProtocolVersion></tt>_
              -protMajor=_<tt><majorProtocolVersion></tt>_ </pre>

<div class="variablelist">

<dl>

<dt><span class="term">name</span></dt>

<dd>This is the name of the hopping rule. Rules are checked in alphabetic order concerning their names.</dd>

<dt><span class="term">pattern</span></dt>

<dd>

`pattern` is a [storage class](#secStorageClass "Storage Classes") pattern. If the incoming storage class matches this pattern, this rule is processed.

</dd>

<dt><span class="term">precious|cached|keep</span></dt>

<dd>

`precious|cached|keep` determines the mode of the replicated file. With `keep` the mode of the file will be determined by the mode of the destination pool.

</dd>

<dt><span class="term">-destination</span></dt>

<dd>

This defines which `cell` to use for the pool to pool transfer. By default this is the `PoolManager` and this should not be changed.

</dd>

<dt><span class="term">-overwrite</span></dt>

<dd>

In case, a rule with the same name already exists, it is overwritten.

</dd>

<dt><span class="term">-continue</span></dt>

<dd>

If a rule has been triggered and the corresponding action has been performed, no other rules are checked. If the `continue` option is specified, rule checking continues. This is for debugging purposes only.

</dd>

<dt><span class="term">-source</span></dt>

<dd>

`-source` defines the event on the pool which has triggered the hopping. Possible values are `restore` and `write`. `restore` means that the rule should be triggered if the file was restored from a tape and `write` means that it should be triggered if the file was written by a client.

</dd>

<dt><span class="term">-host</span></dt>

<dd>

Choose the id of a node of the farm of worker-nodes that should be allowed to access the file. Configure the `poolmanager` respectively.

</dd>

<dt><span class="term">-protType, -protMajor, -protMinor</span></dt>

<dd>

Specify the protocol which should be used to access the replicated files.

</dd>

</dl>

</div>

</div>

<div class="section" title="HoppingManager configuration examples">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp3004016"></a>`HoppingManager` configuration examples

</div>

</div>

</div>

In order to instruct a particular pool to send a `replicateFile` message to the `hoppingmanager` service, you need to add the line `pool.destination.replicate=HoppingManager` to the layout file.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">[exampleDomain]
[exampleDomain/pool]

name=write-pool
path=/path/to/write-pool-exp-a
pool.wait-for-files=${path}/data
pool.destination.replicate=HoppingManager
...</pre>

Assume that all files of experiment-a will be written to an expensive write pool and subsequently flushed to tape. Now some of these files need to be accessed without delay. The files that need fast acceess possibility will be given the storage class `exp-a:need-fast-access@osm`.

In this example we will configure the file hopping such that a user who wants to access a file that has the above storage info with the `NFSv4.1` protocol will be able to do so.

Define a rule for hopping in the `<span>/var/lib/dcache</span>/config/HoppingManager.conf` file.

<pre class="programlisting">define hop nfs-hop exp-a:need-fast-access@osm cached -protType=nfs -protMajor=4 -protMinor=1</pre>

This assumes that the storage class of the file is `exp-a:nfs@osm`. The mode of the file, which was `precious` on the write pool will have to be changed to `cached` on the read pool.

The corresponding `<span>/var/lib/dcache</span>/config/poolmanager.conf` file could read like this:

<pre class="programlisting">#
# define the units
#
psu create unit -protocol   */*
psu create unit -net        0.0.0.0/0.0.0.0
psu create unit -store      exp-a:need-fast-access@osm
#
#
#  define unit groups
#
psu create ugroup  any-protocol
psu create ugroup  exp-a-copy-store
psu create ugroup allnet-cond
#
psu addto ugroup any-protocol */*
psu addto ugroup exp-a-copy-store    exp-a:need-fast-access@osm
psu addto ugroup allnet-cond 0.0.0.0/0.0.0.0
#
#
#  define the write-pool
#
psu create pool write-pool
#
#
#  define the read-pool
#
psu create pool read-pool
#
#
#  define the exp-a-read-pools poolgroup and add a pool
#
psu create pgroup exp-a-read-pools
psu addto pgroup exp-a-read-pools read-pool
#
#
#  define the exp-a-write-pools poolgroup and add a pool
#
psu create pgroup exp-a-write-pools
psu addto pgroup exp-a-write-pools write-pool
#
#
# define the exp-a-read-link, add exp-a-read-pools and set transfer preferences
#
psu create link exp-a-read-link exp-a-copy-store any-protocol allnet-cond
psu addto link exp-a-read-link exp-a-read-pools
psu set link exp-a-read-link -readpref=10 -writepref=0 -cachepref=10 -p2ppref=-1
#
#
# define the exp-a-write-link, add exp-a-write-pools and set transfer preferences
#
psu create link exp-a-write-link exp-a-copy-store any-protocol allnet-cond
psu addto link exp-a-write-link exp-a-write-pools
psu set link exp-a-write-link -readpref=0 -writepref=10 -cachepref=0 -p2ppref=-1
#
#
#</pre>

</div>

</div>

</div>

</div>

</div>

</div>

<div class="chapter" title="Chapter 10\. Authorization in dCache">

<div class="titlepage">

<div>

<div>

## <a name="cf-gplazma"></a>Chapter 10\. Authorization in <span class="productname">dCache</span>

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Basics](#cf-gplazma-basics)</span></dt>

<dt><span class="section">[Configuration](#cf-gplazma-gp2-configuration)</span></dt>

<dd>

<dl>

<dt><span class="section">[Plug-ins](#cf-gplazma-gp2-configuration-plug-ins)</span></dt>

</dl>

</dd>

<dt><span class="section">[Using `X.509` Certificates](#cf-gplazma-certificates)</span></dt>

<dd>

<dl>

<dt><span class="section">[CA Certificates](#cf-gplazma-certificates-cacerts)</span></dt>

<dt><span class="section">[User Certificate](#cf-gplazma-certificates-usercert)</span></dt>

<dt><span class="section">[Host Certificate](#cf-gplazma-certificates-hostcert)</span></dt>

<dt><span class="section">[<span class="productname">VOMS</span> Proxy Certificate](#cb-voms-proxy-glite)</span></dt>

</dl>

</dd>

<dt><span class="section">[Configuration files](#cf-gplazma-plug-inconfig)</span></dt>

<dd>

<dl>

<dt><span class="section">[`storage-authzdb`](#cf-gplazma-plug-inconfig-authzdb)</span></dt>

<dt><span class="section">[The gplazmalite-vorole-mapping plug-in](#cf-gplazma-plug-inconfig-vorolemap)</span></dt>

<dt><span class="section">[Authorizing a VO](#cf-gplazma-plug-inconfig-voauth)</span></dt>

<dt><span class="section">[The kpwd plug-in](#cf-gplazma-kpwd)</span></dt>

<dt><span class="section">[The `gridmap` plug-in](#cf-gplazma-gridmap)</span></dt>

</dl>

</dd>

<dt><span class="section">[`gPlazma` specific <span class="productname">dCache</span> configuration](#cf-gplazma-setup)</span></dt>

<dd>

<dl>

<dt><span class="section">[Enabling Username/Password Access for `WebDAV`](#cf-gplazma-username-password-webdav-example)</span></dt>

<dt><span class="section">[`gPlazma` config example to work with authenticated webadmin](#cf-gplazma-webadmin-example)</span></dt>

</dl>

</dd>

</dl>

</div>

To limit access to data, <span class="productname">dCache</span> comes with an authentication and authorization interface called `gPlazma2`. `gPlazma` is an acronym for Grid-aware PLuggable AuthorZation Management. Earlier versions of <span class="productname">dCache</span> worked with `gPlazma1` which has now been completely removed from <span class="productname">dCache</span>. So if you are upgrading, you have to reconfigure `gPlazma` if you used `gPlazma1` until now.

<div class="section" title="Basics">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-gplazma-basics"></a>Basics

</div>

</div>

</div>

Though it is possible to allow anonymous access to <span class="productname">dCache</span> it is usually desirable to authenticate users. The user then has to connect to one of the different doors (e.g., ``GridFTP` door`, ``dCap` door`) and login with credentials that prove his identity. In Grid-World these credentials are very often `X.509` certificates, but dCache also supports other methods like username/password and kerberos authentication.

The door collects the credential information from the user and sends a login request to the configured authorization service (i.e., `gPlazma`) Within `gPlazma` the configured plug-ins try to verify the users identity and determine his access rights. From this a response is created that is then sent back to the door and added to the entity representing the user in <span class="productname">dCache</span>. This entity is called `subject`. While for authentication usually more global services (e.g., <span class="productname">ARGUS</span>) may be used, the mapping to site specific <acronym class="acronym">UID</acronym>s has to be configured on a per site basis.

</div>

<div class="section" title="Configuration">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-gplazma-gp2-configuration"></a>Configuration

</div>

</div>

</div>

`gPlazma2` is configured by the <acronym class="acronym">PAM</acronym>-style configuration file `<span>/etc/dcache</span>/gplazma.conf`. Each line of the file is either a comment (i.e., starts with `#`, is empty, or defines a plugin. Plugin defining lines start with the plugin stack type (one of `auth`, `map`, `account`, `session` `identity`), followed by a <acronym class="acronym">PAM</acronym>-style modifier (one of `optional`, `sufficient`, `required`, `requisite`), the plugin name and an optional list of key-value pairs of parameters. During the login process they will be executed in the order `auth`, `map`, `account` and `session`. The `identity` plugins are not used during login, but later on to map from <acronym class="acronym">UID</acronym>+<acronym class="acronym">GID</acronym> back to user names (e.g., for NFS). Within these groups they are used in the order they are specified.

<pre class="programlisting">auth|map|account|session|identity optional|required|requisite|sufficient _<tt><plug-in></tt>_ ["_<tt><key></tt>_=_<tt><value></tt>_" ...]</pre>

A complete configuration file will look something like this:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting"># Some comment
auth    optional  x509
auth    optional  voms
map     requisite vorolemap
map     requisite authzdb authzdb=/etc/grid-security/authzdb
session requisite authzdb</pre>

</div>

</div>

<div class="variablelist" title="Login Phases">

**Login Phases**

<dl>

<dt><span class="term">`auth`</span></dt>

<dd>

`auth`-plug-ins are used to read the users public and private credentials and ask some authority, if those are valid for accessing the system.

</dd>

<dt><span class="term">`map`</span></dt>

<dd>

`map`-plug-ins map the user information obtained in the `auth` step to <acronym class="acronym">UID</acronym> and <acronym class="acronym">GID</acronym>s. This may also be done in several steps (e.g., the `vorolemap` plug-in maps the users <acronym class="acronym">DN</acronym>+<acronym class="acronym">FQAN</acronym> to a username which is then mapped to <acronym class="acronym">UID</acronym>/<acronym class="acronym">GID</acronym>s by the `authzdb` plug-in.

</dd>

<dt><span class="term">`account`</span></dt>

<dd>

`account`-plug-ins verify the validity of a possibly mapped identity of the user and may reject the login depending on information gathered within the map step.

</dd>

<dt><span class="term">`session`</span></dt>

<dd>

`session` plug-ins usually enrich the session with additional attributes like the user’s home directory.

</dd>

<dt><span class="term">`identity`</span></dt>

<dd>

`identity` plug-ins are responsible for mapping <acronym class="acronym">UID</acronym> and <acronym class="acronym">GID</acronym> to user names and vice versa during the work with <span class="productname">dCache</span>.

</dd>

</dl>

</div>

The meaning of the modifiers follow the <acronym class="acronym">PAM</acronym> specification:

<div class="variablelist" title="Modifiers">

**Modifiers**

<dl>

<dt><span class="term">`optional`</span></dt>

<dd>

The success or failure of this plug-in is only important if it is the only plug-in in the stack associated with this type.

</dd>

<dt><span class="term">`sufficient`</span></dt>

<dd>

Success of such a plug-in is enough to satisfy the authentication requirements of the stack of plug-ins (if a prior required plug-in has failed the success of this one is ignored). A failure of this plug-in is not deemed as fatal for the login attempt. If the plug-in succeeds `gPlazma2` immediately proceeds with the next plug-in type or returns control to the door if this was the last stack.

</dd>

<dt><span class="term">`required`</span></dt>

<dd>

Failure of such a plug-in will ultimately lead to `gPlazma2` returning failure but only after the remaining plug-ins for this type have been invoked.

</dd>

<dt><span class="term">`requisite`</span></dt>

<dd>

Like `required`, however, in the case that such a plug-in returns a failure, control is directly returned to the door.

</dd>

</dl>

</div>

<div class="section" title="Plug-ins">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-gplazma-gp2-configuration-plug-ins"></a>Plug-ins

</div>

</div>

</div>

`gPlazma2` functionality is configured by combining different types of plug-ins to work together in a way that matches your requirements. For this purpose there are five different types of plug-ins. These types correspond to the keywords `auth`, `map`, `account`, `session` and `identity` as described in the previous section. The plug-ins can be configured via properties that may be set in `dcache.conf`, the layout-file or in `gplazma.conf`.

<div class="section" title="auth Plug-ins">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-gplazma-gp2-configuration-plug-ins-auth"></a>`auth` Plug-ins

</div>

</div>

</div>

<div class="section" title="kpwd">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-kpwd-auth"></a>kpwd

</div>

</div>

</div>

The `kpwd` plug-in authorizes users by username and password, by pairs of <acronym class="acronym">DN</acronym> and <acronym class="acronym">FQAN</acronym> and by `Kerberos` principals.

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.kpwd.file`</span></dt>

<dd>

Path to `dcache.kpwd`

Default: `<span>/etc/dcache</span>/dcache.kpwd`

</dd>

</dl>

</div>

</div>

<div class="section" title="voms">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-voms-auth"></a>voms

</div>

</div>

</div>

The `voms` plug-in is an `auth` plug-in. It can be used to verify `X.509` credentials. It takes the certificates and checks their validity by testing them against the trusted CAs. The verified certificates are then stored and passed on to the other plug-ins in the stack.

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.vomsdir.ca`</span></dt>

<dd>

Path to ca certificates

Default: `/etc/grid-security/certificates`

</dd>

<dt><span class="term">`gplazma.vomsdir.dir`</span></dt>

<dd>

Path to `vomsdir`

Default: `/etc/grid-security/vomsdir`

</dd>

</dl>

</div>

</div>

<div class="section" title="X.509 plug-in">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-x509-auth"></a>`X.509` plug-in

</div>

</div>

</div>

The `X.509` plug-in is a `auth` plug-in that extracts `X.509` certificate chains from the credentials of a user to be used by other plug-ins.

</div>

</div>

<div class="section" title="map Plug-ins">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-gplazma-gp2-configuration-plug-ins-map"></a>`map` Plug-ins

</div>

</div>

</div>

<div class="section" title="kpwd">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-kpwd-map"></a>kpwd

</div>

</div>

</div>

As a `map` plug-in it maps usernames to <acronym class="acronym">UID</acronym> and <acronym class="acronym">GID</acronym>. And as a `session` plug-in it adds root and home path information to the session based on the user’s username.

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.kpwd.file`</span></dt>

<dd>

Path to `dcache.kpwd`

Default: `<span>/etc/dcache</span>/dcache.kpwd`

</dd>

</dl>

</div>

</div>

<div class="section" title="authzdb">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-authzdb-map"></a>authzdb

</div>

</div>

</div>

The `authzdb` plug-in takes a username and maps it to <acronym class="acronym">UID</acronym>+<acronym class="acronym">GID</acronym> using the `storage-authzdb` file.

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.authzdb.file`</span></dt>

<dd>

Path to `storage-authzdb`

Default: `/etc/grid-security/storage-authzdb`

</dd>

</dl>

</div>

</div>

<div class="section" title="GridMap">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-gridmap-map"></a>GridMap

</div>

</div>

</div>

The `gridmap` plug-in maps <span class="productname">GLOBUS</span> identities and `Kerberos` identities to usernames.

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.gridmap.file`</span></dt>

<dd>

Path to `grid-mapfile`

Default: `/etc/grid-security/grid-mapfile`

</dd>

</dl>

</div>

</div>

<div class="section" title="vorolemap">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-vorolemap-map"></a>vorolemap

</div>

</div>

</div>

The `voms` plug-in maps pairs of <acronym class="acronym">DN</acronym> and <acronym class="acronym">FQAN</acronym> to usernames via a [vorolemap](#cf-gplazma-plug-inconfig-vorolemap-gridvorolemap "Preparing grid-vorolemap") file.

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.vorolemap.file`</span></dt>

<dd>

Path to `grid-vorolemap`

`/etc/grid-security/grid-vorolemap`

</dd>

</dl>

</div>

</div>

<div class="section" title="krb5">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-krb5-map"></a>krb5

</div>

</div>

</div>

The `krb5` plug-in maps a kerberos principal to a username by removing the domain part from the principal.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<div class="literallayout">

`user@KRB-DOMAIN.EXAMPLE.ORG` to `user`  

</div>

</div>

</div>

</div>

<div class="section" title="nsswitch">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-nsswitch-map"></a>nsswitch

</div>

</div>

</div>

The `nsswitch` plug-in uses the system’s `nsswitch` configuration to provide mapping.

Typically `nsswitch` plug-in will be combined with `vorolemap` plug-in, `gridmap` plug-in or `krb5` plug-in:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting"># Map grid users to local accounts
auth    optional  x509 #1
auth    optional  voms #2
map     requisite vorolemap #3
map     requisite nsswitch #4
session requisite nsswitch #5</pre>

In this example following is happening: extract user’s DN (1), extract and verify VOMS attributes (2), map DN+Role to a local account (3), extract uid and gids for a local account (4) and, finally, extract users home directory (5).

</div>

</div>

</div>

<div class="section" title="nis">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plugins-nis-map"></a>nis

</div>

</div>

</div>

The `nis` plug-in uses an existing `NIS` service to map username+password to a username.

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.nis.server`</span></dt>

<dd>

`NIS` server host

Default: `nisserv.domain.com`

</dd>

<dt><span class="term">`gplazma.nis.domain`</span></dt>

<dd>

`NIS` domain

Default: `domain.com`

</dd>

</dl>

</div>

The result of `nis` plug-in can be used by other plug-ins:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting"># Map grid or kerberos users to local accounts
auth    optional  x509 #1
auth    optional  voms #2
map     requisite vorolemap #3
map     optional  krb5 #4
map     optional  nis #5
session requisite nis #6</pre>

In this example two access methods are considered: grid based and kerberos based. If user comes with grid certificate and VOMS role: extract user’s DN (1), extract and verify VOMS attributes (2), map DN+Role to a local account (3). If user comes with `Kerberos` ticket: extract local account (4). After this point in both cases we talk to `NIS` to get uid and gids for a local account (5) and, finally, adding users home directory (6).

</div>

</div>

</div>

</div>

<div class="section" title="account Plug-ins">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-gplazma-gp2-configuration-plug-ins-account"></a>`account` Plug-ins

</div>

</div>

</div>

<div class="section" title="argus">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-argus-account"></a>argus

</div>

</div>

</div>

The `argus` plug-in bans users by their <acronym class="acronym">DN</acronym>. It talks to your site’s <span class="productname">ARGUS</span> system (see [https://twiki.cern.ch/twiki/bin/view/EGEE/AuthorizationFramework](https://twiki.cern.ch/twiki/bin/view/EGEE/AuthorizationFramework) ) to check for banned users.

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.argus.hostcert`</span></dt>

<dd>

Path to host certificate

Default: `/etc/grid-security/hostcert.pem`

</dd>

<dt><span class="term">`gplazma.argus.hostkey`</span></dt>

<dd>

Path to host key

Default: `/etc/grid-security/hostkey.pem`

</dd>

<dt><span class="term">`gplazma.argus.hostkey.password`</span></dt>

<dd>

Password for host key

Default:

</dd>

<dt><span class="term">`gplazma.argus.ca`</span></dt>

<dd>

Path to CA certificates

Default: `/etc/grid-security/certificates`

</dd>

<dt><span class="term">`gplazma.argus.endpoint`</span></dt>

<dd>

<acronym class="acronym">URL</acronym> of PEP service

Default: `https://localhost:8154/authz`

</dd>

</dl>

</div>

</div>

<div class="section" title="banfile">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-banfile-account"></a>banfile

</div>

</div>

</div>

The `banfile` plug-in bans users by their principal class and the associated name. It is configured via a simple plain text file.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting"># Ban users by principal
alias dn=org.globus.gsi.jaas.GlobusPrincipal
alias kerberos=javax.security.auth.kerberos.KerberosPrincipal
alias fqan=org.dcache.auth.FQANPrincipal
alias name=org.dcache.auth.LoginNamePrincipal

ban name:ernie
ban kerberos:BERT@EXAMPLE.COM
ban com.example.SomePrincipal:Samson</pre>

In this example the first line is a comment. Lines 2 to 5 define aliases for principal class names that can then be used in the following banning section. The four aliases defined in this example are actually hard coded into `gPlazma`, therefore you can use these short names without explicitly defining them in your configuration file. Line 7 to 9 contain ban definitions. Line 9 directly uses the class name of a principal class instead of using an alias.

Please note that the plug-in only supports principals whose assiciated name is a single line of plain text. In programming terms this means the constructor of the principal class has to take exactly one single string parameter.

For the plugin to work, the configuration file has to exist even if it is empty.

</div>

</div>

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.banfile.path`</span></dt>

<dd>

Path to configuration file

Default: `<span>/etc/dcache</span>/ban.conf`

</dd>

</dl>

</div>

To activate the `banfile` plug-in it has to be added to `gplazma.conf`:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting"># Map grid or kerberos users to local accounts
auth    optional  x509
auth    optional  voms
map     requisite vorolemap
map     optional  krb5
map     optional  nis
session requisite nis
account requisite banfile</pre>

</div>

</div>

</div>

</div>

<div class="section" title="session Plug-ins">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-gplazma-gp2-configuration-plug-ins-session"></a>`session` Plug-ins

</div>

</div>

</div>

<div class="section" title="kpwd">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-kpwd-session"></a>kpwd

</div>

</div>

</div>

The `kpwd` plug-in adds root and home path information to the session, based on the username.

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.kpwd.file`</span></dt>

<dd>

Path to `dcache.kpwd`

Default: `<span>/etc/dcache</span>/dcache.kpwd`

</dd>

</dl>

</div>

</div>

<div class="section" title="authzdb">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-authzdb-session"></a>authzdb

</div>

</div>

</div>

The `authzdb` plug-in adds root and home path information to the session, based and username using the `storage-authzdb` file.

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.authzdb.file`</span></dt>

<dd>

Path to `storage-authzdb`

Default: `/etc/grid-security/storage-authzdb`

</dd>

</dl>

</div>

</div>

<div class="section" title="nsswitch">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-nsswitch-session"></a>nsswitch

</div>

</div>

</div>

The `nsswitch` plug-in adds root and home path information to the session, based on the username using your system’s `nsswitch` service.

Typically `nsswitch` plug-in will be combined with `vorolemap` plug-in, `gridmap` plug-in or `krb5` plug-in:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting"># Map grid users to local accounts
auth    optional  x509 #1
auth    optional  voms #2
map     requisite vorolemap #3
map     requisite nsswitch #4
session requisite nsswitch #5</pre>

In this example following is happening: extract user’s DN (1), extract and verify VOMS attributes (2), map DN+Role to a local account (3), extract uid and gids for a local account (4) and, finally, extract users home directory (5).

</div>

</div>

</div>

<div class="section" title="nis">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plugins-nis-session"></a>nis

</div>

</div>

</div>

The `nis` plug-in adds root and home path information to the session, based on the username using your site’s `NIS` service.

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.nis.server`</span></dt>

<dd>

`NIS` server host

Default: `nisserv.domain.com`

</dd>

<dt><span class="term">`gplazma.nis.domain`</span></dt>

<dd>

`NIS` domain

Default: `domain.com`

</dd>

</dl>

</div>

The result of `nis` plug-in can be used by other plug-ins:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting"># Map grid or kerberos users to local accounts
auth    optional  x509 #1
auth    optional  voms #2
map     requisite vorolemap #3
map     optional  krb5 #4
map     optional  nis #5
session requisite nis #6</pre>

In this example two access methods are considered: grid based and kerberos based. If user comes with grid certificate and VOMS role: extract user’s DN (1), extract and verify VOMS attributes (2), map DN+Role to a local account (3). If user comes with `Kerberos` ticket: extract local account (4). After this point in both cases we talk to `NIS` to get uid and gids for a local account (5) and, finally, adding users home directory (6).

</div>

</div>

</div>

</div>

<div class="section" title="identity Plug-ins">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-gplazma-gp2-configuration-plug-ins-identity"></a>`identity` Plug-ins

</div>

</div>

</div>

<div class="section" title="nsswitch">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plug-ins-nsswitch-identity"></a>nsswitch

</div>

</div>

</div>

The `nsswitch` plug-in provides forward and reverse mapping for `NFSv4.1` using your system’s `nsswitch` service.

</div>

<div class="section" title="nis">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-gp2-configuration-plugins-nis-identity"></a>nis

</div>

</div>

</div>

The `nis` plug-in forward and reverse mapping for `NFSv4.1` using your site’s `NIS` service.

<div class="variablelist" title="Properties">

**Properties**

<dl>

<dt><span class="term">`gplazma.nis.server`</span></dt>

<dd>

`NIS` server host

Default: `nisserv.domain.com`

</dd>

<dt><span class="term">`gplazma.nis.domain`</span></dt>

<dd>

`NIS` domain

Default: `domain.com`

</dd>

</dl>

</div>

</div>

</div>

</div>

</div>

<div class="section" title="Using X.509 Certificates">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-gplazma-certificates"></a>Using `X.509` Certificates

</div>

</div>

</div>

Most plug-ins of `gPlazma` support `X.509` certificates for authentication and authorisation. `X.509` certificates are used to identify entities (e.g., persons, hosts) in the Internet. The certificates contain a <acronym class="acronym">DN</acronym> (Distinguished Name) that uniquely describes the entity. To give the certificate credibility it is issued by a CA (Certificate Authority) which checks the identity upon request of the certificate (e.g., by checking the persons id). For the use of `X.509` certificates with <span class="productname">dCache</span> your users will have to request a certificate from a CA you trust and you need host certificates for every host of your <span class="productname">dCache</span> instance.

<div class="section" title="CA Certificates">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-gplazma-certificates-cacerts"></a>CA Certificates

</div>

</div>

</div>

To be able to locally verify the validity of the certificates, you need to store the CA certificates on your system. Most operating systems come with a number of commercial CA certificates, but for the <span class="emphasis">_Grid_</span> you will need the certificates of the Grid CAs. For this, CERN packages a number of CA certificates. These are deployed by most grid sites. By deploying these certificates, you state that you trust the CA’s procedure for the identification of individuals and you agree to act promptly if there are any security issues.

To install the CERN CA certificates follow the following steps:

    [root] #

This will create the directory `/etc/grid-security/certificates` which contains the Grid CA certificates.

Certificates which have been revoked are collected in certificate revocation lists (<acronym class="acronym">CRL</acronym>s). To get the <acronym class="acronym">CRL</acronym>s install the <span class="command">**fetch-crl**</span> command as described below.

    [root] #

<span class="command">**fetch-crl**</span> adds `X.509` <acronym class="acronym">CRL</acronym>s to `/etc/grid-security/certificates`. It is recommended to set up a cron job to periodically update the <acronym class="acronym">CRL</acronym>s.

</div>

<div class="section" title="User Certificate">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-gplazma-certificates-usercert"></a>User Certificate

</div>

</div>

</div>

If you do not have a valid grid user certificate yet, you have to request one from your CA. Follow the instructions from your CA on how to get a certificate. After your request was accepted you will get a URL pointing to your new certificate. Install it into your browser to be able to access grid resources with it. Once you have the certificate in your browser, make a backup and name it `userCertificate.p12`. Copy the user certificate to the directory `~/.globus/` on your worker node and convert it to `usercert.pem` and `userkey.pem` as described below.

    [user] $

During the backup your browser asked you for a password to encrypt the certificate. Enter this password here when asked for a password. This will create your user certificate.

    [user] $

In this step you need to again enter the backup password. When asked for the <acronym class="acronym">PEM</acronym> pass phrase choose a secure password. If you want to use your key without having to type in the pass phrase every time, you can remove it by executing the following command.

    [root] #

Now change the file permissions to make the key only readable by you and the certificate world readable and only writable by you.

    [root] #

</div>

<div class="section" title="Host Certificate">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-gplazma-certificates-hostcert"></a>Host Certificate

</div>

</div>

</div>

To request a host certificate for your server host, follow again the instructions of your CA.

The conversion to `hostcert.pem` and `hostkey.pem` works analogous to the user certificate. For the hostkey you have to remove the pass phrase. How to do this is also explained in the previous section. Finally copy the `host*.pem` files to `/etc/grid-security/` as `root` and change the file permissions in favour of the user running the grid application.

</div>

<div class="section" title="VOMS Proxy Certificate">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-voms-proxy-glite"></a><span class="productname">VOMS</span> Proxy Certificate

</div>

</div>

</div>

For very large groups of people, it is often more convenient to authorise people based on their membership of some group. To identify that they are a member of some group, the certificate owner can create a new short-lived `X.509` certificate that includes their membership of various groups. This short-lived certificate is called a proxy-certificate and, if the membership information comes from a <span class="productname">VOMS</span> server, it is often referred to as a <span class="productname">VOMS</span>-proxy.

    [root] #

<div class="section" title="Creating a VOMS proxy">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-gplazma-certificates-voms-proxy-init"></a><span class="command">**Creating a <span class="productname">VOMS</span> proxy**</span>

</div>

</div>

</div>

To create a <span class="productname">VOMS</span> proxy for your user certificate you need to execute the <span class="command">**voms-proxy-init**</span> as a user.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

</div>

</div>

<div class="section" title="Certifying your membership of a VO">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-gplazma-certificates-voms-proxy-init-voms"></a>Certifying your membership of a VO

</div>

</div>

</div>

You can certify your membership of a VO by using the command <span class="command">**voms-proxy-init -voms _<tt><yourVO></tt>_**</span>. This is useful as in <span class="productname">dCache</span> authorization can be done by VO (see [the section called “Authorizing a VO”](#cf-gplazma-plug-inconfig-voauth "Authorizing a VO")). To be able to use the extension <span class="command">**-voms _<tt><yourVO></tt>_**</span> you need to be able to access <span class="productname">VOMS</span> servers. To this end you need the the <span class="productname">VOMS</span> server’s and the CA’s DN. Create a file `/etc/grid-security/vomsdir/_<tt><VO></tt>_/_<tt><hostname></tt>_.lsc` per <span class="productname">VOMS</span> server containing on the 1st line the <span class="productname">VOMS</span> server’s DN and on the 2nd line, the corresponding CA’s DN. The name of this file should be the fully qualified hostname followed by an `.lsc` extension and the file must appear in a subdirectory `/etc/grid-security/vomsdir/_<tt><VO></tt>_` for each VO that is supported by that <span class="productname">VOMS</span> server and by the site.

At [http://operations-portal.egi.eu/vo](http://operations-portal.egi.eu/vo) you can search for a VO and find this information.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

For example, the file /etc/grid-security/vomsdir/desy/grid-voms.desy.de.lsc contains:

<pre class="programlisting">/C=DE/O=GermanGrid/OU=DESY/CN=host/grid-voms.desy.de
/C=DE/O=GermanGrid/CN=GridKa-CA</pre>

where the first entry is the DN of the DESY <span class="productname">VOMS</span> server and the second entry is the DN of the CA which signed the DESY <span class="productname">VOMS</span> server’s certificate.

</div>

</div>

In addition, you need to have a file `/opt/glite/etc/vomses` containing your VO’s <span class="productname">VOMS</span> server.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

For DESY the file `/opt/glite/etc/vomses` should contain the entry

<pre class="programlisting">"desy" "grid-voms.desy.de" "15104" "/C=DE/O=GermanGrid/OU=DESY/CN=host/grid-voms.desy.de" "desy" "24"</pre>

The first entry <span class="quote">“<span class="quote">desy</span>”</span> is the real name or a nickname of your VO. <span class="quote">“<span class="quote">grid-voms.desy.de</span>”</span> is the hostname of the <span class="productname">VOMS</span> server. The number <span class="quote">“<span class="quote">15104</span>”</span> is the port number the server is listening on. The forth entry is the DN of the server’s <span class="productname">VOMS</span> certificate. The fifth entry, <span class="quote">“<span class="quote">desy</span>”</span>, is the VO name and the last entry is the globus version number which is not used anymore and can be omitted.

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Use the command <span class="command">**voms-proxy-init -voms**</span> to create a <span class="productname">VOMS</span> proxy with VO <span class="quote">“<span class="quote">desy</span>”</span>.

    [user] $

View the information about your <span class="productname">VOMS</span> proxy with <span class="command">**voms-proxy-info**</span>

    [user] $

The last line tells you how much longer your proxy will be valid.

If your proxy is expired you will get

    [user] $

The command <span class="command">**voms-proxy-info -all**</span> gives you information about the proxy and about the VO.

    [user] $

Use the command <span class="command">**voms-proxy-destroy**</span> to destroy your <span class="productname">VOMS</span> proxy.

    [user] $

</div>

</div>

</div>

</div>

</div>

</div>

<div class="section" title="Configuration files">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-gplazma-plug-inconfig"></a>Configuration files

</div>

</div>

</div>

In this section we explain the format of the the `storage-authzdb`, `kpwd` and `vorolemap` files. They are used by the `authzdb` plug-in, `vorolemap` plug-in,and `kpwd` plug-in.

<div class="section" title="storage-authzdb">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-gplazma-plug-inconfig-authzdb"></a>`storage-authzdb`

</div>

</div>

</div>

In `gPlazma`, except for the `kpwd` plug-in, authorization is a two-step process. First, a username is obtained from a mapping of the user’s <acronym class="acronym">DN</acronym> or his <acronym class="acronym">DN</acronym> and role, then a mapping of username to <acronym class="acronym">UID</acronym> and <acronym class="acronym">GID</acronym> with optional additional session parameters like the root path is performed. For the second mapping usually the file called `storage-authzdb` is used.

<div class="section" title="Preparing storage-authzdb">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-gplazma-plug-inconfig-authzdb-preparation"></a>Preparing `storage-authzdb`

</div>

</div>

</div>

The default location of the `storage-authzdb` is `/etc/grid-security`. Before the mapping entries there has to be a line specifying the version of the used file format.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">version 2.1</pre>

</div>

</div>

<span class="productname">dCache</span> supports versions 2.1 and to some extend 2.2.

Except for empty lines and comments (lines start with `#`) the configuration lines have the following format:

<pre class="programlisting"> authorize _<tt><username></tt>_ (read-only|read-write) _<tt><<acronym class="acronym">UID</acronym>></tt>_ _<tt><<acronym class="acronym">GID</acronym>></tt>_[,_<tt><GID></tt>_]* _<tt><homedir></tt>_ _<tt><rootdir></tt>_ </pre>

For legacy reasons there may be a third path entry which is ignored by <span class="productname">dCache</span>. The username here has to be the name the user has been mapped to in the first step (e.g., by his <acronym class="acronym">DN</acronym>).

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">authorize john read-write 1001 100 / /data/experiments /</pre>

In this example user _<tt><john></tt>_ will be mapped to <acronym class="acronym">UID</acronym> 1001 and <acronym class="acronym">GID</acronym> 100 with read access on the directory `/data/experiments`. You may choose to set the user’s root directory to `/`.

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">authorize adm read-write 1000 100 / / /</pre>

In this case the user _<tt><adm></tt>_ will be granted read/write access in any path, given that the file system permissions in <span class="productname">Chimera</span> also allow the transfer.

</div>

</div>

The first path is nearly always left as <span class="quote">“<span class="quote">`/`</span>”</span>, but it may be used as a home directory in interactive session, as a subdirectory of the root path. Upon login, the second path is used as the user’s root, and a <span class="quote">“<span class="quote">cd</span>”</span> is performed to the first path. The first path is always defined as being relative to the second path.

Multiple <acronym class="acronym">GID</acronym>s can be assigned by using comma-separated values for the <acronym class="acronym">GID</acronym> file, as in

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">authorize john read-write 1001 100,101,200 / / /</pre>

</div>

</div>

The lines of the `storage-authzdb` file are similar to the <span class="quote">“<span class="quote">login</span>”</span> lines of the `dcache.kpwd` file. If you already have a `dcache.kwpd` file, you can easily create `storage-authzdb` by taking the lines from your `dcache.kpwd` file that start with the word `login`, for example,

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">login john read-write 1001 100 / /data/experiments /</pre>

</div>

</div>

and replace the word `login` with `authorize`. The following line does this for you.

    [root] #

</div>

</div>

<div class="section" title="The gplazmalite-vorole-mapping plug-in">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-gplazma-plug-inconfig-vorolemap"></a>The gplazmalite-vorole-mapping plug-in

</div>

</div>

</div>

The second is the `storage-authzdb` used in other plug-ins. See the above documentation on [`storage-authdb`](#cf-gplazma-plug-inconfig-authzdb "storage-authzdb") for how to create the file.

<div class="section" title="Preparing grid-vorolemap">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-gplazma-plug-inconfig-vorolemap-gridvorolemap"></a>Preparing `grid-vorolemap`

</div>

</div>

</div>

The file is similar in format to the `grid-mapfile`, however there is an additional field following the <acronym class="acronym">DN</acronym> (Certificate Subject), containing the <acronym class="acronym">FQAN</acronym> (Fully Qualified Attribute Name).

<pre class="programlisting">"/C=DE/O=GermanGrid/OU=DESY/CN=John Doe" "/some-vo" doegroup
"/C=DE/DC=GermanGrid/O=DESY/CN=John Doe" "/some-vo/Role=NULL" doegroup
"/C=DE/DC=GermanGrid/O=DESY/CN=John Doe" "/some-vo/Role=NULL/Capability=NULL" doegroup </pre>

Therefore each line has three fields: the user’s <acronym class="acronym">DN</acronym>, the user’s <acronym class="acronym">FQAN</acronym>, and the username that the <acronym class="acronym">DN</acronym> and <acronym class="acronym">FQAN</acronym> combination are to be mapped to.

The <acronym class="acronym">FQAN</acronym> is sometimes semantically referred to as the <span class="quote">“<span class="quote">role</span>”</span>. The same user can be mapped to different usernames depending on what their <acronym class="acronym">FQAN</acronym> is. The <acronym class="acronym">FQAN</acronym> is determined by how the user creates their proxy, for example, using [<span class="command">**voms-proxy-init**</span>](#cb-voms-proxy-glite "VOMS Proxy Certificate") . The <acronym class="acronym">FQAN</acronym> contains the user’s Group, Role (optional), and Capability (optional). The latter two may be set to the string <span class="quote">“<span class="quote">NULL</span>”</span>, in which case they will be ignored by the plug-in. Therefore the three lines in the example above are equivalent.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

If a user is authorized in multiple roles, for example

<pre class="programlisting">"/DC=org/DC=doegrids/OU=People/CN=John Doe" "/some-vo/sub-grp" vo_sub_grp_user
"/DC=org/DC=doegrids/OU=People/CN=John Doe" "/some-vo/sub-grp/Role=user" vouser
"/DC=org/DC=doegrids/OU=People/CN=John Doe" "/some-vo/sub-grp/Role=admin" voadmin
"/DC=org/DC=doegrids/OU=People/CN=John Doe" "/some-vo/sub-grp/Role=prod" voprod</pre>

he will get the username corresponding to the <acronym class="acronym">FQAN</acronym> found in the proxy that the user creates for use by the client software. If the user actually creates several roles in his proxy, authorization (and subsequent check of path and file system permissions) will be attempted for each role in the order that they are found in the proxy.

In a `GridFTP` <acronym class="acronym">URL</acronym>, the user may also explicitly request a username.

<pre class="programlisting">gsiftp://doeprod@ftp-door.example.org:2811/testfile1</pre>

in which case other roles will be disregarded.

</div>

</div>

</div>

</div>

<div class="section" title="Authorizing a VO">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-gplazma-plug-inconfig-voauth"></a>Authorizing a VO

</div>

</div>

</div>

Instead of individual <acronym class="acronym">DN</acronym>s, it is allowed to use `*` or `"*"` as the first field, such as

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">"*" "/desy/Role=production/" desyprod </pre>

In that case, any <acronym class="acronym">DN</acronym> with the corresponding role will match. It should be noted that a match is first attempted with the explicit <acronym class="acronym">DN</acronym>. Therefore if both <acronym class="acronym">DN</acronym> and `"*"` matches can be made, the <acronym class="acronym">DN</acronym> match will take precedence. This is true for the revocation matches as well (see below).

Thus a user with subject `/C=DE/O=GermanGrid/OU=DESY/CN=John Doe` and role `/desy/Role=production` will be mapped to username `desyprod` via the above `storage-authzdb` line with `"*"` for the <acronym class="acronym">DN</acronym>, except if there is also a line such as

<pre class="programlisting">"/C=DE/O=GermanGrid/OU=DESY/CN=John Doe" "/desy/Role=production" desyprod2</pre>

in which case the username will be `desyprod2`.

</div>

</div>

<div class="section" title="Revocation Entries">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp3485168"></a>Revocation Entries

</div>

</div>

</div>

To create a revocation entry, add a line with a dash (`-`) as the username, such as

<pre class="programlisting">"/C=DE/O=GermanGrid/OU=DESY/CN=John Doe" "/desy/production" -</pre>

or modify the username of the entry if it already exists. The behaviour is undefined if there are two entries which differ only by username.

Since <acronym class="acronym">DN</acronym> is matched first, if a user would be authorized by his VO membership through a `"*"` entry, but is matched according to his <acronym class="acronym">DN</acronym> to a revocation entry, authorization would be denied. Likewise if a whole VO were denied in a revocation entry, but some user in that VO could be mapped to a username through his <acronym class="acronym">DN</acronym>, then authorization would be granted.

</div>

<div class="section" title="More Examples">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp3491168"></a>More Examples

</div>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Suppose that there are users in production roles that are expected to write into the storage system data which will be read by other users. In that case, to protect the data the non-production users would be given read-only access. Here in `/etc/grid-security/grid-vorolemap` the production role maps to username `cmsprod`, and the role which reads the data maps to `cmsuser`.

<pre class="programlisting">"*" "/cms/uscms/Role=cmsprod" cmsprod "*" "/cms/uscms/Role=cmsuser" cmsuser</pre>

The read-write privilege is controlled by the third field in the lines of `/etc/grid-security/storage-authzdb`

<pre class="programlisting">authorize cmsprod  read-write  9811 5063 / /data /
authorize cmsuser  read-only  10001 6800 / /data /</pre>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Another use case is when users are to have their own directories within the storage system. This can be arranged within the `gPlazma` configuration files by mapping each user’s <acronym class="acronym">DN</acronym> to a unique username and then mapping each username to a unique root path. As an example, lines from `/etc/grid-security/grid-vorolemap` would therefore be written

<pre class="programlisting">"/DC=org/DC=doegrids/OU=People/CN=Selby Booth" "/cms" cms821
"/DC=org/DC=doegrids/OU=People/CN=Kenja Kassi" "/cms" cms822
"/DC=org/DC=doegrids/OU=People/CN=Ameil Fauss" "/cms" cms823</pre>

and the corresponding lines from `/etc/grid-security/storage-authzdb` would be

<pre class="programlisting">authorize cms821 read-write 10821 7000 / /data/cms821 /
authorize cms822 read-write 10822 7000 / /data/cms822 /
authorize cms823 read-write 10823 7000 / /data/cms823 /</pre>

</div>

</div>

</div>

</div>

<div class="section" title="The kpwd plug-in">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-gplazma-kpwd"></a>The kpwd plug-in

</div>

</div>

</div>

The section in the `gPlazma` policy file for the kpwd plug-in specifies the location of the `dcache.kpwd` file, for example

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting"># dcache.kpwd
kpwdPath="<span>/etc/dcache</span>/dcache.kpwd"</pre>

</div>

</div>

To maintain only one such file, make sure that this is the same location as defined in `<span>/usr/share/dcache</span>/defaults/dcache.properties`.

Use `<span>/usr/share/dcache</span>/examples/gplazma/dcache.kpwd` to create this file.

To be able to alter entries in the `dcache.kpwd` file conveniantly the dcache script offers support for doing this.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

adds this to the kpwd file:

<pre class="programlisting">passwd testuser ae39aec3 read-write 12345 1000 / /</pre>

</div>

</div>

There are many more commands for altering the kpwd-file, see the dcache-script help for further commands available.

</div>

<div class="section" title="The gridmap plug-in">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-gplazma-gridmap"></a>The `gridmap` plug-in

</div>

</div>

</div>

Two file locations are defined in the policy file for this plug-in:

<pre class="programlisting"># grid-mapfile
gridMapFilePath="/etc/grid-security/grid-mapfile"
storageAuthzPath="/etc/grid-security/storage-authzdb"</pre>

<div class="section" title="Preparing the grid-mapfile">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp3519488"></a>Preparing the `grid-mapfile`

</div>

</div>

</div>

The `grid-mapfile` is the same as that used in other applications. It can be created in various ways, either by connecting directly to <span class="productname">VOMS</span> or <span class="productname">GUMS</span> servers, or by hand.

Each line contains two fields: a <acronym class="acronym">DN</acronym> (Certificate Subject) in quotes, and the username it is to be mapped to.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">"/C=DE/O=GermanGrid/OU=DESY/CN=John Doe" johndoe</pre>

</div>

</div>

When using the `gridmap` plug-in, the `storage-authzdb` file must also be configured. See [the section called “`storage-authzdb`”](#cf-gplazma-plug-inconfig-authzdb "storage-authzdb") for details.

</div>

</div>

</div>

<div class="section" title="gPlazma specific dCache configuration">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-gplazma-setup"></a>`gPlazma` specific <span class="productname">dCache</span> configuration

</div>

</div>

</div>

<span class="productname">dCache</span> has many parameters that can be used to configure the systems behaviour. You can find all these parameters well documented and together with their default values in the properties files in `<span>/usr/share/dcache</span>/defaults/`. To use non-default values, you have to set the new values in `<span>/etc/dcache</span>/dcache.conf` or in the layout file. Do not change the defaults in the properties files! After changing a parameter you have to restart the concerned cells.

Refer to the file `gplazma.properties` for a full list of properties for `gPlazma` One commonly used property is `gplazma.cell.limits.threads`, which is used to set the maximum number of concurrent requests to `gPlazma`. The default value is `30`.

Setting the value for `gplazma.cell.limits.threads` too high may result in large spikes of CPU activity and the potential to run out of memory. Setting the number too low results in potentially slow login activity.

<div class="section" title="Enabling Username/Password Access for WebDAV">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-gplazma-username-password-webdav-example"></a>Enabling Username/Password Access for `WebDAV`

</div>

</div>

</div>

This section describes how to activate the Username/Password access for `WebDAV`. It uses `dcache.kwpd` file as an example format for storing Username/Password information. First make sure `gPlazma2` is enabled in the `<span>/etc/dcache</span>/dcache.conf` or in the layout file.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Check your `WebDAV` settings: enable the `HTTP` access, disallow the anonymous access, disable requesting and requiring the client authentication and activate basic authentication.

<pre class="programlisting">webdav.authn.protocol=http
webdav.authz.anonymous-operations=NONE
webdav.authn.accept-client-cert=false
webdav.authn.require-client-cert=false
webdav.authn.basic=true</pre>

Adjust the `<span>/etc/dcache</span>/gplazma.conf` to use the `kpwd` plug-in (for more information see also [the section called “Plug-ins”](#cf-gplazma-gp2-configuration-plug-ins "Plug-ins")).

It will look something like this:

<pre class="programlisting">auth optional kpwd
map requisite kpwd
session requisite kpwd</pre>

The `<span>/etc/dcache</span>/dcache.kpwd` file is the place where you can specify the username/password record. It should contain the username and the password hash, as well as <acronym class="acronym">UID</acronym>, <acronym class="acronym">GID</acronym>, access mode and the home, root and fsroot directories:

<pre class="programlisting"># set passwd
passwd tanja 6a4cd089 read-write 500 100 / / /</pre>

The passwd-record could be automatically generated by the <span class="productname">dCache</span> kpwd-utility, for example:

    [root] #

</div>

</div>

Some file access examples:

<pre class="programlisting">curl -u tanja:dickerelch http://webdav-door.example.org:2880/pnfs/</pre>

<pre class="programlisting">wget --user=tanja --password=dickerelch http://webdav-door.example.org:2880/pnfs/</pre>

</div>

<div class="section" title="gPlazma config example to work with authenticated webadmin">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-gplazma-webadmin-example"></a>`gPlazma` config example to work with authenticated webadmin

</div>

</div>

</div>

This section describes how to configure `gplazma` to enable the webadmin servlet in authenticated mode with a grid certificate as well as with a username/password and how to give a user administrator access.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

In this example for the `<span>/etc/dcache</span>/gplazma.conf` file the `X.509` plug-in plugin is used for the authentication step with the grid certificate and the `kpwd` plug-in plugin is used for the authentication step with username/password.

<pre class="programlisting">auth optional x509
auth optional kpwd
map requisite kpwd
session requisite kpwd</pre>

The following example will show how to set up the `<span>/etc/dcache</span>/dcache.kpwd` file:

<pre class="programlisting">version 2.1

mapping "/C=DE/O=ExampleOrganisation/OU=EXAMPLE/CN=John Doe" john
# the following are the user auth records
login john read-write 1700 1000 / / /
/C=DE/O=ExampleOrganisation/OU=EXAMPLE/CN=John Doe

# set pwd
passwd john 8402480 read-write 1700 1000 / / /</pre>

This maps the DN of a grid certificate `subject=/C=DE/O=ExampleOrganisation/OU=EXAMPLE/CN=John Doe` to the user `john` and the entry

<pre class="programlisting">login john read-write 1700 1000 / / /
  /C=DE/O=GermanGrid/OU=DESY/CN=John Doe</pre>

applies unix-like values to `john`, most important is the `1000`, because it is the assigned <acronym class="acronym">GID</acronym>. This must match the value of the `httpd.authz.admin-gid` configured in your webadmin. This is sufficient for login using a certificate. The entry:

<pre class="programlisting">passwd john 8402480 read-write 1700 1000 / / /</pre>

enables username/password login, such as a valid login would be user `john` with some password. The password is encrypted with the kpwd-algorithm (also see [the section called “The kpwd plug-in”](#cf-gplazma-kpwd "The kpwd plug-in")) and then stored in the file. Again the `1000` here is the assigned <acronym class="acronym">GID</acronym>.

</div>

</div>

</div>

</div>

</div>

<div class="chapter" title="Chapter 11\. dCache as xRootd-Server">

<div class="titlepage">

<div>

<div>

## <a name="cf-xrootd"></a>Chapter 11\. dCache as xRootd-Server

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Setting up](#cf-xrootd-setup)</span></dt>

<dd>

<dl>

<dt><span class="section">[Parameters](#cf-xrootd-setup-params)</span></dt>

</dl>

</dd>

<dt><span class="section">[Quick tests](#cf-xrootd-tests)</span></dt>

<dd>

<dl>

<dt><span class="section">[Copying files with xrdcp](#cf-xrootd-tests-xrdcp)</span></dt>

<dt><span class="section">[Accessing files from within ROOT](#cf-xrootd-tests-ROOT)</span></dt>

</dl>

</dd>

<dt><span class="section">[`xrootd` security](#cf-xrootd-sec)</span></dt>

<dd>

<dl>

<dt><span class="section">[Read-Write access](#cf-xrootd-sec-ro)</span></dt>

<dt><span class="section">[Permitting read/write access on selected directories](#cf-xrootd-sec-selected)</span></dt>

<dt><span class="section">[Token-based authorization](#cf-xrootd-sec-authz)</span></dt>

<dt><span class="section">[Strong authentication](#cf-xrootd-sec-authn)</span></dt>

<dt><span class="section">[Precedence of security mechanisms](#cf-xrootd-sec-precedence)</span></dt>

<dt><span class="section">[Other configuration options](#cf-xrootd-other-configuration)</span></dt>

</dl>

</dd>

</dl>

</div>

This chapter explains how to configure <span class="productname">dCache</span> in order to access it via the `xrootd` protocol, allowing `xrootd`-Clients like ROOT’s TXNetfile and xrdcp to do file operations against a <span class="productname">dCache</span> instance in a transparent manner. <span class="productname">dCache</span> implements version 2.1.6 of `xrootd` protocol.

<div class="section" title="Setting up">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-xrootd-setup"></a>Setting up

</div>

</div>

</div>

To allow file transfers in and out of <span class="productname">dCache</span> using xrootd, a new ``xrootd` door` must be started. This door acts then as the entry point to all `xrootd` requests. Compared to the native xrootd server-implementation (produced by SLAC), the ``xrootd` door` corresponds to the `redirector node`.

To enable the ``xrootd` door`, you have to change the layout file corresponding to your <span class="productname">dCache</span>-instance. Enable the xrootd-service within the domain that you want to run it by adding the following line

<pre class="programlisting">..
[_<tt><domainName></tt>_/xrootd]
..</pre>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

You can just add the following lines to the layout file:

<pre class="programlisting">..
[xrootd-${host.name}Domain]
[xrootd-${host.name}Domain/xrootd]
..</pre>

</div>

</div>

After a restart of the domain running the ``xrootd` door`, done e.g. by executing

    [root] #

the ``xrootd` door` should be running. A few minutes later it should appear at the web monitoring interface under "Cell Services" (see [the section called “The Web Interface for Monitoring <span class="productname">dCache</span>”](#intouch-web "The Web Interface for Monitoring dCache")).

<div class="section" title="Parameters">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-xrootd-setup-params"></a>Parameters

</div>

</div>

</div>

The default port the ``xrootd` door` is listening on is 1094\. This can be changed two ways:

<div class="orderedlist">

1.  <span class="emphasis">_Per door:_</span> Edit your instance’s layout file, for example `<span>/etc/dcache</span>/layouts/example.conf` and add the desired port for the ``xrootd` door` in a separate line (a restart of the domain(s) running the ``xrootd` door` is required):

    <pre class="screen">..
    [xrootd-${host.name}Domain]
    [xrootd-${host.name}Domain/xrootd]
        port = 1095
    ..</pre>

2.  <span class="emphasis">_Globally:_</span> Edit `<span>/etc/dcache</span>/dcache.conf` and add the variable `xrootd.net.port` with the desired value (a restart of the domain(s) running the ``xrootd` door` is required):

    <pre class="screen">..
    xrootd.net.port=1095
    ..</pre>

</div>

For controlling the `TCP`-portrange within which `xrootd`-movers will start listening in the `_<tt><pool></tt>_Domain`, you can add the properties `dcache.net.lan.port.min` and `dcache.net.lan.port.max` to `<span>/etc/dcache</span>/dcache.conf` and adapt them according to your preferences. The default values can be viewed in `<span>/usr/share/dcache</span>/defaults/dcache.properties`.

<pre class="programlisting">..
dcache.net.lan.port.min=30100
dcache.net.lan.port.max=30200
..</pre>

</div>

</div>

<div class="section" title="Quick tests">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-xrootd-tests"></a>Quick tests

</div>

</div>

</div>

The subsequent paragraphs describe a quick guide on how to test `xrootd` using the `xrdcp` and `ROOT` clients.

<div class="section" title="Copying files with xrdcp">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-xrootd-tests-xrdcp"></a>Copying files with xrdcp

</div>

</div>

</div>

A simple way to get files in and out of <span class="productname">dCache</span> via `xrootd` is the command xrdcp. It is included in every xrootd and ROOT distribution.

To transfer a single file in and out of <span class="productname">dCache</span>, just issue

    [user] $

</div>

<div class="section" title="Accessing files from within ROOT">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-xrootd-tests-ROOT"></a>Accessing files from within ROOT

</div>

</div>

</div>

This simple ROOT example shows how to write a randomly filled histogram to a file in <span class="productname">dCache</span>:

<pre class="screen">root [0] TH1F h("testhisto", "test", 100, -4, 4);
root [1] h->FillRandom("gaus", 10000);
root [2] TFile *f = new TXNetFile("root://_<tt><door_hostname></tt>_//pnfs/_<tt><example.org></tt>_/data/test.root","new");
061024 12:03:52 001 Xrd: Create: (C) 2004 SLAC INFN XrdClient 0.3
root [3] h->Write();
root [4] f->Write();
root [5] f->Close();
root [6] 061101 15:57:42 14991 Xrd: XrdClientSock::RecvRaw: Error reading from socket: Success
061101 15:57:42 14991 Xrd: XrdClientMessage::ReadRaw: Error reading header (8 bytes)</pre>

Closing remote `xrootd` files that live in <span class="productname">dCache</span> produces this warning, but has absolutely no effect on subsequent ROOT commands. It happens because <span class="productname">dCache</span> closes all `TCP` connections after finishing a file transfer, while xrootd expects to keep them open for later reuse.

To read it back into ROOT from <span class="productname">dCache</span>:

<pre class="screen">root [7] TFile *reopen = TXNetFile ("root://_<tt><door_hostname></tt>_//pnfs/_<tt><example.org></tt>_/data/test.root","read");
root [8] reopen->ls();
TXNetFile**             //pnfs/_<tt><example.org></tt>_/data/test.root
 TXNetFile*             //pnfs/_<tt><example.org></tt>_/data/test.root
  KEY: TH1F     testhisto;1     test</pre>

</div>

</div>

<div class="section" title="xrootd security">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-xrootd-sec"></a>`xrootd` security

</div>

</div>

</div>

<div class="section" title="Read-Write access">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-xrootd-sec-ro"></a>Read-Write access

</div>

</div>

</div>

Per default <span class="productname">dCache</span> `xrootd` is restricted to read-only, because plain `xrootd` is completely unauthenticated. A typical error message on the clientside if the server is read-only looks like:

<pre class="screen"> `[user] <pre class="screen" **`xrdcp -d 1 /bin/sh root://ford.desy.de//pnfs/desy.de/data/xrd_test2`**
Setting debug level 1
061024 18:43:05 001 Xrd: main: (C) 2004 SLAC INFN xrdcp 0.2 beta
061024 18:43:05 001 Xrd: Create: (C) 2004 SLAC INFN XrdClient kXR_ver002+kXR_asyncap
061024 18:43:05 001 Xrd: ShowUrls: The converted URLs count is 1
061024 18:43:05 001 Xrd: ShowUrls: URL n.1: root://ford.desy.de:1094//pnfs/desy.de/data/asdfas.
061024 18:43:05 001 Xrd: Open: Access to server granted.
061024 18:43:05 001 Xrd: Open: Opening the remote file /pnfs/desy.de/data/asdfas
061024 18:43:05 001 Xrd: XrdClient::TryOpen: doitparallel=1
061024 18:43:05 001 Xrd: Open: File open in progress.
061024 18:43:06 5819 Xrd: SendGenCommand: Server declared: <span class="command">**Permission denied. Access is read only.(error code: 3003)**</span>
061024 18:43:06 001 Xrd: Close: File not opened.
Error accessing path/file for root://ford//pnfs/desy.de/data/asdfas</pre>

To enable read-write access, add the following line to `${dCacheHome}/etc/dcache.conf`

<pre class="programlisting">..
xrootdIsReadOnly=false
..</pre>

and restart any domain(s) running a ``xrootd` door`.

Please note that due to the unauthenticated nature of this access mode, files can be written and read to/from any subdirectory in the <span class="productname">`pnfs`</span> namespace (including the automatic creation of parent directories). If there is no user information at the time of request, new files/subdirectories generated through `xrootd` will inherit UID/GID from its parent directory. The user used for this can be configured via the `xrootd.authz.user` property.

</div>

<div class="section" title="Permitting read/write access on selected directories">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-xrootd-sec-selected"></a>Permitting read/write access on selected directories

</div>

</div>

</div>

To overcome the security issue of uncontrolled `xrootd` read and write access mentioned in the previous section, it is possible to restrict read and write access on a per-directory basis (including subdirectories).

To activate this feature, a colon-seperated list containing the full paths of authorized directories must be added to `<span>/etc/dcache</span>/dcache.conf`. You will need to specify the read and write permissions separately.

<pre class="programlisting">..
xrootd.authz.read-paths=/pnfs/_<tt><example.org></tt>_/rpath1:/pnfs/_<tt><example.org></tt>_/rpath2
xrootd.authz.write-paths=/pnfs/_<tt><example.org></tt>_/wpath1:/pnfs/_<tt><example.org></tt>_/wpath2
..</pre>

A restart of the ``xrootd` door` is required to make the changes take effect. As soon as any of the above properties are set, all read or write requests to directories not matching the allowed path lists will be refused. Symlinks are however not restricted to these prefixes.

</div>

<div class="section" title="Token-based authorization">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-xrootd-sec-authz"></a>Token-based authorization

</div>

</div>

</div>

The `xrootd` <span class="productname">dCache</span> implementation includes a generic mechanism to plug in different authorization handlers. The only plugin available so far implements token-based authorization as suggested in [http://people.web.psi.ch/feichtinger/doc/authz.pdf](http://people.web.psi.ch/feichtinger/doc/authz.pdf).

The first thing to do is to setup the keystore. The keystore file basically specifies all RSA-keypairs used within the authorization process and has exactly the same syntax as in the native xrootd tokenauthorization implementation. In this file, each line beginning with the keyword `KEY` corresponds to a certain Virtual Organisation (VO) and specifies the remote public (owned by the file catalogue) and the local private key belonging to that VO. A line containing the statement `"KEY VO:*"` defines a default keypair that is used as a fallback solution if no VO is specified in token-enhanced `xrootd` requests. Lines not starting with the `KEY` keyword are ignored. A template can be found in `<span>/usr/share/dcache</span>/examples/xrootd/keystore`.

The keys itself have to be converted into a certain format in order to be loaded into the authorization plugin. <span class="productname">dCache</span> expects both keys to be binary DER-encoded (Distinguished Encoding Rules for ASN.1). Furthermore the private key must be PKCS #8-compliant and the public key must follow the X.509-standard.

The following example demonstrates how to create and convert a keypair using OpenSSL:

<pre class="screen">_<span class="lineannotation">Generate new RSA private key</span>_
`[root] #` **`openssl genrsa -rand 12938467 -out key.pem 1024`**

_<span class="lineannotation">Create certificate request</span>_
`[root] #` **`openssl req -new -inform PEM -key key.pem -outform PEM -out certreq.pem`**

_<span class="lineannotation">Create certificate by self-signing certificate request</span>_
`[root] #` **`openssl x509 -days 3650 -signkey key.pem -in certreq.pem -req -out cert.pem`**

_<span class="lineannotation">Extract public key from certificate</span>_
`[root] #` **`openssl x509 -pubkey -in cert.pem -out pkey.pem`**
`[root] #` **`openssl pkcs8 -in key.pem -topk8 -nocrypt -outform DER -out _<tt><new_private_key></tt>_`**
`[root] #` **`openssl enc -base64 -d -in pkey.pem -out _<tt><new_public_key></tt>_`**</pre>

Only the last two lines are performing the actual conversion, therefore you can skip the previous lines in case you already have a keypair. Make sure that your keystore file correctly points to the converted keys.

To enable the plugin, it is necessary to add the following two lines to the file `<span>/etc/dcache</span>/dcache.conf`, so that it looks like

<pre class="programlisting">..
	xrootdAuthzPlugin=org.dcache.xrootd.security.plugins.tokenauthz.TokenAuthorizationFactory
	xrootdAuthzKeystore=_<tt><Path_to_your_Keystore></tt>_
	..</pre>

After doing a restart of <span class="productname">dCache</span>, any requests without an appropriate token should result in an error saying "`authorization check failed: No authorization token found in open request, access denied.(error code: 3010)`".

If both tokenbased authorization and read-only access are activated, the read-only restriction will dominate (local settings have precedence over remote file catalogue permissions).

</div>

<div class="section" title="Strong authentication">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-xrootd-sec-authn"></a>Strong authentication

</div>

</div>

</div>

The `xrootd`-implementation in <span class="productname">dCache</span> includes a pluggable authentication framework. To control which authentication mechanism is used by `xrootd`, add the `xrootdAuthNPlugin` option to your <span class="productname">dCache</span> configuration and set it to the desired value.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

For instance, to enable `GSI` authentication in `xrootd`, add the following line to `<span>/etc/dcache</span>/dcache.conf`:

<pre class="programlisting">..
xrootdAuthNPlugin=gsi
..</pre>

When using `GSI` authentication, depending on your setup, you may or may not want <span class="productname">dCache</span> to fail if the host certificate chain can not be verified against trusted certificate authorities. Whether <span class="productname">dCache</span> performs this check can be controlled by setting the option `dcache.authn.hostcert.verify`:

<pre class="programlisting">..
dcache.authn.hostcert.verify=true
..
</pre>

</div>

</div>

<span class="emphasis">_Authorization_</span> of the user information obtained by strong authentication is performed by contacting the `gPlazma` service. Please refer to [Chapter 10, _Authorization in <span class="productname">dCache</span>_](#cf-gplazma "Chapter 10\. Authorization in dCache") for instructions about how to configure `gPlazma`.

<div class="warning" title="Security consideration" style="margin-left: 0.5in; margin-right: 0.5in;">

### Security consideration

In general `GSI` on `xrootd` is not secure. It does not provide confidentiality and integrity guarantees and hence does not protect against man-in-the-middle attacks.

</div>

</div>

<div class="section" title="Precedence of security mechanisms">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-xrootd-sec-precedence"></a>Precedence of security mechanisms

</div>

</div>

</div>

The previously explained methods to restrict access via `xrootd` can also be used together. The precedence applied in that case is as following:

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

The `xrootd`-door can be configured to use either token authorization or strong authentication with `gPlazma` authorization. A combination of both is currently not possible.

</div>

The permission check executed by the authorization plugin (if one is installed) is given the lowest priority, because it can controlled by a remote party. E.g. in the case of token based authorization, access control is determined by the file catalogue (global namespace).

The same argument holds for many strong authentication mechanisms - for example, both the `GSI` protocol as well as the `Kerberos` protocols require trust in remote authorities. However, this only affects user <span class="emphasis">_authentication_</span>, while authorization decisions can be adjusted by local site administrators by adapting the `gPlazma` configuration.

To allow local site’s administrators to override remote security settings, write access can be further restricted to few directories (based on the local namespace, the <span class="productname">`pnfs`</span>). Setting `xrootd` access to read-only has the highest priority, overriding all other settings.

</div>

<div class="section" title="Other configuration options">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-xrootd-other-configuration"></a>Other configuration options

</div>

</div>

</div>

The `xrootd`-door has several other configuration properties. You can configure various timeout parameters, the thread pool sizes on pools, queue buffer sizes on pools, the `xrootd` root path, the `xrootd` user and the `xrootd` IO queue. Full descriptions on the effect of those can be found in `<span>/usr/share/dcache</span>/defaults/xrootd.properties`.

</div>

</div>

</div>

<div class="chapter" title="Chapter 12\. dCache as NFSv4.1 Server">

<div class="titlepage">

<div>

<div>

## <a name="cf-nfs4"></a>Chapter 12\. <span class="productname">dCache</span> as `NFSv4.1` Server

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Setting up](#cf-nfs4-setup)</span></dt>

<dt><span class="section">[Configuring ``NFSv4.1` door` with GSS-API support](#cf-nfs4-gss)</span></dt>

<dt><span class="section">[Configuring principal-id mapping for NFS access](#cf-idmap)</span></dt>

</dl>

</div>

This chapter explains how to configure <span class="productname">dCache</span> in order to access it via the `NFSv4.1` protocol, allowing clients to mount <span class="productname">dCache</span> and perform <acronym class="acronym">POSIX</acronym> IO using standard `NFSv4.1` clients.

<div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

### Important

The `pNFS` mentioned in this chapter is the protocol `NFSv4.1/pNFS` and not the namespace <span class="productname">`pnfs`</span>.

</div>

<div class="section" title="Setting up">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-nfs4-setup"></a>Setting up

</div>

</div>

</div>

To allow file transfers in and out of <span class="productname">dCache</span> using `NFSv4.1/pNFS`, a new ``NFSv4.1` door` must be started. This door acts then as the mount point for `NFS` clients.

To enable the ``NFSv4.1` door`, you have to change the layout file corresponding to your <span class="productname">dCache</span>-instance. Enable the `nfs` within the domain that you want to run it by adding the following line

<pre class="programlisting">..
[_<tt><domainName></tt>_/nfs]
nfs.version = 4.1
..</pre>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

You can just add the following lines to the layout file:

<pre class="programlisting">..
[nfs-${host.name}Domain]
[nfs-${host.name}Domain/nfs]
nfs.version = 4.1
..</pre>

</div>

</div>

In addition to run an ``NFSv4.1` door` you need to add exports to the `/etc/exports` file. The format of `/etc/exports` is similar to the one which is provided by Linux:

<pre class="programlisting">#
<path> [host [(options)]]</pre>

Where _<tt><options></tt>_ is a comma separated combination of:

<div class="variablelist">

<dl>

<dt><span class="term">`ro`</span></dt>

<dd>

matching clients can access this export only in read-only mode

</dd>

<dt><span class="term">`rw`</span></dt>

<dd>

matching clients can access this export only in read-write mode

</dd>

<dt><span class="term">`sec=krb5`</span></dt>

<dd>

matching clients must access `NFS` using <acronym class="acronym">RPCSEC_GSS</acronym> authentication. The Quality of Protection (QOP) is <span class="emphasis">_NONE_</span>, e.g., the data is neither encrypted nor signed when sent over the network. Nevertheless the RPC packets header still protected by checksum.

</dd>

<dt><span class="term">`sec=krb5i`</span></dt>

<dd>

matching clients have to access `NFS` using <acronym class="acronym">RPCSEC_GSS</acronym> authentication. The Quality of Protection (QOP) is <span class="emphasis">_INTEGRITY_</span>. The RPC requests and response are protected by checksum.

</dd>

<dt><span class="term">`sec=krb5p`</span></dt>

<dd>

matching clients have to access `NFS` using <acronym class="acronym">RPCSEC_GSS</acronym> authentication. The Quality of Protection (QOP) is <span class="emphasis">_PRIVACY_</span>. The RPC requests and response are protected by encryption.

</dd>

</dl>

</div>

For example:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">#
/pnfs/dcache.org/data *.dcache.org (rw,sec=krb5i)</pre>

</div>

</div>

Notice, that security flavour used at mount time will be used for client - pool comminication as well.

</div>

<div class="section" title="Configuring NFSv4.1 door with GSS-API support">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-nfs4-gss"></a>Configuring ``NFSv4.1` door` with GSS-API support

</div>

</div>

</div>

Adding `sec=krb5` into `/etc/exports` is not sufficient to get kerberos authentication to work.

All clients, pool nodes and node running ``NFSv4.1` door` must have a valid kerberos configuration. Each clients, pool node and node running ``NFSv4.1` door` must have a `/etc/krb5.keytab` with `nfs` service principal:

<pre class="programlisting">nfs/host.domain@_<tt><YOUR.REALM></tt>_</pre>

The `<span>/etc/dcache</span>/dcache.conf` on pool nodes and node running ``NFSv4.1` door` must enable kerberos and <acronym class="acronym">RPCSEC_GSS</acronym>:

<pre class="programlisting">nfs.rpcsec_gss=true
dcache.authn.kerberos.realm=_<tt><YOUR.REALM></tt>_
dcache.authn.jaas.config=<span>/etc/dcache</span>/gss.conf
dcache.authn.kerberos.key-distribution-center-list=your.kdc.server</pre>

The `<span>/etc/dcache</span>/gss.conf` on pool nodes and node running ``NFSv4.1` door` must configure Java’s security module:

<pre class="programlisting">com.sun.security.jgss.accept {
com.sun.security.auth.module.Krb5LoginModule required
doNotPrompt=true
useKeyTab=true
keyTab="${/}etc${/}krb5.keytab"
debug=false
storeKey=true
principal="nfs/host.domain@_<tt><YOUR.REALM></tt>_";
};</pre>

Now your `NFS` client can securely access <span class="productname">dCache</span>.

</div>

<div class="section" title="Configuring principal-id mapping for NFS access">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-idmap"></a>Configuring principal-id mapping for NFS access

</div>

</div>

</div>

The `NFSv4.1` uses utf8 based strings to represent user and group names. This is the case even for non-kerberos based accesses. Nevertheless UNIX based clients as well as <span class="productname">dCache</span> internally use numbers to represent uid and gids. A special service, called `idmapd`, takes care for principal-id mapping. On the client nodes the file `/etc/idmapd.conf` is usually responsible for consistent mapping on the client side. On the server side, in case of <span class="productname">dCache</span> mapping done through gplazma2\. The `identity` type of plug-in required by id-mapping service. Please refer to [Chapter 10, _Authorization in <span class="productname">dCache</span>_](#cf-gplazma "Chapter 10\. Authorization in dCache") for instructions about how to configure `gPlazma`.

Note, that `nfs4 domain` on clients must match `nfs.domain` value in `dcache.conf`.

To avoid big latencies and avoiding multiple queries for the same information, like ownership of a files in a big directory, the results from `gPlazma` are cached within ``NFSv4.1` door`. The default values for cache size and life time are good enough for typical installation. Nevertheless they can be overriden in `dcache.conf` or layoutfile:

<pre class="programlisting">..
# maximal number of entries in the cache
nfs.idmap.cache.size = 512

# cache entry maximal lifetime
nfs.idmap.cache.timeout = 30

# time unit used for timeout. Valid values are:
# SECONDS, MINUTES, HOURS and DAYS
nfs.idmap.cache.timeout.unit = SECONDS
..</pre>

</div>

</div>

<div class="chapter" title="Chapter 13\. dCache Storage Resource Manager">

<div class="titlepage">

<div>

<div>

## <a name="cf-srm"></a>Chapter 13\. <span class="productname">dCache</span> Storage Resource Manager

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Introduction](#cf-srm-intro)</span></dt>

<dt><span class="section">[Configuring the `srm` service](#cf-srm-srm)</span></dt>

<dd>

<dl>

<dt><span class="section">[The Basic Setup](#idp3868496)</span></dt>

<dt><span class="section">[Important `srm` configuration options](#idp3893328)</span></dt>

</dl>

</dd>

<dt><span class="section">[Utilization of Space Reservations for Data Storage](#idp3913392)</span></dt>

<dd>

<dl>

<dt><span class="section">[Properties of Space Reservation](#cf-srm-intro-spaceReservation)</span></dt>

</dl>

</dd>

<dt><span class="section">[<span class="productname">dCache</span> specific concepts](#idp3967952)</span></dt>

<dd>

<dl>

<dt><span class="section">[Activating `SRM` `SpaceManager`](#idp3969184)</span></dt>

<dt><span class="section">[Explicit and Implicit Space Reservations for Data Storage in <span class="productname">dCache</span>](#idp3978640)</span></dt>

</dl>

</dd>

<dt><span class="section">[`SpaceManager` configuration for Explicit Space Reservations](#cf-srm-space)</span></dt>

<dd>

<dl>

<dt><span class="section">[`SRM` `SpaceManager` and Link Groups](#cf-srm-space-linkgroups)</span></dt>

<dt><span class="section">[Making a Space Reservation](#idp4032304)</span></dt>

<dt><span class="section">[`SRM` configuration for experts](#cf-srm-expert-config)</span></dt>

</dl>

</dd>

<dt><span class="section">[Configuring the <span class="productname">PostgreSQL</span> Database](#cf-srm-psql)</span></dt>

<dd>

<dl>

<dt><span class="section">[`SRM` or srm monitoring on a separate node](#idp4425056)</span></dt>

</dl>

</dd>

<dt><span class="section">[General `SRM` Concepts (for developers)](#idp4433440)</span></dt>

<dd>

<dl>

<dt><span class="section">[The `SRM` service](#idp4435088)</span></dt>

<dt><span class="section">[Space Management Functions](#cf-srm-intro-spaceManagementFunct)</span></dt>

<dt><span class="section">[Data Transfer Functions](#cf-srm-intro-dataTransferFunct)</span></dt>

<dt><span class="section">[Request Status Functions](#cf-srm-intro-requestStatusFunct)</span></dt>

<dt><span class="section">[Directory Functions](#cf-srm-intro-directoryFunct)</span></dt>

<dt><span class="section">[Permission functions](#cf-srm-intro-permissionFunct)</span></dt>

</dl>

</dd>

</dl>

</div>

<div class="section" title="Introduction">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-srm-intro"></a>Introduction

</div>

</div>

</div>

_Storage Resource Managers_ (`SRM`s) are middleware components whose function is to provide dynamic space allocation and file management on shared storage components on the Grid. `SRM`s support protocol negotiation and a reliable replication mechanism. The [`SRM` specification](https://sdm.lbl.gov/srm-wg/doc/SRM.v2.2.html) standardizes the interface, thus allowing for a uniform access to heterogeneous storage elements.

The `SRM` utilizes the Grid Security Infrastructure (`GSI`) for authentication. The `SRM` is a Web Service implementing a published <acronym class="acronym">WSDL</acronym> document. Please visit the [`SRM` Working Group Page](http://sdm.lbl.gov/srm-wg/) to see the `SRM` Version 1.1 and `SRM` Version 2.2 protocol specification documents.

The `SRM` protocol uses `HTTP` over `GSI` as a transport. The <span class="productname">dCache</span> `SRM` implementation added `HTTPS` as a transport layer option. The main benefits of using `HTTPS` rather than `HTTP` over `GSI` is that `HTTPS` is a standard protocol and has support for sessions, improving latency in case a client needs to connect to the same server multiple times. The current implementation does not offer a delegation service. Hence `srmCopy` will not work with `SRM` over `HTTPS`. A separate delegation service will be added in a later release.

</div>

<div class="section" title="Configuring the srm service">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-srm-srm"></a>Configuring the `srm` service

</div>

</div>

</div>

<div class="section" title="The Basic Setup">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp3868496"></a>The Basic Setup

</div>

</div>

</div>

Like other services, the `srm` service can be enabled in the layout file `<span>/etc/dcache</span>/layouts/_<tt><mylayout></tt>_` of your <span class="productname">dCache</span> installation. For an overview of the layout file format, please see [the section called “Defining domains and services”](#in-install-layout "Defining domains and services").

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

To enable `SRM` in a separate _<tt><srm-${host.name}Domain></tt>_ in <span class="productname">dCache</span>, add the following lines to your layout file:

<pre class="programlisting">[_<tt><srm-${host.name}Domain></tt>_]
[_<tt><srm-${host.name}Domain></tt>_/srm]</pre>

</div>

</div>

The use of the `srm` service requires an authentication setup, see [Chapter 10, _Authorization in <span class="productname">dCache</span>_](#cf-gplazma "Chapter 10\. Authorization in dCache") for a general description or [the section called “Authentication and Authorization in <span class="productname">dCache</span>”](#intouch-certificates "Authentication and Authorization in dCache") for an example setup with `X.509` certificates.

You can now copy a file into your <span class="productname">dCache</span> using the `SRM`,

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Please make sure to use latest srmcp client otherwise you will need to specify `-2` in order to use the right version.

</div>

    [user] $

copy it back

    [user] $

and delete it

    [user] $

</div>

<div class="section" title="Important srm configuration options">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp3893328"></a>Important `srm` configuration options

</div>

</div>

</div>

The defaults for the following configuration parameters can be found in the `.properties` files in the directory `<span>/usr/share/dcache</span>/defaults`.

If you want to modify parameters, copy them to `<span>/etc/dcache</span>/dcache.conf` or to your layout file `<span>/etc/dcache</span>/layouts/_<tt><mylayout></tt>_` and update their value.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Change the value for `srm.db.host` in the layout file.

<pre class="programlisting">[_<tt><srm-${host.name}Domain></tt>_]
[_<tt><srm-${host.name}Domain></tt>_/srm]
srm.db.host=hostname</pre>

</div>

</div>

The property `srm.limits.request.copy.scheduler.thread.pool.size` controls number of copy requests in the running state. Copy requests are 3-rd party srm transfers and therefore the property `transfermanagers.limits.external-transfers` is best to be set to the same value as shown below.

<pre class="programlisting">srm.limits.request.copy.scheduler.thread.pool.size=250
transfermanagers.limits.external-transfers=${srm.limits.request.copy.scheduler.thread.pool.size}</pre>

The common value should be the roughly equal to the maximum number of the `SRM` - to -`SRM` copies your system can sustain.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

So if you think about 3 gridftp transfers per pool and you have 30 pools then the number should be 3x30=90.

<pre class="programlisting">srm.limits.request.copy.scheduler.thread.pool.size=90
transfermanagers.limits.external-transfers=90</pre>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

US-CMS T1 has:

<pre class="programlisting">srm.limits.request.copy.scheduler.thread.pool.size=2000
transfermanagers.limits.external-transfers=2000</pre>

</div>

</div>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

`SRM` might produce a lot of log entries, especially if it runs in debug mode. It is recommended to make sure that logs are redirected into a file on a large disk.

</div>

</div>

</div>

<div class="section" title="Utilization of Space Reservations for Data Storage">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="idp3913392"></a>Utilization of Space Reservations for Data Storage

</div>

</div>

</div>

`SRM` version 2.2 introduced a concept of space reservation. Space reservation guarantees that the requested amount of storage space of a specified type is made available by the storage system for a specified amount of time.

The <span class="productname">dCache</span> administrator can make space reservations for VOs (see [the section called “`SpaceManager` configuration for Explicit Space Reservations”](#cf-srm-space "SpaceManager configuration for Explicit Space Reservations"). Each space reservation has an associated ID (or space token). VOs then can copy directly into space tokens assigned to them by the dcache administrator.

When a file is about to be transferred to a storage system, the space available in the space reservation is checked if it can accomodate the entire file. If yes, this chunk of space is marked as allocated, so that it can not be taken by another, concurrently transferred file. If the file is transferred successfully the allocated space becomes used space within the space reservation, else the allocated space is released back to the space reservation.

`SRM` space reservation can be assigned a non-unique description which can be used to query the system for space reservations with a given description.

<span class="productname">dCache</span> only manages write space, i.e. space on disk can be reserved only for write operations. Once files are migrated to tape, and if no copy is required on disk, space used by these files is returned back into space reservation. When files are read back from tape and cached on disk, they are not counted as part of any space.

<div class="section" title="Properties of Space Reservation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-srm-intro-spaceReservation"></a>Properties of Space Reservation

</div>

</div>

</div>

The administrator can specify a _`RetentionPolicy`_ and an _`AccessLatency`_ for the space reservation.

`RetentionPolicy` describes the quality of the storage service that will be provided for the data (files) stored in this space reservation and `AccessLatency` describes the availability of this data. The specification requires that if a space reservation is given, then the specified `RetentionPolicy` or `AccessLatency` must match those of the space reservation.

The default values for the `RetentionPolicy` and `AccessLatency` can be changed in the file `<span>/etc/dcache</span>/dcache.conf`.

<div class="variablelist">

<dl>

<dt><span class="term">`RetentionPolicy`</span></dt>

<dd>

The values of `RetentionPolicy` used in <span class="productname">dCache</span> are `REPLICA` and `CUSTODIAL`.

<div class="itemizedlist">

*   `REPLICA` corresponds to the lowest quality of the service, usually associated with storing a single copy of each file on the disk.

*   `CUSTODIAL` is the highest quality service, usually interpreted as storage of the data on tape.

</div>

Once a file is written into a given space reservation, it inherits the reservation’s `RetentionPolicy`.

If the space reservation request does not specify a retention policy we will assign `pnfsmanager.default-retention-policy` a retention policy by default. The default value is `CUSTODIAL`.

Edit the file `<span>/etc/dcache</span>/dcache.conf` to change the default value.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Change the default value to `REPLICA`.

<pre class="programlisting">pnfsmanager.default-retention-policy=REPLICA</pre>

</div>

</div>

</dd>

<dt><span class="term">`AccessLatency`</span></dt>

<dd>

The two values allowed for `AccessLatency` are `NEARLINE` and `ONLINE`.

<div class="itemizedlist">

*   `NEARLINE` means that data stored in this reservation is allowed to migrate to permanent media. Retrieving these data may result in delays associated with preparatory steps that the storage system has to perform to make these data available for the user I/O (e.g., staging data from tape to a disk cache).

*   `ONLINE` means that data is readily available allowing for faster access.

</div>

In case of <span class="productname">dCache</span> `ONLINE` means that there will always be a copy of the file on disk, while `NEARLINE` does not provide such guarantee. As with `RetentionPolicy`, once a file is written into a given space reservation, it inherits the reservation’s `AccessLatency`.

If a space reservation request does not specify an access latency we will assign `spacemanager.default-access-latency` an access latency by default. The default value is `NEARLINE`.

Edit the file `<span>/etc/dcache</span>/dcache.conf` to change the default value.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Change the default value to `ONLINE`.

<pre class="programlisting">spacemanager.default-access-latency=ONLINE</pre>

</div>

</div>

</dd>

</dl>

</div>

<div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

### Important

Please make sure to use capital letters for `REPLICA`, `CUSTODIAL`, `ONLINE` and `NEARLINE` otherwise you will receive an error message.</div>

</div>

</div>

<div class="section" title="dCache specific concepts">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="idp3967952"></a><span class="productname">dCache</span> specific concepts

</div>

</div>

</div>

<div class="section" title="Activating SRM SpaceManager">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp3969184"></a>Activating `SRM` `SpaceManager`

</div>

</div>

</div>

In order to enable the `SRM` `SpaceManager` you need to add the `spacemanager` service to your layout file

<pre class="programlisting">[_<tt><srm-${host.name}Domain></tt>_]
[_<tt><srm-${host.name}Domain></tt>_/srm]
[_<tt><srm-${host.name}Domain></tt>_/spacemanager]</pre>

and add (uncomment) the following definition in the file `<span>/etc/dcache</span>/dcache.conf`

<pre class="programlisting">dcache.enable.space-reservation=true</pre>

</div>

<div class="section" title="Explicit and Implicit Space Reservations for Data Storage in dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp3978640"></a>Explicit and Implicit Space Reservations for Data Storage in <span class="productname">dCache</span>

</div>

</div>

</div>

<div class="section" title="Explicit Space Reservations">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp3979920"></a>Explicit Space Reservations

</div>

</div>

</div>

Each `SRM` space reservation is made against the total available disk space of a particular link group. If <span class="productname">dCache</span> is configured correctly each byte of disk space, that can be reserved, belongs to one and only one link group. See [the section called “`SpaceManager` configuration for Explicit Space Reservations”](#cf-srm-space "SpaceManager configuration for Explicit Space Reservations") for a detailed description.

<div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

### Important

Make sure that no pool belongs to more than one pool group, no pool group belongs to more than one link and no link belongs to more than one link group.

</div>

If a space reservation is specified, the file will be stored in it (assuming the user has permission to do so in the name space).

Files written into a space made within a particular link group will end up on one of the pools belonging to this link group. The difference between the link group’s available space and the sum of all the current space reservation sizes is the available space in the link group.

The total space in <span class="productname">dCache</span> that can be reserved is the sum of the available spaces of all link groups.

</div>

<div class="section" title="Implicit Space Reservations">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp3987056"></a>Implicit Space Reservations

</div>

</div>

</div>

<span class="productname">dCache</span> can perform implicit space reservations for non-`SRM` transfers, `SRM` Version 1 transfers and for `SRM` Version 2.2 data transfers that are not given the space token explicitly. The parameter that enables this behavior is `srm.enable.space-reservation.implicit`, which is described in [the section called “`SRM` configuration for experts”](#cf-srm-expert-config "SRM configuration for experts"). If no implicit space reservation can be made, the transfer will fail.

In case of `SRM` version 1.1 data transfers, when the access latency and retention policy cannot be specified, and in case of `SRM` V2.2 clients, when the access latency and retention policy are not specified, the default values will be used. First `SRM` will attempt to use the values of `AccessLatency` and `RetentionPolicy` tags from the directory to which a file is being written. If the tags are present, then the `AccessLatency` and `RetentionPolicy` will be set on basis of the system wide defaults, which are controlled by `pnfsmanager.default-retention-policy` and `spacemanager.default-access-latency` variables in `<span>/etc/dcache</span>/dcache.conf`.

You can check if the `AccessLatency` and `RetentionPolicy` tags are present by using the following commands:

    [root] #

If the output contains the lines `AccessLatency` and `RetentionPolicy` then the tags are already present and you can get the actual values of these tags by executing the following commands, which are shown together with example outputs:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [root] #

</div>

</div>

The valid `AccessLatency` values are `ONLINE` and `NEARLINE`, valid `RetentionPolicy` values are `REPLICA` and `CUSTODIAL`.

To create/change the values of the tags, please execute :

    [root] #

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Some clients also have default values, which are used when not explicitly specified by the user. I this case server side defaults will have no effect.

</div>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

If the implicit space reservation is not enabled the pools in the link groups will be excluded from consideration and only the remaining pools will be considered for storing the incoming data, and classical pool selection mechanism will be used.

</div>

</div>

</div>

</div>

<div class="section" title="SpaceManager configuration for Explicit Space Reservations">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-srm-space"></a>`SpaceManager` configuration for Explicit Space Reservations

</div>

</div>

</div>

<div class="section" title="SRM SpaceManager and Link Groups">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-srm-space-linkgroups"></a>`SRM` `SpaceManager` and Link Groups

</div>

</div>

</div>

`SpaceManager` is making reservations against free space available in [link groups](#cf-pm-linkgroups "Link Groups"). The total free space in the given link group is the sum of available spaces in all links. The available space in each link is the sum of all sizes of available space in all pools assinged to a given link. Therefore for the space reservation to work correctly it is essential that each pool belongs to one and only one link, and each link belongs to only one link group. Link groups are assigned several parameters that determine what kind of space the link group corresponds to and who can make reservations against this space.

</div>

<div class="section" title="Making a Space Reservation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp4032304"></a>Making a Space Reservation

</div>

</div>

</div>

Now that the `SRM` `SpaceManager` is activated you can make a space reservation. As mentioned above you need link groups to make a space reservation.

<div class="section" title="Prerequisites for Space Reservations">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-srm-spaceres-prereq"></a>Prerequisites for Space Reservations

</div>

</div>

</div>

Login to the [admin interface](#intouch-admin "The Admin Interface") and <span class="command">**cd**</span> to the cell `SrmSpaceManager`.

    [user] $

Type <span class="command">**ls**</span> to get information about reservations and link groups.

    (SrmSpaceManager) admin >

This output tells you that there are no reservations yet and no link groups. As there are no link groups no space can be reserved.

<div class="section" title="The Link Groups">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-srm-linkgroups"></a>The Link Groups

</div>

</div>

</div>

For a general introduction about link groups see [the section called “Link Groups”](#cf-pm-linkgroups "Link Groups").

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

In this example we will create a link group for the VO `desy`. In order to do so we need to have a pool, a pool group and a link. Moreover, we define unit groups named `any-store`, `world-net` and `any-protocol`. (See [the section called “Types of Units”](#cf-pm-links-units "Types of Units").)

Define a pool in your layout file, add it to your pool directory and restart the `poolDomain`.

<pre class="programlisting">[poolDomain]
[poolDomain/pool]
path=/srv/dcache/spacemanager-pool
name=spacemanager-pool</pre>

    [root] #

In the Admin Interface <span class="command">**cd**</span> to the `PoolManager` and create a pool group, a link and a link group.

    (SrmSpaceManager) admin >

Check whether the link group is available.

    (local) admin >

The link group `spacemanager_WriteLinkGroup` was created and has the id `0`.

</div>

</div>

</div>

<div class="section" title="The SpaceManagerLinkGroupAuthorizationFile">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-srm-linkgroupauthfile"></a>The `SpaceManagerLinkGroupAuthorizationFile`

</div>

</div>

</div>

Now you need to edit the `LinkGroupAuthorization.conf` file. This file contains a list of the link groups and all the VOs and the VO Roles that are permitted to make reservations in a given link group.

Specify the location of the `LinkGroupAuthorization.conf` file in the `<span>/etc/dcache</span>/dcache.conf` file.

<pre class="programlisting">spacemanager.authz.link-group-file-name=/path/to/LinkGroupAuthorization.conf</pre>

The file `LinkGroupAuthorization.conf` has following syntax:

LinkGroup _<tt><NameOfLinkGroup></tt>_ followed by the list of the Fully Qualified Attribute Names (FQANs). Each FQAN on a separate line, followed by an empty line, which is used as a record separator, or by the end of the file.

FQAN is usually a string of the form _<tt><VO></tt>_/Role=_<tt><VORole></tt>_. Both _<tt><VO></tt>_ and _<tt><VORole></tt>_ could be set to `*`, in this case all VOs or VO Roles will be allowed to make reservations in this link group. Any line that starts with # is a comment and may appear anywhere.

<pre class="programlisting">#SpaceManagerLinkGroupAuthorizationFile

LinkGroup _<tt><NameOfLinkGroup></tt>_
/_<tt><VO></tt>_/Role=_<tt><VORole></tt>_</pre>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

You do not need to restart the `srm` or <span class="productname">dCache</span> after changing the `LinkGroupAuthorization.conf` file. The changes will be applied automatically after a few minutes.

Use <span class="command">**update link groups**</span> to be sure that the `LinkGroupAuthorization.conf` file and the link groups have been updated.

    (SrmSpaceManager) admin >

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

In the example above you created the link group `spacemanager_WriteLinkGroup`. Now you want to allow members of the VO `desy` with the role `production` to make a space reservation in this link group.

<pre class="programlisting">#SpaceManagerLinkGroupAuthorizationFile
# this is comment and is ignored

LinkGroup spacemanager_WriteLinkGroup
#
/desy/Role=production</pre>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

In this more general example for a `SpaceManagerLinkGroupAuthorizationFile` members of the VO `desy` with role `test` get the right to make a space reservation in a link group called `desy-test-LinkGroup`. Moreover, all members of the VO `desy` get the right to make a reservation in the link group called `desy-anyone-LinkGroup` and anyone will get the right to make a space reservation in the link group called `default-LinkGroup`.

<pre class="programlisting">#SpaceManagerLinkGroupAuthorizationFile
# this is comment and is ignored

LinkGroup desy-test-LinkGroup
/desy/Role=/test

LinkGroup desy-anyone-LinkGroup
/desy/Role=*

LinkGroup default-LinkGroup
# allow anyone :-)
*/Role=*</pre>

</div>

</div>

</div>

</div>

<div class="section" title="Making and Releasing a Space Reservation as dCache Administrator">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-srm-reservation"></a>Making and Releasing a Space Reservation as <span class="productname">dCache</span> Administrator

</div>

</div>

</div>

<div class="section" title="Making a Space Reservation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-srm-make-res"></a>Making a Space Reservation

</div>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Now you can make a space reservation for the VO `desy`.

    (SrmSpaceManager) admin >

The id of the space token is `110000`.

Check the status of the reservation by

    (SrmSpaceManager) admin >

You can now copy a file into that space token.

    [user] $

Now you can check via the [Webadmin Interface](#cf-webadmin "Chapter 17\. dCache Webadmin Interface") or the [Web Interface](#intouch-web "The Web Interface for Monitoring dCache") that the file has been copied to the pool `spacemanager-pool`.

</div>

</div>

There are several parameters to be specified for a space reservation.

    (SrmSpaceManager) admin >

<div class="variablelist">

<dl>

<dt><span class="term">[-vog=voGroup]</span></dt>

<dd>

`voGroup` should match the VO you specified in the `LinkGroupAuthorization.conf` file. If you do not want to make a space reservation for a certain VO then the entry in the `LinkGroupAuthorization.conf` should read

<pre class="programlisting">LinkGroup NameOfLinkGroup
*/Role=*</pre>

</dd>

<dt><span class="term">[-vor=voRole]</span></dt>

<dd>

`voRole` can be specified if it is used in the `LinkGroupAuthorization.conf` file.

</dd>

<dt><span class="term">[-acclat=AccessLatency]</span></dt>

<dd>

`AccessLatency` needs to match one of the access latencies allowed for the link group.

</dd>

<dt><span class="term">[-retpol=RetentionPolicy]</span></dt>

<dd>

`RetentionPolicy` needs to match one of the retention policies allowed for the link group.

</dd>

<dt><span class="term">[-desc=Description]</span></dt>

<dd>

You can chose a value to describe your space reservation.

</dd>

<dt><span class="term">[-lgid=LinkGroupId]</span></dt>

<dd>

You can either use the `LinkGroupId` to make a space reservation or

</dd>

<dt><span class="term">[-lg=LinkGroupName]</span></dt>

<dd>

you use the `LinkGroupName` to make a space reservation.

</dd>

<dt><span class="term">_<tt><sizeInBytes></tt>_</span></dt>

<dd>

The size of the space reservation should be specified in bytes.

</dd>

<dt><span class="term">_<tt><lifetimeInSecs></tt>_</span></dt>

<dd>

The life time of the space reservation should be specified in seconds. Choose `"-1"` for a space reservation that will never expire (use quotes around the negative `one`).

</dd>

</dl>

</div>

</div>

<div class="section" title="Releasing a Space Reservation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-srm-release-spaceres"></a>Releasing a Space Reservation

</div>

</div>

</div>

If a space reservation is not needet anymore it can be released with

    (SrmSpaceManager) admin >

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    (SrmSpaceManager) admin >

You can see that the value for `state` has changed from `RESERVED` to `RELEASED`

</div>

</div>

</div>

</div>

<div class="section" title="Making and Releasing a Space Reservation as a User">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cf-srm-spaceres-VO"></a>Making and Releasing a Space Reservation as a User

</div>

</div>

</div>

A user who has been given the right to make a space reservation can make a space reservation. To achieve this the right entry in the `LinkGroupAuthorization.conf` file is required.

<div class="section" title="VO based Authorization Prerequisites">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="idp4176576"></a>VO based Authorization Prerequisites

</div>

</div>

</div>

In order to be able to take advantage of the virtual organization (VO) infrastructure and VO based authorization and VO based access control to the space in <span class="productname">dCache</span>, certain things need to be in place:

<div class="itemizedlist">

*   User needs to be registered with the VO.

*   User needs to use [<span class="command">**voms-proxy-init**</span>](#cf-gplazma-certificates-voms-proxy-init "Creating a VOMS proxy") to create a VO proxy.

*   <span class="productname">dCache</span> needs to use `gPlazma` with modules that extract VO attributes from the user’s proxy. (See [Chapter 10, _Authorization in <span class="productname">dCache</span>_](#cf-gplazma "Chapter 10\. Authorization in dCache"), have a look at `gplazmalite-vorole-mapping` plugin and see [the section called “Authentication and Authorization in <span class="productname">dCache</span>”](#intouch-certificates "Authentication and Authorization in dCache") for an example with `gplazmalite-vorole-mapping`.

</div>

Only if these 3 conditions are satisfied the VO based authorization of the `SpaceManager` will work.

</div>

<div class="section" title="VO based Access Control Configuration">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="idp4187968"></a>VO based Access Control Configuration

</div>

</div>

</div>

As mentioned [above](#cf-srm-space-linkgroups "SRM SpaceManager and Link Groups") <span class="productname">dCache</span> space reservation functionality access control is currently performed at the level of the link groups. Access to making reservations in each link group is controlled by the [`SpaceManagerLinkGroupAuthorizationFile`](#cf-srm-linkgroupauthfile "The SpaceManagerLinkGroupAuthorizationFile").

This file contains a list of the link groups and all the VOs and the VO Roles that are permitted to make reservations in a given link group.

When a `SRM` Space Reservation request is executed, its parameters, such as reservation size, lifetime, `AccessLatency`and `RetentionPolicy` as well as user’s VO membership information is forwarded to the `SRM` `SpaceManager`.

Once a space reservation is created, no access control is performed, any user can store the files in this space reservation, provided he or she knows the exact space token.

</div>

<div class="section" title="Making and Releasing a Space Reservation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-srm-spaceres-client"></a>Making and Releasing a Space Reservation

</div>

</div>

</div>

A user who is given the rights in the `SpaceManagerLinkGroupAuthorizationFile` can make a space reservation by

    [user] $

and release it by

    [user] $

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Please note that it is obligatory to specify the retention policy while it is optional to specify the access latency.

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

The space reservation can be released by:

    [user] $

</div>

</div>

</div>

<div class="section" title="Space Reservation without VOMS certificate">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="idp4212400"></a>Space Reservation without VOMS certificate

</div>

</div>

</div>

If a client uses a regular grid proxy, created with <span class="command">**grid-proxy-init**</span>, and not a VO proxy, which is created with the <span class="command">**voms-proxy-init**</span>, when it is communicating with `SRM` server in <span class="productname">dCache</span>, then the VO attributes can not be extracted from its credential. In this case the name of the user is extracted from the Distinguished Name (DN) to use name mapping. For the purposes of the space reservation the name of the user as mapped by `gplazma` is used as its VO Group name, and the VO Role is left empty. The entry in the `SpaceManagerLinkGroupAuthorizationFile` should be:

<pre class="programlisting">#LinkGroupAuthorizationFile
#
_<tt><userName></tt>_</pre>

</div>

<div class="section" title="Space Reservation for non SRM Transfers">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="idp4219600"></a>Space Reservation for non `SRM` Transfers

</div>

</div>

</div>

Edit the file `<span>/etc/dcache</span>/dcache.conf` to enable space reservation for non `SRM` transfers.

<pre class="programlisting">spacemanager.enable.reserve-space-for-non-srm-tranfers=true</pre>

If the `spacemanager` is enabled, `spacemanager.enable.reserve-space-for-non-srm-tranfers` is set to `true`, and if the transfer request comes from a door, and there was no prior space reservation made for this file, the `SpaceManager` will try to reserve space before satisfying the request.

Possible values are `true` or `false` and the default value is `false`.

</div>

</div>

</div>

<div class="section" title="SRM configuration for experts">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-srm-expert-config"></a>`SRM` configuration for experts

</div>

</div>

</div>

There are a few parameters in `<span>/usr/share/dcache</span>/defaults/*.properties` that you might find useful for nontrivial `SRM` deployment.

<div class="section" title="dcache.enable.space-reservation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4235216"></a>dcache.enable.space-reservation

</div>

</div>

</div>

`dcache.enable.space-reservation` tells if the space management is activated in `SRM`.

Possible values are `true` and `false`. Default is `true`.

Usage example:

<pre class="programlisting">dcache.enable.space-reservation=true</pre>

</div>

<div class="section" title="srm.enable.space-reservation.implicit">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4241296"></a>srm.enable.space-reservation.implicit

</div>

</div>

</div>

`srm.enable.space-reservation.implicit` tells if the space should be reserved for `SRM` Version 1 transfers and for `SRM` Version 2 transfers that have no space token specified.

Possible values are `true` and `false`. This is enabled by default. It has no effect if `dcache.enable.space-reservation` is set to `true`.

Usage example:

<pre class="programlisting">srm.enable.space-reservation.implicit=true</pre>

</div>

<div class="section" title="dcache.enable.overwrite">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4249184"></a>dcache.enable.overwrite

</div>

</div>

</div>

`dcache.enable.overwrite` tells `SRM` and `GridFTP` servers if the overwrite is allowed. If enabled on the `SRM` node, should be enabled on all `GridFTP` nodes.

Possible values are `true` and `false`. Default is `false`.

Usage example:

<pre class="programlisting">dcache.enable.overwrite=true</pre>

</div>

<div class="section" title="srm.enable.overwrite-by-default">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4258480"></a>srm.enable.overwrite-by-default

</div>

</div>

</div>

`srm.enable.overwrite-by-default` Set this to `true` if you want overwrite to be enabled for `SRM` v1.1 interface as well as for `SRM` v2.2 interface when client does not specify desired overwrite mode. This option will be considered only if `dcache.enable.overwrite` is set to `true`.

Possible values are `true` and `false`. Default is `false`.

Usage example:

<pre class="programlisting">srm.enable.overwrite-by-default=false </pre>

</div>

<div class="section" title="srm.db.host">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4267792"></a>srm.db.host

</div>

</div>

</div>

`srm.db.host` tells `SRM` which database host to connect to.

Default value is `localhost`.

Usage example:

<pre class="programlisting">srm.db.host=database-host.example.org</pre>

</div>

<div class="section" title="spaceManagerDatabaseHost">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4272400"></a>spaceManagerDatabaseHost

</div>

</div>

</div>

`spaceManagerDatabaseHost` tells `SpaceManager` which database host to connect to.

Default value is `localhost`.

Usage example:

<pre class="programlisting">spaceManagerDatabaseHost=database-host.example.org</pre>

</div>

<div class="section" title="pinmanager.db.host">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4277088"></a>pinmanager.db.host

</div>

</div>

</div>

`pinmanager.db.host` tells `PinManager` which database host to connect to.

Default value is `localhost`.

Usage example:

<pre class="programlisting">pinmanager.db.host=database-host.example.org</pre>

</div>

<div class="section" title="srm.db.name">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4281744"></a>srm.db.name

</div>

</div>

</div>

`srm.db.name` tells `SRM` which database to connect to.

Default value is `dcache`.

Usage example:

<pre class="programlisting">srm.db.name=dcache</pre>

</div>

<div class="section" title="srm.db.user">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4286320"></a>srm.db.user

</div>

</div>

</div>

`srm.db.user` tells `SRM` which database user name to use when connecting to database. Do not change unless you know what you are doing.

Default value is `srmdcache`.

Usage example:

<pre class="programlisting">srm.db.user=srmdcache</pre>

</div>

<div class="section" title="srm.db.password">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4290992"></a>srm.db.password

</div>

</div>

</div>

`srm.db.password` tells `SRM` which database password to use when connecting to database. The default value is `srmdcache`.

Usage example:

<pre class="programlisting">srm.db.password=NotVerySecret</pre>

</div>

<div class="section" title="srm.db.password.file">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4295216"></a>srm.db.password.file

</div>

</div>

</div>

`srm.db.password.file` tells `SRM` which database password file to use when connecting to database. Do not change unless you know what you are doing. It is recommended that MD5 authentication method is used. To learn about file format please see [http://www.postgresql.org/docs/8.1/static/libpq-pgpass.html](http://www.postgresql.org/docs/8.1/static/libpq-pgpass.html). To learn more about authentication methods please visit [http://www.postgresql.org/docs/8.1/static/encryption-options.html](http://www.postgresql.org/docs/8.1/static/encryption-options.html), Please read "Encrypting Passwords Across A Network" section.

This option is not set by default.

Usage example:

<pre class="programlisting">srm.db.password.file=/root/.pgpass</pre>

</div>

<div class="section" title="srm.request.enable.history-database">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4300912"></a>srm.request.enable.history-database

</div>

</div>

</div>

`srm.request.enable.history-database` enables logging of the transition history of the `SRM` request in the database. The request transitions can be examined through the command line interface. Activation of this option might lead to the increase of the database activity, so if the <span class="productname">PostgreSQL</span> load generated by `SRM` is excessive, disable it.

Possible values are `true` and `false`. Default is `false`.

Usage example:

<pre class="programlisting">srm.request.enable.history-database=true</pre>

</div>

<div class="section" title="transfermanagers.enable.log-to-database">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4308880"></a>transfermanagers.enable.log-to-database

</div>

</div>

</div>

`transfermanagers.enable.log-to-database` tells `SRM` to store the information about the remote (copy, srmCopy) transfer details in the database. Activation of this option might lead to the increase of the database activity, so if the <span class="productname">PostgreSQL</span> load generated by `SRM` is excessive, disable it.

Possible values are `true` and `false`. Default is `false`.

Usage example:

<pre class="programlisting">transfermanagers.enable.log-to-database=false</pre>

</div>

<div class="section" title="srmVersion">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4316544"></a>srmVersion

</div>

</div>

</div>

`srmVersion` is not used by `SRM`; it was mentioned that this value is used by some publishing scripts.

Default is `version1`.

</div>

<div class="section" title="srm.root">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4320064"></a>srm.root

</div>

</div>

</div>

`srm.root` tells `SRM` what the root of all `SRM` paths is in pnfs. `SRM` will prepend path to all the local <acronym class="acronym">SURL</acronym> paths passed to it by `SRM` client. So if the `srm.root` is set to `/pnfs/fnal.gov/THISISTHEPNFSSRMPATH` and someone requests the read of `srm://srm.example.org:8443/file1`, `SRM` will translate the <acronym class="acronym">SURL</acronym> path `/file1` into `/pnfs/fnal.gov/THISISTHEPNFSSRMPATH/file1`. Setting this variable to something different from `/` is equivalent of performing Unix <span class="command">**chroot**</span> for all `SRM` operations.

Default value is `/`.

Usage example:

<pre class="programlisting">srm.root="/pnfs/fnal.gov/data/experiment"</pre>

</div>

<div class="section" title="srm.limits.parallel-streams">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4334624"></a>srm.limits.parallel-streams

</div>

</div>

</div>

`srm.limits.parallel-streams` specifies the number of the parallel streams that `SRM` will use when performing third party transfers between this system and remote `GSI-FTP` servers, in response to `SRM` v1.1 copy or `SRM` V2.2 srmCopy function. This will have no effect on srmPrepareToPut and srmPrepareToGet command results and parameters of `GridFTP` transfers driven by the `SRM` clients.

Default value is `10`.

Usage example:

<pre class="programlisting">srm.limits.parallel-streams=20</pre>

</div>

<div class="section" title="srm.limits.transfer-buffer.size">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4344304"></a>srm.limits.transfer-buffer.size

</div>

</div>

</div>

`srm.limits.transfer-buffer.size` specifies the number of bytes to use for the in memory buffers for performing third party transfers between this system and remote `GSI-FTP` servers, in response to `SRM` v1.1 copy or `SRM` V2.2 srmCopy function. This will have no effect on srmPrepareToPut and srmPrepareToGet command results and parameters of `GridFTP` transfers driven by the `SRM` clients.

Default value is `1048576`.

Usage example:

<pre class="programlisting">srm.limits.transfer-buffer.size=1048576</pre>

</div>

<div class="section" title="srm.limits.transfer-tcp-buffer.size">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4353344"></a>srm.limits.transfer-tcp-buffer.size

</div>

</div>

</div>

`srm.limits.transfer-tcp-buffer.size` specifies the number of bytes to use for the tcp buffers for performing third party transfers between this system and remote `GSI-FTP` servers, in response to `SRM` v1.1 copy or `SRM` V2.2 srmCopy function. This will have no effect on srmPrepareToPut and srmPrepareToGet command results and parameters of `GridFTP` transfers driven by the `SRM` clients.

Default value is `1048576`.

Usage example:

<pre class="programlisting">srm.limits.transfer-tcp-buffer.size=1048576</pre>

</div>

<div class="section" title="srm.service.gplazma.cache.timeout">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4362400"></a>srm.service.gplazma.cache.timeout

</div>

</div>

</div>

`srm.service.gplazma.cache.timeout` specifies the duration that authorizations will be cached. Caching decreases the volume of messages to the `gPlazma` cell or other authorization mechanism. To turn off caching, set the value to `0`.

Default value is `120`.

Usage example:

<pre class="programlisting">srm.service.gplazma.cache.timeout=60</pre>

</div>

<div class="section" title="srm.limits.request.bring-online.lifetime, srm.limits.request.put.lifetime and srm.limits.request.copy.lifetime">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4367856"></a>srm.limits.request.bring-online.lifetime, srm.limits.request.put.lifetime and srm.limits.request.copy.lifetime

</div>

</div>

</div>

`srm.limits.request.bring-online.lifetime`, `srm.limits.request.put.lifetime` and `srm.limits.request.copy.lifetime` specify the lifetimes of the srmPrepareToGet (srmBringOnline) srmPrepareToPut and srmCopy requests lifetimes in millisecond. If the system is unable to fulfill the requests before the request lifetimes expire, the requests are automatically garbage collected.

Default value is `14400000` (4 hours)

Usage example:

<pre class="programlisting">srm.limits.request.bring-online.lifetime=14400000
srm.limits.request.put.lifetime=14400000
srm.limits.request.copy.lifetime=14400000</pre>

</div>

<div class="section" title="srm.limits.request.scheduler.ready.max, srm.limits.request.put.scheduler.ready.max, srm.limits.request.scheduler.ready-queue.size and srm.limits.request.put.scheduler.ready-queue.size">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4373120"></a>srm.limits.request.scheduler.ready.max, srm.limits.request.put.scheduler.ready.max, srm.limits.request.scheduler.ready-queue.size and srm.limits.request.put.scheduler.ready-queue.size

</div>

</div>

</div>

`srm.limits.request.scheduler.ready.max` and `srm.limits.request.put.scheduler.ready.max` specify the maximum number of the files for which the transfer <acronym class="acronym">URL</acronym>s will be computed and given to the users in response to `SRM` get (srmPrepareToGet) and put (srmPrepareToPut) requests. The rest of the files that are ready to be transfered are put on the `Ready` queues, the maximum length of these queues are controlled by `srm.limits.request.scheduler.ready-queue.size` and `srm.limits.request.put.scheduler.ready-queue.size` parameters. These parameters should be set according to the capacity of the system, and are usually greater than the maximum number of the `GridFTP` transfers that this <span class="productname">dCache</span> instance `GridFTP` doors can sustain.

Usage example:

<pre class="programlisting">srm.limits.request.scheduler.ready-queue.size=10000
srm.limits.request.scheduler.ready.max=2000
srm.limits.request.put.scheduler.ready-queue.size=10000
srm.limits.request.put.scheduler.ready.max=1000</pre>

</div>

<div class="section" title="srm.limits.request.copy.scheduler.thread.pool.size and transfermanagers.limits.external-transfers">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4382864"></a>srm.limits.request.copy.scheduler.thread.pool.size and transfermanagers.limits.external-transfers

</div>

</div>

</div>

`srm.limits.request.copy.scheduler.thread.pool.size` and `transfermanagers.limits.external-transfers`. `srm.limits.request.copy.scheduler.thread.pool.size` is used to specify how many parallel srmCopy file copies to execute simultaneously. Once the `SRM` contacted the remote `SRM` system, and obtained a Transfer <acronym class="acronym">URL</acronym> (usually `GSI-FTP` <acronym class="acronym">URL</acronym>), it contacts a Copy Manager module (usually `RemoteGSIFTPTransferManager`), and asks it to perform a `GridFTP` transfer between the remote `GridFTP` server and a <span class="productname">dCache</span> pool. The maximum number of simultaneous transfers that `RemoteGSIFTPTransferManager` will support is `transfermanagers.limits.external-transfers`, therefore it is important that `transfermanagers.limits.external-transfers` is greater than or equal to `srm.limits.request.copy.scheduler.thread.pool.size`.

Usage example:

<pre class="programlisting">srm.limits.request.copy.scheduler.thread.pool.size=250
transfermanagers.limits.external-transfers=260</pre>

</div>

<div class="section" title="srm.enable.custom-get-host-by-address">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4396016"></a>srm.enable.custom-get-host-by-address

</div>

</div>

</div>

`srm.enable.custom-get-host-by-address` `srm.enable.custom-get-host-by-address` enables using the BNL developed procedure for host by IP resolution if standard InetAddress method failed.

Usage example:

<pre class="programlisting">srm.enable.custom-get-host-by-address=true</pre>

</div>

<div class="section" title="srm.enable.recursive-directory-creation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4399344"></a>srm.enable.recursive-directory-creation

</div>

</div>

</div>

`srm.enable.recursive-directory-creation` allows or disallows automatic creation of directories via `SRM`. Set this to `true` or `false`.

Automatic directory creation is allowed by default.

Usage example:

<pre class="programlisting">srm.enable.recursive-directory-creation=true</pre>

</div>

<div class="section" title="hostCertificateRefreshPeriod">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4405056"></a>hostCertificateRefreshPeriod

</div>

</div>

</div>

This option allows you to control how often the `SRM` door will reload the server’s host certificate from the filesystem. For the specified period, the host certificate will be kept in memory. This speeds up the rate at which the door can handle requests, but also causes it to be unaware of changes to the host certificate (for instance in the case of renewal).

By changing this parameter you can control how long the host certificate is cached by the door and consequently how fast the door will be able to detect and reload a renewed host certificate.

Please note that the value of this parameter has to be specified in seconds.

Usage example:

<pre class="programlisting">hostCertificateRefreshPeriod=86400</pre>

</div>

<div class="section" title="trustAnchorRefreshPeriod">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4409840"></a>trustAnchorRefreshPeriod

</div>

</div>

</div>

The `trustAnchorRefreshPeriod` option is similar to `hostCertificateRefreshPeriod`. It applies to the set of CA certificates trusted by the `SRM` door for signing end-entity certificates (along with some metadata, these form so called _trust anchors_). The trust anchors are needed to make a decision about the trustworthiness of a certificate in <abbr class="abbrev">X.509</abbr> client authentication. The `GSI` security protocol used by `SRM` builds upon <abbr class="abbrev">X.509</abbr> client authentication.

By changing this parameter you can control how long the set of trust anchors remains cached by the door. Conversely, it also influences how often the door reloads the set of trusted certificates.

Please note that the value of this parameter has to be specified in seconds.

<div class="tip" title="Tip" style="margin-left: 0.5in; margin-right: 0.5in;">

### Tip

Trust-anchors usually change more often than the host certificate. Thus, it might be sensible to set the refresh period of the trust anchors lower than the refresh period of the host certificate.

</div>

Usage example:

<pre class="programlisting">trustAnchorRefreshPeriod=3600</pre>

</div>

</div>

</div>

<div class="section" title="Configuring the PostgreSQL Database">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-srm-psql"></a>Configuring the <span class="productname">PostgreSQL</span> Database

</div>

</div>

</div>

We highly recommend to make sure that <span class="productname">PostgreSQL</span> database files are stored on a separate disk that is not used for anything else (not even <span class="productname">PostgreSQL</span> logging). BNL Atlas Tier 1 observed a great improvement in srm-database communication performance after they deployed <span class="productname">PostgreSQL</span> on a separate dedicated machine.

<div class="section" title="SRM or srm monitoring on a separate node">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp4425056"></a>`SRM` or srm monitoring on a separate node

</div>

</div>

</div>

If `SRM` or srm monitoring is going to be installed on a separate node, you need to add an entry in the file `/var/lib/pgsql/data/pg_hba.conf` for this node as well:

<pre class="programlisting">host    all         all       _<tt><monitoring node></tt>_    trust
host    all         all       _<tt><srm node></tt>_    trust</pre>

The file `postgresql.conf` should contain the following:

<pre class="programlisting">#to enable network connection on the default port
max_connections = 100
port = 5432
...
shared_buffers = 114688
...
work_mem = 10240
...
#to enable autovacuuming
stats_row_level = on
autovacuum = on
autovacuum_vacuum_threshold = 500  # min # of tuple updates before
                                   # vacuum
autovacuum_analyze_threshold = 250      # min # of tuple updates before
                                        # analyze
autovacuum_vacuum_scale_factor = 0.2    # fraction of rel size before
                                        # vacuum
autovacuum_analyze_scale_factor = 0.1   # fraction of rel size before
#
# setting vacuum_cost_delay might be useful to avoid
# autovacuum penalize general performance
# it is not set in US-CMS T1 at Fermilab
#
# In IN2P3 add_missing_from = on
# In Fermilab it is commented out

# - Free Space Map -
max_fsm_pages = 500000

# - Planner Cost Constants -
effective_cache_size = 16384            # typically 8KB each</pre>

</div>

</div>

<div class="section" title="General SRM Concepts (for developers)">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="idp4433440"></a>General `SRM` Concepts (for developers)

</div>

</div>

</div>

<div class="section" title="The SRM service">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp4435088"></a>The `SRM` service

</div>

</div>

</div>

<span class="productname">dCache</span> `SRM` is implemented as a Web Service running in a <span class="productname">Jetty</span> servlet container and an <span class="productname">Axis</span> Web Services engine. The <span class="productname">Jetty</span> server is executed as a cell, embedded in <span class="productname">dCache</span> and started automatically by the `SRM` service. Other cells started automatically by `SRM` are `SpaceManager`, `PinManager` and `RemoteGSIFTPTransferManager`. Of these services only `SRM` and `SpaceManager` require special configuration.

</div>

The `SRM` consists of the five categories of functions:

<div class="itemizedlist">

*   [Space Management Functions](#cf-srm-intro-spaceManagementFunct "Space Management Functions")
*   [Data Transfer Functions](#cf-srm-intro-dataTransferFunct "Data Transfer Functions")
*   [Request Status Functions](#cf-srm-intro-requestStatusFunct "Request Status Functions")
*   [Directory Functions](#cf-srm-intro-directoryFunct "Directory Functions")
*   [Permission Functions](#cf-srm-intro-permissionFunct "Permission functions")

</div>

<div class="section" title="Space Management Functions">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-srm-intro-spaceManagementFunct"></a>Space Management Functions

</div>

</div>

</div>

`SRM` version 2.2 introduces a concept of space reservation. Space reservation guarantees that the requested amount of storage space of a specified type is made available by the storage system for a specified amount of time.

We use three functions for space management:

<div class="itemizedlist">

*   `srmReserveSpace`
*   `SrmGetSpaceMetadata`
*   `srmReleaseSpace`

</div>

Space reservation is made using the `srmReserveSpace` function. In case of successful reservation, a unique name, called _space token_ is assigned to the reservation. A space token can be used during the transfer operations to tell the system to put the files being manipulated or transferred into an associated space reservation. A storage system ensures that the reserved amount of the disk space is indeed available, thus providing a guarantee that a client does not run out of space until all space promised by the reservation has been used. When files are deleted, the space is returned to the space reservation.

<span class="productname">dCache</span> only manages write space, i.e. space on disk can be reserved only for write operations. Once files are migrated to tape, and if no copy is required on disk, space used by these files is returned back into space reservation. When files are read back from tape and cached on disk, they are not counted as part of any space. `SRM` space reservation can be assigned a non-unique description that can be used to query the system for space reservations with a given description.

[Properties of the `SRM` space reservations](#cf-srm-intro-spaceReservation "Properties of Space Reservation") can be discovered using the `SrmGetSpaceMetadata` function.

Space Reservations might be released with the function `srmReleaseSpace`.

For a complete description of the available space management functions please see the [`SRM` Version 2.2 Specification](http://sdm.lbl.gov/srm-wg/doc/SRM.v2.2.html#_Toc241633085).

</div>

<div class="section" title="Data Transfer Functions">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-srm-intro-dataTransferFunct"></a>Data Transfer Functions

</div>

</div>

</div>

<div class="section" title="SURLs and TURLs">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4472032"></a><acronym class="acronym">SURL</acronym>s and <acronym class="acronym">TURL</acronym>s

</div>

</div>

</div>

`SRM` defines a protocol named `SRM`, and introduces a way to address the files stored in the `SRM` managed storage by site <acronym class="acronym">URL</acronym> (_<acronym class="acronym">SURL</acronym>_ of the format `srm://<host>:<port>/[<web service path>?SFN=]<path>`.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Examples of the <acronym class="acronym">SURL</acronym>s a.k.a. `SRM` <acronym class="acronym">URL</acronym>s are:

<pre class="screen">srm://fapl110.fnal.gov:8443/srm/managerv2?SFN=//pnfs/fnal.gov/data/test/file1
srm://fapl110.fnal.gov:8443/srm/managerv1?SFN=/pnfs/fnal.gov/data/test/file2
srm://srm.cern.ch:8443/castor/cern.ch/cms/store/cmsfile23</pre>

</div>

</div>

A transfer <acronym class="acronym">URL</acronym> (_<acronym class="acronym">TURL</acronym>_) encodes the file transport protocol in the <acronym class="acronym">URL</acronym>.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="screen">gsiftp://gridftpdoor.fnal.gov:2811/data/test/file1</pre>

</div>

</div>

</div>

`SRM` version 2.2 provides three functions for performing data transfers:

<div class="itemizedlist">

*   `srmPrepareToGet`
*   `srmPrepareToPut`
*   `srmCopy`

</div>

(in `SRM` version 1.1 these functions were called `get`, `put` and `copy`).

All three functions accept lists of <acronym class="acronym">SURL</acronym>s as parameters. All data transfer functions perform file/directory access verification and `srmPrepareToPut` and `srmCopy` check if the receiving storage element has sufficient space to store the files.

`srmPrepareToGet` prepares files for read. These files are specified as a list of source <acronym class="acronym">SURL</acronym>s, which are stored in an `SRM` managed storage element. `srmPrepareToGet` is used to bring source files online and assigns transfer <acronym class="acronym">URL</acronym>s (<acronym class="acronym">TURL</acronym>s) that are used for actual data transfer.

`srmPrepareToPut` prepares an `SRM` managed storage element to receive data into the list of destination <acronym class="acronym">SURL</acronym>s. It prepares a list of <acronym class="acronym">TURL</acronym>s where the client can write data into.

Both functions support transfer protocol negotiation. A client supplies a list of transfer protocols and the `SRM` server computes the <acronym class="acronym">TURL</acronym> using the first protocol from the list that it supports. Function invocation on the Storage Element depends on implementation and may range from simple <acronym class="acronym">SURL</acronym> to <acronym class="acronym">TURL</acronym> translation to stage from tape to disk cache and dynamic selection of transfer host and transfer protocol depending on the protocol availability and current load on each of the transfer server load.

The function `srmCopy` is used to copy files between `SRM` managed storage elements. If both source and target are local to the `SRM`, it performes a local copy. There are two modes of remote copies:

<div class="itemizedlist">

*   PULL mode : The target `SRM` initiates an `srmCopy` request. Upon the client\u0411\u2500\u2265s `srmCopy` request, the target `SRM` makes a space at the target storage, executes `srmPrepareToGet` on the source `SRM`. When the <acronym class="acronym">TURL</acronym> is ready at the source `SRM`, the target `SRM` transfers the file from the source <acronym class="acronym">TURL</acronym> into the prepared target storage. After the file transfer completes, `srmReleaseFiles` is issued to the source `SRM`.

*   PUSH mode : The source `SRM` initiates an `srmCopy` request. Upon the client\u0411\u2500\u2265s `srmCopy` request, the source `SRM` prepares a file to be transferred out to the target `SRM`, executes `srmPrepareToPut` on the target `SRM`. When the <acronym class="acronym">TURL</acronym> is ready at the target `SRM`, the source `SRM` transfers the file from the prepared source into the prepared target <acronym class="acronym">TURL</acronym>. After the file transfer completes, `srmPutDone` is issued to the target `SRM`.

</div>

When a specified target space token is provided, the files will be located in the space associated with the space token.

`SRM` Version 2.2 `srmPrepareToPut` and `srmCopy` PULL mode transfers allow the user to specify a space reservation token or a `RetentionPolicy` and `AccessLatency`. Any of these parameters are optional, and it is up to the implementation to decide what to do, if these properties are not specified. The specification requires that if a space reservation is given, then the specified `AccessLatency` or `RetentionPolicy` must match those of the space reservation.

The Data Transfer Functions are asynchronous, an initial `SRM` call starts a request execution on the server side and returns a request status that contains a unique request token. The status of request is polled periodically by `SRM` get request status functions. Once a request is completed and the client receives the <acronym class="acronym">TURL</acronym>s the data transfers are initiated. When the transfers are completed the client notifies the `SRM` server by executing `srmReleaseFiles` in case of `srmPrepareToGet` or `srmPutDone` in case of `srmPrepareToPut`. In case of `srmCopy`, the system knows when the transfers are completed and resources can be released, so it requires no special function at the end.

Clients are free to cancel the requests at any time by execution of `srmAbortFiles` or `srmAbortRequest`.

</div>

<div class="section" title="Request Status Functions">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-srm-intro-requestStatusFunct"></a>Request Status Functions

</div>

</div>

</div>

The functions for checking the request status are:

<div class="itemizedlist">

*   `srmStatusOfReserveSpaceRequest`
*   `srmStatusOfUpdateSpaceRequest`
*   `srmStatusOfChangeSpaceForFilesRequest`
*   `srmStatusOfChangeSpaceForFilesRequest`
*   `srmStatusOfBringOnlineRequest`
*   `srmStatusOfPutRequest`
*   `srmStatusOfCopyRequest`

</div>

</div>

<div class="section" title="Directory Functions">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-srm-intro-directoryFunct"></a>Directory Functions

</div>

</div>

</div>

`SRM` Version 2.2, interface provides a complete set of directory management functions. These are

<div class="itemizedlist">

*   `srmLs`, `srmRm`
*   `srmMkDir`, `srmRmDir`
*   `srmMv`

</div>

</div>

<div class="section" title="Permission functions">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-srm-intro-permissionFunct"></a>Permission functions

</div>

</div>

</div>

`SRM` Version 2.2 supports the following three file permission functions:

<div class="itemizedlist">

*   `srmGetPermission`
*   `srmCheckPermission` and
*   `srmSetPermission`

</div>

<span class="productname">dCache</span> contains an implementation of these functions that allows setting and checking of Unix file permissions.

</div>

</div>

</div>

<div class="chapter" title="Chapter 14\. The statistics Service">

<div class="titlepage">

<div>

<div>

## <a name="cf-statistics"></a>Chapter 14\. The `statistics` Service

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[The Basic Setup](#cf-statistics-basic)</span></dt>

<dt><span class="section">[The Statistics Web Page](#cf-statistics-webPage)</span></dt>

<dt><span class="section">[Explanation of the File Format of the `xxx.raw` Files](#cf-statistics-raw)</span></dt>

</dl>

</div>

The `statistics` service collects information on the amount of data stored on all pools and the total data flow including streams from and to tertiary storage systems.

Once per hour an <acronym class="acronym">ASCII</acronym> file is produced, containing a table with information on the amount of used disk space and the data transferred starting midnight up to this point in time. Data is sorted per pool and storage class.

In addition to the hourly statistics, files are produced reporting on the daily, monthly and yearly <span class="productname">dCache</span> activities. An <acronym class="acronym">HTML</acronym> tree is produced and updated once per hour allowing to navigate through the collected statistics information.

<div class="section" title="The Basic Setup">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-statistics-basic"></a>The Basic Setup

</div>

</div>

</div>

Define the `statistics` service in the domain, where the `httpd` is running.

<pre class="programlisting">[httpdDomain]
[httpdDomain/httpd]
...
[httpdDomain/statistics]</pre>

The `statistics` service automatically creates a directory tree, structured according to years, months and days.

Once per hour, a `total.raw` file is produced underneath the active `year`, `month` and `day` directories, containing the sum over all pools and storage classes of the corresponding time interval. The `day` directory contains detailed statistics per hour and for the whole day.

<pre class="programlisting"><span>/var/lib/dcache</span>/statistics/YYYY/total.raw
<span>/var/lib/dcache</span>/statistics/YYYY/MM/total.raw
<span>/var/lib/dcache</span>/statistics/YYYY/MM/DD/total.raw
<span>/var/lib/dcache</span>/statistics/YYYY/MM/DD/YYYY-MM-DD-day.raw
<span>/var/lib/dcache</span>/statistics/YYYY/MM/DD/YYYY-MM-DD-HH.raw</pre>

In the same directory tree the <acronym class="acronym">HTML</acronym> files are created for each day, month and year.

<pre class="programlisting"><span>/var/lib/dcache</span>/statistics/YYYY/index.html
<span>/var/lib/dcache</span>/statistics/YYYY/MM/index.html
<span>/var/lib/dcache</span>/statistics/YYYY/MM/DD/index.html</pre>

By default the path for the statistics data is `/var/lib/dcache/statistics`. You can modify this path by setting the property `dcache.paths.statistics` to a different value.

</div>

<div class="section" title="The Statistics Web Page">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-statistics-webPage"></a>The Statistics Web Page

</div>

</div>

</div>

Point a web browser to your <span class="productname">dCache</span> webpage at `http://_<tt><head-node.example.org></tt>_:2288/`. On the bottom you find the link to `Statistics`.

The statistics data needs to be collected for a day before it will appear on the web page.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

You will get an error if you try to read the statistics web page right after you enabled the `statistics` as the web page has not yet been created.

Create data and the web page by logging in to the admin interface and running the commands <span class="command">**create stat**</span> and <span class="command">**create html**</span>.

    (local) admin >

Now you can see a statistics web page.

</div>

Statistics is calculated once per hour at `_<tt><HH></tt>_:55`. The daily stuff is calculated at `23:55`. Without manual intervention, it takes two midnights before all <acronym class="acronym">HTML</acronym> statistics pages are available. There is a way to get this done after just one midnight. After the first midnight following the first startup of the statistics module, log into the `PoolStatistics` cell and run the following commands in the given sequence. The specified date has to be the Year/Month/Day of today.

    (PoolStatistics@)<httpdDomain> admin >

You will see an empty statistics page at `http://_<tt><head-node.example.org></tt>_:2288/statistics/`.

On the `Statistics Help Page` `http://_<tt><head-node.example.org></tt>_:2288/docs/statisticsHelp.html` you find an explanation for the colors.

</div>

<div class="section" title="Explanation of the File Format of the xxx.raw Files">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-statistics-raw"></a>Explanation of the File Format of the `xxx.raw` Files

</div>

</div>

</div>

The file formats of the `<span>/var/lib/dcache</span>/statistics/YYYY/MM/DD/YYYY-MM-DD-HH.raw` and the `<span>/var/lib/dcache</span>/statistics/YYYY/MM/DD/YYYY-MM-DD-day.raw` files are similar. The file `<span>/var/lib/dcache</span>/statistics/YYYY/MM/DD/YYYY-MM-DD-HH.raw` does not contain columns 2 and 3 as these are related to the day and not to the hour.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

The file format of the `<span>/var/lib/dcache</span>/statistics/YYYY/MM/DD/YYYY-MM-DD-day.raw` files:

<pre class="programlisting">#
# timestamp=1361364900897
# date=Wed Feb 20 13:55:00 CET 2013
#
pool1 StoreA:GroupB@osm 21307929 10155 2466935 10155 0 925 0  0   0   0   85362 0</pre>

</div>

</div>

Format of `YYYY-MM-DD-day.raw` files.

<div class="informaltable">

<table border="1"><colgroup><col align="center" class="Column"><col align="center" class="Description"></colgroup>

<thead>

<tr>

<th align="center">Column Number</th>

<th align="center">Column Description</th>

</tr>

</thead>

<tbody>

<tr>

<td align="center">0</td>

<td align="center">Pool Name</td>

</tr>

<tr>

<td align="center">1</td>

<td align="center">Storage Class</td>

</tr>

<tr>

<td align="center">2</td>

<td align="center">Bytes stored on this pool for this storage class at beginning of day — green bar</td>

</tr>

<tr>

<td align="center">3</td>

<td align="center">Number of files stored on this pool for this storage class at beginning of day</td>

</tr>

<tr>

<td align="center">4</td>

<td align="center">Bytes stored on this pool for this storage class at this hour or end of day — red bar</td>

</tr>

<tr>

<td align="center">5</td>

<td align="center">Number of files stored on this pool for this storage class at this hour or end of day</td>

</tr>

<tr>

<td align="center">6</td>

<td align="center">Total Number of transfers (in and out, dCache-client)</td>

</tr>

<tr>

<td align="center">7</td>

<td align="center">Total Number of restores (HSM to dCache)</td>

</tr>

<tr>

<td align="center">8</td>

<td align="center">Total Number of stores (dCache to HSM)</td>

</tr>

<tr>

<td align="center">9</td>

<td align="center">Total Number errors</td>

</tr>

<tr>

<td align="center">10</td>

<td align="center">Total Number of bytes transferred from client into dCache — blue bar</td>

</tr>

<tr>

<td align="center">11</td>

<td align="center">Total Number of bytes transferred from dCache to clients — yellow bar</td>

</tr>

<tr>

<td align="center">12</td>

<td align="center">Total Number of bytes tranferred from HSM to dCache — pink bar</td>

</tr>

<tr>

<td align="center">13</td>

<td align="center">Total Number of bytes tranferred from dCache to HSM — orange bar</td>

</tr>

</tbody>

</table>

</div>

The `YYYY/MM/DD/YYYY-MM-DD-HH.raw` files do not contain line 2 and 3.

</div>

</div>

<div class="chapter" title="Chapter 15\. The billing Service">

<div class="titlepage">

<div>

<div>

## <a name="cf-billing"></a>Chapter 15\. The `billing` Service

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[The billing log files](#cf-billing-log-files)</span></dt>

<dt><span class="section">[The <span class="database">billing</span> database](#cf-billing-db)</span></dt>

<dd>

<dl>

<dt><span class="section">[Customizing the database](#billing-customize)</span></dt>

</dl>

</dd>

<dt><span class="section">[Generating and Displaying Billing Plots](#config-billing-plots)</span></dt>

<dt><span class="section">[Upgrading a Previous Installation](#cf-billing-upgrade)</span></dt>

</dl>

</div>

<span class="productname">dCache</span> has built-in monitoring capabilities which provide an overview of the activity and performance of the installation’s doors and pools. There are two options for how this data can be represented and stored:

<div class="itemizedlist">

*   a set of log files written to a known location
*   a database (the <span class="database">billing</span> database).

</div>

These options can be enabled simultaneously. If the database option is selected, the data in those tables will also be displayed as a set of histogram plots on the installation’s web page.

<div class="section" title="The billing log files">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-billing-log-files"></a>The billing log files

</div>

</div>

</div>

If you installed <span class="productname">dCache</span> following the instructions in the Chapter [Installing <span class="productname">dCache</span>](#in "Chapter 2\. Installing dCache") you enabled the `billing` in the domain where the `httpd` service is running (see the extract of the layout file).

<pre class="programlisting">...
[httpdDomain]
[httpdDomain/billing]
[httpdDomain/httpd]
[httpdDomain/loginbroker]
...</pre>

Use the property `billing.text.dir` to set the location of the log files and the property `billing.enable.text` to control whether the plain-text log files are generated.

By default the log files are located in the directory `<span>/var/lib/dcache</span>/billing`. Under this directory the log files are organized in a tree data structure based on date (YYYY/MM). A separate file is generated for errors. The log file and the error file are tagged with the date.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

log file: `<span>/var/lib/dcache</span>/billing/2012/09/billing-2012.09.25`

error file: `<span>/var/lib/dcache</span>/billing/2012/09/billing-error-2012.09.25`

</div>

</div>

The log files may contain information about the time, the pool, the pnfsID and size of the transferred file, the storage class, the actual number of bytes transferred, the number of milliseconds the transfer took, the protocol, the subject (identity of the user given as a collection of principals), the data transfer listen port, the return status and a possible error message. The logged information depends on the protocol.

A log entry for a write operation has the default format:

<pre class="programlisting">_<tt><MM.dd></tt>_ _<tt><HH:mm:ss></tt>_ [pool:_<tt><pool-name></tt>_:transfer]
[_<tt><pnfsId></tt>_,_<tt><filesize></tt>_] [_<tt><path></tt>_]
_<tt><StoreName></tt>_:_<tt><StorageGroup></tt>_@_<tt><type-of-storage-system></tt>_
_<tt><transferred-bytes></tt>_  _<tt><connectionTime></tt>_ _<tt><true/false></tt>_ {_<tt><protocol></tt>_}
_<tt><initiator></tt>_  {_<tt><return-status></tt>_:"_<tt><error-message></tt>_"}</pre>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

A typical logging entry would look like this for writing. In the log file each entry is in one line. For readability we split it into separate lines in this documentation.:

<pre class="programlisting">12.10 14:19:42 [pool:pool2@poolDomain-1:transfer]
[0000062774D07847475BA78AC99C60F2C2FC,10475] [Unknown]
<Unknown>:<Unknown>@osm 10475 40 true {GFtp-1.0 131.169.72.103 37850}
[door:WebDAV-example.org@webdavDomain:1355145582248-1355145582485] {0:""}</pre>

</div>

</div>

The formatting of the log messages can be customized by redefining the `_<tt><billing.format.someInfoMessage></tt>_` properties in the layout configuration, where _<tt><billing.format.someInfoMessage></tt>_ can be replaced by

<div class="itemizedlist">

*   `billing.text.format.mover-info-message`
*   `billing.text.format.remove-file-info-message`
*   `billing.text.format.door-request-info-message`
*   `billing.text.format.storage-info-message`

</div>

A full explanation of the formatting is given in the `<span>/usr/share/dcache</span>/defaults/billing.properties` file. For syntax questions please consult [StringTemplate v3 documentation](http://www.antlr.org/wiki/display/ST/StringTemplate+3+Documentation) or the [cheat sheet](http://www.antlr.org/wiki/display/ST/StringTemplate+cheat+sheet).

On the web page generated by the `httpd` service (default port 2288), there is a link to `Action Log`. The table which appears there gives a summary overview extracted from the data contained in the billing log files.

</div>

<div class="section" title="The billing database">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-billing-db"></a>The <span class="database">billing</span> database

</div>

</div>

</div>

In order to enable the database, the following steps must be taken.

<div class="orderedlist">

1.  If the billing database does not already exist (see further below on migrating from an existing one), create it (we assume <span class="productname">PostgreSQL</span> here):

        [root] #

    If you are using a version of <span class="productname">PostgreSQL</span> prior to 8.4, you will also need to do:

        [root] #

    No further manual preparation is needed, as the necessary tables, indices, functions and triggers will automatically be generated when you (re)start the domain with the <span class="database">billing</span> database logging turned on (see below).

2.  The property `billing.enable.db` controls whether the billing cell sends billing messages to the database. By default the option is disabled. To activate, set the value to `true` and restart the domain in which the `httpd` service is running.

    <div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

    ### Note

    Please take care to define the `billing` service before the `httpd` service in your layout file. If the `billing` service is defined in a separate domain, this domain should be defined before the domain in which the `httpd` service is running.

    </div>

    <div class="informalexample">

    **Example:**

    <div class="informalexamplebody">

    Extract from the layout file:

    <pre class="programlisting">[httpdDomain]
         billing.enable.db=true
    [httpdDomain/billing]
    [httpdDomain/httpd]
    ...</pre>

        [root] #

    </div>

    </div>

</div>

<div class="section" title="Customizing the database">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="billing-customize"></a>Customizing the database

</div>

</div>

</div>

In most cases, the billing service will be run out-of-the-box; nevertheless, the administrator does have control, if this is desired, over the database configuration.

<div class="itemizedlist">

*   Database name, host, user, and password can be easily modified using the properties:

    <div class="itemizedlist">

    *   `billing.db.name`
    *   `billing.db.host`
    *   `billing.db.user`
    *   `billing.db.password`

    </div>

    The current database values can be checked with the <span class="command">**dcache database ls**</span> command.

    <div class="informalexample">

    **Example:**

    <div class="informalexamplebody">

    <pre class="screen"># dcache database ls
    DOMAIN          CELL        DATABASE HOST      USER      MANAGEABLE AUTO
    namespaceDomain PnfsManager chimera  localhost chimera   Yes        Yes
    namespaceDomain cleaner     chimera  localhost chimera   No         No
    httpdDomain     billing     billing  localhost srmdcache Yes        Yes</pre>

    </div>

    </div>

*   Database inserts are batched for performance, and are controlled by the following properties:

    <div class="itemizedlist">

    *   `billing.db.inserts.max-before-commit` (defaults to `10000`)
    *   `billing.db.inserts.timeout-before-commit` (defaults to `5`)

    </div>

    The default settings should usually be sufficient.

*   Should finer control over the DataNucleus layer (which talks to the database) be needed, then a new `datanucleus.properties` file must be provided. The path to this file, which will override the internal settings, should be indicated using:

    <div class="itemizedlist">

    *   `billing.db.config.path` (defaults to `""`)

    </div>

    Changing this configuration requires an understanding of [DataNucleus](http://www.datanucleus.org) , and we expect it will be rather uncommon to utilize this option (it is suggested that the administrator in this case consult with a member of the <span class="productname">dCache</span> team).

*   Changing the database type (which defaults to <span class="productname">PostgreSQL</span>) to something else would entail the above-mentioned necessary modification of the `datanucleus.properties` as well as changing the `billing.db.driver` and `billing.db.url` properties appropriately. This is not a recommended procedure, though in certain exceptional circumstances, it may be desirable or necessary. Once again, consultation with the <span class="productname">dCache</span> team is suggested in this case.

</div>

</div>

</div>

<div class="section" title="Generating and Displaying Billing Plots">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="config-billing-plots"></a>Generating and Displaying Billing Plots

</div>

</div>

</div>

If you have selected to store billing messages to the database, it is also possible to generate and display a set of histograms from the data in these tables. To turn on plot generation, set the property `httpd.enable.plots.billing` to `true` and restart the domain in which the `httpd` is running.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Extract from the layout file:

<pre class="programlisting">[httpdDomain]
     billing.enable.db=true
     httpd.enable.plots.billing=true
[httpdDomain/httpd]
[httpdDomain/billing]
...</pre>

</div>

</div>

The the frequency of plot refreshing and the type of plot produced can be controlled by:

<div class="itemizedlist">

*   `billingPlotsTimeoutInMins` (defaults to `30`)
*   `httpd.plots.billing.type` (defaults to `png` and can be set to `gif`)

</div>

The plots provide aggregate views of the data for 24-hour, 7-day, 30-day and 365-day periods.

The plot types are:

<div class="itemizedlist">

*   (Giga)bytes read and written for both <span class="productname">dCache</span> and <abbr class="abbrev">HSM</abbr> backend (if any)

*   Number of transactions/transfers for both <span class="productname">dCache</span> and <abbr class="abbrev">HSM</abbr> backend (if any)

*   Maximum, minimum and average connection time

*   Cache hits and misses

    <div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

    ### Note

    The data for this last histogram is not automatically sent, since it contributes significantly to message traffic between the pool manager and the billing service. To store this data (and thus generate the relevant plots), the `poolmanager.enable.cache-hit-message` property must be set either in `dcache.conf` or in the layout file for the domain where the `poolmanager` runs:

    <pre class="programlisting">poolmanager.enable.cache-hit-message=true</pre>

    </div>

</div>

Each individual plot can be magnified by clicking on it.

</div>

<div class="section" title="Upgrading a Previous Installation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-billing-upgrade"></a>Upgrading a Previous Installation

</div>

</div>

</div>

Because it is possible that the newer version may be deployed over an existing installation which already uses the <span class="database">billing</span> database, the Liquibase change-set has been written in such a way as to look for existing tables and to modify them only as necessary.

If you start the domain containing the `billing` service over a pre-existing installation of the <span class="database">billing</span> database, depending on what was already there, you may observe some messages like the following in the domain log having to do with the logic governing table initialization.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">INFO 8/23/12 10:35 AM:liquibase: Successfully acquired change log lock
INFO 8/23/12 10:35 AM:liquibase: Reading from databasechangelog
INFO 8/23/12 10:35 AM:liquibase: Reading from databasechangelog
INFO 8/23/12 10:35 AM:liquibase: Successfully released change log lock
INFO 8/23/12 10:35 AM:liquibase: Successfully released change log lock
INFO 8/23/12 10:35 AM:liquibase: Successfully acquired change log lock
INFO 8/23/12 10:35 AM:liquibase: Reading from databasechangelog
INFO 8/23/12 10:35 AM:liquibase: Reading from databasechangelog
INFO 8/23/12 10:35 AM:liquibase: ChangeSet org/dcache/services/billing/
   db/sql/billing.changelog-1.9.13.xml::4.1.7::arossi ran successfully in 264ms
INFO 8/23/12 10:35 AM:liquibase: Marking ChangeSet: org/dcache/services/
   billing/db/sql/billing.changelog-1.9.13.xml::4.1.8::arossi::(Checksum:
   3:faff07731c4ac867864824ca31e8ae81) ran despite precondition failure due
   to onFail='MARK_RAN': classpath:org/dcache/services/billing/db/sql/
   billing.changelog-master.xml : SQL Precondition failed. Expected '0' got '1'
INFO 8/23/12 10:35 AM:liquibase: ChangeSet org/dcache/services/billing/db/sql/
   billing.changelog-1.9.13.xml::4.1.9::arossi ran successfully in 14ms
INFO 8/23/12 10:35 AM:liquibase: Successfully released change log lock
INFO 8/23/12 10:35 AM:liquibase: Successfully released change log lock</pre>

</div>

</div>

Anything logged at a level lower than `ERROR` is usually entirely normal. Liquibase regularly reports when the preconditions determining whether it needs to do something are not met. All this means is that the update step was not necessary and it will be skipped in the future.

If, on the other hand, there is an `ERROR` logged by Liquibase, it is possible there may be some other conflict resulting from the upgrade (this should be rare). Such an error will block the domain from starting. One remedy which often works in this case is to do a clean re-initialization by dropping the Liquibase tables from the database:

    [root] #

and then restarting the domain.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

If the <span class="database">billing</span> database already exists, but contains tables other than the following:

    [root] #

that is, if it has been previously modified by hand or out-of-band to include custom tables not used directly by <span class="productname">dCache</span>, the existence of such extraneous tables should not impede <span class="productname">dCache</span> from working correctly, provided those other tables are `READ`-accessible by the database user for billing, which by default is `srmdcache`. This is a requirement imposed by the use of Liquibase. You thus may need explicitly to grant `READ` privileges to the <span class="database">billing</span> database user on any such tables if they are owned by another database user.

</div>

</div>

</div>

<div class="chapter" title="Chapter 16\. The alarms Service">

<div class="titlepage">

<div>

<div>

## <a name="cf-alarms"></a>Chapter 16\. The `alarms` Service

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[The Basic Setup](#cf-alarms-basic)</span></dt>

<dd>

<dl>

<dt><span class="section">[Configure where the `alarms` service is Running](#cf-alarms-basic-remoteServer)</span></dt>

<dt><span class="section">[The Defined Alarms](#cf-alarms-basic-definedAlarms)</span></dt>

</dl>

</dd>

<dt><span class="section">[Using the Alarms Web Page](#cf-alarms-webPage)</span></dt>

<dt><span class="section">[Alarms Database](#cf-alarms-db)</span></dt>

<dt><span class="section">[Advanced](#cf-alarms-advanced)</span></dt>

<dd>

<dl>

<dt><span class="section">[Email on Alarm](#cf-alarms-advanced-email)</span></dt>

<dt><span class="section">[Defining an Alarm](#cf-alarms-advanced-defineAlarm)</span></dt>

<dt><span class="section">[Run the Logback Server Independently from <span class="productname">dCache</span>](#cf-alarms-advanced-logbackServer)</span></dt>

</dl>

</dd>

<dt><span class="section">[Properties of the `alarms` Service](#cf-alarms-prop)</span></dt>

</dl>

</div>

<span class="productname">dCache</span> has an `alarms` service which allows any logging event to be marked as an _alarm_. This capability allows administrators to be directly notified of problems which need immediate attention and rectification. The alarms data can be stored in an <abbr class="abbrev">XML</abbr> file or in a database. In the basic configuration the data will be stored in an <abbr class="abbrev">XML</abbr> file.

The webadmin servlet running inside the `httpd` service has a special page for querying, displaying and tracking these alarms.

<div class="section" title="The Basic Setup">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-alarms-basic"></a>The Basic Setup

</div>

</div>

</div>

It is advisable to run the `alarms` service in a separate domain and list this domain first in the layout file. That way the `alarms` service gets booted first and can catch startup errors reported by the other domains. Since both the `httpd` service and the `alarms` service will access the storage file generated at `<span>/var/lib/dcache</span>/alarms/alarms.xml` the `alarms` service should be defined on the same host as the `httpd` service. You can modify where this file is placed by setting the property `httpd.alarms.db.xml.path` to a different location.

Add a domain for the `alarms` service to the layout file where the `httpd` service is defined.

<pre class="programlisting">[alarmserverDomain]
[alarmserverDomain/alarms]
...

[httpdDomain]</pre>

If all of the <span class="productname">dCache</span> domains run on the same host, then the default setting (localhost) will work.

<div class="section" title="Configure where the alarms service is Running">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-alarms-basic-remoteServer"></a>Configure where the `alarms` service is Running

</div>

</div>

</div>

In general your <span class="productname">dCache</span> will not be configured to run on one node. In this case each node needs to know on which node the `alarms` service is running. The `alarms` service and the `httpd` will run on one of the nodes. On all the other nodes you need to modify the `<span>/etc/dcache</span>/dcache.conf` file or the layout file to set the `alarms.server.host` property to the host on which the `alarms` service is running and restart <span class="productname">dCache</span>.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Look at an example of a <span class="productname">dCache</span> which consists of a head node, some door nodes and some pool nodes. Assume that the `httpd` service and the `alarms` service are running on the head node. Then you would need to set the property `alarms.server.host` on the pool nodes and on the door nodes to the host on which the `alarms` service is running.

<pre class="programlisting">alarms.server.host=_<tt><head-node></tt>_</pre>

</div>

</div>

</div>

<div class="section" title="The Defined Alarms">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-alarms-basic-definedAlarms"></a>The Defined Alarms

</div>

</div>

</div>

The alarms defined are listed below. There are four different levels of severity, `CRITICAL`, `HIGH`, `MODERATE` and `LOW`.

<div class="variablelist">

<dl>

<dt><span class="term">`CRITICAL`</span></dt>

<dd>

<div class="itemizedlist">

*   `SERVICE_CREATION_FAILURE`
*   `DB_OUT_OF_CONNECTIONS`
*   `DB_UNAVAILABLE`
*   `JVM_OUT_OF_MEMORY`
*   `OUT_OF_FILE_DESCRIPTORS`

</div>

The affected <span class="productname">dCache</span> can’t work (is down).

</dd>

<dt><span class="term">`HIGH`</span></dt>

<dd>

<div class="itemizedlist">

*   `IO_ERROR`
*   `HSM_READ_FAILURE`
*   `HSM_WRITE_FAILURE`
*   `LOCATION_MANAGER_UNAVAILABLE`
*   `POOL_MANAGER_UNAVAILABLE`

</div>

These functions are affected and not working or not working properly, even though the <span class="productname">dCache</span> domain may be running.

</dd>

<dt><span class="term">`MODERATE`</span></dt>

<dd>

<div class="itemizedlist">

*   `POOL_DISABLED`
*   `CHECKSUM`

</div>

There is an issue which should be taken care of in the interest of performance or usability, but which is not impeding the functioning of the system as a whole.

</dd>

<dt><span class="term">`LOW`</span></dt>

<dd>

This issue might be worth investigating if it occurs, but is not urgent.

</dd>

</dl>

</div>

</div>

Given that an alarm has been triggered, you will find an entry in the file `<span>/var/lib/dcache</span>/alarms/alarms.xml`.

As it is not very convenient to read an <abbr class="abbrev">XML</abbr> file, the Alarms Web Page can be used to inspect and manage the generated warnings.

</div>

<div class="section" title="Using the Alarms Web Page">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-alarms-webPage"></a>Using the Alarms Web Page

</div>

</div>

</div>

The Alarms Web Page is an admin page and thus requires authentication. You must enable `HTTPS` and you can give a gid (by default the gid is 1000):

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

For the authenticated mode you need to have a host certificate for your server host and place the `hostcert.p12` in the directory `/etc/dcache`.

</div>

<pre class="programlisting">[httpdDomain]
    httpd.enable.authn=true
    httpd.authz.admin-gid=_<tt><1234></tt>_
[httpdDomain/httpd]</pre>

<div class="informalfigure"><a name="fig-alarms-webpage"></a>

<div class="mediaobject" align="center">

<table border="0" summary="manufactured viewport for HTML img" cellspacing="0" cellpadding="0" width="100%">

<tbody>

<tr>

<td align="center">![](/images/Alarms.png)</td>

</tr>

</tbody>

</table>

</div>

</div>

<div class="orderedlist">

1.  The QUERY FILTER form can be used to limit the display of alarms in the table. The top three rows control an actual query to the database based on `after date`, `before date`, `severity` and `alarm type` name. (The date is the last update of the alarm, not the first arrival.) Each click of the `Refresh` button will reload the data from the database based on these three settings. The default behavior is `ALL` (unspecified properties). Placing a single date in the Beginning box will give you all alarms from that date up to today (inclusive); a single date in the Ending box will give all alarms up to that date (inclusive).
2.  The `Match Expression` filters in memory by appending all fields to a single string and doing a search. If the `Regular Expression` box is checked, the expression given is considered a regex (Java-style).
3.  The header to the table contains two checkboxes which allow you to check or uncheck the respective columns for all displayed items. Checking `Delete` and then clicking `Refresh` will actually eliminate the entry from persistent store.
4.  `Closed` is a way of marking the alarm as having been dealt with while maintaining a record of it. The `Show Closed Alarms` checkbox allows you to display them (turned off by default).
5.  All column titles appearing in white can be clicked to sort the table by that column.
6.  `Notes` is an editable field to be used for any special remarks.

</div>

When `Refresh` is clicked, any updates to `Closed` and `Notes` are first saved, then any `Deletes` are processed, and finally, the table is repopulated using the current query filter. The entire form is set to auto-refresh every 60 seconds.

An additional feature of the alarms infrastructure is automatic cleanup of processed alarms. An internal thread runs every so often, and purges all alarms marked as `closed` with a timestamp earlier than the given window. This daemon can be configured using the properties `httpd.enable.alarm-cleaner`, `httpd.alarm-cleaner.timeout` and `httpd.alarm-cleaner.delete-entries-before`.

</div>

<div class="section" title="Alarms Database">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-alarms-db"></a>Alarms Database

</div>

</div>

</div>

It might be useful to have a history of alarms. The <abbr class="abbrev">XML</abbr> file that is (in the default setup) used to store the alarms is cleaned on a regular basis as it would grow too big otherwise. You can configure to use a database instead of the <abbr class="abbrev">XML</abbr> file to obtain a history. Another advantage of the use of a database is that it is easier to search through a database than through a series of log files.

To use a database instead of the <abbr class="abbrev">XML</abbr> file you need to modify the `<span>/etc/dcache</span>/dcache.conf` file. Set the property `httpd.alarms.db.type` to `rdbms`. Moreover, as you want to maintain a history you should disable the `httpd.enable.alarm-cleaner`.

Create the alarms database.

    [root] #

Modify the `<span>/etc/dcache</span>/dcache.conf` file

<pre class="programlisting">httpd.alarms.db.type=rdbms
httpd.enable.alarm-cleaner=false</pre>

and restart <span class="productname">dCache</span>.

    [root] #

</div>

<div class="section" title="Advanced">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-alarms-advanced"></a>Advanced

</div>

</div>

</div>

<div class="section" title="Email on Alarm">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-alarms-advanced-email"></a>Email on Alarm

</div>

</div>

</div>

To configure to send an email on alarm you need to modify the `<span>/etc/dcache</span>logback.xml` file.

<pre class="programlisting"><appender name="ALARM_MAIL" class="ch.qos.logback.classic.net.SMTPAppender">
        <!-- this filter ensures that only events sent marked as ALARM
             are received by this appender -->
        <filter class="org.dcache.alarms.logback.AlarmMarkerFilter"/>
        <smtpHost></smtpHost>
        <to></to>
        <to></to>
        <from></from>
        <subject>dCache Alarm</subject>
        <layout class="ch.qos.logback.classic.PatternLayout">
            <pattern>%d{dd MMM yyyy HH:mm:ss} \(%X{cells.cell}\) [%X{org.dcache.ndc}] %m%n</pattern>
        </layout>
        <cyclicBufferTracker class="ch.qos.logback.core.spi.CyclicBufferTrackerImpl">
            <!-- send just one log entry per email -->
            <bufferSize>1</bufferSize>
        </cyclicBufferTracker>
    </appender></pre>

</div>

<div class="section" title="Defining an Alarm">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-alarms-advanced-defineAlarm"></a>Defining an Alarm

</div>

</div>

</div>

The file `logback.xml` found in the `<span>/etc/dcache</span>` directory adds an `org.dcache.alarms.logback.AlarmDefinitionAppender` to the root logger. This alarm appender embeds a child SocketAppender set to send events on the port specified by the property `alarms.server.port` to a host specified by the property `alarms.server.host`.

The alarms defined are listed in the [the section called “The Defined Alarms”](#cf-alarms-basic-definedAlarms "The Defined Alarms").

Define additional alarms simply by including other `<alarmType>` elements in the `<filter>` element.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Extract of the definition of the `SERVICE_CREATION_FAILURE` and the `CHECKSUM` alarms in the `<span>/etc/dcache</span>/logback.xml` file.

<pre class="programlisting">            <alarmType>
                regex:"(.+) from ac_create",
                type:SERVICE_CREATION_FAILURE,
                level:ERROR,
                severity:CRITICAL,
                include-in-key:group1 type host domain service
            </alarmType>
            .
            .
            .
            <alarmType>
                logger:org.dcache.pool.classic.ChecksumScanner,
                regex:"Checksum mismatch detected for (.+) - marking as BROKEN",
                type:CHECKSUM,
                level:ERROR,
                severity:MODERATE,
                include-in-key:group1 type host service domain
            </alarmType></pre>

</div>

</div>

The text of the `<alarmType>` element must be formed as a [JSON](http://www.json.org) string but without the beginning and ending braces ( ’{’, ’}’ ); this means, in essence, a comma-delimited list of `NAME:VALUE` pairs, with arbitrary whitespace between the pairs. The set of properties and their possible values is as follows:

<div class="small">

<table border="1"><colgroup><col align="left"><col align="left"><col align="left"></colgroup>

<thead>

<tr>

<th align="left">Property</th>

<th align="left">Possible values</th>

<th align="left">Required</th>

</tr>

</thead>

<tbody>

<tr>

<td align="left">`logger`</td>

<td align="left">name of the logger (see example above)</td>

<td align="left">at least one of `logger`, `regex`</td>

</tr>

<tr>

<td align="left">`regex`</td>

<td align="left">A pattern to match the message with.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

It is advisable to place the regex pattern in double quotes, so that the JSON parser will accept the special characters used in regular expressions: e.g., "[=].[\w]*"</div>

</td>

<td align="left">at least one of `logger`, `regex`</td>

</tr>

<tr>

<td align="left">`match-exception`</td>

<td align="left"><span class="emphasis">_False_</span>, <span class="emphasis">_True_</span></td>

<td align="left">`NO`</td>

</tr>

<tr>

<td align="left">`depth`</td>

<td align="left">Integer ≥ 0</td>

<td align="left">`NO`</td>

</tr>

<tr>

<td align="left">`type`</td>

<td align="left">An arbitrary name which will serve as the alarm’s marker.</td>

<td align="left">`YES`</td>

</tr>

<tr>

<td align="left">`level`</td>

<td align="left">`TRACE`, `DEBUG`, `INFO`, `WARN`, `ERROR`</td>

<td align="left">`YES`</td>

</tr>

<tr>

<td align="left">`severity`</td>

<td align="left">`INDETERMINATE` (default), `LOW`, `MODERATE`, `HIGH`, `CRITICAL`</td>

<td align="left">`NO`</td>

</tr>

<tr>

<td align="left">`regex-flags`</td>

<td align="left">A string representation of the (Java) regex flags options, joined by the 'or' pipe symbol: e.g., `CASE_INSENSITIVE | DOTALL`. For fuller explanation, see the Java Tutorials on [Regular Expressions](http://docs.oracle.com/javase/tutorial/essential/regex).</td>

<td align="left">`NO`</td>

</tr>

<tr>

<td align="left">`thread`</td>

<td align="left">Thread name (restricts this alarm type only to this particular thread).</td>

<td align="left">`NO`</td>

</tr>

<tr>

<td align="left">`include-in-key`</td>

<td align="left">Concatenation of key field names (see below)</td>

<td align="left">`YES`</td>

</tr>

</tbody>

</table>

</div>

<div class="section" title="The Properties match-exception and depth">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4960288"></a>The Properties `match-exception` and `depth`

</div>

</div>

</div>

The property `match-exception` is <span class="emphasis">_False_</span> by default. If set to <span class="emphasis">_True_</span>, it applies the regex pattern to all embedded exception messages, recursively, until a match is found.

The property `depth` is to be used with the property `match-exception`. The default is undefined (null), meaning unbounded. Setting `depth` to an integer > 0 indicates the level to which the match will be applied (in terms of nested messages). Setting it to 0 is equivalent to setting `match-exception` to false.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Have a look at the extract of the definition of the `DB_UNAVAILABLE` alarm in the `<span>/etc/dcache</span>/logback.xml` file.

<pre class="programlisting">            <alarmType>
                regex:"Unable to open a test connection to the given database|Connections could not be acquired from the underlying database",
                match-exception:true,
                depth:1,
                type:DB_UNAVAILABLE,
                level:ERROR,
                severity:CRITICAL,
                include-in-key:type host
            </alarmType></pre>

</div>

</div>

</div>

<div class="section" title="The property include-in-key">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp4970608"></a>The property `include-in-key`

</div>

</div>

</div>

The alarm key (the property `include-in-key`) is the set of properties whose values uniquely identify the alarm instance. For example, the checksum alarm defined above does not include the timestamp in its key, as all reports of this kind of error for a given file (PNFS id is given in the message body) are to be considered as duplicates of the first such alarm. The key field names which can be used to constitute the key are those which all alarms have in common:

`groupN`, `timestamp`, `message`, `logger`, `type`, `domain`, `service`, `host` and `thread`.

These property names should be delimited by (an arbitrary number of) whitespace characters. Note that `logger`, `timestamp` and `message` derive from the logging event, `host` is determined by static lookup, and `domain` and `service` correspond to the `cells.domain` and `cells.cell` properties in the event’s MDC map.

The key field name `groupN`, where `N` is an integer, means that the `Nth` substring (specified by parentheses) will be included. For `N=0`, `group0` is identical to `message`, which means that the whole message string should be included as an identifier.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

**Matching on Regex Groups.** Have a look at the extract of the definition of the `CHECKSUM` alarm in the `<span>/etc/dcache</span>/logback.xml` file.

<pre class="programlisting">            <alarmType>
                logger:org.dcache.pool.classic.ChecksumScanner,
                regex:"Checksum mismatch detected for (.+) - marking as BROKEN",
                type:CHECKSUM,
                level:ERROR,
                severity:MODERATE,
                include-in-key:group1 type host service domain
            </alarmType></pre>

Here the tag `group1` in the `include-in-key` extracts the `PNFS-ID` from the message and includes only that portion of the message string as an identifier. As usual, group0 is the same as the entire message.

</div>

</div>

When the appender applies this alarm definition filter, it relies on an implicit matching function: (logger, level, regex, thread) ⇒ type; hence a given alarm can be generated by more than one logger, and a logger in turn can send multiple types of alarms if these are mapped to different logging levels, thread names and/or regex patterns for the message body.

</div>

</div>

<div class="section" title="Run the Logback Server Independently from dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-alarms-advanced-logbackServer"></a>Run the Logback Server Independently from <span class="productname">dCache</span>

</div>

</div>

</div>

In most cases, running the alarm server as a <span class="productname">dCache</span> service will be adequate. Nevertheless, it is always possible to run the logback server entirely independently from <span class="productname">dCache</span>. In that case, you must be sure that the classpath carries the necessary <span class="productname">dCache</span> dependencies to provide the alarm appending functionality. Here is a bash snippet which will sufficiently define the classpath based on the <span class="productname">dCache</span> classes directory:

<pre class="programlisting"> #!/bin/sh
case $# in
    0)
        PORT=60001
	;;
    1)
        PORT=${1}
        ;;
    *)
        echo "Usage: $(basename $0) [PORT]" >&2
	exit 1
	;;
esac
DC=/etc/dcache
CL=/usr/share/dcache/classes

CP=.
CP=${CP}:`find ${CL} -name "activation-*.jar"`
CP=${CP}:`find ${CL} -name "datanucleus-api-jdo-*.jar"`
CP=${CP}:`find ${CL} -name "datanucleus-cache*.jar"`
CP=${CP}:`find ${CL} -name "datanucleus-core*.jar"`
CP=${CP}:`find ${CL} -name "datanucleus-xml*.jar"`
CP=${CP}:`find ${CL} -name "dcache-core*.jar"`
CP=${CP}:`find ${CL} -name "guava-*.jar"`
CP=${CP}:`find ${CL} -name "jargs-*.jar"`
CP=${CP}:`find ${CL} -name "jaxb-*.jar" | tr '\n' ':'`
CP=${CP}:`find ${CL} -name "jaxrpc-*.jar" | tr '\n' ':'`
CP=${CP}:`find ${CL} -name "jdo-api-*.jar"`
CP=${CP}:`find ${CL} -name "json-*.jar"`
CP=${CP}:`find ${CL} -name "log4j-over-slf4j-*.jar"`
CP=${CP}:`find ${CL} -name "logback-classic-*.jar"`
CP=${CP}:`find ${CL} -name "logback-core-*.jar"`
CP=${CP}:`find ${CL} -name "mail-*.jar"`
CP=${CP}:`find ${CL} -name "slf4j-api-*.jar"`

java -cp ${CP} ch.qos.logback.classic.net.SimpleSocketServer ${PORT} /var/lib/dcache/alarms/logback-server.xml &</pre>

</div>

</div>

<div class="section" title="Properties of the alarms Service">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-alarms-prop"></a>Properties of the `alarms` Service

</div>

</div>

</div>

This is a set of properties you might want to modify. Check the files `<span>/usr/share/dcache</span>/alarms.properties` and `<span>/usr/share/dcache</span>/httpd.properties` for the complete list.

<div class="variablelist">

<dl>

<dt><span class="term">alarms.dir</span></dt>

<dd>

Default: `<span>/var/lib/dcache</span>/alarms`

The main alarms area.

</dd>

<dt><span class="term">alarms.server.port</span></dt>

<dd>

Default: `60001`

The port on which the alarm server will listen.

</dd>

<dt><span class="term">alarms.server.host</span></dt>

<dd>

Default: `localhost`

The host on which the `alarms` service is running.

</dd>

<dt><span class="term">alarms.log.config.path</span></dt>

<dd>

Default: `${alarms.dir}/logback-server.xml`

The logback configuration for the alarm server.

</dd>

<dt><span class="term">httpd.alarms.db.type</span></dt>

<dd>

Default: `xml`

Defines what kind of database (either XML or <span class="productname">PostgreSQL</span>). Set `httpd.alarms.db.type`=`rdbms` to use <span class="productname">PostgreSQL</span>.

</dd>

<dt><span class="term">httpd.alarms.db.xml.path</span></dt>

<dd>

Default: `${alarms.dir}/alarms.xml`

The path of the `alarms.xml`. Used if `httpd.alarms.db.type`=`xml`.

</dd>

<dt><span class="term">alarms.db.rdbms.type</span></dt>

<dd>

Default: `postgresql`

If this value is changed from its default the `httpd.alarms.db.driver` property must also be changed.

</dd>

<dt><span class="term">httpd.alarms.db.driver</span></dt>

<dd>

Default: `org.postgresql.Driver`

This property should give the correct namespace for the RDBMS set by the property `alarms.db.rdbms.type`.

</dd>

<dt><span class="term">alarms.db.host</span></dt>

<dd>

Default: `localhost`

RDBMS/JDBC Database host name.

</dd>

<dt><span class="term">httpd.alarms.db.user</span></dt>

<dd>

Default:

RDBMS/JDBC Database user name.

</dd>

<dt><span class="term">httpd.alarms.db.password</span></dt>

<dd>

Default: `no password`

RDBMS/JDBC Database user password.

</dd>

<dt><span class="term">httpd.alarms.db.config.path</span></dt>

<dd>

Default: `${alarms.dir}/datanucleus.properties`

Path for overriding the internally set DAO (DataNucleus) properties for alarm storage, for instance, to configure an RDBMS database; will be used only if the <acronym class="acronym">URL</acronym> does not point to the <abbr class="abbrev">XML</abbr> default.

</dd>

<dt><span class="term">httpd.enable.alarm-cleaner</span></dt>

<dd>

Default: `true`

If set to true a thread which automatically removes closed alarms older than a given threshold will run.

</dd>

<dt><span class="term">httpd.alarm-cleaner.timeout</span></dt>

<dd>

Default: `168` (24 x 7 hours)

Wait interval between successive sweeps of the cleanup daemon.

</dd>

<dt><span class="term">httpd.alarm-cleaner.delete-entries-before</span></dt>

<dd>

Default: `336` (24 X 14 hours)

Closed alarms will be deleted after this time.

</dd>

</dl>

</div>

</div>

</div>

<div class="chapter" title="Chapter 17\. dCache Webadmin Interface">

<div class="titlepage">

<div>

<div>

## <a name="cf-webadmin"></a>Chapter 17\. <span class="productname">dCache</span> Webadmin Interface

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Installation](#cf-webadmin-install)</span></dt>

</dl>

</div>

This part describes how to configure the `webadmin` service which runs inside the `httpdDomain` and offers additional features to admins like sending admin-commands equal to those of admin interface (CLI) to chosen cells or displaying billing plots.

For authentication and authorisation it offers usage of username/password (currently the kpwd-Plugin) or grid certificate talking to `gPlazma2`. It also offers a non-authenticated read-only mode.

If you are logged in as admin it is possible to send a command to multiple pools or a whole poolgroup in one go. It is even possible to send a command to any <span class="productname">dCache</span> cell. Also, there is information like their size, their id and used space on linkgroups and spacetokens available.

From the technical point of view the `webadmin` service uses a Jetty-Server which is embedded in an ordinary `httpd` cell. It is using apache-wicket (a webfrontend-framework) and <abbr class="abbrev">YAML</abbr> (a CSS-Template Framework).

<div class="section" title="Installation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-webadmin-install"></a>Installation

</div>

</div>

</div>

For the authenticated mode a configured `gPlazma` is required (see also [the section called “`gPlazma` config example to work with authenticated webadmin”](#cf-gplazma-webadmin-example "gPlazma config example to work with authenticated webadmin")). The user may either authenticate by presenting his grid certificate or by entering a valid username/password combination. This way it is possible to login even if the user does not have a grid certificate. For a non-authenticated `webadmin` service you just need to start the `httpd` service.

For the authenticated mode using a grid certificate the host certificate has to be imported into the <span class="productname">dCache</span>-keystore. In the grid world host certificates are usually signed by national Grid-CAs. Refer to the documentation provided by the Grid-CA to find out how to request a certificate. To import them into the <span class="productname">dCache</span>-keystore use this command:

    [root] #

Now you have to initialise your truststore (this is the certificate-store used for the SSL connections) by using this command:

    [root] #

The `webadmin` service uses the same truststore as `webdav` service, so you can skip this step if you have `webdav` configured with SSL.

The default instance name is the name of the host which runs the httpdDomain and the default http port number is `2288` (this is the default port number of the `httpd` service). Now you should be able to have a read-only access to the webpage `http://example.com:2288/webadmin`.

In the following example we will enable the authenticated mode.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">[httpdDomain]
      authenticated=true</pre>

</div>

</div>

The most important value is `httpd.authz.admin-gid`, because it configures who is allowed to alter <span class="productname">dCache</span> behaviour, which certainly should not be everyone:

<pre class="programlisting"># # When a user has this GID he can become an admin for the webadmin interface #
httpd.authz.admin-gid=0</pre>

To see all webadmin specific property values have a look at `<span>/usr/share/dcache</span>/defaults/httpd.properties`.

For information on `gPlazma` configuration have a look at [Chapter 10, _Authorization in <span class="productname">dCache</span>_](#cf-gplazma "Chapter 10\. Authorization in dCache") and for a special example [the section called “`gPlazma` config example to work with authenticated webadmin”](#cf-gplazma-webadmin-example "gPlazma config example to work with authenticated webadmin").

</div>

</div>

<div class="chapter" title="Chapter 18\.  ACLs in dCache">

<div class="titlepage">

<div>

<div>

## <a name="cf-acl"></a>Chapter 18\. <acronym class="acronym">ACL</acronym>s in <span class="productname">dCache</span>

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Introduction](#cf-acl-introduction)</span></dt>

<dt><span class="section">[Database configuration](#cf-acl-db-install)</span></dt>

<dt><span class="section">[Configuring <acronym class="acronym">ACL</acronym> support](#cf-acl-dcachesetup)</span></dt>

<dd>

<dl>

<dt><span class="section">[Enabling <acronym class="acronym">ACL</acronym> support](#cf-acl-config-enable)</span></dt>

</dl>

</dd>

<dt><span class="section">[Administrating <acronym class="acronym">ACL</acronym>s](#cf-acl-admin)</span></dt>

<dd>

<dl>

<dt><span class="section">[How to set <acronym class="acronym">ACL</acronym>s](#idp5159312)</span></dt>

<dt><span class="section">[Viewing configured <acronym class="acronym">ACL</acronym>s](#cf-acl-view)</span></dt>

</dl>

</dd>

</dl>

</div>

<span class="productname">dCache</span> includes support for Access Control Lists (<acronym class="acronym">ACL</acronym>s). This support is conforming to the [NFS version 4 Protocol specification](http://www.nfsv4-editor.org/draft-25/draft-ietf-nfsv4-minorversion1-25.html).

This chapter provides some background information and details on configuring <span class="productname">dCache</span> to use <acronym class="acronym">ACL</acronym>s and how to administer the resulting system.

<div class="note" title="ACLs and pnfs" style="margin-left: 0.5in; margin-right: 0.5in;">

### <acronym class="acronym">ACL</acronym>s and <span class="productname">`pnfs`</span>

<acronym class="acronym">ACL</acronym>s are only supported with the <span class="productname">Chimera</span> name space backend. Versions before 1.9.12 had partial support for <acronym class="acronym">ACL</acronym>s with the <span class="productname">`pnfs`</span> backend, however due to the limitations of that implementation <acronym class="acronym">ACL</acronym>s were practically useless with <span class="productname">`pnfs`</span>.

</div>

<div class="section" title="Introduction">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-acl-introduction"></a>Introduction

</div>

</div>

</div>

<span class="productname">dCache</span> allows control over namespace operations (e.g., creating new files and directories, deleting items, renaming items) and data operations (reading data, writing data) using the standard Unix permission model. In this model, files and directories have both owner and group-owner attributes and a set of permissions that apply to the owner, permissions for users that are members of the group-owner group and permissions for other users.

Although Unix permission model is flexible enough for many deployment scenarios there are configurations that either cannot configured easily or are impossible. To satisfy these more complex permission handling <span class="productname">dCache</span> has support for <acronym class="acronym">ACL</acronym>-based permission handling.

An Access Control List (<acronym class="acronym">ACL</acronym>) is a set of rules for determining whether an end-user is allowed to undertake some specific operation. Each <acronym class="acronym">ACL</acronym> is tied to a specific namespace entry: a file or directory. When an end-user wishes to undertake some operation then the <acronym class="acronym">ACL</acronym> for that namespace entry is checked to see if that user is authorised. If the operation is to create a new file or directory then the <acronym class="acronym">ACL</acronym> of the parent directory is checked.

<div class="note" title="File- and directory- ACLs" style="margin-left: 0.5in; margin-right: 0.5in;">

### File- and directory- <acronym class="acronym">ACL</acronym>s

Each <acronym class="acronym">ACL</acronym> is associated with a specific file or directory in <span class="productname">dCache</span>. Although the general form is the same whether the <acronym class="acronym">ACL</acronym> is associated with a file or directory, some aspects of an <acronym class="acronym">ACL</acronym> may change. Because of this, we introduce the terms _file-<acronym class="acronym">ACL</acronym>_ and _directory-<acronym class="acronym">ACL</acronym>_ when taking about <acronym class="acronym">ACL</acronym>s associated with a file or a directory respectively. If the term _<acronym class="acronym">ACL</acronym>_ is used then it refers to both file-<acronym class="acronym">ACL</acronym>s and directory-<acronym class="acronym">ACL</acronym>s.

</div>

Each <acronym class="acronym">ACL</acronym> contains a list of one or more Access Control Entries (<acronym class="acronym">ACE</acronym>s). The <acronym class="acronym">ACE</acronym>s describe how <span class="productname">dCache</span> determines whether an end-user is authorised. Each <acronym class="acronym">ACE</acronym> contains information about which group of end users it applies to and describes whether this group is authorised for some subset of possible operations.

The order of the <acronym class="acronym">ACE</acronym>s within an <acronym class="acronym">ACL</acronym> is significant. When checking whether an end-user is authorised each <acronym class="acronym">ACE</acronym> is checked in turn to see if it applies to the end-user and the requested operation. If it does then that <acronym class="acronym">ACE</acronym> determines whether that end-user is authorised. If not then the next <acronym class="acronym">ACE</acronym> is checked. Thus an <acronym class="acronym">ACL</acronym> can have several <acronym class="acronym">ACE</acronym>s and the first matched <acronym class="acronym">ACE</acronym> <span class="quote">“<span class="quote">wins</span>”</span>.

One of the problems with traditional Unix-based permission model is its inflexible handling of newly created files and directories. With transitional filesystems, the permissions that are set are under the control of the user-process creating the file. The sysadmin has no direct control over the permissions that newly files or directories will have. The <acronym class="acronym">ACL</acronym> permission model solves this problem by allowing explicit configuration using inheritance.

<acronym class="acronym">ACL</acronym> inheritance is when a new file or directory is created with an <acronym class="acronym">ACL</acronym> containing a set of <acronym class="acronym">ACE</acronym>s from the parent directory’s <acronym class="acronym">ACL</acronym>. The inherited <acronym class="acronym">ACE</acronym>s are specially marked so that only those that are intended will be inherited.

Inheritance only happens when a new file or directory is created. After creation, the <acronym class="acronym">ACL</acronym> of the new file or directory is completely decoupled from the parent directory’s <acronym class="acronym">ACL</acronym>: the <acronym class="acronym">ACL</acronym> of the parent directory may be altered without affecting the <acronym class="acronym">ACL</acronym> of the new file or directory and visa versa.

Inheritance is optional. Within a directory’s <acronym class="acronym">ACL</acronym> some <acronym class="acronym">ACE</acronym>s may be inherited whilst others are not. New files or directories will receive only those <acronym class="acronym">ACE</acronym>s that are configured; the remaining <acronym class="acronym">ACE</acronym>s will not be copied.

</div>

<div class="section" title="Database configuration">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-acl-db-install"></a>Database configuration

</div>

</div>

</div>

<acronym class="acronym">ACL</acronym> support requires database tables to store <acronym class="acronym">ACL</acronym> and <acronym class="acronym">ACE</acronym> information. These tables are part of the <span class="productname">Chimera</span> name space backend and for a new installation no additional steps are needed to prepare the database.

Early versions of <span class="productname">Chimera</span> (before <span class="productname">dCache</span> 1.9.3) did not create the <acronym class="acronym">ACL</acronym> table during installation. If the database is lacking the extra table then it has to be created before enabling <acronym class="acronym">ACL</acronym> support. This is achieved by applying two SQL files:

    [root] #

</div>

<div class="section" title="Configuring ACL support">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-acl-dcachesetup"></a>Configuring <acronym class="acronym">ACL</acronym> support

</div>

</div>

</div>

The `dcache.conf` and layout files contain a number of settings that may be adjusted to configure <span class="productname">dCache</span>’s permission settings. These settings are are described in this section.

<div class="section" title="Enabling ACL support">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-acl-config-enable"></a>Enabling <acronym class="acronym">ACL</acronym> support

</div>

</div>

</div>

To enable <acronym class="acronym">ACL</acronym> support set `pnfsmanager.enable.acl`=`true` in the layout file.

<pre class="programlisting">..
[_<tt><domainName></tt>_/pnfsmanager]
pnfsmanager.enable.acl=true
..</pre>

</div>

</div>

<div class="section" title="Administrating ACLs">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-acl-admin"></a>Administrating <acronym class="acronym">ACL</acronym>s

</div>

</div>

</div>

Altering <span class="productname">dCache</span> <acronym class="acronym">ACL</acronym> behaviour is achieved by connecting to the `PnfsManager` [_well-known cell_](#gl-well-known-cell) using the administrator interface. For further details about how to use the administrator interface, see [the section called “The Admin Interface”](#intouch-admin "The Admin Interface").

The <span class="command">**info**</span> and <span class="command">**help**</span> commands are available within `PnfsManager` and fulfil their usual functions.

<div class="section" title="How to set ACLs">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp5159312"></a>How to set <acronym class="acronym">ACL</acronym>s

</div>

</div>

</div>

The <span class="command">**setfacl**</span> command is used to set a new <acronym class="acronym">ACL</acronym>. This command accepts arguments with the following form:

<div class="cmdsynopsis">

`setfacl` _<tt><ID></tt>_ _<tt><ACE></tt>_ [_<tt><ACE></tt>_...]

</div>

The _<tt><ID></tt>_ argument is either a <span class="productname">`pnfs`</span>-ID or the absolute path of some file or directory in <span class="productname">dCache</span>. The <span class="command">**setfacl**</span> command requires one or more _<tt><ACE></tt>_ arguments seperated by spaces.

The <span class="command">**setfacl**</span> command creates a new <acronym class="acronym">ACL</acronym> for the file or directory represented by _<tt><ID></tt>_. This new <acronym class="acronym">ACL</acronym> replaces any existing <acronym class="acronym">ACE</acronym>s for _<tt><ID></tt>_.

An <acronym class="acronym">ACL</acronym> has one or more <acronym class="acronym">ACE</acronym>s. Each <acronym class="acronym">ACE</acronym> defines permissions to access this resource for some [Subject](#ebnf.ace.subject). The <acronym class="acronym">ACE</acronym>s are space-separated and the ordering is significant. The format and description of these <acronym class="acronym">ACE</acronym> values are described below.

<div class="section" title="Description of the ACE structure">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp5176800"></a>Description of the <acronym class="acronym">ACE</acronym> structure

</div>

</div>

</div>

The _<tt><ACE></tt>_ arguments to the <span class="command">**setfacl**</span> command have a specific format. This format is described below in Extended Backus-Naur Form (<abbr class="abbrev">EBNF</abbr>).

<table width="100%" cellpadding="5" bgcolor="#F5DCB3" border="1" class="productionset" summary="EBNF">

<tbody>

<tr>

<td>

<table border="0" width="99%" cellpadding="0" bgcolor="#F5DCB3" class="productionset" summary="EBNF productions">

<tbody>

<tr>

<td align="left" valign="top" width="3%">[1]</td>

<td align="right" valign="top" width="10%"><a name="ebnf.ace"></a>ACE</td>

<td valign="top" width="5%" align="center">`::=`</td>

<td valign="top" width="52%">[Subject](#ebnf.ace.subject) ':' [Access](#ebnf.ace.access) |  
[Subject](#ebnf.ace.subject) ':' [Access](#ebnf.ace.access) ':' [Inheritance](#ebnf.ace.inheritance)</td>

</tr>

<tr>

<td align="left" valign="top" width="3%">[2]</td>

<td align="right" valign="top" width="10%"><a name="ebnf.ace.subject"></a>Subject</td>

<td valign="top" width="5%" align="center">`::=`</td>

<td valign="top" width="52%">'USER:' [UserID](#ebnf.ace.user) |  
'GROUP:' [GroupID](#ebnf.ace.group) |  
'OWNER@' |  
'GROUP@' |  
'EVERYONE@' |  
'ANONYMOUS@' |  
'AUTHENTICATED@'</td>

</tr>

<tr>

<td align="left" valign="top" width="3%">[3]</td>

<td align="right" valign="top" width="10%"><a name="ebnf.ace.access"></a>Access</td>

<td valign="top" width="5%" align="center">`::=`</td>

<td valign="top" width="52%">'+' [Mask](#ebnf.ace.mask) |  
'-' [Mask](#ebnf.ace.mask)</td>

</tr>

<tr>

<td align="left" valign="top" width="3%">[4]</td>

<td align="right" valign="top" width="10%"><a name="ebnf.ace.mask"></a>Mask</td>

<td valign="top" width="5%" align="center">`::=`</td>

<td valign="top" width="52%">[Mask](#ebnf.ace.mask) [MaskItem](#ebnf.ace.maskItem) |  
[MaskItem](#ebnf.ace.maskItem)</td>

</tr>

<tr>

<td align="left" valign="top" width="3%">[5]</td>

<td align="right" valign="top" width="10%"><a name="ebnf.ace.maskItem"></a>MaskItem</td>

<td valign="top" width="5%" align="center">`::=`</td>

<td valign="top" width="52%">'r' | 'l' | 'w' | 'f' | 's' | 'a' | 'n' | 'N' | 'x' | 'd' | 'D' | 't' | 'T' | 'c' | 'C' | 'o'</td>

</tr>

<tr>

<td align="left" valign="top" width="3%">[6]</td>

<td align="right" valign="top" width="10%"><a name="ebnf.ace.inheritance"></a>Inheritance</td>

<td valign="top" width="5%" align="center">`::=`</td>

<td valign="top" width="52%">[Inheritance](#ebnf.ace.inheritance) [Flag](#ebnf.ace.flag) |  
[Flag](#ebnf.ace.flag)</td>

</tr>

<tr>

<td align="left" valign="top" width="3%">[7]</td>

<td align="right" valign="top" width="10%"><a name="ebnf.ace.flag"></a>Flag</td>

<td valign="top" width="5%" align="center">`::=`</td>

<td valign="top" width="52%">'f' | 'd' | 'o'</td>

</tr>

<tr>

<td align="left" valign="top" width="3%">[8]</td>

<td align="right" valign="top" width="10%"><a name="ebnf.ace.user"></a>UserID</td>

<td valign="top" width="5%" align="center">`::=`</td>

<td valign="top" width="52%">INTEGER</td>

</tr>

<tr>

<td align="left" valign="top" width="3%">[9]</td>

<td align="right" valign="top" width="10%"><a name="ebnf.ace.group"></a>GroupID</td>

<td valign="top" width="5%" align="center">`::=`</td>

<td valign="top" width="52%">INTEGER</td>

</tr>

</tbody>

</table>

</td>

</tr>

</tbody>

</table>

The various options are described below.

<div class="section" title="The Subject">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="idp5207440"></a>The Subject

</div>

</div>

</div>

The [Subject](#ebnf.ace.subject) defines to which user or group of users the <acronym class="acronym">ACE</acronym> will apply. It acts as a filter so that only those users that match the Subject will have their access rights affected.

As indicated by the EBNF above, the Subject of an <acronym class="acronym">ACE</acronym> can take one of several forms. These are described below:

<div class="variablelist">

<table border="0" summary="values of the subject"><colgroup><col align="left" valign="top"></colgroup>

<tbody>

<tr>

<td>

**<span class="term">`USER:`_<tt><id></tt>_</span>**

</td>

<td>

The `USER:` prefix indicates that the <acronym class="acronym">ACE</acronym> applies only to the specific end-user: the <span class="productname">dCache</span> user with ID _<tt><id></tt>_. For example, `USER:0:+w` is an <acronym class="acronym">ACE</acronym> that allows user 0 to write over a file’s existing data.

</td>

</tr>

<tr>

<td>

**<span class="term">`GROUP:`_<tt><id></tt>_</span>**

</td>

<td>

The `GROUP:` prefix indicates that the <acronym class="acronym">ACE</acronym> applies only to those end-users who are a member of the specific group: the <span class="productname">dCache</span> group with ID _<tt><id></tt>_. For example, `GROUP:20:+a` is an <acronym class="acronym">ACE</acronym> that allows any user who is a member of group 20 to append data to the end of a file.

</td>

</tr>

<tr>

<td>

**<span class="term">`OWNER@`</span>**

</td>

<td>

The `OWNER@` subject indicates that the <acronym class="acronym">ACE</acronym> applies only to whichever end-user owns the file or directory. For example, `OWNER@:+d` is an <acronym class="acronym">ACE</acronym> that allows the file’s or directory’s owner to delete it.

</td>

</tr>

<tr>

<td>

**<span class="term">`GROUP@`</span>**

</td>

<td>

The `GROUP@` subject indicates that the <acronym class="acronym">ACE</acronym> applies only to all users that are members of the group-owner of the file or directory. For example, `GROUP@:+l` is an <acronym class="acronym">ACE</acronym> that allows any user that is in a directory’s group-owner to list the directory’s contents.

</td>

</tr>

<tr>

<td>

**<span class="term">`EVERYONE@`</span>**

</td>

<td>

The `EVERYONE@` subject indicates that the <acronym class="acronym">ACE</acronym> applies to all users. For example, `EVERYONE@:+r` is an <acronym class="acronym">ACE</acronym> that makes a file world-readable.

</td>

</tr>

<tr>

<td>

**<span class="term">`ANONYMOUS@`</span>**

</td>

<td>

The `ANONYMOUS@` Subject indicates that the <acronym class="acronym">ACE</acronym> applies to all users who have not authenticated themselves. For example, `ANONYMOUS@:-l` is an <acronym class="acronym">ACE</acronym> that prevents unauthenticated users from listing the contents of a directory.

</td>

</tr>

<tr>

<td>

**<span class="term">`AUTHENTICATED@`</span>**

</td>

<td>

The `AUTHENTICATED@` Subject indicates that an <acronym class="acronym">ACE</acronym> applies to all authenticated users. For example, `AUTHENTICATED@:+r` is an <acronym class="acronym">ACE</acronym> that allows any authenticated user to read a file’s contents.

</td>

</tr>

</tbody>

</table>

</div>

</div>

<div class="note" title="Authenticated or anonymous" style="margin-left: 0.5in; margin-right: 0.5in;">

### Authenticated or anonymous

An end user of <span class="productname">dCache</span> is either authenticated or is unauthenticated, but never both. Because of this, an end user operation will either match <acronym class="acronym">ACE</acronym>s with `ANONYMOUS@` Subjects or `AUTHENTICATED@` Subjects but the request will never match both at the same time.

</div>

<div class="section" title="Access mask">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="idp5249792"></a>Access mask

</div>

</div>

</div>

[Access](#ebnf.ace.access) (defined in the [<acronym class="acronym">ACE</acronym> EBNF](#ebnf.ace) above) describes what kind of operations are being described by the <acronym class="acronym">ACE</acronym> and whether the <acronym class="acronym">ACE</acronym> is granting permission or denying it.

An individual <acronym class="acronym">ACE</acronym> can either grant permissions or deny them, but never both. However, an <acronym class="acronym">ACL</acronym> may be composed of any mixture of authorising- and denying- <acronym class="acronym">ACE</acronym>s. The first character of [Access](#ebnf.ace.access) describes whether the <acronym class="acronym">ACE</acronym> is authorising or denying.

If [Access](#ebnf.ace.access) begins with a plus symbol (`+`) then the <acronym class="acronym">ACE</acronym> authorises the [Subject](#ebnf.ace.subject) some operations. The <acronym class="acronym">ACE</acronym> `EVERYONE@:+r` authorises all users to read a file since the [Access](#ebnf.ace.access) begins with a `+`.

If the [Access](#ebnf.ace.access) begins with a minus symbol (`-`) then the <acronym class="acronym">ACE</acronym> denies the [Subject](#ebnf.ace.subject) some operations. The <acronym class="acronym">ACE</acronym> `EVERYONE@:-r` prevents any user from reading a file since the Access begins with a `-`.

The first character of [Access](#ebnf.ace.access) must be `+` or `-`, no other possibility is allowed. The initial `+` or `-` of [Access](#ebnf.ace.access) is followed by one or more operation letters. These letters form the <acronym class="acronym">ACE</acronym>’s _access mask_ ([Mask](#ebnf.ace.mask) in [<acronym class="acronym">ACE</acronym> EBNF](#ebnf.ace) above).

The access mask describes which operations may be allowed or denied by the <acronym class="acronym">ACE</acronym>. Each type of operation has a corresponding letter; for example, obtaining a directory listing has a corresponding letter `l`. If a user attempts an operation of a type corresponding to a letter present in the access mask then the <acronym class="acronym">ACE</acronym> may affect whether the operation is authorised. If the corresponding letter is absent from the access mask then the <acronym class="acronym">ACE</acronym> will be ignored for this operation.

The following table describes the access mask letters and the corresponding operations:

<div class="note" title="File- and directory- specific operations" style="margin-left: 0.5in; margin-right: 0.5in;">

### File- and directory- specific operations

Some operations and, correspondingly, some access mask letters only make sense for <acronym class="acronym">ACL</acronym>s attached to certain types of items. Some operations only apply to directories, some operations are only for files and some operations apply to both files and directories.

When configuring an <acronym class="acronym">ACL</acronym>, if an <acronym class="acronym">ACE</acronym> has an operation letter in the access mask that is not applicable to whatever the <acronym class="acronym">ACL</acronym> is associated with then the letter is converted to an equivalent. For example, if `l` (list directory) is in the access mask of an <acronym class="acronym">ACE</acronym> that is part of a file-<acronym class="acronym">ACL</acronym> then it is converted to `r`. These mappings are described in the following table.

</div>

<div class="variablelist">

<table border="0" summary="access mask"><colgroup><col align="left" valign="top"></colgroup>

<tbody>

<tr>

<td>

**<span class="term">`r`</span>**

</td>

<td>

reading data from a file. Specifying `r` in an <acronym class="acronym">ACE</acronym>’s access mask controls whether end-users are allowed to read a file’s contents. If the <acronym class="acronym">ACE</acronym> is part of a directory-<acronym class="acronym">ACL</acronym> then the letter is converted to `l`.

</td>

</tr>

<tr>

<td>

**<span class="term">`l`</span>**

</td>

<td>

listing the contents of a directory. Specifying `l` in an <acronym class="acronym">ACE</acronym>’s access mask controls whether end-users are allowed to list a directory’s contents. If the <acronym class="acronym">ACE</acronym> is part of a file-<acronym class="acronym">ACL</acronym> then the letter is converted to `r`.

</td>

</tr>

<tr>

<td>

**<span class="term">`w`</span>**

</td>

<td>

overwriting a file’s existing contents. Specifying `w` in an <acronym class="acronym">ACE</acronym>’s access mask controls whether end-users are allowed to write data anywhere within the file’s current offset range. This includes the ability to write to any arbitrary offset and, as a result, to grow the file. If the <acronym class="acronym">ACE</acronym> is part of a directory-<acronym class="acronym">ACL</acronym> then the letter is converted to `f`.

</td>

</tr>

<tr>

<td>

**<span class="term">`f`</span>**

</td>

<td>

creating a new file within a directory. Specifying `f` in an <acronym class="acronym">ACE</acronym>’s access mask controls whether end-users are allowed to create a new file. If the <acronym class="acronym">ACE</acronym> is part of an file-<acronym class="acronym">ACL</acronym> then then the letter is converted to `w`.

</td>

</tr>

<tr>

<td>

**<span class="term">`s`</span>**

</td>

<td>

creating a subdirectory within a directory. Specifying `s` in an <acronym class="acronym">ACE</acronym>’s access mask controls whether end-users are allowed to create new subdirectories. If the <acronym class="acronym">ACE</acronym> is part of a file-<acronym class="acronym">ACL</acronym> then the letter is converted to `a`.

</td>

</tr>

<tr>

<td>

**<span class="term">`a`</span>**

</td>

<td>

appending data to the end of a file. Specifying `a` in an <acronym class="acronym">ACE</acronym>’s access mask controls whether end-users are allowed to add data to the end of a file. If the <acronym class="acronym">ACE</acronym> is part of a directory-<acronym class="acronym">ACL</acronym> then the letter is converted to `s`.

</td>

</tr>

<tr>

<td>

**<span class="term">`n`</span>**

</td>

<td>

reading attributes. Specifying `n` in an <acronym class="acronym">ACE</acronym>’s access mask controls whether end-users are allowed to read attributes. This letter may be specified in <acronym class="acronym">ACE</acronym>s that are part of a file-<acronym class="acronym">ACL</acronym> and those that are part of a directory-<acronym class="acronym">ACL</acronym>.

</td>

</tr>

<tr>

<td>

**<span class="term">`N`</span>**

</td>

<td>

write attributes. Specifying `N` in an <acronym class="acronym">ACE</acronym>’s access mask controls whether end-users are allowed to write attributes. This letter may be specified in <acronym class="acronym">ACE</acronym>s that are part of a file-<acronym class="acronym">ACL</acronym> and those that are part of a directory-<acronym class="acronym">ACL</acronym>.

</td>

</tr>

<tr>

<td>

**<span class="term">`x`</span>**

</td>

<td>

executing a file or entering a directory. `x` may be specified in an <acronym class="acronym">ACE</acronym> that is part of a file-<acronym class="acronym">ACL</acronym> or a directory-<acronym class="acronym">ACL</acronym>; however, the operation that is authorised will be different.

Specifying `x` in an <acronym class="acronym">ACE</acronym>s access mask that is part of a file-<acronym class="acronym">ACL</acronym> will control whether end users matching the <acronym class="acronym">ACE</acronym> Subject are allowed to execute that file.

Specifying `x` in an <acronym class="acronym">ACE</acronym>s access mask that is part of a directory-<acronym class="acronym">ACL</acronym> will control whether end users matching <acronym class="acronym">ACE</acronym> Subject are allowed to search a directory for a named file or subdirectory. This operation is needed for end users to change their current working directory.

</td>

</tr>

<tr>

<td>

**<span class="term">`d`</span>**

</td>

<td>

deleting a namespace entry. Specifying `d` in an <acronym class="acronym">ACE</acronym>’s access mask controls whether end-users are allowed to delete the file or directory the <acronym class="acronym">ACL</acronym> is attached. The end user must be also authorised for the parent directory (see `D`).

</td>

</tr>

<tr>

<td>

**<span class="term">`D`</span>**

</td>

<td>

deleting a child of a directory. Specifying `D` in the access mask of an <acronym class="acronym">ACE</acronym> that is part of a directory-<acronym class="acronym">ACL</acronym> controls whether end-users are allowed to delete items within that directory. The end user must be also authorised for the existing item (see `d`).

</td>

</tr>

<tr>

<td>

**<span class="term">`t`</span>**

</td>

<td>

reading basic attributes. Specifying `t` in the access mask of an <acronym class="acronym">ACE</acronym> controls whether end users are allowed to read basic (i.e., non-<acronym class="acronym">ACL</acronym>) attributes of that item.

</td>

</tr>

<tr>

<td>

**<span class="term">`T`</span>**

</td>

<td>

altering basic attributes. Specifying `T` in an <acronym class="acronym">ACE</acronym>’s access mask controls whether end users are allowed to alter timestamps of the item the <acronym class="acronym">ACE</acronym>’s <acronym class="acronym">ACL</acronym> is attached.

</td>

</tr>

<tr>

<td>

**<span class="term">`c`</span>**

</td>

<td>

reading <acronym class="acronym">ACL</acronym> information. Specifying `c` in an <acronym class="acronym">ACE</acronym>’s access mask controls whether end users are allowed to read the <acronym class="acronym">ACL</acronym> information of the item to which the <acronym class="acronym">ACE</acronym>’s <acronym class="acronym">ACL</acronym> is attached.

</td>

</tr>

<tr>

<td>

**<span class="term">`C`</span>**

</td>

<td>

writing <acronym class="acronym">ACL</acronym> information. Specifying `C` in an <acronym class="acronym">ACE</acronym>’s access mask controls whether end users are allowed to update <acronym class="acronym">ACL</acronym> information of the item to which the <acronym class="acronym">ACE</acronym>’s <acronym class="acronym">ACL</acronym> is attached.

</td>

</tr>

<tr>

<td>

**<span class="term">`o`</span>**

</td>

<td>

altering owner and owner-group information. Specifying `o` controls whether end users are allowed to change ownership information of the item to which the <acronym class="acronym">ACE</acronym>’s <acronym class="acronym">ACL</acronym> is attached.

</td>

</tr>

</tbody>

</table>

</div>

</div>

<div class="section" title="ACL inheritance">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cf-acl-inheritance"></a><acronym class="acronym">ACL</acronym> inheritance

</div>

</div>

</div>

To enable <acronym class="acronym">ACL</acronym> inheritance, the optional [inheritance flags](#ebnf.ace.inheritance) must be defined. The flag is a list of letters. There are three possible letters that may be included and the order doesn’t matter.

<div class="variablelist" title="ACE Inheritance Flags">

**<acronym class="acronym">ACE</acronym> Inheritance Flags**

<table border="0" summary="Inheritance Flags"><colgroup><col align="left" valign="top"></colgroup>

<tbody>

<tr>

<td>

**<span class="term">`f`</span>**

</td>

<td>

This inheritance flag only affects those <acronym class="acronym">ACE</acronym>s that form part of an directory-<acronym class="acronym">ACL</acronym>. If the <acronym class="acronym">ACE</acronym> is part of a file-<acronym class="acronym">ACL</acronym> then specifying `f` has no effect.

If a file is created in a directory with an <acronym class="acronym">ACE</acronym> with `f` in inheritance flags then the <acronym class="acronym">ACE</acronym> is copied to the newly created file’s <acronym class="acronym">ACL</acronym>. This <acronym class="acronym">ACE</acronym> copy will not have the `f` inheritance flag.

Specifying `f` in an <acronym class="acronym">ACE</acronym>’s inheritance flags does not affect whether this <acronym class="acronym">ACE</acronym> is inherited by a newly created subdirectory. See `d` for more details.

</td>

</tr>

<tr>

<td>

**<span class="term">`d`</span>**

</td>

<td>

This inheritance flag only affect those <acronym class="acronym">ACE</acronym>s that form part of an directory-<acronym class="acronym">ACL</acronym>. If the <acronym class="acronym">ACE</acronym> is part of a file-<acronym class="acronym">ACL</acronym> then specifying `d` has no effect.

Specifying `d` in an <acronym class="acronym">ACE</acronym>’s inheritance flags does not affect whether this <acronym class="acronym">ACE</acronym> is inherited by a newly created file. See `f` for more details.

If a subdirectory is created in a directory with an <acronym class="acronym">ACE</acronym> with `d` in the <acronym class="acronym">ACE</acronym>’s inheritance flag then the <acronym class="acronym">ACE</acronym> is copied to the newly created subdirectory’s <acronym class="acronym">ACL</acronym>. This <acronym class="acronym">ACE</acronym> copy will have the `d` inheritance flag specified. If the `f` inheritance flag is specified then this, too, will be copied.

</td>

</tr>

<tr>

<td>

**<span class="term">`o`</span>**

</td>

<td>

The `o` flag may only be used when the <acronym class="acronym">ACE</acronym> also has the `f`, `d` or both `f` and `d` inheritance flags.

Specifying `o` in the inheritance flag will suppress the <acronym class="acronym">ACE</acronym>. No user operations will be authorised or denied as a result of such an <acronym class="acronym">ACE</acronym>.

When a file or directory inherits from an <acronym class="acronym">ACE</acronym> with `o` in the inheritance flags then the `o` is <span class="emphasis">_not_</span> present in the newly created file or directory’s <acronym class="acronym">ACE</acronym>. Since the newly created file or directory will not have the `o` in it’s inheritance flags the <acronym class="acronym">ACE</acronym> will take effect.

An `o` in the inheritance flag allows child files or directories to inherit authorisation behaviour that is different from the parent directory.

</td>

</tr>

</tbody>

</table>

</div>

</div>

</div>

<div class="section" title="Examples">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp5402304"></a>Examples

</div>

</div>

</div>

This section gives some specific examples of how to set <acronym class="acronym">ACL</acronym>s to achieve some specific behaviour.

<div class="example"><a name="cf-acl-eg-delete"></a>

**Example 18.1\. <acronym class="acronym">ACL</acronym> allowing specific user to delete files in a directory**

<div class="example-contents">

This example demonstrates how to configure a directory-<acronym class="acronym">ACL</acronym> so user 3750 can delete any file within the directory `/pnfs/example.org/data/exampleDir`.

    (PnfsManager) admin >

The first command creates an <acronym class="acronym">ACL</acronym> for the directory. This <acronym class="acronym">ACL</acronym> has three <acronym class="acronym">ACE</acronym>s. The first <acronym class="acronym">ACE</acronym> allows anyone to list the contents of the directory. The second <acronym class="acronym">ACE</acronym> allows user 3750 to delete content within the directory in general. The third <acronym class="acronym">ACE</acronym> is inherited by all newly created files and specifies that user 3750 is authorised to delete the file independent of that file’s ownership.

The second and third commands creates an <acronym class="acronym">ACL</acronym> for files that already exists within the directory. Since <acronym class="acronym">ACL</acronym> inheritance only applies to newly created files or directories, any existing files must have an <acronym class="acronym">ACL</acronym> explicitly set.

</div>

</div>

<div class="example"><a name="idp5418400"></a>

**Example 18.2\. <acronym class="acronym">ACL</acronym> to deny a group**

<div class="example-contents">

The following example demonstrates authorising all end users to list a directory. Members of group 1000 can also create subdirectories. However, any member of group 2000 can do neither.

    (PnfsManager) admin >

The first <acronym class="acronym">ACE</acronym> denies any member of group 2000 the ability to create subdirectories or list the directory contents. As this <acronym class="acronym">ACE</acronym> is first, it takes precedence over other <acronym class="acronym">ACE</acronym>s.

The second <acronym class="acronym">ACE</acronym> allows everyone to list the directory’s content. If an end user who is a member of group 2000 attempts to list a directory then their request will match the first <acronym class="acronym">ACE</acronym> so will be denied. End users attempting to list a directory that are not a member of group 2000 will not match the first <acronym class="acronym">ACE</acronym> but will match the second <acronym class="acronym">ACE</acronym> and will be authorised.

The final <acronym class="acronym">ACE</acronym> authorises members of group 1000 to create subdirectories. If an end user who is a member of group 1000 and group 2000 attempts to create a subdirectory then their request will match the first <acronym class="acronym">ACE</acronym> and be denied.

</div>

</div>

<div class="example"><a name="idp5428016"></a>

**Example 18.3\. <acronym class="acronym">ACL</acronym> to allow a user to delete all files and subdirectories**

<div class="example-contents">

This example is an extension to [Example 18.1, “<acronym class="acronym">ACL</acronym> allowing specific user to delete files in a directory”](#cf-acl-eg-delete "Example 18.1\. ACL allowing specific user to delete files in a directory"). The previous example allowed deletion of the contents of a directory but not the contents of any subdirectories. This example allows user 3750 to delete all files and subdirectories within the directory.

    (PnfsManager) admin >

The first <acronym class="acronym">ACE</acronym> is `USER:3750:+D:d`. This authorises user 3750 to delete any contents of directory `/pnfs/example.org/data/exampleDir` that has an <acronym class="acronym">ACL</acronym> authorising them with `d` operation.

The first <acronym class="acronym">ACE</acronym> also contains the inheritance flag `d` so newly created subdirectories will inherit this <acronym class="acronym">ACE</acronym>. Since the inherited <acronym class="acronym">ACE</acronym> will also contain the `d` inheritance flag, this <acronym class="acronym">ACE</acronym> will be copied to all subdirectories when they are created.

The second <acronym class="acronym">ACE</acronym> is `USER:3750:+d:odf`. The <acronym class="acronym">ACE</acronym> authorises user 3750 to delete whichever item the <acronym class="acronym">ACL</acronym> containing this <acronym class="acronym">ACE</acronym> is associated with. However, since the <acronym class="acronym">ACE</acronym> contains the `o` in the inheritance flags, user 3750 is <span class="emphasis">_not_</span> authorised to delete the directory `/pnfs/example.org/data/exampleDir`

Since the second <acronym class="acronym">ACE</acronym> has both the `d` and `f` inheritance flags, it will be inherited by all files and subdirectories of `/pnfs/example.org/data/exampleDir`, but without the `o` flag. This authorises user 3750 to delete these items.

Subdirectories (and files) will inherit the second <acronym class="acronym">ACE</acronym> with both `d` and `f` inheritance flags. This implies that all files and sub-subdirecties within a subdirectory of `/pnfs/example.org/data/exampleDir` will also inherit this <acronym class="acronym">ACE</acronym>, so will also be deletable by user 3750.

</div>

</div>

</div>

</div>

<div class="section" title="Viewing configured ACLs">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cf-acl-view"></a>Viewing configured <acronym class="acronym">ACL</acronym>s

</div>

</div>

</div>

The <span class="command">**getfacl**</span> is used to obtain the current <acronym class="acronym">ACL</acronym> for some item in <span class="productname">dCache</span> namespace. It takes the following arguments.

<div class="cmdsynopsis">

`getfacl` [_<tt><pnfsId></tt>_] | [_<tt><globalPath></tt>_]

</div>

The <span class="command">**getfacl**</span> command fetches the <acronym class="acronym">ACL</acronym> information of a namespace item (a file or directory). The item may be specified by its <span class="productname">`pnfs`</span>-ID or its absolute path.

<div class="example"><a name="idp5465040"></a>

**Example 18.4\. Obtain <acronym class="acronym">ACL</acronym> information by absolute path**

<div class="example-contents">

    (PnfsManager) admin >

</div>

</div>

The information is provided twice. The first part gives detailed information about the <acronym class="acronym">ACL</acronym>. The second part, after the `In extra format:` heading, provides a list of <acronym class="acronym">ACE</acronym>s that may be used when updating the <acronym class="acronym">ACL</acronym> using the <span class="command">**setfacl**</span> command.

</div>

</div>

</div>

<div class="chapter" title="Chapter 19\. GLUE Info Provider">

<div class="titlepage">

<div>

<div>

## <a name="cf-glue"></a>Chapter 19\. <acronym class="acronym">GLUE</acronym> Info Provider

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Internal collection of information](#cf-glue-info)</span></dt>

<dt><span class="section">[Configuring the info provider](#cf-glue-cf-info-provider)</span></dt>

<dt><span class="section">[Testing the info provider](#cf-glue-testing-info-provider)</span></dt>

<dt><span class="section">[Decommissioning the old info provider](#cf-glue-decommission)</span></dt>

<dt><span class="section">[Publishing <span class="productname">dCache</span> information](#cf-glue-publishing)</span></dt>

<dt><span class="section">[Troubleshooting <acronym class="acronym">BDII</acronym> problems](#cf-glue-troubleshooting)</span></dt>

<dt><span class="section">[Updating information](#cf-glue-updating)</span></dt>

</dl>

</div>

The GLUE information provider supplied with <span class="productname">dCache</span> provides the information about the <span class="productname">dCache</span> instance in a standard format called <acronym class="acronym">GLUE</acronym>. This is necessary so that <acronym class="acronym">WLCG</acronym> infrastructure (such as FTS) and clients using <acronym class="acronym">WLCG</acronym> tools can discover the <span class="productname">dCache</span> instance and use it correctly.

The process of configuring the info-provider is designed to have the minimum overhead so you can configure it manually; however, you may prefer to use an automatic configuration tool, such as <abbr class="abbrev">YAIM</abbr>.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Be sure you have at least v2.0.8 of glue-schema RPM installed on the node running the info-provider.</div>

This chapter describes how to enable and test the <span class="productname">dCache</span>-internal collection of information needed by the info-provider. It also describes how to configure the info-provider and verify that it is working correctly. Finally, it describes how to publish this information within <acronym class="acronym">BDII</acronym>, verify that this is working and troubleshoot any problems.

<div class="warning" title="Warning" style="margin-left: 0.5in; margin-right: 0.5in;">

### Warning

Please be aware that changing information provider may result in a brief interruption to published information. This may have an adverse affect on client software that make use of this information.

</div>

<div class="section" title="Internal collection of information">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-glue-info"></a>Internal collection of information

</div>

</div>

</div>

The info-provider takes as much information as possible from <span class="productname">dCache</span>. To achieve this, it needs the internal information-collecting service, `info`, to be running and a means to collect that information: `httpd`. Make sure that both the `httpd` and `info` services are running within your <span class="productname">dCache</span> instance. By default, the `info` service is started on the admin-node; but it is possible to configure <span class="productname">dCache</span> so it runs on a different node. You should run only one `info` service per <span class="productname">dCache</span> instance.

The traditional (pre-1.9.7) allocation of services to domains has the `info` cell running in the `infoDomain` domain. A <span class="productname">dCache</span> system that has been migrated from this old configuration will have the following fragment in the node’s layout file:

<pre class="programlisting">[infoDomain]
[infoDomain/info]</pre>

It is also possible to run the `info` service inside a domain that runs other services. The following example show the `information` domain that hosts the `admin`, `httpd`, `topo` and `info` services.

<pre class="programlisting">[information]
[information/admin]
[information/httpd]
[information/topo]
[information/info]</pre>

For more information on configuring <span class="productname">dCache</span> layout files, see [the section called “Defining domains and services”](#in-install-layout "Defining domains and services").

Use the <span class="command">**dcache services**</span> command to see if a particular node is configured to run the `info` service. The following shows the output if the node has an `information` domain that is configured to run the `info` cell.

    [root] #

If a node has no domain configured to host the `info` service then the above <span class="command">**dcache services**</span> command will give no output:

    [root] #

If no running domain within <span class="emphasis">_any_</span> node of your <span class="productname">dCache</span> instance is running the `info` service then you must add the service to a domain and restart that domain.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

In this example, the `info` service is added to the `example` domain. Note that the specific choice of domain (`example`) is just to give a concrete example; the same process may be applied to a different domain.

The layouts file for this node includes the following definition for the `example` domain:

<pre class="programlisting">[example]
[example/admin]
[example/httpd]
[example/topo]</pre>

By adding the extra line `[example/info]` to the layouts file, in future, the `example` domain will host the `info` service.

<pre class="programlisting">[example]
[example/admin]
[example/httpd]
[example/topo]
[example/info]</pre>

To actually start the `info` cell, the `example` domain must be restarted.

    [root] #

With the `example` domain restarted, the `info` service is now running.

</div>

</div>

You can also verify both the `httpd` and `info` services are running using the <span class="command">**wget**</span> command. The specific command assumes that you are logged into the node that has the `httpd` service (by default, the admin node). You may run the command on any node by replacing `localhost` with the hostname of the node running the `httpd` service.

The following example shows the output from the <span class="command">**wget**</span> when the `info` service is running correctly:

    [root] #

If the `httpd` service isn’t running then the command will generate the following output:

    [root] #

To fix the problem, ensure that the `httpd` service is running within your <span class="productname">dCache</span> instance. This is the service that provides the web server monitoring within <span class="productname">dCache</span>. To enable the service, follow the same procedure for enabling the `info` cell, but add the `httpd` service within one of the domains in <span class="productname">dCache</span>.

If running the <span class="command">**wget**</span> command gives an error message with `Unable to contact the info cell. Please ensure the info cell is running`:

    [root] #

This means that the `info` service is not running. Follow the instructions for starting the `info` service given above.

</div>

<div class="section" title="Configuring the info provider">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-glue-cf-info-provider"></a>Configuring the info provider

</div>

</div>

</div>

In the directory `<span>/etc/dcache</span>` you will find the file `info-provider.xml`. This file is where you configure the info-provider. It provides information that is difficult or impossible to obtain from the running <span class="productname">dCache</span> directly.

You must edit the `info-provider.xml` to customise its content to match your <span class="productname">dCache</span> instance. In some places, the file contains place-holder values. These place-holder values must be changed to the correct values for your <span class="productname">dCache</span> instance.

<div class="important" title="Careful with < and &amp; charaters" style="margin-left: 0.5in; margin-right: 0.5in;">

### Careful with < and & charaters

Take care when editing the `info-provider.xml` file! After changing the contents, the file must remain valid, well-formed <abbr class="abbrev">XML</abbr>. In particular, be very careful when writing a less-than symbol (`<`) or an ampersand symbol (`&`).

<div class="itemizedlist">

*   Only use an ampersand symbol (`&`) if it is part of an entity reference. An entity reference is a sequence that starts with an ampersand symbol and is terminated with a semi-colon (`;`), for example `&gt;` and `&apos;` are entity markups.

    If you want to include an ampersand character in the text then you must use the `&amp;` entity; for example, to include the text <span class="quote">“<span class="quote">me & you</span>”</span> the <abbr class="abbrev">XML</abbr> file would include `me &amp; you`.

*   Only use a less-than symbol (`<`) when starting an <abbr class="abbrev">XML</abbr> element; for example, `<constant id="TEST">A test value</constant>`.

    If you want to include a less-than character in the text then you must use the `&lt;` entity; for example, to include the text <span class="quote">“<span class="quote">1 < 2</span>”</span> the <abbr class="abbrev">XML</abbr> file would include `1 &lt; 2`.

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

The following example shows the `SE-NAME` constant (which provides a human-readable description of the <span class="productname">dCache</span> instance) from a well-formed `info-provider.xml` configuration file:

<pre class="programlisting"><constant id="SE-NAME">Simple &amp; small dCache instance for small VOs
(typically &lt; 20 users)</constant></pre>

The `SE-NAME` constant is configured to have the value <span class="quote">“<span class="quote">Simple & small dCache instance for small VOs (typically < 20 users)</span>”</span>. This illustrates how to include ampersand and less-than characters in an <abbr class="abbrev">XML</abbr> file.

</div>

</div>

</div>

When editing the `info-provider.xml` file, you should <span class="emphasis">_only_</span> edit text between two elements or add more elements (for lists and mappings). You should <span class="emphasis">_never_</span> alter the text inside double-quote marks.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

This example shows how to edit the `SITE-UNIQUE-ID` constant. This constant has a default value `EXAMPLESITE-ID`, which is a place-holder value and must be edited.

<pre class="programlisting"><constant id="SITE-UNIQUE-ID">EXAMPLESITE-ID</constant></pre>

To edit the constant’s value, you must change the text between the start- and end-element tags: `EXAMPLESITE-ID`. You <span class="emphasis">_should not_</span> edit the text `SITE-UNIQUE-ID` as it is in double-quote marks. After editing, the file may read:

<pre class="programlisting"><constant id="SITE-UNIQUE-ID">DESY-HH</constant></pre>

</div>

</div>

The `info-provider.xml` contains detailed descriptions of all the properties that are editable. You should refer to this documentation when editing the `info-provider.xml`.

</div>

<div class="section" title="Testing the info provider">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-glue-testing-info-provider"></a>Testing the info provider

</div>

</div>

</div>

Once you have configured `info-provider.xml` to reflect your site’s configuration, you may test that the info provider produces meaningful results.

Running the info-provider script should produce <acronym class="acronym">GLUE</acronym> information in <acronym class="acronym">LDIF</acronym> format; for example:

    [root] #

The actual values you see will be site-specific and depend on the contents of the `info-provider.xml` file and your <span class="productname">dCache</span> configuration.

To verify that there are no problems, redirect standard-out to `/dev/null` to show only the error messages:

    [root] #

If you see error messages (which may be repeated several times) of the form:

    [root] #

then it is likely that either the `httpd` or `info` service has not been started. Use the above <span class="command">**wget**</span> test to check that both services are running. You can also see which services are available by running the <span class="command">**dcache services**</span> and <span class="command">**dcache status**</span> commands.

</div>

<div class="section" title="Decommissioning the old info provider">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-glue-decommission"></a>Decommissioning the old info provider

</div>

</div>

</div>

Sites that were using the old (pre-1.9.5) info provider should ensure that there are no remnants of this old info-provider on their machine. Although the old info-provider has been removed from <span class="productname">dCache</span>, it relied on static <acronym class="acronym">LDIF</acronym> files, which might still exist. If so, then <acronym class="acronym">BDII</acronym> will obtain some information from the current info-provider and some out-of-date information from the static <acronym class="acronym">LDIF</acronym> files. <acronym class="acronym">BDII</acronym> will then attempt to merge the two sources of information. The merged information may provide a confusing description of your <span class="productname">dCache</span> instance, which may prevent clients from working correctly.

The old info provider had two static <acronym class="acronym">LDIF</acronym> files and a symbolic link for <acronym class="acronym">BDII</acronym>. These are:

<div class="itemizedlist">

*   The file `lcg-info-static-SE.ldif`,

*   The file: `lcg-info-static-dSE.ldif`,

*   The symbolic link `/opt/glite/etc/gip/plugin`, which points to `/opt/d-cache/jobs/infoDynamicSE-plugin-dcache`.

</div>

The two files (`lcg-info-static-SE.ldif` and `lcg-info-static-dSE.ldif`) appear in the `/opt/lcg/var/gip/ldif` directory; however, it is possible to alter the location <acronym class="acronym">BDII</acronym> will use. In <acronym class="acronym">BDII</acronym> v4, the directory is controlled by the `static_dir` variable (see `/opt/glite/etc/gip/glite-info-generic.conf` or `/opt/lcg/etc/lcg-info-generic.conf`). For <acronym class="acronym">BDII</acronym> v5, the `BDII_LDIF_DIR` variable (defined in `/opt/bdii/etc/bdii.conf`) controls this behaviour.

You must delete the above three entries: `lcg-info-static-SE.ldif`, `lcg-info-static-dSE.ldif` and the `plugin` symbolic link.

The directory with the static <acronym class="acronym">LDIF</acronym>, `/opt/lcg/var/gip/ldif` or `/opt/glite/etc/gip/ldif` by default, may contain other static <acronym class="acronym">LDIF</acronym> entries that are relics of previous info-providers. These may have filenames like `static-file-SE.ldif`.

Delete any static <acronym class="acronym">LDIF</acronym> file that contain information about <span class="productname">dCache</span>. With the info-provider, all <acronym class="acronym">LDIF</acronym> information comes from the info-provider; there should be no static <acronym class="acronym">LDIF</acronym> files. Be careful not to delete any static <acronym class="acronym">LDIF</acronym> files that come as part of <acronym class="acronym">BDII</acronym>; for example, the `default.ldif` file, if present.

</div>

<div class="section" title="Publishing dCache information">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-glue-publishing"></a>Publishing <span class="productname">dCache</span> information

</div>

</div>

</div>

<acronym class="acronym">BDII</acronym> obtains information by querying different sources. One such source of information is by running an info-provider command and taking the resulting <acronym class="acronym">LDIF</acronym> output. To allow <acronym class="acronym">BDII</acronym> to obtain <span class="productname">dCache</span> information, you must allow <acronym class="acronym">BDII</acronym> to run the <span class="productname">dCache</span> info-provider. This is achieved by symbolically linking the `<span>dcache-info-provider</span>` script into the <acronym class="acronym">BDII</acronym> plugins directory:

    [root] #

If the <acronym class="acronym">BDII</acronym> daemons are running, then you will see the information appear in <acronym class="acronym">BDII</acronym> after a short delay; by default this is (at most) 60 seconds.

You can verify that information is present in <acronym class="acronym">BDII</acronym> by querying <acronym class="acronym">BDII</acronym> using the <span class="command">**ldapsearch**</span> command. Here is an example that queries for <acronym class="acronym">GLUE</acronym> v1.3 objects:

    [root] #

<div class="note" title="Careful with the hostname" style="margin-left: 0.5in; margin-right: 0.5in;">

### Careful with the hostname

You must replace `_<tt><dcache-host></tt>_` in the <acronym class="acronym">URI</acronym> `ldap://_<tt><dcache-host></tt>_:2170/` with the actual hostname of your node.

It’s tempting to use `localhost` in the <acronym class="acronym">URI</acronym> when executing the <span class="command">**ldapsearch**</span> command; however, <acronym class="acronym">BDII</acronym> binds to the ethernet device (e.g., <span class="hardware">eth0</span>). Typically, `localhost` is associated with the loopback device (<span class="hardware">lo</span>), so querying <acronym class="acronym">BDII</acronym> with the <acronym class="acronym">URI</acronym> `ldap://localhost:2170/` will fail.

</div>

The <acronym class="acronym">LDAP</acronym> query uses the `o=grid` object as the base; all reported objects are descendant objects of this base object. The `o=grid` base selects only the <acronym class="acronym">GLUE</acronym> v1.3 objects. To see <acronym class="acronym">GLUE</acronym> v2.0 objects, the base object must be `o=glue`.

The above <span class="command">**ldapsearch**</span> command queries <acronym class="acronym">BDII</acronym> using the `(objectClass=GlueSE)` filter. This filter selects only objects that provide the highest-level summary information about a storage-element. Since each storage-element has only one such object and this <acronym class="acronym">BDII</acronym> instance only describes a single <span class="productname">dCache</span> instance, the command returns only the single <acronym class="acronym">LDAP</acronym> object.

To see all <acronym class="acronym">GLUE</acronym> v1.3 objects in <acronym class="acronym">BDII</acronym>, repeat the above <span class="command">**ldapsearch**</span> command but omit the `(objectClass=GlueSE)` filter: **`ldapsearch -LLL -x -H ldap://_<tt><dcache-host></tt>_:2170 -b o=grid`**. This command will output all <acronym class="acronym">GLUE</acronym> v1.3 <acronym class="acronym">LDAP</acronym> objects, which includes all the <acronym class="acronym">GLUE</acronym> v1.3 objects from the info-provider.

Searching for all <acronym class="acronym">GLUE</acronym> v2.0 objects in <acronym class="acronym">BDII</acronym> is achieved by repeating the above <span class="command">**ldapsearch**</span> command but omitting the `(objectClass=GlueSE)` filter and changing the search base to `o=glue`: **`ldapsearch -LLL -x -H ldap://_<tt><dcache-host></tt>_:2170 -b o=glue`**. This command returns a completely different set of objects from the <acronym class="acronym">GLUE</acronym> v1.3 queries.

You should be able to compare this output with the output from running the info-provider script manually: <acronym class="acronym">BDII</acronym> should contain all the objects that the <span class="productname">dCache</span> info-provider is supplying. Unfortunately, the order in which the objects are returned and the order of an object’s properties is not guaranteed; therefore a direct comparison of the output isn’t possible. However, it is possible to calculate the number of objects in <acronym class="acronym">GLUE</acronym> v1.3 and <acronym class="acronym">GLUE</acronym> v2.0.

First, calculate the number of <acronym class="acronym">GLUE</acronym> v1.3 objects in <acronym class="acronym">BDII</acronym> and compare that to the number of <acronym class="acronym">GLUE</acronym> v1.3 objects that the info-provider supplies.

    [root] #

Now calculate the number of <acronym class="acronym">GLUE</acronym> v2.0 objects in <acronym class="acronym">BDII</acronym> describing your <span class="productname">dCache</span> instance and compare that to the number provided by the info-provider:

    [root] #

If there is a discrepancy in the pair of numbers obtains in the above commands then <acronym class="acronym">BDII</acronym> has rejecting some of the objects. This is likely due to malformed <acronym class="acronym">LDAP</acronym> objects from the info-provider.

</div>

<div class="section" title="Troubleshooting BDII problems">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-glue-troubleshooting"></a>Troubleshooting <acronym class="acronym">BDII</acronym> problems

</div>

</div>

</div>

The <acronym class="acronym">BDII</acronym> log file should explain why objects are not accepted; for example, due to a badly formatted attribute. The default location of the log file is `/var/log/bdii/bdii-update.log`, but the location is configured by the `BDII_LOG_FILE` option in the `/opt/bdii/etc/bdii.conf` file.

The <acronym class="acronym">BDII</acronym> log files may show entries like:

<pre class="programlisting">2011-05-11 04:04:58,711: [WARNING] dn: o=shadow
2011-05-11 04:04:58,711: [WARNING] ldapadd: Invalid syntax (21)
2011-05-11 04:04:58,711: [WARNING] additional info: objectclass: value #1 invalid per syntax</pre>

This problem comes when <acronym class="acronym">BDII</acronym> is attempting to inject new information. Unfortunately, the information isn’t detailed enough for further investigation. To obtain more detailed information from <acronym class="acronym">BDII</acronym>, switch the `BDII_LOG_LEVEL` option in `/opt/bdii/etc/bdii.conf` to `DEBUG`. This will provide more information in the <acronym class="acronym">BDII</acronym> log file.

Logging at `DEBUG` level has another effect; <acronym class="acronym">BDII</acronym> no longer deletes some temporary files. These temporary files are located in the directory controlled by the `BDII_VAR_DIR` option. This is `/var/run/bdii` by default.

There are several temporary files located in the `/var/run/bdii` directory. When <acronym class="acronym">BDII</acronym> decides which objects to add, modify and remove, it creates <acronym class="acronym">LDIF</acronym> instructions inside temporary files `add.ldif`, `modify.ldif` and `delete.ldif` respectively. Any problems in the attempt to add, modify and delete <acronym class="acronym">LDAP</acronym> objects are logged to corresponding error files: errors with `add.ldif` are logged to `add.err`, `modify.ldif` to `modify.err` and so on.

Once information in <acronym class="acronym">BDII</acronym> has stablised, the only new, incoming objects for <acronym class="acronym">BDII</acronym> come from those objects that it was unable to add previously. This means that `add.ldif` will contain these badly formatted objects and `add.err` will contain the corresponding errors.

</div>

<div class="section" title="Updating information">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-glue-updating"></a>Updating information

</div>

</div>

</div>

The information contained within the `info` service may take a short time to achieve a complete overview of <span class="productname">dCache</span>’s state. For certain gathered information it may take a few minutes before the information stabilises. This delay is intentional and prevents the gathering of information from adversely affecting <span class="productname">dCache</span>’s performance.

The information presented by the <acronym class="acronym">LDAP</acronym> server is updated periodically by <acronym class="acronym">BDII</acronym> requesting fresh information from the info-provider. The info-provider obtains this information by requesting <span class="productname">dCache</span>’s current status from `info` service. By default, <acronym class="acronym">BDII</acronym> will query the info-provider every 60 seconds. This will introduce an additional delay between a change in <span class="productname">dCache</span>’s state and that information propagating.

Some information is hard-coded within the `info-provider.xml` file; that is, you will need to edit this file before the published value(s) will change. These values are ones that typically a site-admin must choose independently of <span class="productname">dCache</span>’s current operations.

</div>

</div>

<div class="chapter" title="Chapter 20\.  Stage Protection">

<div class="titlepage">

<div>

<div>

## <a name="cf-stage-protection"></a>Chapter 20\. Stage Protection

</div>

<div>

<div class="author">

### <span class="firstname">Irina</span> <span class="surname">Kozlova</span>

</div>

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Configuration of Stage Protection](#cf-stage-protection-configuration)</span></dt>

<dt><span class="section">[Definition of the White List](#cf-stage-protection-whiteList)</span></dt>

</dl>

</div>

A <span class="productname">dCache</span> system administrator may specify a list of <acronym class="acronym">DN</acronym>s/<acronym class="acronym">FQAN</acronym>s which are allowed to trigger tape restores for files not being available on disk. Users, requesting tape-only files, and not being on that _white list_, will receive a permission error and no tape operation is launched. Stage protection can be enhanced to allow authorization specific to a <span class="productname">dCache</span> storage group. The additional configuration parameter is optional allowing the stage protection to be backwards compatible when stage authorization is not specific to a storage group.

<div class="section" title="Configuration of Stage Protection">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-stage-protection-configuration"></a>Configuration of Stage Protection

</div>

</div>

</div>

Stage protection can optionally be configured in the `poolmanager` rather than on the doors and the `pinmanager`. Thus the white list needs to be present on a single node only. To enable this, define the following parameter in `<span>/etc/dcache</span>/dcache.conf`:

<pre class="programlisting">dcache.authz.staging.pep=PoolManager</pre>

The file name of the white list must be configured by setting the `dcache.authz.staging` parameter in `<span>/etc/dcache</span>/dcache.conf`:

<pre class="programlisting">dcache.authz.staging=<span>/etc/dcache</span>/StageConfiguration.conf</pre>

The parameter needs to be defined on all nodes which enforce the stage protection, i.e., either on the doors and the `pinmanager`, or in the `poolmanager` depending on the stage policy enforcement point.

</div>

<div class="section" title="Definition of the White List">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cf-stage-protection-whiteList"></a>Definition of the White List

</div>

</div>

</div>

The Stage Configuration File will contain a white list. Each line of the white list may contain up to three regular expressions enclosed in double quotes. The regular expressions match the <acronym class="acronym">DN</acronym>, <acronym class="acronym">FQAN</acronym>, and the Storage Group written in the following format:

<div class="cmdsynopsis">

"_<tt><DN></tt>_" ["_<tt><FQAN></tt>_" ["_<tt><StorageGroup></tt>_"] ]

</div>

Lines starting with a hash symbol `#` are discarded as comments.

The regular expression syntax follows the syntax defined for the [Java Pattern class](http://java.sun.com/javase/6/docs/api/java/util/regex/Pattern.html) .

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Here are some examples of the White List Records:

<pre class="programlisting">".*" "/atlas/Role=production"
"/C=DE/O=DESY/CN=Kermit the frog"
"/C=DE/O=DESY/CN=Beaker" "/desy"
"/O=GermanGrid/.*" "/desy/Role=.*"</pre>

This example authorizes a number of different groups of users:

<div class="itemizedlist">

*   Any user with the <span><acronym class="acronym">FQAN</acronym> `/atlas/Role=production`</span>.
*   The user with the <span><acronym class="acronym">DN</acronym> `/C=DE/O=DESY/CN=Kermit the frog`</span>, irrespective of which VOMS groups he belongs to.
*   The user with the <span><acronym class="acronym">DN</acronym> `/C=DE/O=DESY/CN=Beaker`</span> but only if he is also identified as a member of VO `desy` (<span><acronym class="acronym">FQAN</acronym> `/desy`</span>)
*   Any user with <acronym class="acronym">DN</acronym> and <acronym class="acronym">FQAN</acronym> that match `/O=GermanGrid/.*` and `/desy/Role=.*` respectively.

</div>

</div>

</div>

If a storage group is specified all three parameters must be provided. The regular expression `".*"` may be used to authorize any <acronym class="acronym">DN</acronym> or any <acronym class="acronym">FQAN</acronym>. Consider the following example:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

<pre class="programlisting">".*" "/atlas/Role=production" "h1:raw@osm"
"/C=DE/O=DESY/CN=Scooter" ".*" "sql:chimera@osm"</pre>

In the example above:

<div class="itemizedlist">

*   Any user with <span><acronym class="acronym">FQAN</acronym> `/atlas/Role=production`</span> is allowed to stage files located in the storage group `h1:raw@osm`.
*   The user `/C=DE/O=DESY/CN=Scooter`, irrespective of which VOMS groups he belongs to, is allowed to stage files located in the storage group `sql:chimera@osm`.

</div>

</div>

</div>

With the plain `dCap` protocol the <acronym class="acronym">DN</acronym> and <acronym class="acronym">FQAN</acronym> are not known for any users.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

In order to allow all `dCap` users to stage files the white list should contain the following record:

<pre class="programlisting">"" ""</pre>

In case this line is commented or not present in the white list, all `dCap` users will be disallowed to stage files.

</div>

</div>

It is possible to allow all `dCap` users to stage files located in a certain storage group.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

In this example, all `dCap` users are allowed to stage files located in the storage group `h1:raw@osm`:

<pre class="programlisting">"" "" "h1:raw@osm"</pre>

</div>

</div>

</div>

</div>

</div>

<div class="part" title="Part III. Cookbook">

<div class="titlepage">

<div>

<div>

# <a name="cb"></a>Part III. Cookbook

</div>

</div>

</div>

<div class="partintro" title="Cookbook">

This part contains guides for specific tasks a system administrator might want to perform.

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="chapter">[21\. <span class="productname">dCache</span> Clients.](#cb-clients)</span></dt>

<dd>

<dl>

<dt><span class="section">[`GSI-FTP`](#cb-clients-gridftp)</span></dt>

<dd>

<dl>

<dt><span class="section">[Listing a directory](#cb-clients-gridftp-ls)</span></dt>

<dt><span class="section">[Checking a file exists](#cb-clients-gridftp-exists)</span></dt>

<dt><span class="section">[Deleting files](#cb-clients-gridftp-rm)</span></dt>

<dt><span class="section">[Copying files](#cb-clients-gridftp-cp)</span></dt>

</dl>

</dd>

<dt><span class="section">[`dCap`](#cb-clients-dcap)</span></dt>

<dd>

<dl>

<dt><span class="section">[<span class="command">**dccp**</span>](#cb-clients-dcap-dcc)</span></dt>

<dt><span class="section">[Using the <span class="productname">dCache</span> client interposition library.](#cb-clients-dcap-interposition)</span></dt>

</dl>

</dd>

<dt><span class="section">[`SRM`](#cb-clients-srm)</span></dt>

<dd>

<dl>

<dt><span class="section">[Creating a new directory.](#cb-clients-srm-mkdir)</span></dt>

<dt><span class="section">[Removing files from <span class="productname">dCache</span>](#cb-clients-srm-rm)</span></dt>

<dt><span class="section">[Removing empty directories from <span class="productname">dCache</span>](#cb-clients-srm-rmdir)</span></dt>

<dt><span class="section">[srmcp for `SRM` v1](#cb-clients-srm-1-cp)</span></dt>

<dt><span class="section">[srmcp for `SRM` v2.2](#cb-clients-srm-2)</span></dt>

</dl>

</dd>

<dt><span class="section">[ldap](#cb-clients-ldap)</span></dt>

<dt><span class="section">[Using the <acronym class="acronym">LCG</acronym> commands with <span class="productname">dCache</span>](#cb-clients-lcg)</span></dt>

<dd>

<dl>

<dt><span class="section">[The <span class="command">**lcg-gt**</span> Application](#cb-clients-lcg-gt)</span></dt>

<dt><span class="section">[The <span class="command">**lcg-sd**</span> Application](#cb-clients-lcg-sd)</span></dt>

</dl>

</dd>

</dl>

</dd>

<dt><span class="chapter">[22\. Pool Operations](#cb-pool)</span></dt>

<dd>

<dl>

<dt><span class="section">[Checksums](#cb-pool-checksumming)</span></dt>

<dd>

<dl>

<dt><span class="section">[How to configure checksum calculation](#cb-pool-checksumming-config)</span></dt>

</dl>

</dd>

<dt><span class="section">[Migration Module](#cb-pool-migration)</span></dt>

<dd>

<dl>

<dt><span class="section">[Overview and Terminology](#idp6194560)</span></dt>

<dt><span class="section">[Command Summary](#idp6207104)</span></dt>

<dt><span class="section">[Examples](#idp6286544)</span></dt>

</dl>

</dd>

<dt><span class="section">[Renaming a Pool](#cb-pool-rename)</span></dt>

<dt><span class="section">[Pinning Files to a Pool](#cb-pool-pin)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[23\. <span class="productname">PostgreSQL</span> and <span class="productname">dCache</span>](#cb-postgres)</span></dt>

<dd>

<dl>

<dt><span class="section">[Installing a <span class="productname">PostgreSQL</span> Server](#cb-postgres-install)</span></dt>

<dt><span class="section">[Configuring Access to <span class="productname">PostgreSQL</span>](#cb-postgres-configure)</span></dt>

<dt><span class="section">[Performance of the <span class="productname">PostgreSQL</span> Server](#cb-postgres-perf)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[24\. Complex Network Configuration](#cb-net)</span></dt>

<dd>

<dl>

<dt><span class="section">[Firewall Configuration](#cb-net-firewall)</span></dt>

<dd>

<dl>

<dt><span class="section">[Basic Installation](#idp6488512)</span></dt>

<dt><span class="section">[Multi-Node with Firewalls](#idp6499952)</span></dt>

</dl>

</dd>

<dt><span class="section">[`GridFTP` Connections via two or more Network Interfaces](#cb-net-second-if)</span></dt>

<dt><span class="section">[`GridFTP` with Pools in a Private Subnet](#cb-net-pool-priv)</span></dt>

</dl>

</dd>

<dt><span class="chapter">[25\. Advanced Tuning](#cb-tuning)</span></dt>

<dd>

<dl>

<dt><span class="section">[Multiple Queues for Movers in each Pool](#cb-adv-multi-mover-queues)</span></dt>

<dd>

<dl>

<dt><span class="section">[Description](#cb-adv-multi-mover-queues-d)</span></dt>

<dt><span class="section">[Solution](#cb-adv-multi-mover-queues-s)</span></dt>

<dt><span class="section">[Configuration](#cb-adv-multi-mover-queues-c)</span></dt>

<dt><span class="section">[Tunable Properties for Multiple Queues](#cb-adv-multi-mover-queues-t)</span></dt>

</dl>

</dd>

<dt><span class="section">[Tunable Properties](#cb-tuning-parameters)</span></dt>

<dd>

<dl>

<dt><span class="section">[`dCap`](#cb-tuning-parameters-dcap)</span></dt>

<dt><span class="section">[`GridFTP`](#cb-tuning-parameters-gsiftp)</span></dt>

<dt><span class="section">[`SRM`](#cb-tuning-parameters-srm)</span></dt>

</dl>

</dd>

</dl>

</dd>

</dl>

</div>

</div>

<div class="chapter" title="Chapter 21\. dCache Clients.">

<div class="titlepage">

<div>

<div>

## <a name="cb-clients"></a>Chapter 21\. <span class="productname">dCache</span> Clients.

</div>

<div>

<div class="authorgroup">

<div class="author">

### <span class="firstname">Owen</span> <span class="surname">Synge</span>

</div>

</div>

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[`GSI-FTP`](#cb-clients-gridftp)</span></dt>

<dd>

<dl>

<dt><span class="section">[Listing a directory](#cb-clients-gridftp-ls)</span></dt>

<dt><span class="section">[Checking a file exists](#cb-clients-gridftp-exists)</span></dt>

<dt><span class="section">[Deleting files](#cb-clients-gridftp-rm)</span></dt>

<dt><span class="section">[Copying files](#cb-clients-gridftp-cp)</span></dt>

</dl>

</dd>

<dt><span class="section">[`dCap`](#cb-clients-dcap)</span></dt>

<dd>

<dl>

<dt><span class="section">[<span class="command">**dccp**</span>](#cb-clients-dcap-dcc)</span></dt>

<dt><span class="section">[Using the <span class="productname">dCache</span> client interposition library.](#cb-clients-dcap-interposition)</span></dt>

</dl>

</dd>

<dt><span class="section">[`SRM`](#cb-clients-srm)</span></dt>

<dd>

<dl>

<dt><span class="section">[Creating a new directory.](#cb-clients-srm-mkdir)</span></dt>

<dt><span class="section">[Removing files from <span class="productname">dCache</span>](#cb-clients-srm-rm)</span></dt>

<dt><span class="section">[Removing empty directories from <span class="productname">dCache</span>](#cb-clients-srm-rmdir)</span></dt>

<dt><span class="section">[srmcp for `SRM` v1](#cb-clients-srm-1-cp)</span></dt>

<dt><span class="section">[srmcp for `SRM` v2.2](#cb-clients-srm-2)</span></dt>

</dl>

</dd>

<dt><span class="section">[ldap](#cb-clients-ldap)</span></dt>

<dt><span class="section">[Using the <acronym class="acronym">LCG</acronym> commands with <span class="productname">dCache</span>](#cb-clients-lcg)</span></dt>

<dd>

<dl>

<dt><span class="section">[The <span class="command">**lcg-gt**</span> Application](#cb-clients-lcg-gt)</span></dt>

<dt><span class="section">[The <span class="command">**lcg-sd**</span> Application](#cb-clients-lcg-sd)</span></dt>

</dl>

</dd>

</dl>

</div>

There are many client tools for <span class="productname">dCache</span>. These can most easily be classified by communication protocol.

<div class="section" title="GSI-FTP">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-clients-gridftp"></a>`GSI-FTP`

</div>

</div>

</div>

<span class="productname">dCache</span> provides a `GSI-FTP` door, which is in effect a `GSI` authenticated `FTP` access point to <span class="productname">dCache</span>

<div class="section" title="Listing a directory">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-gridftp-ls"></a>Listing a directory

</div>

</div>

</div>

To list the content of a <span class="productname">dCache</span> directory, the `GSI-FTP` protocol can be used;

    [user] $

</div>

<div class="section" title="Checking a file exists">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-gridftp-exists"></a>Checking a file exists

</div>

</div>

</div>

To check the existence of a file with `GSI-FTP`.

    [user] $

<div class="note" title="Use the return code" style="margin-left: 0.5in; margin-right: 0.5in;">

### Use the return code

Please note the **`echo $?`** show the return code of the last run application. The error message returned from the client this should not be scripted against as it is one of many possible errors.

</div>

</div>

<div class="section" title="Deleting files">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-gridftp-rm"></a>Deleting files

</div>

</div>

</div>

To delete files with `GSI-FTP` use the <span class="command">**edg-gridftp-rm**</span> command.

    [user] $

This deletes the file `filler_test20050811160948926780000` from the `/pnfs/example.org/data/dteam` using the door running on the host `gridftp-door.example.org` within the <span class="productname">dCache</span> cluster `example.org`

</div>

<div class="section" title="Copying files">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-gridftp-cp"></a>Copying files

</div>

</div>

</div>

<div class="cmdsynopsis">

globus-url-copy [[command line options]] [_<tt><srcUrl></tt>_] [_<tt><destinationUrl></tt>_] ...

</div>

Copying file with <span class="command">**globus-url-copy**</span> follows the syntax source, destination.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

The following example copies the file `/etc/group` into <span class="productname">dCache</span> as the file `/pnfs/example.org/data/dteam/test_GlobusUrlCopy.clinton.504.22080.20071102160121.2`

    [user] $

Please note that the five slashes are really needed.

</div>

</div>

</div>

</div>

<div class="section" title="dCap">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-clients-dcap"></a>`dCap`

</div>

</div>

</div>

When using <span class="command">**dccp**</span> client or using the interposition library the errors `Command failed!` can be safely ignored.

<div class="section" title="dccp">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-dcap-dcc"></a><span class="command">**dccp**</span>

</div>

</div>

</div>

The following example shows <span class="command">**dccp**</span> being used to copy the file `/etc/group` into <span class="productname">dCache</span> as the the file `/pnfs/example.org/data/dteam/test6`. The <span class="command">**dccp**</span> program will connect to <span class="productname">dCache</span> without authenticating.

    [user] $

The following example shows <span class="command">**dccp**</span> being used to upload the file `/etc/group`. In this example, <span class="command">**dccp**</span> will authenticate with <span class="productname">dCache</span> using the `GSI` protocol.

    [user] $

The following example shows <span class="command">**dccp**</span> with the debugging enabled. The value `63` controls how much information is displayed.

    [user] $

</div>

<div class="section" title="Using the dCache client interposition library.">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-dcap-interposition"></a>Using the <span class="productname">dCache</span> client interposition library.

</div>

</div>

</div>

<div class="tip" title="Finding the GSI tunnel." style="margin-left: 0.5in; margin-right: 0.5in;">

### Finding the `GSI` tunnel.

When the `LD_PRELOAD` library `libpdcap.so` variable produces errors finding the `GSI` tunnel it can be useful to specify the location of the `GSI` tunnel library directly using the following command:

    [user] $

Please see [http://www.dcache.org/manuals/experts_docs/tunnel-HOWTO.html](http://www.dcache.org/manuals/experts_docs/tunnel-HOWTO.html) for further details on tunnel setup for the server.

</div>

`dCap` is a <acronym class="acronym">POSIX</acronym> like interface for accessing <span class="productname">dCache</span>, allowing unmodified applications to access <span class="productname">dCache</span> transparently. This access method uses a proprietary data transfer protocol, which can emulate <acronym class="acronym">POSIX</acronym> access across the <acronym class="acronym">LAN</acronym> or <acronym class="acronym">WAN</acronym>.

Unfortunately the client requires inbound connectivity and so it is not practical to use this protocol over the <acronym class="acronym">WAN</acronym> as most sites will not allow inbound connectivity to worker nodes.

To make non <span class="productname">dCache</span> aware applications access files within <span class="productname">dCache</span> through `dCap` all that is needed is set the `LD_PRELOAD` environment variable to `/opt/d-cache/dcap/lib/libpdcap.so`.

    [user] $

Setting the `LD_PRELOAD` environment variable results in the library `libpdcap.so` overriding the operating system calls. After setting this environment variable, the standard shell command should work with `dCap` and `GSIdCap` <acronym class="acronym">URL</acronym>s.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

The following session demonstrates copying a file into <span class="productname">dCache</span>, checking the file is present with the <span class="command">**ls**</span> command, reading the first 3 lines from <span class="productname">dCache</span> and finally deleting the file.

    [user] $

</div>

</div>

</div>

</div>

<div class="section" title="SRM">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-clients-srm"></a>`SRM`

</div>

</div>

</div>

<span class="productname">dCache</span> provides a series of clients one of which is the `SRM` client which supports a large number operations, but is just one Java application, the script name is sent to the Java applications command line to invoke each operation.

This page just shows the scripts command line and not the invocation of the Java application directly.

<div class="section" title="Creating a new directory.">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-srm-mkdir"></a>Creating a new directory.

</div>

</div>

</div>

Usage:

<div class="cmdsynopsis">

srmmkdir [[command line options]] [_<tt><srmUrl></tt>_]

</div>

Example:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

The following example creates the directory `/pnfs/example.org/data/dteam/myDir`.

    [user] $

</div>

</div>

</div>

<div class="section" title="Removing files from dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-srm-rm"></a>Removing files from <span class="productname">dCache</span>

</div>

</div>

</div>

Usage:

<div class="cmdsynopsis">

srmrm [[command line options]] [_<tt><srmUrl></tt>_ ...]

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

</div>

</div>

</div>

<div class="section" title="Removing empty directories from dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-srm-rmdir"></a>Removing empty directories from <span class="productname">dCache</span>

</div>

</div>

</div>

It is allowed to remove only empty directories as well as trees of empty directories.

Usage:

<div class="cmdsynopsis">

srmrmdir [command line options] [_<tt><srmUrl></tt>_]

</div>

Examples:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

</div>

</div>

</div>

<div class="section" title="srmcp for SRM v1">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-srm-1-cp"></a>srmcp for `SRM` v1

</div>

</div>

</div>

Usage:

<div class="cmdsynopsis">

srmcp [command line options] _<tt><source></tt>_... [_<tt><destination></tt>_]

</div>

or

<div class="cmdsynopsis">

srmcp [command line options] [-copyjobfile] _<tt><file></tt>_

</div>

<div class="section" title="Copying files to dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cb-clients-srm-1-cp-to"></a>Copying files to <span class="productname">dCache</span>

</div>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

</div>

</div>

</div>

<div class="section" title="Copying files from dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cb-clients-srm-1-cp-from"></a>Copying files from <span class="productname">dCache</span>

</div>

</div>

</div>

    [user] $

</div>

</div>

<div class="section" title="srmcp for SRM v2.2">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-srm-2"></a>srmcp for `SRM` v2.2

</div>

</div>

</div>

<div class="section" title="Getting the dCache Version">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cb-clients-srm-ping"></a>Getting the <span class="productname">dCache</span> Version

</div>

</div>

</div>

The <span class="command">**srmping**</span> command will tell you the version of <span class="productname">dCache</span>. This only works for authorized users and not just authenticated users.

    [user] $

</div>

<div class="section" title="Space Tokens">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cb-clients-srm-st"></a>Space Tokens

</div>

</div>

</div>

Space token support must be set up and reserving space with the admin interface this is also documented [in the `SRM` section](#cf-srm-intro "Introduction") and in [the <span class="productname">dCache</span> wiki](http://trac.dcache.org/projects/dcache/wiki/manuals/SRM_2.2_Setup).

<div class="section" title="Space Token Listing">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cb-clients-srm-st-ls"></a>Space Token Listing

</div>

</div>

</div>

Usage:

<div class="cmdsynopsis">

get-space-tokens [command line options] [_<tt><srmUrl></tt>_]

</div>

<div class="example"><a name="idp5981488"></a>

**Example 21.1\. surveying the space tokens available in a directory.**

<div class="example-contents">

    [user] $

A successful result:

<pre class="screen">return status code : SRM_SUCCESS
return status expl. : OK
Space Reservation Tokens:
148241
148311
148317
28839
148253
148227
148229
148289
148231
148352</pre>

</div>

</div>

<div class="example"><a name="idp5985440"></a>

**Example 21.2\. Listing the space tokens for a `SRM`:**

<div class="example-contents">

    [user] $

</div>

</div>

</div>

<div class="section" title="Space Reservation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cb-clients-srm-st-reserve"></a>Space Reservation

</div>

</div>

</div>

Usage:

<div class="cmdsynopsis">

srm-reserve-space [[command line options]] [_<tt><srmUrl></tt>_]

</div>

    [user] $

A successful result:

<pre class="screen">Space token =144573</pre>

A typical failure

<pre class="screen">SRMClientV2 : srmStatusOfReserveSpaceRequest , contacting service httpg://srm-door.example.org:8443/srm/managerv2
status: code=SRM_NO_FREE_SPACE explanantion= at Thu Nov 08 15:29:44 CET 2007 state Failed :  no space available
lifetime = null
access latency = ONLINE
retention policy = REPLICA
guaranteed size = null
total size = 34</pre>

Also you can get info for this space token `144573`:

    [user] $

Possible result:

<pre class="screen">Space Reservation with token=120047
                   owner:VoGroup=/dteam VoRole=NULL
               totalSize:1024
          guaranteedSize:1024
              unusedSize:1024
        lifetimeAssigned:36000
            lifetimeLeft:25071
           accessLatency:ONLINE
         retentionPolicy:REPLICA</pre>

</div>

<div class="section" title="Writing to a Space Token">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cb-clients-srm-st-write"></a>Writing to a Space Token

</div>

</div>

</div>

Usage: srmcp [command line options] source(s) destination

Examples:

    [user] $

    [user] $

</div>

<div class="section" title="Space Metadata">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cb-clients-srm-st-metadata"></a>Space Metadata

</div>

</div>

</div>

Users can get the metadata available for the space, but the ability to query the metadata of a space reservation may be restricted so that only certain users can obtain this information.

    [user] $

</div>

<div class="section" title="Space Token Release">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

##### <a name="cb-clients-srm-st-strm"></a>Space Token Release

</div>

</div>

</div>

Removes a space token from the `SRM`.

    [user] $

</div>

</div>

<div class="section" title="Listing a file in SRM">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="cb-clients-srm-2-ls"></a>Listing a file in `SRM`

</div>

</div>

</div>

`SRM` version 2.2 has a much richer set of file listing commands.

Usage:

<div class="cmdsynopsis">

srmls [command line options] _<tt><srmUrl></tt>_...

</div>

<div class="example"><a name="idp6022896"></a>

**Example 21.3\. Using `srmls -l`:**

<div class="example-contents">

    [user] $

</div>

</div>

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

The `-l` option results in <span class="command">**srmls**</span> providing additional information. Collecting this additional information may result in a dramatic increase in execution time.

</div>

<div class="example"><a name="idp6028768"></a>

**Example 21.4\. Using `srmls -l`:**

<div class="example-contents">

    [user] $

</div>

</div>

If you have more than 1000 entries in your directory then <span class="productname">dCache</span> will return only the first 1000\. To view directories with more than 1000 entries, please use the following parameters:

<div class="variablelist" title="srmls parameters">

**srmls parameters**

<dl>

<dt><span class="term">-count=_<tt><integer></tt>_</span></dt>

<dd>

The number of entries to report.

</dd>

<dt><span class="term">-offset=_<tt><integer></tt>_</span></dt>

</dl>

</div>

<div class="example"><a name="idp6039408"></a>

**Example 21.5\. Limited directory listing**

<div class="example-contents">

The first command shows the output without specifying `-count` or `-offset`. Since the directory contains less than 1000 entries, all entries are listed.

    [user] $

The following examples shows the result when using the `-count` option to listing the first three entries.

    [user] $

In the next command, the `-offset` option is used to view a different set of entries.

    [user] $

</div>

</div>

</div>

</div>

</div>

<div class="section" title="ldap">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-clients-ldap"></a>ldap

</div>

</div>

</div>

<span class="productname">dCache</span> is commonly deployed with the BDII. The information provider within <span class="productname">dCache</span> publishes information to BDII. To querying the <span class="productname">dCache</span> BDII is a matter of using the standard command ldapsearch. For grid the standard ldap port is set to 2170 from the previous value of 2135.

    [user] $

</div>

As can be seen from above even a single node standard install of <span class="productname">dCache</span> returns a considerable number of lines and for this reason we have not included the output, in this case 205 lines where written.

<div class="section" title="Using the LCG commands with dCache">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-clients-lcg"></a>Using the <acronym class="acronym">LCG</acronym> commands with <span class="productname">dCache</span>

</div>

</div>

</div>

The `lcg_util` <acronym class="acronym">RPM</acronym> contains many small command line applications which interact with `SRM` implementations, these where developed independently from <span class="productname">dCache</span> and provided by the <acronym class="acronym">LCG</acronym> grid computing effort.

Each command line application operates on a different method of the `SRM` interface. These applications where not designed for normal use but to provide components upon which operations can be built.

<span class="command">**lcg-gt**</span> queries the <acronym class="acronym">BDII</acronym> information server. This adds an additional requirement that the <acronym class="acronym">BDII</acronym> information server can be found by <span class="command">**lcg-gt**</span>, please only attempt to contact servers found on your user interface using.

    [user] $

<div class="section" title="The lcg-gt Application">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-lcg-gt"></a>The <span class="command">**lcg-gt**</span> Application

</div>

</div>

</div>

`SRM` provides a protocol negotiating interface, and returns a <acronym class="acronym">TURL</acronym> (transfer <acronym class="acronym">URL</acronym>). The protocol specified by the client will be returned by the server if the server supports the requested protocol.

To read a file from <span class="productname">dCache</span> using <span class="command">**lcg-gt**</span> you must specify two parameters the <acronym class="acronym">SURL</acronym> (storage <acronym class="acronym">URL</acronym>), and the protcol (`GSIdCap` or `GSI-FTP`) you wish to use to access the file.

    [user] $

Each of the above three lines contains different information. These are explained below.

`gsidcap://gsidcap-door.example.org:22128/pnfs/example.org/data/dteam/group` is the transfer <acronym class="acronym">URL</acronym> (<acronym class="acronym">TURL</acronym>).

`-2147365977` is the `SRM` `Request Id`, Please note that it is a negative number in this example, which is allowed by the specification.

`-2147365976` is the Unique identifier for the file with respect to the `Request Id`. Please note that with this example this is a negative number.

<div class="important" title="Remember to return your Request Id" style="margin-left: 0.5in; margin-right: 0.5in;">

### Remember to return your `Request Id`

<span class="productname">dCache</span> limits the number of `Request Id`s a user may have. All `Request Id`s should be returned to <span class="productname">dCache</span> using the command <span class="command">**lcg-sd**</span>.

</div>

If you use <span class="command">**lcg-gt**</span> to request a file with a protocol that is not supported by <span class="productname">dCache</span> the command will block for some time as <span class="productname">dCache</span>’s `SRM` interface times out after approximately 10 minutes.

</div>

<div class="section" title="The lcg-sd Application">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-clients-lcg-sd"></a>The <span class="command">**lcg-sd**</span> Application

</div>

</div>

</div>

This command should be used to return any <acronym class="acronym">TURL</acronym>s given by <span class="productname">dCache</span>’s `SRM` interface. This is because <span class="productname">dCache</span> provides a limited number of <acronym class="acronym">TURL</acronym>s available concurrently.

<span class="command">**lcg-sd**</span> takes four parameters: the <acronym class="acronym">SURL</acronym>, the `Request Id`, the `File Id` with respect to the `Request Id`, and the direction of data transfer.

The following example is to complete the get operation, the values are taken form the above example of <span class="command">**lcg-gt**</span>.

    [user] $

<div class="note" title="Negative numbers" style="margin-left: 0.5in; margin-right: 0.5in;">

### Negative numbers

<span class="productname">dCache</span> returns negative numbers for `Request Id` and `File Id`. Please note that <span class="command">**lcg-sd**</span> requires that these values are places in double-quotes with a single space before the `-` sign.

</div>

The `Request Id` is one of the values returned by the <span class="command">**lcg-gt**</span> command. In this example, the value (`-2147365977`) comes from the above example <span class="command">**lcg-gt**</span>.

The `File Id` is also one of the values returned returned by the <span class="command">**lcg-gt**</span> command. In this example, the value (`-2147365976`) comes from the above example <span class="command">**lcg-gt**</span>.

The direction parameter indicates in which direction data was transferred: `0` for reading data and `1` for writing data.

</div>

</div>

</div>

<div class="chapter" title="Chapter 22\. Pool Operations">

<div class="titlepage">

<div>

<div>

## <a name="cb-pool"></a>Chapter 22\. Pool Operations

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Checksums](#cb-pool-checksumming)</span></dt>

<dd>

<dl>

<dt><span class="section">[How to configure checksum calculation](#cb-pool-checksumming-config)</span></dt>

</dl>

</dd>

<dt><span class="section">[Migration Module](#cb-pool-migration)</span></dt>

<dd>

<dl>

<dt><span class="section">[Overview and Terminology](#idp6194560)</span></dt>

<dt><span class="section">[Command Summary](#idp6207104)</span></dt>

<dt><span class="section">[Examples](#idp6286544)</span></dt>

</dl>

</dd>

<dt><span class="section">[Renaming a Pool](#cb-pool-rename)</span></dt>

<dt><span class="section">[Pinning Files to a Pool](#cb-pool-pin)</span></dt>

</dl>

</div>

<div class="section" title="Checksums">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-pool-checksumming"></a>Checksums

</div>

</div>

</div>

In <span class="productname">dCache</span> the storage of a checksum is part of a successful transfer.

<div class="itemizedlist">

*   For an incoming transfer a checksum can be sent by the client (_Client Checksum_, it can be calculated during the transfer (_Transfer Checksum_) or it can be calculated on the server after the file has been written to disk (_Server File Checksum_).

*   For a pool to pool transfer a Transfer Checksum or a Server File Checksum can be calculated.

*   For data that is flushed to or restored from tape a checksum can be calculated before flushed to tape or after restored from tape, respectively.

</div>

<div class="variablelist">

<dl>

<dt><span class="term">Client Checksum</span></dt>

<dd>

The client calculates the checksum before or while the data is sent to <span class="productname">dCache</span>. The checksum value, depending on when it has been calculated, may be sent together with the open request to the door and stored into <span class="productname">Chimera</span> before the data transfer begins or it may be sent with the close operation after the data has been transferred.

The `dCap` protocol provides both methods, but the `dCap` clients use the latter by default.

The `FTP` protocol does not provide a mechanism to send a checksum. Nevertheless, some `FTP` clients can (mis-)use the <span class="quote">“<span class="quote">`site`</span>”</span> command to send the checksum prior to the actual data transfer.

</dd>

<dt><span class="term">Transfer Checksum</span></dt>

<dd>

While data is coming in, the server data mover may calculate the checksum on the fly.

</dd>

<dt><span class="term">Server File Checksum</span></dt>

<dd>

After all the file data has been received by the <span class="productname">dCache</span> server and the file has been fully written to disk, the server may calculate the checksum, based on the disk file.

</dd>

</dl>

</div>

The default configuration is that a checksum is calculated on write, i.e. a Server File Checksum.

<div class="section" title="How to configure checksum calculation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-pool-checksumming-config"></a>How to configure checksum calculation

</div>

</div>

</div>

Configure the calculation of checksums in the [admin interface](#intouch-admin "The Admin Interface"). The configuration has to be done for each pool separately.

    (local) admin >

The configuration will be saved in the file `_<tt><path/to/pool></tt>_/_<tt><nameOfPooldirectory></tt>_/setup`.

Use the command <span class="command">**csm info**</span> to see the checksum policy of the pool.

    (<poolname>) admin >

The default configuration is to check checksums on write.

Use the command <span class="command">**help csm set policy**</span> to see the configuration options.

The syntax of the command <span class="command">**csm set policy**</span> is

<div class="cmdsynopsis">

`csm set policy` [_`-_<tt><option></tt>_`_=on [|off]]

</div>

where _<tt><option></tt>_ can be replaced by

<div class="variablelist" title="OPTIONS">

**OPTIONS**

<dl>

<dt><span class="term">`ontransfer`</span></dt>

<dd>

If supported by the protocol, the checksum is calculated during file transfer.

</dd>

<dt><span class="term">`onwrite`</span></dt>

<dd>

The checksum is calculated after the file has been written to disk.

</dd>

<dt><span class="term">`onrestore`</span></dt>

<dd>

The checksum is calculated after data has been restored from tape.

</dd>

<dt><span class="term">`onflush`</span></dt>

<dd>

The checksum is calculated before data is flushed to tape.

</dd>

<dt><span class="term">`getcrcfromhsm`</span></dt>

<dd>

If the <abbr class="abbrev">HSM</abbr> script supports it, the `_<tt><pnfsid></tt>_.crcval` file is read and stored in <span class="productname">Chimera</span>.

</dd>

<dt><span class="term">`scrub`</span></dt>

<dd>

Pool data will periodically be veryfied against checksums. Use the command <span class="command">**help csm set policy**</span> to see the configuration options.

</dd>

<dt><span class="term">`enforcecrc`</span></dt>

<dd>

If no checksum has been calculated after or during the transfer, this option ensures that a checksum is calculated and stored in <span class="productname">Chimera</span>.

</dd>

</dl>

</div>

The option `onread` has not yet been implemented.

If an option is enabled a checksum is calculated as described. If there is already another checksum, the checksums are compared and if they match stored in <span class="productname">Chimera</span>.

<div class="important" title="Important" style="margin-left: 0.5in; margin-right: 0.5in;">

### Important

Do not change the default configuration for the option `enforcecrc`. This option should always be enabled as this ensures that there will always be a checksum stored with a file.

</div>

</div>

</div>

<div class="section" title="Migration Module">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-pool-migration"></a>Migration Module

</div>

</div>

</div>

The purpose of the migration module is essentially to copy or move the content of a pool to one or more other pools.

Typical use cases for the migration module include:

<div class="itemizedlist">

*   Vacating pools, that is, moving all files to other pools before decomissioning the pool.

*   Caching data on other pools, thus distributing the load and increasing availability.

*   As an alternative to the hopping manager.

</div>

<div class="section" title="Overview and Terminology">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp6194560"></a>Overview and Terminology

</div>

</div>

</div>

The migration module runs inside pools and hosts a number of migration jobs. Each job operates on a set of files on the pool on which it is executed and can copy or move those files to other pools. The migration module provides filters for defining the set of files on which a job operates.

The act of copying or moving a single file is called a migration task. A task selects a target pool and asks it to perform a pool to pool transfer from the source pool. The actual transfer is performed by the same component performing other pool to pool transfers. The migration module does not perform the transfer; it only orchestrates it.

The state of the target copy (the target state) as well as the source copy (the source state) can be explicitly defined. For instance, for vacating a pool the target state is set to be the same as the original source state, and the source state is changed to removed; for caching files, the target state is set to cached, and the source state is unmodified.

Sticky flags owned by the pin manager are never touched by a migration job, however the migration module can ask the pin manager to move the pin to the target pool. Care has been taken that unless the pin is moved by the pin manager, the source file is not deleted by a migration job, even if asked to do so. To illustrate this, assume a source file marked precious and with two sticky flags, one owned by foobar and the other by the pin manager. If a migration job is configured to delete the source file, but not to move the pin, the result will be that the file is marked cached, and the sticky flag owned by foobar is removed. The pin remains. Once it expires, the file is eligible for garbage collection.

All operations are idempotent. This means that a migration job can be safely rerun, and as long as everything else is unchanged, files will not be transferred again. Because jobs are idempotent they do not need to maintain persistent state, which in turns means the migration module becomes simpler and more robust. Should a pool crash during a migration job, the job can be rerun and the remaining files will be transfered.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Please notice that a job is only idempotent as long as the set of target pools do not change. If pools go offline or are excluded as a result of a an exclude or include expression, then the idempotent nature of a job may be lost.

</div>

It is safe to run migration jobs while pools are in use. Once started, migration jobs run to completion and do only operate on those files that matched the selection filters at the time the migration job started. New files that arrive on the pool are not touched. Neither are files that change state after a migration job has been initialized, even though the selection filters would match the new state of the file. The exception to the rule is when files are deleted from the pool or change state so that they no longer match the selection filter. Such files will be excluded from the migration job, unless the file was already processed. Rerunning a migration job will force it to pick up any new files. Because the job is idempotent, any files copied before are not copied again.

Permanent migration jobs behave differently. Rather than running to completion, permanent jobs keep running until explicitly cancelled. They monitor the pool for any new files or state changes, and dynamically add or remove files from the transfer queue. Permanent jobs are made persistent when the <span class="command">**save**</span> command is executed and will be recreated on pool restart. The main use case for permanent jobs is as an alternative to using a central hopping manager.

Idempotence is achieved by locating existing copies of a file on any of the target pools. If an existing copy is found, rather than creating a new copy, the state of the existing copy is updated to reflect the target state specified for the migration job. Care is taken to never make a file more volatile than it already is: Sticky flags are added, or existing sticky flags are extended, but never removed or shortened; cached files may be marked precious, but not vice versa. One caveat is when the target pool containing the existing copy is offline. In that case the existence of the copy cannot be verified. Rather than creating a new copy, the task fails and the file is put back into the transfer queue. This behaviour can be modified by marking a migration job as eager. Eager jobs create new copies if an existing copy cannot be immediately verified. As a rule of thumb, permanent jobs should never be marked eager. This is to avoid that a large number of unnecessary copies are created when several pools are restarted simultaneously.

A migration task aborts whenever it runs into a problem. The file will be reinserted at the end of the transfer queue. Consequently, once a migration job terminates, all files have been successfully transferred. If for some reason tasks for particular files keep failing, then the migration job will never terminate by itself as it retries indefinitely.

</div>

<div class="section" title="Command Summary">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp6207104"></a>Command Summary

</div>

</div>

</div>

Login to the [admin interface](#intouch-admin "The Admin Interface") and <span class="command">**cd**</span> to a pool to use the <span class="command">**migration**</span> commands. Use the command <span class="command">**help migration**</span> to view the possiblities.

    (local) admin >

The commands <span class="command">**migration copy**</span>, <span class="command">**migration cache**</span> and <span class="command">**migration move**</span> create new migration jobs. These commands are used to copy files to other pools. Unless filter options are specified, all files on the source pool are copied. The syntax for these commands is the same; example <span class="command">**migration copy**</span>:

<div class="cmdsynopsis">

`migration _<tt><copy></tt>_` [_`_<tt><option></tt>_`_] _<tt><target></tt>_

</div>

There are four different types of options. The filter options, transfer options, target options and lifetime options. Please run the command <span class="command">**help migration copy**</span> for a detailed description of the various options.

The commands <span class="command">**migration copy**</span>, <span class="command">**migration move**</span> and <span class="command">**migration cache**</span> take the same options and only differ in default values.

<div class="variablelist">

<dl>

<dt><span class="term">migration move</span></dt>

<dd>

The command <span class="command">**migration move**</span> does the same as the command <span class="command">**migration copy**</span> with the options:

<div class="itemizedlist">

*   `-smode`=`delete` (default for <span class="command">**migration copy**</span> is `same`).
*   `-pins`=`move` (default for <span class="command">**migration copy**</span> is `keep`).

</div>

additionally it uses the option `-verify`.

</dd>

<dt><span class="term">migration cache</span></dt>

<dd>

The command <span class="command">**migration cache**</span> does the same as the command <span class="command">**migration copy**</span> with the option:

<div class="itemizedlist">

*   `-tmode`=`cached`

</div>

</dd>

</dl>

</div>

Jobs are assinged a job ID and are executed in the background. The status of a job may be queried through the <span class="command">**migration info**</span> command. A list of all jobs can be obtained through <span class="command">**migration ls**</span>. Jobs stay in the list even after they have terminated. Terminated jobs can be cleared from the list through the <span class="command">**migration clear**</span> command.

Jobs can be suspended, resumed and cancelled through the <span class="command">**migration suspend**</span>, <span class="command">**migration resume**</span> and <span class="command">**migration cancel**</span> commands. Existing tasks are allowed to finish before a job is suspended or cancelled.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

A migration job can be suspended and resumed with the commands <span class="command">**migration suspend** </span>and <span class="command">**migration resume**</span> respectively.

    (local) admin >

A migration job can be cancelled with the command <span class="command">**migration cancel** </span>.

    (local) admin >

And terminated jobs can be cleared with the command <span class="command">**migration clear**</span>.

    (<poolname>) admin >

Except for the number of concurrent tasks, transfer parameters of existing jobs cannot be changed. This is by design to ensure idempotency of jobs. The concurrency can be altered through the <span class="command">**migration concurrency**</span> command.

    (<poolname>) admin >

</div>

</div>

</div>

<div class="section" title="Examples">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp6286544"></a>Examples

</div>

</div>

</div>

<div class="section" title="Vacating a pool">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp6287216"></a>Vacating a pool

</div>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

To vacate the pool _<tt><sourcePool></tt>_, we first mark the pool `read-only` to avoid that more files are added to the pool, and then move all files to the pool _<tt><targetPool></tt>_. It is not strictly necessary to mark the pool `read-only`, however if not done there is no guarantee that the pool is empty when the migration job terminates. The job can be rerun to move remaining files.

    (<sourcePool>) admin >

</div>

</div>

</div>

<div class="section" title="Caching recently accessed files">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

#### <a name="idp6305424"></a>Caching recently accessed files

</div>

</div>

</div>

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Say we want to cache all files belonging to the storage group `atlas:default` and accessed within the last month on a set of low-cost cache pools defined by the pool group `cache_pools`. We can achieve this through the following command.

    (<sourcePool>) admin >

The files on the source pool will not be altered. Any file copied to one of the target pools will be marked cached.

</div>

</div>

</div>

</div>

</div>

<div class="section" title="Renaming a Pool">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-pool-rename"></a>Renaming a Pool

</div>

</div>

</div>

A pool may be renamed with the following procedure, regardless of the type of files stored on it.

Disable file transfers from and to the pool with

    (<poolname>) admin >

Then make sure, no transfers are being processed anymore. All the following commands should give no output:

    (<poolname>) admin >

Now the files on the pools have to be unregistered on the namespace server with

    (<poolname>) admin >

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

Do not get confused that the commands <span class="command">**pnfs unregister**</span> and <span class="command">**pnfs register**</span> contain `pnfs` in their names. They also apply to <span class="productname">dCache</span> instances with <span class="productname">Chimera</span> and are named like that for legacy reasons.</div>

Even if the pool contains precious files, this is no problem, since we will register them again in a moment. The files might not be available for a short moment, though. Log out of the pool, and stop the domain running the pool:

    [root] #

Adapt the name of the pool in the layout files of your dCache installation to include your new pool-name. For a general overview of layout-files see [the section called “Defining domains and services”](#in-install-layout "Defining domains and services").

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

For example, to rename a pool from `swimmingPool` to `carPool`, change your layout file from

<pre class="programlisting">[_<tt><poolDomain></tt>_]
[_<tt><poolDomain></tt>_/pool]
name=swimmingPool
path=/pool/</pre>

to

<pre class="programlisting">[_<tt><poolDomain></tt>_]
[_<tt><poolDomain></tt>_/pool]
name=carPool
path=/pool/</pre>

</div>

</div>

<div class="warning" title="Warning" style="margin-left: 0.5in; margin-right: 0.5in;">

### Warning

Be careful about renaming pools in the layout after users have already been writing to them. This can cause inconsistencies in other components of <span class="productname">dCache</span>, if they are relying on pool names to provide their functionality. An example of such a component is the <span class="productname">Chimera</span> cache info.

</div>

Start the domain running the pool:

    [root] #

Register the files on the pool with

    (<poolname>) admin >

</div>

<div class="section" title="Pinning Files to a Pool">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-pool-pin"></a>Pinning Files to a Pool

</div>

</div>

</div>

You may pin a file locally within the private pool repository:

    (<poolname>) admin >

the `sticky` mode will stay with the file as long as the file is in the pool. If the file is removed from the pool and recreated afterwards this information gets lost.

You may use the same mechanism globally: in the command line interface (local mode) there is the command

    (local) admin >

This command does:

<div class="orderedlist">

1.  Flags the file as `sticky` in the name space database (<span class="productname">Chimera</span>). So from now the filename is globally set `sticky`.

2.  Will go to all pools where it finds the file and will flag it `sticky` in the pools.

3.  All new copies of the file will become `sticky`.

</div>

</div>

</div>

<div class="chapter" title="Chapter 23\. PostgreSQL and dCache">

<div class="titlepage">

<div>

<div>

## <a name="cb-postgres"></a>Chapter 23\. <span class="productname">PostgreSQL</span> and <span class="productname">dCache</span>

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Installing a <span class="productname">PostgreSQL</span> Server](#cb-postgres-install)</span></dt>

<dt><span class="section">[Configuring Access to <span class="productname">PostgreSQL</span>](#cb-postgres-configure)</span></dt>

<dt><span class="section">[Performance of the <span class="productname">PostgreSQL</span> Server](#cb-postgres-perf)</span></dt>

</dl>

</div>

<span class="productname">PostgreSQL</span> is used for various things in a <span class="productname">dCache</span> system: The [_`SRM`_](#gl-srm), the [_pin manager_](#gl-pinmanager), the [_space manager_](#gl-spacemanager), the [_replica manager_](#gl-replicamanager), the [_`billing`_](#gl-billing), and the <span class="productname">`pnfs`</span> server might make use of one or more databases in a single or several separate <span class="productname">PostgreSQL</span> servers.

The `SRM`, the pin manager, the space manager and the replica manager will use the <span class="productname">PostgreSQL</span> database as configured at cell start-up in the corresponding batch files. The `billing` will only write the accounting information into a database if it is configured with the option `-useSQL`. The <span class="productname">`pnfs`</span> server will use a <span class="productname">PostgreSQL</span> server if the `pnfs-posgresql` version is used. It will use several databases in the <span class="productname">PostgreSQL</span> server.

<div class="section" title="Installing a PostgreSQL Server">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-postgres-install"></a>Installing a <span class="productname">PostgreSQL</span> Server

</div>

</div>

</div>

The preferred way to set up a <span class="productname">PostgreSQL</span> server should be the installation of the version provided by your OS distribution; however, version 8.3 or later is required.

Install the <span class="productname">PostgreSQL</span> server, client and JDBC support with the tools of the operating system.

Initialize the database directory (for <span class="productname">PostgreSQL</span> version 9.2 this is `/var/lib/pgsql/9.2/data/`) , start the database server, and make sure that it is started at system start-up.

    [root] #

</div>

<div class="section" title="Configuring Access to PostgreSQL">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-postgres-configure"></a>Configuring Access to <span class="productname">PostgreSQL</span>

</div>

</div>

</div>

In the installation guide instructions are given for configuring one <span class="productname">PostgreSQL</span> server on the admin node for all the above described purposes with generous access rights. This is done to make the installation as easy as possible. The access rights are configured in the file `_<tt><database_directory_name></tt>_/data/pg_hba.conf`. According to the installation guide the end of the file should look like

<pre class="programlisting">...
# TYPE  DATABASE    USER        IP-ADDRESS        IP-MASK           METHOD
local   all         all                                             trust
host    all         all         127.0.0.1/32                        trust
host    all         all         ::1/128                             trust
host    all         all         _<tt><HostIP></tt>_/32          trust</pre>

This gives access to all databases in the <span class="productname">PostgreSQL</span> server to all users on the admin host.

The databases can be secured by restricting access with this file. E.g.

<pre class="programlisting">...
# TYPE  DATABASE    USER        IP-ADDRESS        METHOD
local   all         postgres                      ident sameuser
local   all         pnfsserver                    password
local   all         all                           md5
host    all         all         127.0.0.1/32      md5
host    all         all         ::1/128           md5
host    all         all         _<tt><HostIP></tt>_/32          md5</pre>

To make the server aware of this you need to reload the configuration file as the user `postgres` by:

    [root] #

And the password for e.g. the user `pnfsserver` can be set with

    [postgres] #

The <span class="productname">`pnfs`</span> server is made aware of this password by changing the variable `dbConnectString` in the file `/usr/etc/pnfsSetup`:

<pre class="programlisting">...
export dbConnectString="user=pnfsserver password=_<tt><yourPassword></tt>_"</pre>

User access should be prohibited to this file with

    [root] #

</div>

<div class="section" title="Performance of the PostgreSQL Server">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-postgres-perf"></a>Performance of the <span class="productname">PostgreSQL</span> Server

</div>

</div>

</div>

On small systems it should never be a problem to use one single <span class="productname">PostgreSQL</span> server for all the functions listed above. In the standard installation, the `ReplicaManager` is not activated by default. The `billing` will only write to a file by default.

Whenever the <span class="productname">PostgreSQL</span> server is going to be used for another functionality, the impact on performance should be checked carefully. To improve the performance, the functionality should be installed on a separate host. Generally, a <span class="productname">PostgreSQL</span> server for a specific funcionality should be on the same host as the <span class="productname">dCache</span> cell accessing that <span class="productname">PostgreSQL</span> server, and the <span class="productname">PostgreSQL</span> server containing the databases for <span class="productname">Chimera</span> should run on the same host as <span class="productname">Chimera</span> and the `PnfsManager` cell of the <span class="productname">dCache</span> system accessing it.

It is especially useful to use a separate <span class="productname">PostgreSQL</span> server for the `billing` cell.

<div class="note" title="Note" style="margin-left: 0.5in; margin-right: 0.5in;">

### Note

The following is <span class="emphasis">_work-in-progress_</span>.

</div>

Create <span class="productname">PostgreSQL</span> user with the name you will be using to run <span class="productname">`pnfs`</span> server. Make sure it has `CREATEDB` privilege.

    [user] $

<div class="cellattributes"><a name="idp6442256"></a>

**Table 23.1\. Protocol Overview**

<div class="cellattributes-contents">

<table summary="Protocol Overview" border="1"><colgroup><col align="left" class="Component"><col align="left" class="Database Host"><col align="left" class="Database Name"><col align="left" class="Database User"><col align="left" class="Database Password"></colgroup>

<thead>

<tr>

<th align="left">Component</th>

<th align="left">Database Host</th>

<th align="left">Database Name</th>

<th align="left">Database User</th>

<th align="left">Database Password</th>

</tr>

</thead>

<tbody>

<tr>

<td align="left">SRM</td>

<td align="left">`srm.db.host`or if not set: `srmDbHost` or if not set: `localhost`</td>

<td align="left">dcache</td>

<td align="left"><span class="database">srmdcache</span></td>

<td align="left">**`srmdcache`**</td>

</tr>

<tr>

<td align="left">pin manag</td>

<td align="left">`pinManagerDatabaseHost` or if not set: `srmDbHost` or if not set: `localhost`</td>

<td align="left">dcache</td>

<td align="left"><span class="database">srmdcache</span></td>

<td align="left">**`srmdcache`**</td>

</tr>

<tr>

<td align="left">`ReplicaManager`</td>

<td align="left">`replica.db.host` or if not set: `localhost`</td>

<td align="left">replicas</td>

<td align="left"><span class="database">srmdcache</span></td>

<td align="left">**`srmdcache`**</td>

</tr>

<tr>

<td align="left"><span class="productname">`pnfs`</span> server</td>

<td align="left">`localhost`</td>

<td align="left">admin, data1, exp0, ...</td>

<td align="left"><span class="database">pnfsserver</span></td>

<td align="left">--free--</td>

</tr>

<tr>

<td align="left">billing</td>

<td align="left">`billingDatabaseHost` or if not set: `localhost`</td>

<td align="left">billing</td>

<td align="left"><span class="database">srmdcache</span></td>

<td align="left">**`srmdcache`**</td>

</tr>

</tbody>

</table>

</div>

</div>

</div>

</div>

<div class="chapter" title="Chapter 24\. Complex Network Configuration">

<div class="titlepage">

<div>

<div>

## <a name="cb-net"></a>Chapter 24\. Complex Network Configuration

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Firewall Configuration](#cb-net-firewall)</span></dt>

<dd>

<dl>

<dt><span class="section">[Basic Installation](#idp6488512)</span></dt>

<dt><span class="section">[Multi-Node with Firewalls](#idp6499952)</span></dt>

</dl>

</dd>

<dt><span class="section">[`GridFTP` Connections via two or more Network Interfaces](#cb-net-second-if)</span></dt>

<dt><span class="section">[`GridFTP` with Pools in a Private Subnet](#cb-net-pool-priv)</span></dt>

</dl>

</div>

This chapter contains solutions for several non-trivial network configurations. The first section discusses the interoperation of <span class="productname">dCache</span> with firewalls and does not require any background knowledge about <span class="productname">dCache</span> other than what is given in the installation guide ([Chapter 2, _Installing <span class="productname">dCache</span>_](#in "Chapter 2\. Installing dCache")) and the first steps tutorial ([Chapter 3, _Getting in Touch with <span class="productname">dCache</span>_](#intouch "Chapter 3\. Getting in Touch with dCache")). The following sections will deal with more complex network topologies, e.g. private subnets. Even though not every case is covered, these cases might help solve other problems, as well. Intermediate knowledge about <span class="productname">dCache</span> is required.

<div class="section" title="Firewall Configuration">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-net-firewall"></a>Firewall Configuration

</div>

</div>

</div>

The components of a <span class="productname">dCache</span> instance may be distributed over several hosts (nodes). Some of these components are accessed from outside and consequently the firewall needs to be aware of that. We contemplate two communication types, the <span class="productname">dCache</span> internal communication and the interaction from <span class="productname">dCache</span> with clients.

Since <span class="productname">dCache</span> is very flexible, most port numbers may be changed in the configuration. The command <span class="command">**dcache ports**</span> will provide you with a list of services and the ports they are using.

<div class="section" title="Basic Installation">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp6488512"></a>Basic Installation

</div>

</div>

</div>

This section assumes that all nodes are behind a firewall and have full access to each other.

**<span class="productname">dCache</span> internal.**

<div class="itemizedlist">

*   As we assume that all nodes are behind a firewall and have full access to each other there is nothing to be mentioned here.

*   On the pool nodes the LAN range ports need to be opened to allow pool to pool communication. By default these are ports `33115-33145` (set by the properties `dcache.net.lan.port.min` and `dcache.net.lan.port.max`).

</div>

**<span class="productname">dCache</span> communication with client.**

<div class="itemizedlist">

*   The door ports need to be opened to allow the clients to connect to the doors.

*   The WAN/LAN range ports need to be opened to allow the clients to connect to the pools. The default values for the WAN port range are `20000-25000`. The WAN port range is defined by the properties `dcache.net.wan.port.min` and `dcache.net.wan.port.max`.

</div>

</div>

<div class="section" title="Multi-Node with Firewalls">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp6499952"></a>Multi-Node with Firewalls

</div>

</div>

</div>

Multinode setup with firewalls on the nodes.

**<span class="productname">dCache</span> internal.**

<div class="itemizedlist">

*   The `LocationManager` server runs in the `dCacheDomain`. By default it is listening on UDP port `11111`. Hence, on the head node port `11111` needs to be opened in the firewall to allow connections to the `LocationManager`.

*   On the pool nodes the LAN range ports need to be opened to allow pool to pool communication. By default these are ports `33115-33145` (set by the properties `dcache.net.lan.port.min` and `dcache.net.lan.port.max`).

</div>

**<span class="productname">dCache</span> communication with client.**

<div class="itemizedlist">

*   The door ports need to be opened to allow the clients to connect to the doors.

*   The WAN/LAN range ports need to be opened to allow the clients to connect to the pools. The default values for the WAN port range are `20000-25000`. The WAN port range is defined by the properties `dcache.net.wan.port.min` and `dcache.net.wan.port.max`.

</div>

More complex setups are described in the following sections.

</div>

</div>

<div class="section" title="GridFTP Connections via two or more Network Interfaces">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-net-second-if"></a>`GridFTP` Connections via two or more Network Interfaces

</div>

</div>

</div>

<div class="section" title="Description">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp6517504"></a>Description

</div>

</div>

</div>

The host on which the `GridFTP` door is running has several network interfaces and is supposed to accept client connections via all those interfaces. The interfaces might even belong to separate networks with no routing from one network to the other.

As long as the data connection is opened by the `GridFTP` server (passive FTP mode), there is no problem with having more than one interface. However, when the client opens the data connection (active FTP mode), the door (FTP server) has to supply it with the correct interface it should connect to. If this is the wrong interface, the client might not be able to connect to it, because there is no route or the connection might be inefficient.

Also, since a `GridFTP` server has to authenticate with an `X.509` grid certificate and key, there needs to be a separate certificate and key pair for each name of the host or a certificate with alternative names. Since each network interface might have a different name, several certificates and keys are needed and the correct one has to be used, when authenticating via each of the interfaces.

</div>

<div class="section" title="Solution">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp6524560"></a>Solution

</div>

</div>

</div>

Define two domains, one for the internal and one for the external use. Start a separate `loginbroker`, `srm` and `gridftp` service in these domains.

The `srm` and the `gridftp` service have to be configured with the property `listen`, only to listen on the interface they should serve. The locations of the grid host certificate and key files for the interface have to be specified explicitly with the properties `dcache.authn.hostcert.cert` and `dcache.authn.hostcert.key`.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

In this example we show a setup for two `GridFTP` doors serving two network interfaces with the hostnames `door-internal` (111.111.111.5) and `door-external` (222.222.222.5) which are served by two `GridFTP` doors in two domains.

<pre class="programlisting">[internalDomain]
listen=111.111.111.5
dcache.authn.hostcert.cert=<span>/etc/dcache</span>/interface-cert-internal.pem
dcache.authn.hostcert.key=<span>/etc/dcache</span>/interface-key-internal.pem
[internalDomain/loginbroker]
loginbroker.cell.name=loginbroker-internal
[internalDomain/srm]
srm.cell.name=srm-internal
srm.protocols.loginbroker=loginbroker-internal
srm.net.host=door-internal
[internalDomain/ftp]
ftp.authn.protocol = gsi
ftp.cell.name=GFTP-door-internal
dcache.service.loginbroker=loginbroker-internal

[externalDomain]
listen=222.222.222.5
dcache.authn.hostcert.cert=<span>/etc/dcache</span>/interface-cert-external.pem
dcache.authn.hostcert.key=<span>/etc/dcache</span>/interface-key-external.pem
[externalDomain/loginbroker]
loginbroker.cell.name=loginbroker-external
[externalDomain/srm]
srm.cell.name=srm-external
srm.protocols.loginbroker=loginbroker-external
srm.net.host=door-external
[externalDomain/ftp]
ftp.authn.protocol = gsi
ftp.cell.name=GFTP-door-external
dcache.service.loginbroker=loginbroker-external</pre>

</div>

</div>

</div>

</div>

<div class="section" title="GridFTP with Pools in a Private Subnet">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-net-pool-priv"></a>`GridFTP` with Pools in a Private Subnet

</div>

</div>

</div>

<div class="section" title="Description">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp6542704"></a>Description

</div>

</div>

</div>

If pool nodes of a dCache instance are connected to a secondary interface of the `GridFTP` door, e.g. because they are in a private subnet, the `GridFTP` door will still tell the pool to connect to its primary interface, which might be unreachable.

The reason for this is that the control communication between the door and the pool is done via the network of `TCP` connections which have been established at start-up. In the standard setup this communication is routed via the <span class="productname">dCache</span> domain. However, for the data transfer, the pool connects to the `GridFTP` door. The IP address it connects to is sent by the `GridFTP` door to the pool via the control connection. Since the `GridFTP` door cannot find out which of its interfaces the pool should use, it normally sends the IP address of the primary interface.

</div>

<div class="section" title="Solution">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="idp6551984"></a>Solution

</div>

</div>

</div>

Tell the `GridFTP` door explicitly which IP it should send to the pool for the data connection with the `ftp.net.internal` property.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

E.g. if the pools should connect to the secondary interface of the `GridFTP` door host which has the IP address `10.0.1.1`, set

<pre class="programlisting">ftp.net.internal=10.0.1.1</pre>

in the `<span>/etc/dcache</span>/dcache.conf` file.

</div>

</div>

</div>

</div>

</div>

<div class="chapter" title="Chapter 25\. Advanced Tuning">

<div class="titlepage">

<div>

<div>

## <a name="cb-tuning"></a>Chapter 25\. Advanced Tuning

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Multiple Queues for Movers in each Pool](#cb-adv-multi-mover-queues)</span></dt>

<dd>

<dl>

<dt><span class="section">[Description](#cb-adv-multi-mover-queues-d)</span></dt>

<dt><span class="section">[Solution](#cb-adv-multi-mover-queues-s)</span></dt>

<dt><span class="section">[Configuration](#cb-adv-multi-mover-queues-c)</span></dt>

<dt><span class="section">[Tunable Properties for Multiple Queues](#cb-adv-multi-mover-queues-t)</span></dt>

</dl>

</dd>

<dt><span class="section">[Tunable Properties](#cb-tuning-parameters)</span></dt>

<dd>

<dl>

<dt><span class="section">[`dCap`](#cb-tuning-parameters-dcap)</span></dt>

<dt><span class="section">[`GridFTP`](#cb-tuning-parameters-gsiftp)</span></dt>

<dt><span class="section">[`SRM`](#cb-tuning-parameters-srm)</span></dt>

</dl>

</dd>

</dl>

</div>

The use cases described in this chapter are only relevant for large-scale <span class="productname">dCache</span> instances which require special tuning according to a longer experience with client behaviour.

<div class="section" title="Multiple Queues for Movers in each Pool">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-adv-multi-mover-queues"></a>Multiple Queues for Movers in each Pool

</div>

</div>

</div>

<div class="section" title="Description">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-adv-multi-mover-queues-d"></a>Description

</div>

</div>

</div>

Client requests to a <span class="productname">dCache</span> system may have rather diverse behaviour. Sometimes it is possible to classify them into several typical usage patterns. An example are the following two concurrent usage patterns:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Data is copied with a high transfer rate to the <span class="productname">dCache</span> system from an external source. This is done via the `GridFTP` protocol. At the same time batch jobs on a local farm process data. Since they only need a small part of each file, they use the `dCap` protocol via the `dCap` library and seek to the position in the file they are interested in, read a few bytes, do a few hours of calculations, and finally read some more data.

As long as the number of active requests does not exceed the maximum number of allowed active requests, the two types of requests are processed concurrently. The `GridFTP` transfers complete at a high rate while the processing jobs take hours to finish. This maximum number of allowed requests is set with [<span class="refentrytitle"><span class="command">**mover set max active**</span></span>](#cmd-mover_set_max_active "mover set max active") and should be tuned according to capabilities of the pool host.

However, if requests are queued, the slow processing jobs might clog up the queue and not let the fast `GridFTP` request through, even though the pool just sits there waiting for the processing jobs to request more data. While this could be temporarily remedied by setting the maximum active requests to a higher value, then in turn `GridFTP` request would put a very high load on the pool host.

</div>

</div>

The above example is pretty realistic: As a rule of thumb, `GridFTP` requests are fastest, `dCap` requests with the <span class="command">**dccp**</span> program are a little slower and `dCap` requests with the `dCap` library are very slow. However, the usage patterns might be different at other sites and also might change over time.

</div>

<div class="section" title="Solution">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-adv-multi-mover-queues-s"></a>Solution

</div>

</div>

</div>

Use separate queues for the movers, depending on the door initiating them. This easily allows for a separation of requests of separate protocols. (Transfers from and to a [_tape backend_](#gl-tape_backend) and [_pool-to-pool transfers_](#gl-p2p) are handled by separate queues, one for each of these transfers.)

A finer grained queue selection mechanism based on, e.g. the `IP` address of the client or the file which has been requested, is not possible with this mechanism. However, the [_pool selection unit (PSU)_](#gl-pm-comp-psu) may provide a separation onto separate pools using those criteria.

In the above example, two separate queues for fast `GridFTP` transfers and slow `dCap` library access would solve the problem. The maximum number of active movers for the `GridFTP` queue should be set to a lower value compared to the `dCap` queue since the fast `GridFTP` transfers will put a high load on the system while the `dCap` requests will be mostly idle.

</div>

<div class="section" title="Configuration">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-adv-multi-mover-queues-c"></a>Configuration

</div>

</div>

</div>

For a multi mover queue setup, the pools have to be told to start several queues and the doors have to be configured to use one of these. It makes sense to create the same queues on all pools. This is done by the following change to the file `<span>/etc/dcache</span>/dcache.conf`:

<pre class="programlisting">pool.queues=queueA,queueB</pre>

Each door may be configured to use a particular mover queue. The pool, selected for this request, does not depend on the selected mover queue. So a request may go to a pool which does not have the particular mover queue configured and will consequently end up in the default mover queue of that pool.

<pre class="programlisting">ftp.mover.queue=queueA
dcap.mover.queue=queueB</pre>

All requests send from this kind of door will ask to be scheduled to the given mover queue. The selection of the pool is not affected.

The doors are configured to use a particular mover queue as in the following example:

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Create the queues `queueA` and `queueB`, where `queueA` shall be the queue for the `GridFTP` transfers and `queueB` for `dCap`.

<pre class="programlisting">pool.queues=queueA,queueB
ftp.mover.queue=queueA
dcap.mover.queue=queueB</pre>

</div>

</div>

If the pools should not all have the same queues you can define queues for pools in the layout file. Here you might as well define that a specific door is using a specific queue.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

In this example `queueC`is defined for `pool1` and `queueD` is defined for `pool2`. The `GridFTP` door running in the domain `myDoors` is using the queue `queueB`.

<pre class="programlisting">[myPools]
[myPools/pool1]
pool.queues=queueC
[myPools/pool2]
pool.queues=queueD

[myDoors]
[myDoors/dcap]
dcap.mover.queue=queueC
[myDoors/ftp]
ftp.authn.protocol = gsi
ftp.mover.queue=queueD</pre>

</div>

</div>

There is always a default queue called `regular`. Transfers not requesting a particular mover queue or requesting a mover queue not existing on the selected pool, are handled by the `regular` queue.

The pool cell commands [<span class="refentrytitle"><span class="command">**mover ls**</span></span>](#cmd-mover_ls "mover ls") and [<span class="refentrytitle"><span class="command">**mover set max active**</span></span>](#cmd-mover_set_max_active "mover set max active") have a `-queue` option to select the mover queue to operate on. Without this option, [<span class="refentrytitle"><span class="command">**mover set max active**</span></span>](#cmd-mover_set_max_active "mover set max active") will act on the default queue while [<span class="refentrytitle"><span class="command">**mover ls**</span></span>](#cmd-mover_ls "mover ls") will list all active and waiting client transfer requests.

For the `dCap` protocol, it is possible to allow the client to choose another queue name than the one defined in the file `dcache.conf`. To achieve this the property `dcap.authz.mover-queue-overwrite` needs to be set to `allowed`.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

Create the queues `queueA` and `queue_dccp`, where `queueA` shall be the queue for `dCap`.

<pre class="programlisting">pool.queues=queueA,queue_dccp
dcap.mover.queue=queueA
dcap.authz.mover-queue-overwrite=allowed</pre>

With the <span class="command">**dccp**</span> command the queue can now be specified as follows:

    [user] $

</div>

</div>

Since <span class="command">**dccp**</span> requests may be quite different from other requests with the `dCap` protocol, this feature may be used to use separate queues for <span class="command">**dccp**</span> requests and other `dCap` library requests. Therefore, the <span class="command">**dccp**</span> command may be changed in future releases to request a special <span class="command">**dccp**</span>-queue by default.

</div>

<div class="section" title="Tunable Properties for Multiple Queues">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-adv-multi-mover-queues-t"></a>Tunable Properties for Multiple Queues

</div>

</div>

</div>

<div class="small">

<table border="1"><colgroup><col align="left" class="Property"><col align="center" class="Default Value"><col align="left" class="Description"></colgroup>

<thead>

<tr>

<th align="center">Property</th>

<th align="center">Default Value</th>

<th align="center">Description</th>

</tr>

</thead>

<tbody>

<tr>

<td align="left">pool.queues</td>

<td align="center"><span class="emphasis">_Not set_</span></td>

<td align="left">I/O queue name</td>

</tr>

<tr>

<td align="left">dcap.mover.queue</td>

<td align="center"><span class="emphasis">_Not set_</span></td>

<td align="left">Insecure `dCap` I/O queue name</td>

</tr>

<tr>

<td align="left">dcap.mover.queue</td>

<td align="center"><span class="emphasis">_Not set_</span></td>

<td align="left">`GSIdCap` I/O queue name</td>

</tr>

<tr>

<td align="left">dcap.authz.mover-queue-overwrite</td>

<td align="center">denied</td>

<td align="left">Controls whether an application is allowed to overwrite a queue name</td>

</tr>

<tr>

<td align="left">dcap.authz.mover-queue-overwrite</td>

<td align="center">denied</td>

<td align="left">Controls whether an application is allowed to overwrite a queue name</td>

</tr>

<tr>

<td align="left">dcap.authz.mover-queue-overwrite</td>

<td align="center">denied</td>

<td align="left">Controls whether an application is allowed to overwrite a queue name</td>

</tr>

<tr>

<td align="left">ftp.mover.queue</td>

<td align="center"><span class="emphasis">_Not set_</span></td>

<td align="left">`GSI-FTP` I/O queue name</td>

</tr>

<tr>

<td align="left">nfs.mover.queue</td>

<td align="center"><span class="emphasis">_Not set_</span></td>

<td align="left">`NFS` I/O queue name</td>

</tr>

<tr>

<td align="left">transfermanagers.mover.queue</td>

<td align="center"><span class="emphasis">_Not set_</span></td>

<td align="left">queue used for SRM third-party transfers (i.e. the srmCopy command)</td>

</tr>

<tr>

<td align="left">webdav.mover.queue</td>

<td align="center"><span class="emphasis">_Not set_</span></td>

<td align="left">`WebDAV` and `HTTP` I/O queue name</td>

</tr>

<tr>

<td align="left">xrootd.mover.queue</td>

<td align="center"><span class="emphasis">_Not set_</span></td>

<td align="left">`xrootd` I/O queue name</td>

</tr>

</tbody>

</table>

</div>

</div>

</div>

<div class="section" title="Tunable Properties">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="cb-tuning-parameters"></a>Tunable Properties

</div>

</div>

</div>

<div class="section" title="dCap">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-tuning-parameters-dcap"></a>`dCap`

</div>

</div>

</div>

<div class="small"><a name="idp6674032"></a>

**Table 25.1\. Property Overview**

<div class="small-contents">

<table summary="Property Overview" border="1"><colgroup><col align="left" class="Property"><col align="center" class="Default Value"><col align="left" class="Description"></colgroup>

<thead>

<tr>

<th align="center">Property</th>

<th align="center">Default Value</th>

<th align="center">Description</th>

</tr>

</thead>

<tbody>

<tr>

<td align="left">dcap.mover.queue</td>

<td align="center"><span class="emphasis">_Not set_</span></td>

<td align="left">`GSIdCap` I/O queue name</td>

</tr>

<tr>

<td align="left">dcap.mover.queue</td>

<td align="center"><span class="emphasis">_Not set_</span></td>

<td align="left">Insecure `dCap` I/O queue name</td>

</tr>

<tr>

<td align="left">dcap.authz.mover-queue-overwrite</td>

<td align="center">denied</td>

<td align="left">Is application allowed to overwrite queue name?</td>

</tr>

<tr>

<td align="left">dcap.authz.mover-queue-overwrite</td>

<td align="center">denied</td>

<td align="left">Is application allowed to overwrite queue name?</td>

</tr>

</tbody>

</table>

</div>

</div>

</div>

<div class="section" title="GridFTP">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-tuning-parameters-gsiftp"></a>`GridFTP`

</div>

</div>

</div>

<div class="small"><a name="idp6693584"></a>

**Table 25.2\. Property Overview**

<div class="small-contents">

<table summary="Property Overview" border="1"><colgroup><col align="left" class="Property"><col align="center" class="Default Value"><col align="left" class="Description"></colgroup>

<thead>

<tr>

<th align="center">Property</th>

<th align="center">Default Value</th>

<th align="center">Description</th>

</tr>

</thead>

<tbody>

<tr>

<td align="left">ftp.net.port.gsi</td>

<td align="center">2811</td>

<td align="left">`GSI-FTP` port listen port</td>

</tr>

<tr>

<td align="left">spaceReservation</td>

<td align="center"><span class="emphasis">_False_</span></td>

<td align="left">Use the space reservation service</td>

</tr>

<tr>

<td align="left">spaceReservationStrict</td>

<td align="center"><span class="emphasis">_False_</span></td>

<td align="left">Use the space reservation service</td>

</tr>

<tr>

<td align="left">ftp.performance-marker-period</td>

<td align="center">180</td>

<td align="left">Performance markers in seconds</td>

</tr>

<tr>

<td align="left">gplazmaPolicy</td>

<td align="center">${ourHomeDir}/etc/dcachesrm-gplazma.policy</td>

<td align="left">Location of the gPlazma Policy File</td>

</tr>

<tr>

<td align="left">ftp.service.poolmanager.timeout</td>

<td align="center">5400</td>

<td align="left">Pool Manager timeout in seconds</td>

</tr>

<tr>

<td align="left">ftp.service.pool.timeout</td>

<td align="center">600</td>

<td align="left">Pool timeout in seconds</td>

</tr>

<tr>

<td align="left">ftp.service.pnfsmanager.timeout</td>

<td align="center">300</td>

<td align="left">Pnfs timeout in seconds</td>

</tr>

<tr>

<td align="left">ftp.limits.retries</td>

<td align="center">80</td>

<td align="left">Number of PUT/GET retries</td>

</tr>

<tr>

<td align="left">ftp.limits.streams-per-client</td>

<td align="center">10</td>

<td align="left">Number of parallel streams per `FTP` PUT/GET</td>

</tr>

<tr>

<td align="left">ftp.enable.delete-on-failure</td>

<td align="center"><span class="emphasis">_True_</span></td>

<td align="left">Delete file on connection closed</td>

</tr>

<tr>

<td align="left">ftp.limits.clients</td>

<td align="center">100</td>

<td align="left">Maximum number of concurrently logged in users</td>

</tr>

<tr>

<td align="left">ftp.net.internal</td>

<td align="center"><span class="emphasis">_Not set_</span></td>

<td align="left">In case of two interfaces</td>

</tr>

<tr>

<td align="left">ftp.net.port-range</td>

<td align="center">20000:25000</td>

<td align="left">The client data port range</td>

</tr>

<tr>

<td align="left">gplazma.kpwd.file</td>

<td align="center">`${ourHomeDir}/etc/dcache.kpwd`</td>

<td align="left">Legacy authorization</td>

</tr>

</tbody>

</table>

</div>

</div>

</div>

<div class="section" title="SRM">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

### <a name="cb-tuning-parameters-srm"></a>`SRM`

</div>

</div>

</div>

<div class="small"><a name="idp6731776"></a>

**Table 25.3\. Property Overview**

<div class="small-contents">

<table summary="Property Overview" border="1"><colgroup><col align="left" class="Property"><col align="center" class="Default Value"><col align="left" class="Description"></colgroup>

<thead>

<tr>

<th align="center">Property</th>

<th align="center">Default Value</th>

<th align="center">Description</th>

</tr>

</thead>

<tbody>

<tr>

<td align="left">srm.net.port</td>

<td align="center">8443</td>

<td align="left">srm.net.port</td>

</tr>

<tr>

<td align="left">srm.db.host</td>

<td align="center">`localhost`</td>

<td align="left">srm.db.host</td>

</tr>

<tr>

<td align="left">srm.limits.external-copy-script.timeout</td>

<td align="center">3600</td>

<td align="left">srm.limits.external-copy-script.timeout</td>

</tr>

<tr>

<td align="left">srmVacuum</td>

<td align="center"><span class="emphasis">_True_</span></td>

<td align="left">srmVacuum</td>

</tr>

<tr>

<td align="left">srmVacuumPeriod</td>

<td align="center">21600</td>

<td align="left">srmVacuumPeriod</td>

</tr>

<tr>

<td align="left">srmProxiesDirectory</td>

<td align="center">`/tmp`</td>

<td align="left">srmProxiesDirectory</td>

</tr>

<tr>

<td align="left">srm.limits.transfer-buffer.size</td>

<td align="center">1048576</td>

<td align="left">srm.limits.transfer-buffer.size</td>

</tr>

<tr>

<td align="left">srm.limits.transfer-tcp-buffer.size</td>

<td align="center">1048576</td>

<td align="left">srm.limits.transfer-tcp-buffer.size</td>

</tr>

<tr>

<td align="left">srm.enable.external-copy-script.debug</td>

<td align="center"><span class="emphasis">_True_</span></td>

<td align="left">srm.enable.external-copy-script.debug</td>

</tr>

<tr>

<td align="left">srm.limits.request.scheduler.thread.queue.size</td>

<td align="center">1000</td>

<td align="left">srm.limits.request.scheduler.thread.queue.size</td>

</tr>

<tr>

<td align="left">srm.limits.request.scheduler.thread.pool.size</td>

<td align="center">100</td>

<td align="left">srm.limits.request.scheduler.thread.pool.size</td>

</tr>

<tr>

<td align="left">srm.limits.request.scheduler.waiting.max</td>

<td align="center">1000</td>

<td align="left">srm.limits.request.scheduler.waiting.max</td>

</tr>

<tr>

<td align="left">srm.limits.request.scheduler.ready-queue.size</td>

<td align="center">1000</td>

<td align="left">srm.limits.request.scheduler.ready-queue.size</td>

</tr>

<tr>

<td align="left">srm.limits.request.scheduler.ready.max</td>

<td align="center">100</td>

<td align="left">srm.limits.request.scheduler.ready.max</td>

</tr>

<tr>

<td align="left">srm.limits.request.scheduler.retries.max</td>

<td align="center">10</td>

<td align="left">srm.limits.request.scheduler.retries.max</td>

</tr>

<tr>

<td align="left">srm.limits.request.scheduler.retry-timeout</td>

<td align="center">60000</td>

<td align="left">srm.limits.request.scheduler.retry-timeout</td>

</tr>

<tr>

<td align="left">srm.limits.request.scheduler.same-owner-running.max</td>

<td align="center">10</td>

<td align="left">srm.limits.request.scheduler.same-owner-running.max</td>

</tr>

<tr>

<td align="left">srm.limits.request.put.scheduler.thread.queue.size</td>

<td align="center">1000</td>

<td align="left">srm.limits.request.put.scheduler.thread.queue.size</td>

</tr>

<tr>

<td align="left">srm.limits.request.put.scheduler.thread.pool.size</td>

<td align="center">100</td>

<td align="left">srm.limits.request.put.scheduler.thread.pool.size</td>

</tr>

<tr>

<td align="left">srm.limits.request.put.scheduler.waiting.max</td>

<td align="center">1000</td>

<td align="left">srm.limits.request.put.scheduler.waiting.max</td>

</tr>

<tr>

<td align="left">srm.limits.request.put.scheduler.ready-queue.size</td>

<td align="center">1000</td>

<td align="left">srm.limits.request.put.scheduler.ready-queue.size</td>

</tr>

<tr>

<td align="left">srm.limits.request.put.scheduler.ready.max</td>

<td align="center">100</td>

<td align="left">srm.limits.request.put.scheduler.ready.max</td>

</tr>

<tr>

<td align="left">srm.limits.request.put.scheduler.retries.max</td>

<td align="center">10</td>

<td align="left">srm.limits.request.put.scheduler.retries.max</td>

</tr>

<tr>

<td align="left">srm.limits.request.put.scheduler.retry-timeout</td>

<td align="center">60000</td>

<td align="left">srm.limits.request.put.scheduler.retry-timeout</td>

</tr>

<tr>

<td align="left">srm.limits.request.put.scheduler.same-owner-running.max</td>

<td align="center">10</td>

<td align="left">srm.limits.request.put.scheduler.same-owner-running.max</td>

</tr>

<tr>

<td align="left">srm.limits.request.copy.scheduler.thread.queue.size</td>

<td align="center">1000</td>

<td align="left">srm.limits.request.copy.scheduler.thread.queue.size</td>

</tr>

<tr>

<td align="left">srm.limits.request.copy.scheduler.thread.pool.size</td>

<td align="center">100</td>

<td align="left">srm.limits.request.copy.scheduler.thread.pool.size</td>

</tr>

<tr>

<td align="left">srm.limits.request.copy.scheduler.waiting.max</td>

<td align="center">1000</td>

<td align="left">srm.limits.request.copy.scheduler.waiting.max</td>

</tr>

<tr>

<td align="left">srm.limits.request.copy.scheduler.retries.max</td>

<td align="center">30</td>

<td align="left">srm.limits.request.copy.scheduler.retries.max</td>

</tr>

<tr>

<td align="left">srm.limits.request.copy.scheduler.retry-timeout</td>

<td align="center">60000</td>

<td align="left">srm.limits.request.copy.scheduler.retry-timeout</td>

</tr>

<tr>

<td align="left">srm.limits.request.copy.scheduler.same-owner-running.max</td>

<td align="center">10</td>

<td align="left">srm.limits.request.copy.scheduler.same-owner-running.max</td>

</tr>

</tbody>

</table>

</div>

</div>

</div>

</div>

</div>

</div>

<div class="part" title="Part IV. Reference">

<div class="titlepage">

<div>

<div>

# <a name="rf"></a>Part IV. Reference

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="chapter">[26\. <span class="productname">dCache</span> Clients](#rf-clients)</span></dt>

<dd>

<dl>

<dt><span class="section">[The `SRM` Client Suite](#rf-clients-srm)</span></dt>

<dd>

<dl>

<dt><span class="refentrytitle">[<span class="command">**srmcp**</span>](#cmd-srmcp)</span> <span class="refpurpose">— Copy a file from or to an `SRM` or between two `SRM`s.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**srmstage**</span>](#cmd-srmstage)</span> <span class="refpurpose">— Request staging of a file.</span></dt>

</dl>

</dd>

<dt><span class="section">[<span class="command">**dccp**</span>](#rf-clients-dccp)</span></dt>

<dd>

<dl>

<dt><span class="refentrytitle">[<span class="command">**<span class="command">**dccp**</span>**</span>](#cmd-dccp)</span> <span class="refpurpose">— Copy a file from or to a <span class="productname">dCache</span> server.</span></dt>

</dl>

</dd>

</dl>

</dd>

<dt><span class="chapter">[27\. <span class="productname">dCache</span> Cell Commands](#rf-cc)</span></dt>

<dd>

<dl>

<dt><span class="section">[Common Cell Commands](#rf-cc-common)</span></dt>

<dd>

<dl>

<dt><span class="refentrytitle">[<span class="command">**pin**</span>](#cmd-pin)</span> <span class="refpurpose">— Adds a comment to the pinboard.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**info**</span>](#cmd-info)</span> <span class="refpurpose">— Print info about the cell.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**dump pinboard**</span>](#cmd-dump_pinboard)</span> <span class="refpurpose">— Dump the full pinboard of the cell to a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**show pinboard**</span>](#cmd-show_pinboard)</span> <span class="refpurpose">— Print a part of the pinboard of the cell to STDOUT.</span></dt>

</dl>

</dd>

<dt><span class="section">[`PnfsManager` Commands](#rf-cc-pnfsm)</span></dt>

<dd>

<dl>

<dt><span class="refentrytitle">[<span class="command">**pnfsidof**</span>](#cmd-pnfsidof)</span> <span class="refpurpose">— Print the <span class="productname">`pnfs`</span> id of a file given by its global path.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**flags remove**</span>](#cmd-flags_remove)</span> <span class="refpurpose">— Remove a flag from a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**flags ls**</span>](#cmd-flags_ls)</span> <span class="refpurpose">— List the flags of a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**flags set**</span>](#cmd-flags_set)</span> <span class="refpurpose">— Set a flag for a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**metadataof**</span>](#cmd-metadataof)</span> <span class="refpurpose">— Print the meta-data of a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**pathfinder**</span>](#cmd-pathfinder)</span> <span class="refpurpose">— Print the global or local path of a file from its PNFS id.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**set meta**</span>](#cmd-set_meta)</span> <span class="refpurpose">— Set the meta-data of a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**storageinfoof**</span>](#cmd-storageinfoof)</span> <span class="refpurpose">— Print the storage info of a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**cacheinfoof**</span>](#cmd-cacheinfoof)</span> <span class="refpurpose">— Print the cache info of a file.</span></dt>

</dl>

</dd>

<dt><span class="section">[Pool Commands](#rf-cc-pool)</span></dt>

<dd>

<dl>

<dt><span class="refentrytitle">[<span class="command">**rep ls**</span>](#cmd-rep_ls)</span> <span class="refpurpose">— List the files currently in the repository of the pool.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**st set max active**</span>](#cmd-st_set_max_active)</span> <span class="refpurpose">— Set the maximum number of active store transfers.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**rh set max active**</span>](#cmd-rh_set_max_active)</span> <span class="refpurpose">— Set the maximum number of active restore transfers.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**mover set max active**</span>](#cmd-mover_set_max_active)</span> <span class="refpurpose">— Set the maximum number of active client transfers.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**mover set max active -queue=p2p**</span>](#cmd-p2p_set_max_active)</span> <span class="refpurpose">— Set the maximum number of active pool-to-pool server transfers.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**pp set max active**</span>](#cmd-pp_set_max_active)</span> <span class="refpurpose">— Set the value used for scaling the performance cost of pool-to-pool client transfers analogous to the other `set max active`-commands.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**set gap**</span>](#cmd-set_gap)</span> <span class="refpurpose">— Set the gap parameter - the size of free space below which it will be assumed that the pool is full within the cost calculations.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**set breakeven**</span>](#cmd-set_breakeven)</span> <span class="refpurpose">— Set the breakeven parameter - used within the cost calculations.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**mover ls**</span>](#cmd-mover_ls)</span> <span class="refpurpose">— List the active and waiting client transfer requests.</span></dt>

<dt><span class="refentrytitle">[migration cache](#cmd-migration-cache)</span> <span class="refpurpose">— Caches replicas on other pools.</span></dt>

<dt><span class="refentrytitle">[migration cancel](#cmd-migration-cancel)</span> <span class="refpurpose">— Cancels a migration job</span></dt>

<dt><span class="refentrytitle">[migration clear](#cmd-migration-clear)</span> <span class="refpurpose">— Removes completed migration jobs.</span></dt>

<dt><span class="refentrytitle">[migration concurrency](#cmd-migration-concurrency)</span> <span class="refpurpose">— Adjusts the concurrency of a job.</span></dt>

<dt><span class="refentrytitle">[migration copy](#cmd-migration-copy)</span> <span class="refpurpose">— Copies files to other pools.</span></dt>

<dt><span class="refentrytitle">[migration info](#cmd-migration-info)</span> <span class="refpurpose">— Shows detailed information about a migration job.</span></dt>

<dt><span class="refentrytitle">[migration ls](#cmd-migration-ls)</span> <span class="refpurpose">— Lists all migration jobs.</span></dt>

<dt><span class="refentrytitle">[migration move](#idp7509968)</span> <span class="refpurpose">— Moves replicas to other pools.</span></dt>

<dt><span class="refentrytitle">[migration suspend](#cmd-migration-suspend)</span> <span class="refpurpose">— Suspends a migration job.</span></dt>

<dt><span class="refentrytitle">[migration resume](#cmd-migration-resume)</span> <span class="refpurpose">— Resumes a suspended migration job.</span></dt>

</dl>

</dd>

<dt><span class="section">[`PoolManager` Commands](#rf-cc-pm)</span></dt>

<dd>

<dl>

<dt><span class="refentrytitle">[<span class="command">**rc ls**</span>](#cmd-rc_ls)</span> <span class="refpurpose">— List the requests currently handled by the `PoolManager`</span></dt>

<dt><span class="refentrytitle">[<span class="command">**cm ls**</span>](#cmd-cm_ls)</span> <span class="refpurpose">— List information about the pools in the [_cost module_](#gl-pm-comp-cm) cache.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**set pool decision**</span>](#cmd-set_pool_decision)</span> <span class="refpurpose">— Set the factors for the calculation of the total costs of the pools.</span></dt>

</dl>

</dd>

</dl>

</dd>

<dt><span class="chapter">[28\. <span class="productname">dCache</span> Default Port Values](#rf-ports)</span></dt>

<dt><span class="chapter">[29\. Glossary](#rf-glossary)</span></dt>

</dl>

</div>

<div class="chapter" title="Chapter 26\. dCache Clients">

<div class="titlepage">

<div>

<div>

## <a name="rf-clients"></a>Chapter 26\. <span class="productname">dCache</span> Clients

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[The `SRM` Client Suite](#rf-clients-srm)</span></dt>

<dd>

<dl>

<dt><span class="refentrytitle">[<span class="command">**srmcp**</span>](#cmd-srmcp)</span> <span class="refpurpose">— Copy a file from or to an `SRM` or between two `SRM`s.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**srmstage**</span>](#cmd-srmstage)</span> <span class="refpurpose">— Request staging of a file.</span></dt>

</dl>

</dd>

<dt><span class="section">[<span class="command">**dccp**</span>](#rf-clients-dccp)</span></dt>

<dd>

<dl>

<dt><span class="refentrytitle">[<span class="command">**<span class="command">**dccp**</span>**</span>](#cmd-dccp)</span> <span class="refpurpose">— Copy a file from or to a <span class="productname">dCache</span> server.</span></dt>

</dl>

</dd>

</dl>

</div>

<div class="section" title="The SRM Client Suite">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="rf-clients-srm"></a>The `SRM` Client Suite

</div>

</div>

</div>

An `SRM` URL has the form `srm://dmx.lbl.gov:6253//srm/DRM/srmv1?SFN=/tmp/try1` and the file URL looks like `file:////tmp/aaa`.

<div class="refentry" title="srmcp"><a name="cmd-srmcp"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**srmcp**</span></span>

<span class="command">**srmcp**</span> — Copy a file from or to an `SRM` or between two `SRM`s.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`srmcp` [`option`...] _<tt><sourceUrl></tt>_ _<tt><destUrl></tt>_

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">sourceUrl</span></dt>

<dd>

The URL of the source file.

</dd>

<dt><span class="term">destUrl</span></dt>

<dd>

The URL of the destination file.

</dd>

</dl>

</div>

<div class="variablelist" title="Options">

**Options**

<dl>

<dt><span class="term">`gss_expected_name`</span></dt>

<dd>

To enable the user to specify the gss expected name in the DN (Distinguished Name) of the srm server. The default value is `host`.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

If the CN of host where srm server is running is `CN=srm/tam01.fnal.gov`, then `gss_expected_name` should be `srm`.

    [user] $

</div>

</div>

</dd>

<dt><span class="term">`globus_tcp_port_range`</span></dt>

<dd>

To enable the user to specify a range of ports open for tcp connections as a pair of positive integers separated by <span class="quote">“<span class="quote">`:`</span>”</span>, not set by default.

This takes care of compute nodes that are behind firewall.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

`globus_tcp_port_range=40000:50000`

    [user] $

</div>

</div>

</dd>

<dt><span class="term">`streams_num`</span></dt>

<dd>

To enable the user to specify the number of streams to be used for data transfer. If set to 1, then stream mode is used, otherwise extended block mode is used.

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

</div>

</div>

</dd>

<dt><span class="term">`server_mode`</span></dt>

<dd>

To enable the user to set the (gridftp) server mode for data transfer. Can be `active` or `passive`, `passive` by default.

This option will have effect only if transfer is performed in a stream mode (see `streams_num`)

<div class="informalexample">

**Example:**

<div class="informalexamplebody">

    [user] $

</div>

</div>

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp6844544"></a>

## Description

</div>

</div>

<div class="refentry" title="srmstage">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-srmstage"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**srmstage**</span></span>

<span class="command">**srmstage**</span> — Request staging of a file.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`srmstage` [_<tt><srmUrl></tt>_...]

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">srmUrl</span></dt>

<dd>

The URL of the file which should be staged.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp6854032"></a>

## Description

Provides an option to the user to stage files from <abbr class="abbrev">HSM</abbr> to <span class="productname">dCache</span> and not transfer them to the user right away. This case will be useful if files are not needed right away at user end, but its good to stage them to dcache for faster access later.

</div>

</div>

</div>

<div class="section" title="dccp">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="rf-clients-dccp"></a><span class="command">**dccp**</span>

</div>

</div>

</div>

<div class="refentry" title="dccp"><a name="cmd-dccp"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**<span class="command">**dccp**</span>**</span></span>

<span class="command">**<span class="command">**dccp**</span>**</span> — Copy a file from or to a <span class="productname">dCache</span> server.

</div>

<div class="refsynopsisdiv" title="Synopsis"><a name="rf-clients-dccp-synopsis"></a>

## Synopsis

<div class="cmdsynopsis">

`<span class="command">**dccp**</span>` [`option`...] _<tt><sourceUrl></tt>_ _<tt><destUrl></tt>_

</div>

</div>

<div class="refsect1" title="Arguments"><a name="rf-clients-dccp-synopsis-options"></a>

## Arguments

The following arguments are required:

<div class="variablelist">

<dl>

<dt><span class="term">`sourceUrl`</span></dt>

<dd>

The <acronym class="acronym">URL</acronym> of the source file.

</dd>

<dt><span class="term">`destUrl`</span></dt>

<dd>

The <acronym class="acronym">URL</acronym> of the destination file.

</dd>

</dl>

</div>

</div>

<div class="refsect1" title="Description"><a name="rf-clients-dccp-synopsis-description"></a>

## Description

The <span class="command">**dccp**</span> utility provides a <span class="command">**cp**</span>(1) like functionality on the <span class="productname">dCache</span> file system. The source must be a single file while the destination could be a directory name or a file name. If the directory is a destination, a new file with the same name as the source name will be created there and the contents of the source will be copied. If the final destination file exists in <span class="productname">dCache</span>, it won’t be overwritten and an error code will be returned. Files in regular file systems will always be overwritten if the `-i` option is not specified. If the source and the final destination file are located on a regular file system, the <span class="command">**dccp**</span> utility can be used similar to the <span class="command">**cp**</span>(1) program.

</div>

<div class="refsect1" title="Options"><a name="rf-clients-dccp-synopsis-optional"></a>

## Options

The following arguments are optional:

<div class="variablelist">

<dl>

<dt><span class="term">`-a`</span></dt>

<dd>

Enable read-ahead functionality.

</dd>

<dt><span class="term">`-b` _<tt><bufferSize></tt>_</span></dt>

<dd>

Set read-ahead buffer size. The default value is `1048570` Bytes. To disable the buffer this can be set to any value below the default. dccp will attempt to allocate the buffer size so very large values should be used with care.

</dd>

<dt><span class="term">`-B` _<tt><bufferSize></tt>_</span></dt>

<dd>

Set buffer size. The size of the buffer is requested in each request, larger buffers will be needed to saturate higher bandwidth connections. The optimum value is network dependent. Too large a value will lead to excessive memory usage, too small a value will lead to excessive network communication.

</dd>

<dt><span class="term">`-d` _<tt><debug level></tt>_</span></dt>

<dd>

Set the debug level. _<tt><debug level></tt>_ is a integer between `0` and `127`. If the value is `0` then no output is generated, otherwise the value is formed by adding together one or more of the following values:

<div class="segmentedlist">

<table border="0">

<thead>

<tr class="segtitle">

<th>Value</th>

<th>Enabled output</th>

</tr>

</thead>

<tbody>

<tr class="seglistitem">

<td class="seg">1</td>

<td class="seg">Error messages</td>

</tr>

<tr class="seglistitem">

<td class="seg">2</td>

<td class="seg">Info messages</td>

</tr>

<tr class="seglistitem">

<td class="seg">4</td>

<td class="seg">Timing information</td>

</tr>

<tr class="seglistitem">

<td class="seg">8</td>

<td class="seg">Trace information</td>

</tr>

<tr class="seglistitem">

<td class="seg">16</td>

<td class="seg">Show stack-trace</td>

</tr>

<tr class="seglistitem">

<td class="seg">32</td>

<td class="seg">IO operations</td>

</tr>

<tr class="seglistitem">

<td class="seg">32</td>

<td class="seg">IO operations</td>

</tr>

<tr class="seglistitem">

<td class="seg">64</td>

<td class="seg">Thread information</td>

</tr>

</tbody>

</table>

</div>

</dd>

<dt><span class="term">`-h` _<tt><replyHostName></tt>_</span></dt>

<dd>

Bind the callback connection to the specific hostname interface.

</dd>

<dt><span class="term">`-i`</span></dt>

<dd>

Secure mode. Do not overwrite the existing files.

</dd>

<dt><span class="term">`-l` _<tt><location></tt>_</span></dt>

<dd>

Set location for pre-stage. if the location is not specified, the local host of the door will be used. This option must be used with the -P option.

</dd>

<dt><span class="term">`-p` _<tt><first_port></tt>_:_<tt><last_port></tt>_</span></dt>

<dd>

Bind the callback data connection to the specified `TCP` port/rangeSet port range. Delimited by the ’:’ character, the _<tt><first_port></tt>_ is required but the _<tt><last_port></tt>_ is optional.

</dd>

<dt><span class="term">`-P`</span></dt>

<dd>

Pre-stage. Do not copy the file to a local host but make sure the file is on disk on the <span class="productname">dCache</span> server.

</dd>

<dt><span class="term">`-r` _<tt><bufferSize></tt>_</span></dt>

<dd>

`TCP` receive buffer size. The default is `256K`. Setting to `0` uses the system default value. Memory useage will increase with higher values, but performance better.

</dd>

<dt><span class="term">`-s` _<tt><bufferSize></tt>_</span></dt>

<dd>

`TCP` send buffer size. The default is `256K`. Setting to `0` uses the system default value.

</dd>

<dt><span class="term">`-t` _<tt><time></tt>_</span></dt>

<dd>

Stage timeout in seconds. This option must be used with the `-P` option.

</dd>

</dl>

</div>

</div>

<div class="refsect1" title="Examples:"><a name="rf-clients-dccp-example"></a>

## Examples:

To copy a file to <span class="productname">dCache</span>:

    [user] $

To copy a file from <span class="productname">dCache</span>:

    [user] $

Pre-Stage request:

    [user] $

stdin:

    [user] $

stdout:

    [user] $

</div>

<div class="refsect1" title="See also"><a name="rf-clients-dccp-seealso"></a>

## See also

<span class="citerefentry"><span class="refentrytitle">cp</span></span>

</div>

</div>

</div>

</div>

<div class="chapter" title="Chapter 27\. dCache Cell Commands">

<div class="titlepage">

<div>

<div>

## <a name="rf-cc"></a>Chapter 27\. <span class="productname">dCache</span> Cell Commands

</div>

</div>

</div>

<div class="toc">

**Table of Contents**

<dl>

<dt><span class="section">[Common Cell Commands](#rf-cc-common)</span></dt>

<dd>

<dl>

<dt><span class="refentrytitle">[<span class="command">**pin**</span>](#cmd-pin)</span> <span class="refpurpose">— Adds a comment to the pinboard.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**info**</span>](#cmd-info)</span> <span class="refpurpose">— Print info about the cell.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**dump pinboard**</span>](#cmd-dump_pinboard)</span> <span class="refpurpose">— Dump the full pinboard of the cell to a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**show pinboard**</span>](#cmd-show_pinboard)</span> <span class="refpurpose">— Print a part of the pinboard of the cell to STDOUT.</span></dt>

</dl>

</dd>

<dt><span class="section">[`PnfsManager` Commands](#rf-cc-pnfsm)</span></dt>

<dd>

<dl>

<dt><span class="refentrytitle">[<span class="command">**pnfsidof**</span>](#cmd-pnfsidof)</span> <span class="refpurpose">— Print the <span class="productname">`pnfs`</span> id of a file given by its global path.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**flags remove**</span>](#cmd-flags_remove)</span> <span class="refpurpose">— Remove a flag from a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**flags ls**</span>](#cmd-flags_ls)</span> <span class="refpurpose">— List the flags of a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**flags set**</span>](#cmd-flags_set)</span> <span class="refpurpose">— Set a flag for a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**metadataof**</span>](#cmd-metadataof)</span> <span class="refpurpose">— Print the meta-data of a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**pathfinder**</span>](#cmd-pathfinder)</span> <span class="refpurpose">— Print the global or local path of a file from its PNFS id.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**set meta**</span>](#cmd-set_meta)</span> <span class="refpurpose">— Set the meta-data of a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**storageinfoof**</span>](#cmd-storageinfoof)</span> <span class="refpurpose">— Print the storage info of a file.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**cacheinfoof**</span>](#cmd-cacheinfoof)</span> <span class="refpurpose">— Print the cache info of a file.</span></dt>

</dl>

</dd>

<dt><span class="section">[Pool Commands](#rf-cc-pool)</span></dt>

<dd>

<dl>

<dt><span class="refentrytitle">[<span class="command">**rep ls**</span>](#cmd-rep_ls)</span> <span class="refpurpose">— List the files currently in the repository of the pool.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**st set max active**</span>](#cmd-st_set_max_active)</span> <span class="refpurpose">— Set the maximum number of active store transfers.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**rh set max active**</span>](#cmd-rh_set_max_active)</span> <span class="refpurpose">— Set the maximum number of active restore transfers.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**mover set max active**</span>](#cmd-mover_set_max_active)</span> <span class="refpurpose">— Set the maximum number of active client transfers.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**mover set max active -queue=p2p**</span>](#cmd-p2p_set_max_active)</span> <span class="refpurpose">— Set the maximum number of active pool-to-pool server transfers.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**pp set max active**</span>](#cmd-pp_set_max_active)</span> <span class="refpurpose">— Set the value used for scaling the performance cost of pool-to-pool client transfers analogous to the other `set max active`-commands.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**set gap**</span>](#cmd-set_gap)</span> <span class="refpurpose">— Set the gap parameter - the size of free space below which it will be assumed that the pool is full within the cost calculations.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**set breakeven**</span>](#cmd-set_breakeven)</span> <span class="refpurpose">— Set the breakeven parameter - used within the cost calculations.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**mover ls**</span>](#cmd-mover_ls)</span> <span class="refpurpose">— List the active and waiting client transfer requests.</span></dt>

<dt><span class="refentrytitle">[migration cache](#cmd-migration-cache)</span> <span class="refpurpose">— Caches replicas on other pools.</span></dt>

<dt><span class="refentrytitle">[migration cancel](#cmd-migration-cancel)</span> <span class="refpurpose">— Cancels a migration job</span></dt>

<dt><span class="refentrytitle">[migration clear](#cmd-migration-clear)</span> <span class="refpurpose">— Removes completed migration jobs.</span></dt>

<dt><span class="refentrytitle">[migration concurrency](#cmd-migration-concurrency)</span> <span class="refpurpose">— Adjusts the concurrency of a job.</span></dt>

<dt><span class="refentrytitle">[migration copy](#cmd-migration-copy)</span> <span class="refpurpose">— Copies files to other pools.</span></dt>

<dt><span class="refentrytitle">[migration info](#cmd-migration-info)</span> <span class="refpurpose">— Shows detailed information about a migration job.</span></dt>

<dt><span class="refentrytitle">[migration ls](#cmd-migration-ls)</span> <span class="refpurpose">— Lists all migration jobs.</span></dt>

<dt><span class="refentrytitle">[migration move](#idp7509968)</span> <span class="refpurpose">— Moves replicas to other pools.</span></dt>

<dt><span class="refentrytitle">[migration suspend](#cmd-migration-suspend)</span> <span class="refpurpose">— Suspends a migration job.</span></dt>

<dt><span class="refentrytitle">[migration resume](#cmd-migration-resume)</span> <span class="refpurpose">— Resumes a suspended migration job.</span></dt>

</dl>

</dd>

<dt><span class="section">[`PoolManager` Commands](#rf-cc-pm)</span></dt>

<dd>

<dl>

<dt><span class="refentrytitle">[<span class="command">**rc ls**</span>](#cmd-rc_ls)</span> <span class="refpurpose">— List the requests currently handled by the `PoolManager`</span></dt>

<dt><span class="refentrytitle">[<span class="command">**cm ls**</span>](#cmd-cm_ls)</span> <span class="refpurpose">— List information about the pools in the [_cost module_](#gl-pm-comp-cm) cache.</span></dt>

<dt><span class="refentrytitle">[<span class="command">**set pool decision**</span>](#cmd-set_pool_decision)</span> <span class="refpurpose">— Set the factors for the calculation of the total costs of the pools.</span></dt>

</dl>

</dd>

</dl>

</div>

This is the reference to all (important) cell commands in <span class="productname">dCache</span>. You should not use any command not documented here, unless you really know what you are doing. Commands not in this reference are used for debugging by the developers.

This chapter serves two purposes: The other parts of this book refer to it, whenever a command is mentioned. Secondly, an administrator may check here, if he wonders what a command does.

<div class="section" title="Common Cell Commands">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="rf-cc-common"></a>Common Cell Commands

</div>

</div>

</div>

<div class="refentry" title="pin"><a name="cmd-pin"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**pin**</span></span>

<span class="command">**pin**</span> — Adds a comment to the pinboard.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`pin` _<tt><comment></tt>_

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">comment</span></dt>

<dd>

A string which is added to the pinboard.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp6958976"></a>

## Description

</div>

</div>

<div class="refentry" title="info">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-info"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**info**</span></span>

<span class="command">**info**</span> — Print info about the cell.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`info` [-a] [-l]

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">-a</span></dt>

<dd>

Display more information.

</dd>

<dt><span class="term">-l</span></dt>

<dd>

Display long information.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp6970752"></a>

## Description

The info printed by <span class="command">**info**</span> depends on the cell class.

</div>

</div>

<div class="refentry" title="dump pinboard">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-dump_pinboard"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**dump pinboard**</span></span>

<span class="command">**dump pinboard**</span> — Dump the full pinboard of the cell to a file.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`dump pinboard` _<tt><filename></tt>_

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">filename</span></dt>

<dd>

The file the current content of the pinboard is stored in.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp6982160"></a>

## Description

</div>

</div>

<div class="refentry" title="show pinboard">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-show_pinboard"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**show pinboard**</span></span>

<span class="command">**show pinboard**</span> — Print a part of the pinboard of the cell to STDOUT.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`show pinboard` [ _<tt><lines></tt>_ ]

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">lines</span></dt>

<dd>

The number of lines which are displayed. Default: all.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp6991664"></a>

## Description

</div>

</div>

</div>

<div class="section" title="PnfsManager Commands">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="rf-cc-pnfsm"></a>`PnfsManager` Commands

</div>

</div>

</div>

<div class="refentry" title="pnfsidof"><a name="cmd-pnfsidof"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**pnfsidof**</span></span>

<span class="command">**pnfsidof**</span> — Print the <span class="productname">`pnfs`</span> id of a file given by its global path.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`pnfsidof` _<tt><globalPath></tt>_

</div>

</div>

<div class="refsection" title="Description"><a name="idp7005392"></a>

## Description

Print the <span class="productname">`pnfs`</span> id of a file given by its global path. The global path always starts with the <span class="quote">“<span class="quote">VirtualGlobalPath</span>”</span> as given by the <span class="quote">“<span class="quote"><span class="command">**info**</span></span>”</span>-command.

</div>

</div>

<div class="refentry" title="flags remove">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-flags_remove"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**flags remove**</span></span>

<span class="command">**flags remove**</span> — Remove a flag from a file.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`flags remove` _<tt><pnfsId></tt>_ _<tt><key></tt>_ ...

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">pnfsId</span></dt>

<dd>

The <span class="productname">`pnfs`</span> id of the file of which a flag will be removed.

</dd>

<dt><span class="term">key</span></dt>

<dd>

flags which will be removed.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7022128"></a>

## Description

</div>

</div>

<div class="refentry" title="flags ls">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-flags_ls"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**flags ls**</span></span>

<span class="command">**flags ls**</span> — List the flags of a file.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`flags ls` _<tt><pnfsId></tt>_

</div>

<div class="variablelist">

<dl>

<dt><span class="term">pnfsId</span></dt>

<dd>

The <span class="productname">`pnfs`</span> id of the file of which a flag will be listed.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7032624"></a>

## Description

</div>

</div>

<div class="refentry" title="flags set">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-flags_set"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**flags set**</span></span>

<span class="command">**flags set**</span> — Set a flag for a file.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`flags set` _<tt><pnfsId></tt>_ _<tt><key></tt>_=_<tt><value></tt>_ ...

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">pnfsId</span></dt>

<dd>

The <span class="productname">`pnfs`</span> id of the file of which flags will be set.

</dd>

<dt><span class="term">key</span></dt>

<dd>

The flag which will be set.

</dd>

<dt><span class="term">value</span></dt>

<dd>

The value to which the flag will be set.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7048416"></a>

## Description

</div>

</div>

<div class="refentry" title="metadataof">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-metadataof"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**metadataof**</span></span>

<span class="command">**metadataof**</span> — Print the meta-data of a file.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`metadataof` [ _<tt><pnfsId></tt>_ ] | [ _<tt><globalPath></tt>_ ] [-v] [-n] [-se]

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">pnfsId</span></dt>

<dd>

The <span class="productname">`pnfs`</span> id of the file.

</dd>

<dt><span class="term">globalPath</span></dt>

<dd>

The global path of the file.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7066832"></a>

## Description

</div>

</div>

<div class="refentry" title="pathfinder">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-pathfinder"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**pathfinder**</span></span>

<span class="command">**pathfinder**</span> — Print the global or local path of a file from its PNFS id.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`pathfinder` _<tt><pnfsId></tt>_ [[-global] | [-local]]

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">pnfsId</span></dt>

<dd>

The <span class="productname">`pnfs`</span> Id of the file.

</dd>

<dt><span class="term">-global</span></dt>

<dd>

Print the global path of the file.

</dd>

<dt><span class="term">-local</span></dt>

<dd>

Print the local path of the file.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7083968"></a>

## Description

</div>

</div>

<div class="refentry" title="set meta">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-set_meta"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**set meta**</span></span>

<span class="command">**set meta**</span> — Set the meta-data of a file.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`set meta` [_<tt><pnfsId></tt>_] | [_<tt><globalPath></tt>_] _<tt><uid></tt>_ _<tt><gid></tt>_ _<tt><perm></tt>_ _<tt><levelInfo></tt>_...

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">pnfsId</span></dt>

<dd>

The <span class="productname">`pnfs`</span> id of the file.

</dd>

<dt><span class="term">globalPath</span></dt>

<dd>

The global path oa the file.

</dd>

<dt><span class="term">uid</span></dt>

<dd>

The user id of the new owner of the file.

</dd>

<dt><span class="term">gid</span></dt>

<dd>

The new group id of the file.

</dd>

<dt><span class="term">perm</span></dt>

<dd>

The new file permitions.

</dd>

<dt><span class="term">levelInfo</span></dt>

<dd>

The new level information of the file.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7107296"></a>

## Description

</div>

</div>

<div class="refentry" title="storageinfoof">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-storageinfoof"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**storageinfoof**</span></span>

<span class="command">**storageinfoof**</span> — Print the storage info of a file.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`storageinfoof` [_<tt><pnfsId></tt>_] | [_<tt><globalPath></tt>_] [-v] [-n] [-se]

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">pnfsId</span></dt>

<dd>

The <span class="productname">`pnfs`</span> id of the file.

</dd>

<dt><span class="term">globalPath</span></dt>

<dd>

The global path oa the file.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7124352"></a>

## Description

</div>

</div>

<div class="refentry" title="cacheinfoof">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-cacheinfoof"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**cacheinfoof**</span></span>

<span class="command">**cacheinfoof**</span> — Print the cache info of a file.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`cacheinfoof` [_<tt><pnfsId></tt>_] | [_<tt><globalPath></tt>_]

</div>

<div class="variablelist" title="Arguments">

**Arguments**

<dl>

<dt><span class="term">pnfsId</span></dt>

<dd>

The <span class="productname">`pnfs`</span> id of the file.

</dd>

<dt><span class="term">globalPath</span></dt>

<dd>

The global path oa the file.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7137968"></a>

## Description

</div>

</div>

</div>

<div class="section" title="Pool Commands">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="rf-cc-pool"></a>Pool Commands

</div>

</div>

</div>

<div class="refentry" title="rep ls"><a name="cmd-rep_ls"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**rep ls**</span></span>

<span class="command">**rep ls**</span> — List the files currently in the repository of the pool.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`rep ls` [pnfsId...] | [-l= s | p | l | u | nc | e ... ] [-s= k | m | g | t ]

</div>

<div class="variablelist">

<dl>

<dt><span class="term">pnfsId</span></dt>

<dd>

The <span class="productname">`pnfs`</span> ID(s) for which the files in the repository will be listed.

</dd>

<dt><span class="term">-l</span></dt>

<dd>

List only the files with one of the following properties:

<pre class="screen">s      sticky files
p      precious files
l      locked files
u      files in use
nc     files which are not cached
e      files with an error condition</pre>

</dd>

<dt><span class="term">-s</span></dt>

<dd>

Unit, the filesize is shown:

<pre class="screen">k      data amount in KBytes
m      data amount in MBytes
g      data amount in GBytes
t      data amount in TBytes</pre>

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7169808"></a>

## Description

</div>

</div>

<div class="refentry" title="st set max active">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-st_set_max_active"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**st set max active**</span></span>

<span class="command">**st set max active**</span> — Set the maximum number of active store transfers.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`st set max active` _<tt><maxActiveStoreTransfers></tt>_

</div>

<div class="variablelist">

<dl>

<dt><span class="term">maxActiveStoreTransfers</span></dt>

<dd>

The maximum number of active store transfers.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7179328"></a>

## Description

Any further requests will be queued. This value will also be used by the [_cost module_](#gl-pm-comp-cm) for calculating the [_performance cost_](#gl-performance_cost).

</div>

</div>

<div class="refentry" title="rh set max active">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-rh_set_max_active"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**rh set max active**</span></span>

<span class="command">**rh set max active**</span> — Set the maximum number of active restore transfers.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`rh set max active` _<tt><maxActiveRetoreTransfers></tt>_

</div>

<div class="variablelist">

<dl>

<dt><span class="term">maxActiveRetoreTransfers</span></dt>

<dd>

The maximum number of active restore transfers.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7190432"></a>

## Description

Any further requests will be queued. This value will also be used by the [_cost module_](#gl-pm-comp-cm) for calculating the [_performance cost_](#gl-performance_cost).

</div>

</div>

<div class="refentry" title="mover set max active">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-mover_set_max_active"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**mover set max active**</span></span>

<span class="command">**mover set max active**</span> — Set the maximum number of active client transfers.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`mover set max active` _<tt><maxActiveClientTransfers></tt>_ [`-queue=_<tt><moverQueueName></tt>_`]

</div>

<div class="variablelist">

<dl>

<dt><span class="term">maxActiveClientTransfers</span></dt>

<dd>

The maximum number of active client transfers.

</dd>

<dt><span class="term">moverQueueName</span></dt>

<dd>

The mover queue for which the maximum number of active transfers should be set. If this is not specified, the default queue is assumed, in order to be compatible with previous versions which did not support multiple mover queues (before version 1.6.6).

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7204832"></a>

## Description

Any further requests will be queued. This value will also be used by the [_cost module_](#gl-pm-comp-cm) for calculating the [_performance cost_](#gl-performance_cost).

</div>

</div>

<div class="refentry" title="mover set max active -queue=p2p">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-p2p_set_max_active"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**mover set max active -queue=p2p**</span></span>

<span class="command">**mover set max active -queue=p2p**</span> — Set the maximum number of active pool-to-pool server transfers.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`mover set max active -queue=p2p` _<tt><maxActiveP2PTransfers></tt>_

</div>

<div class="variablelist">

<dl>

<dt><span class="term">maxActiveP2PTransfers</span></dt>

<dd>

The maximum number of active pool-to-pool server transfers.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7215968"></a>

## Description

Any further requests will be queued. This value will also be used by the [_cost module_](#gl-pm-comp-cm) for calculating the [_performance cost_](#gl-performance_cost).

</div>

</div>

<div class="refentry" title="pp set max active">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-pp_set_max_active"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**pp set max active**</span></span>

<span class="command">**pp set max active**</span> — Set the value used for scaling the performance cost of pool-to-pool client transfers analogous to the other `set max active`-commands.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`pp set max active` _<tt><maxActivePPTransfers></tt>_

</div>

<div class="variablelist">

<dl>

<dt><span class="term">maxActivePPTransfers</span></dt>

<dd>

The new scaling value for the cost calculation.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7227840"></a>

## Description

All pool-to-pool client requests will be performed immediately in order to avoid deadlocks. This value will only used by the [_cost module_](#gl-pm-comp-cm) for calculating the [_performance cost_](#gl-performance_cost).

</div>

</div>

<div class="refentry" title="set gap">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-set_gap"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**set gap**</span></span>

<span class="command">**set gap**</span> — Set the gap parameter - the size of free space below which it will be assumed that the pool is full within the cost calculations.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`set gap` _<tt><gapPara></tt>_

</div>

<div class="variablelist">

<dl>

<dt><span class="term">gapPara</span></dt>

<dd>

The size of free space below which it will be assumed that the pool is full. Default is 4GB.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7240368"></a>

## Description

The gap parameter is used within the space cost calculation scheme described in [the section called “The Space Cost”](#cf-pm-classic-space "The Space Cost"). It specifies the size of free space below which it will be assumed that the pool is full and consequently the least recently used file has to be removed if a new file has to be stored on the pool. If, on the other hand, the free space is greater than gapPara, it will be expensive to store a file on the pool which exceeds the free space.

</div>

</div>

<div class="refentry" title="set breakeven">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-set_breakeven"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**set breakeven**</span></span>

<span class="command">**set breakeven**</span> — Set the breakeven parameter - used within the cost calculations.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`set breakeven` _<tt><breakevenPara></tt>_

</div>

<div class="variablelist">

<dl>

<dt><span class="term">breakevenPara</span></dt>

<dd>

The breakeven parameter has to be a positive number smaller than 1.0\. It specifies the impact of the age of the [_least recently used file_](#gl-lru) on space cost. It the LRU file is one week old, the space cost will be equal to `(1 + breakeven)`. Note that this will not be true, if the breakeven parameter has been set to a value greater or equal to 1.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7253104"></a>

## Description

The breakeven parameter is used within the space cost calculation scheme described in [the section called “The Space Cost”](#cf-pm-classic-space "The Space Cost").

</div>

</div>

<div class="refentry" title="mover ls">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-mover_ls"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**mover ls**</span></span>

<span class="command">**mover ls**</span> — List the active and waiting client transfer requests.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`mover ls` [ -queue | -queue=_<tt><queueName></tt>_ ]

</div>

<div class="variablelist">

<dl>

<dt><span class="term">queueName</span></dt>

<dd>

The name of the mover queue for which the transfers should be listed.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7265264"></a>

## Description

Without parameter all transfers are listed. With `-queue` all requests sorted according to the mover queue are listed. If a queue is explicitly specified, only transfers in that mover queue are listed.

</div>

</div>

<div class="refentry" title="migration cache">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-migration-cache"></a>

<div class="refnamediv">

## migration cache

migration cache — Caches replicas on other pools.

</div>

<div class="refsynopsisdiv" title="SYNOPSIS">

## SYNOPSIS

<div class="cmdsynopsis">

`migration cache` [_<tt><options></tt>_] _<tt><target></tt>_...

</div>

</div>

<div class="refsect1" title="DESCRIPTION"><a name="idp7273136"></a>

## DESCRIPTION

Caches replicas on other pools. Similar to <span class="command">**migration copy**</span>, but with different defaults. See <span class="command">**migration copy**</span> for a description of all options. Equivalent to: <span class="command">**migration copy**</span> -smode=same -tmode=cached

</div>

</div>

<div class="refentry" title="migration cancel">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-migration-cancel"></a>

<div class="refnamediv">

## migration cancel

migration cancel — Cancels a migration job

</div>

<div class="refsynopsisdiv" title="SYNOPSIS">

## SYNOPSIS

<div class="cmdsynopsis">

`migration cancel` [-force] job

</div>

</div>

<div class="refsect1" title="DESCRIPTION"><a name="idp7282240"></a>

## DESCRIPTION

Cancels the given migration job. By default ongoing transfers are allowed to finish gracefully.

</div>

</div>

<div class="refentry" title="migration clear">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-migration-clear"></a>

<div class="refnamediv">

## migration clear

migration clear — Removes completed migration jobs.

</div>

<div class="refsynopsisdiv" title="SYNOPSIS">

## SYNOPSIS

<div class="cmdsynopsis">

`migration clear`

</div>

</div>

<div class="refsect1" title="DESCRIPTION"><a name="idp7287296"></a>

## DESCRIPTION

Removes completed migration jobs. For reference, information about migration jobs are kept until explicitly cleared.

</div>

</div>

<div class="refentry" title="migration concurrency">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-migration-concurrency"></a>

<div class="refnamediv">

## migration concurrency

migration concurrency — Adjusts the concurrency of a job.

</div>

<div class="refsynopsisdiv" title="SYNOPSIS">

## SYNOPSIS

<div class="cmdsynopsis">

`migration concurrency` _<tt><job></tt>_ _<tt><n></tt>_

</div>

</div>

<div class="refsect1" title="DESCRIPTION"><a name="idp7294496"></a>

## DESCRIPTION

Sets the concurrency of _<tt><job></tt>_ to _<tt><n></tt>_.

</div>

</div>

<div class="refentry" title="migration copy">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-migration-copy"></a>

<div class="refnamediv">

## migration copy

migration copy — Copies files to other pools.

</div>

<div class="refsynopsisdiv" title="SYNOPSIS">

## SYNOPSIS

<div class="cmdsynopsis">

`migration copy` [_<tt><options></tt>_] _<tt><target></tt>_...

</div>

</div>

<div class="refsect1" title="DESCRIPTION"><a name="idp7302448"></a>

## DESCRIPTION

Copies files to other pools. Unless filter options are specified, all files on the source pool are copied.

The operation is idempotent, that is, it can safely be repeated without creating extra copies of the files. If the replica exists on any of the target pools, then it is not copied again. If the target pool with the existing replica fails to respond, then the operation is retried indefinitely, unless the job is marked as eager.

Please notice that a job is only idempotent as long as the set of target pools does not change. If pools go offline or are excluded as a result of an exclude or include expression then the job may stop being idempotent.

Both the state of the local replica and that of the target replica can be specified. If the target replica already exists, the state is updated to be at least as strong as the specified target state, that is, the lifetime of sticky bits is extended, but never reduced, and cached can be changed to precious, but never the opposite.

Transfers are subject to the checksum computiton policy of the target pool. Thus checksums are verified if and only if the target pool is configured to do so. For existing replicas, the checksum is only verified if the verify option was specified on the migration job.

Jobs can be marked permanent. Permanent jobs never terminate and are stored in the pool setup file with the <span class="command">**save**</span> command. Permanent jobs watch the repository for state changes and copy any replicas that match the selection criteria, even replicas added after the job was created. Notice that any state change will cause a replica to be reconsidered and enqueued if it matches the selection criteria — also replicas that have been copied before.

Several options allow an expression to be specified. The following operators are recognized: `<`, `<=`, `==`, `!=`, `>=`, `>`, `lt`, `le`, `eq`, `ne`, `ge`, `gt`, `~=`, `!~`, `+`, `-`, `*`, `/`, `%`, `div`, `mod`, `|`, `&`, `^`, `~`, `&&`, `||`, `!`, `and`, `or`, `not`, `?:`, `=`. Literals may be integer literals, floating point literals, single or double quoted string literals, and boolean true and false. Depending on the context, the expression may refer to constants.

Please notice that the list of supported operators may change in future releases. For permanent jobs we recommend to limit expressions to the basic operators `<`, `<=`, `==`, `!=`, `>=`, `>`, `+`, `-`, `*`, `/`, `&&`, `||` and `!`.

<div class="variablelist" title="Options">

**Options**

<dl>

<dt><span class="term">-accessed=_<tt><n></tt>_|[_<tt><n></tt>_]..[_<tt><m></tt>_]</span></dt>

<dd>

Only copy replicas accessed _<tt><n></tt>_ seconds ago, or accessed within the given, possibly open-ended, interval; e.g. `-accessed=0..60` matches files accessed within the last minute; `-accesed=60..` matches files accessed one minute or more ago.

</dd>

<dt><span class="term">-al=ONLINE|NEARLINE</span></dt>

<dd>

Only copy replicas with the given access latency.

</dd>

<dt><span class="term">-pnfsid=_<tt><pnfsid></tt>_[,_<tt><pnfsid></tt>_] ...</span></dt>

<dd>

Only copy replicas with one of the given PNFS IDs.

</dd>

<dt><span class="term">-rp=CUSTODIAL|REPLICA|OUTPUT</span></dt>

<dd>

Only copy replicas with the given retention policy.

</dd>

<dt><span class="term">-size=_<tt><n></tt>_|[_<tt><n></tt>_]..[_<tt><m></tt>_]</span></dt>

<dd>

Only copy replicas with size _<tt><n></tt>_, or a size within the given, possibly open-ended, interval.

</dd>

<dt><span class="term">-state=cached|precious</span></dt>

<dd>

Only copy replicas in the given state.

</dd>

<dt><span class="term">-sticky[=_<tt><owner></tt>_[,_<tt><owner></tt>_...]]</span></dt>

<dd>

Only copy sticky replicas. Can optionally be limited to the list of owners. A sticky flag for each owner must be present for the replica to be selected.

</dd>

<dt><span class="term">-storage=_<tt><class></tt>_</span></dt>

<dd>

Only copy replicas with the given storage class.

</dd>

<dt><span class="term">-concurrency=_<tt><concurrency></tt>_</span></dt>

<dd>

Specifies how many concurrent transfers to perform. Defaults to 1.

</dd>

<dt><span class="term">-order=[-]size|[-]lru</span></dt>

<dd>

Sort transfer queue. By default transfers are placed in ascending order, that is, smallest and least recently used first. Transfers are placed in descending order if the key is prefixed by a minus sign. Failed transfers are placed at the end of the queue for retry regardless of the order. This option cannot be used for permanent jobs. Notice that for pools with a large number of files, sorting significantly increases the initialization time of the migration job.

<div class="variablelist">

<dl>

<dt><span class="term">size</span></dt>

<dd>

Sort according to file size.

</dd>

<dt><span class="term">lru</span></dt>

<dd>

Sort according to last access time.

</dd>

</dl>

</div>

</dd>

<dt><span class="term">-pins=move|keep</span></dt>

<dd>

Controls how sticky flags owned by the `PinManager` are handled:

<div class="variablelist">

<dl>

<dt><span class="term">move</span></dt>

<dd>

Ask `PinManager` to move pins to the target pool.

</dd>

<dt><span class="term">keep</span></dt>

<dd>

Keep pins on the source pool.

</dd>

</dl>

</div>

</dd>

<dt><span class="term">-smode=same|cached|precious|removable|delete[+_<tt><owner></tt>_[(_<tt><lifetime></tt>_)] ...]</span></dt>

<dd>

Update the local replica to the given mode after transfer:

<div class="variablelist">

<dl>

<dt><span class="term">same</span></dt>

<dd>

does not change the local state (this is the default).

</dd>

<dt><span class="term">cached</span></dt>

<dd>

marks it cached.

</dd>

<dt><span class="term">precious</span></dt>

<dd>

marks it precious.

</dd>

<dt><span class="term">removable</span></dt>

<dd>

marks it cached and strips all existing sticky flags exluding pins.

</dd>

<dt><span class="term">delete</span></dt>

<dd>

deletes the replica unless it is pinned.

</dd>

</dl>

</div>

An optional list of sticky flags can be specified. The lifetime is in seconds. A lifetime of 0 causes the flag to immediately expire. Notice that existing sticky flags of the same owner are overwritten.

</dd>

<dt><span class="term">-tmode=same|cached|precious[+_<tt><owner></tt>_[(_<tt><lifetime></tt>_)]...]</span></dt>

<dd>

Set the mode of the target replica:

<div class="variablelist">

<dl>

<dt><span class="term">same</span></dt>

<dd>

applies the state and sticky bits excluding pins of the local replica (this is the default).

</dd>

<dt><span class="term">cached</span></dt>

<dd>

marks it cached.

</dd>

<dt><span class="term">precious</span></dt>

<dd>

marks it precious.

</dd>

</dl>

</div>

An optional list of sticky flags can be specified. The lifetime is in seconds.

</dd>

<dt><span class="term">-verify</span></dt>

<dd>Force checksum computation when an existing target is updated.</dd>

<dt><span class="term">-eager</span></dt>

<dd>

Copy replicas rather than retrying when pools with existing replicas fail to respond.

</dd>

<dt><span class="term">-exclude=_<tt><pool></tt>_[,_<tt><pool></tt>_...]</span></dt>

<dd>

Exclude target pools. Single character (`?`) and multi character (`*`) wildcards may be used.

</dd>

<dt><span class="term">-exclude-when=_<tt><expression></tt>_</span></dt>

<dd>

Exclude target pools for which the expression evaluates to true. The expression may refer to the following constants:

<div class="variablelist">

<dl>

<dt><span class="term">source.name or target.name</span></dt>

<dd>

pool name

</dd>

<dt><span class="term">source.spaceCost or target.spaceCost</span></dt>

<dd>

space cost

</dd>

<dt><span class="term">source.cpuCost or target.cpuCost</span></dt>

<dd>

cpu cost

</dd>

<dt><span class="term">source.free or target.free</span></dt>

<dd>

free space in bytes

</dd>

<dt><span class="term">source.total or target.total</span></dt>

<dd>

total space in bytes

</dd>

<dt><span class="term">source.removable or target.removable</span></dt>

<dd>

removable space in bytes

</dd>

<dt><span class="term">source.used or target.used</span></dt>

<dd>

used space in bytes

</dd>

</dl>

</div>

</dd>

<dt><span class="term">-include=_<tt><pool></tt>_[,_<tt><pool></tt>_...]</span></dt>

<dd>

Only include target pools matching any of the patterns. Single character (`?`) and multi character (`*`) wildcards may be used.

</dd>

<dt><span class="term">-include-when=_<tt><expression></tt>_</span></dt>

<dd>

Only include target pools for which the expression evaluates to true. See the description of -exclude-when for the list of allowed constants.

</dd>

<dt><span class="term">-refresh=_<tt><time></tt>_</span></dt>

<dd>

Specifies the period in seconds of when target pool information is queried from the pool manager. The default is 300 seconds.

</dd>

<dt><span class="term">-select=proportional|best|random</span></dt>

<dd>

Determines how a pool is selected from the set of target pools:

<div class="variablelist">

<dl>

<dt><span class="term">proportional</span></dt>

<dd>

selects a pool with a probability inversely proportional to the cost of the pool.

</dd>

<dt><span class="term">best</span></dt>

<dd>

selects the pool with the lowest cost.

</dd>

<dt><span class="term">random</span></dt>

<dd>

selects a pool randomly.

</dd>

</dl>

</div>

The default is proportional.

</dd>

<dt><span class="term">-target=pool|pgroup|link</span></dt>

<dd>

Determines the interpretation of the target names. The default is ’pool’.

</dd>

<dt><span class="term">-pause-when=_<tt><expression></tt>_</span></dt>

<dd>

Pauses the job when the expression becomes true. The job continues when the expression once again evaluates to false. The following constants are defined for this pool:

<div class="variablelist">

<dl>

<dt><span class="term">queue.files</span></dt>

<dd>

The number of files remaining to be transferred.

</dd>

<dt><span class="term">queue.bytes</span></dt>

<dd>

The number of bytes remaining to be transferred.

</dd>

<dt><span class="term">source.name</span></dt>

<dd>

Pool name.

</dd>

<dt><span class="term">source.spaceCost</span></dt>

<dd>

Space cost.

</dd>

<dt><span class="term">source.cpuCost</span></dt>

<dd>

CPU cost.

</dd>

<dt><span class="term">source.free</span></dt>

<dd>

Free space in bytes.

</dd>

<dt><span class="term">source.total</span></dt>

<dd>

Total space in bytes.

</dd>

<dt><span class="term">source.removable</span></dt>

<dd>

Removable space in bytes.

</dd>

<dt><span class="term">source.used</span></dt>

<dd>

Used space in bytes.

</dd>

<dt><span class="term">targets</span></dt>

<dd>

The number of target pools.

</dd>

</dl>

</div>

</dd>

<dt><span class="term">-permanent</span></dt>

<dd>

Mark job as permanent.

</dd>

<dt><span class="term">-stop-when=_<tt><expression></tt>_</span></dt>

<dd>

Terminates the job when the expression becomes true. This option cannot be used for permanent jobs. See the description of -pause-when for the list of constants allowed in the expression.

</dd>

</dl>

</div>

</div>

</div>

<div class="refentry" title="migration info">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-migration-info"></a>

<div class="refnamediv">

## migration info

migration info — Shows detailed information about a migration job.

</div>

<div class="refsynopsisdiv" title="SYNOPSIS">

## SYNOPSIS

<div class="cmdsynopsis">

`migration info` _<tt><job></tt>_

</div>

</div>

<div class="refsect1" title="DESCRIPTION"><a name="idp7462624"></a>

## DESCRIPTION

Shows detailed information about a migration job. Possible job states are:

<div class="variablelist">

<dl>

<dt><span class="term">INITIALIZING</span></dt>

<dd>

Initial scan of repository

</dd>

<dt><span class="term">RUNNING</span></dt>

<dd>

Job runs (schedules new tasks)

</dd>

<dt><span class="term">SLEEPING</span></dt>

<dd>

A task failed; no tasks are scheduled for 10 seconds

</dd>

<dt><span class="term">PAUSED</span></dt>

<dd>

Pause expression evaluates to true; no tasks are scheduled for 10 seconds.

</dd>

<dt><span class="term">STOPPING</span></dt>

<dd>

Stop expression evaluated to true; waiting for tasks to stop.

</dd>

<dt><span class="term">SUSPENDED</span></dt>

<dd>

Job suspended by user; no tasks are scheduled

</dd>

<dt><span class="term">CANCELLING</span></dt>

<dd>

Job cancelled by user; waiting for tasks to stop

</dd>

<dt><span class="term">CANCELLED</span></dt>

<dd>

Job cancelled by user; no tasks are running

</dd>

<dt><span class="term">FINISHED</span></dt>

<dd>

Job completed

</dd>

<dt><span class="term">FAILED</span></dt>

<dd>

Job failed. Please check the log file for details.

</dd>

</dl>

</div>

Job tasks may be in any of the following states:

<div class="variablelist">

<dl>

<dt><span class="term">Queued</span></dt>

<dd>

Queued for execution

</dd>

<dt><span class="term">GettingLocations</span></dt>

<dd>

Querying PnfsManager for file locations

</dd>

<dt><span class="term">UpdatingExistingFile</span></dt>

<dd>

Updating the state of existing target file

</dd>

<dt><span class="term">CancellingUpdate</span></dt>

<dd>

Task cancelled, waiting for update to complete

</dd>

<dt><span class="term">InitiatingCopy</span></dt>

<dd>

Request send to target, waiting for confirmation

</dd>

<dt><span class="term">Copying</span></dt>

<dd>

Waiting for target to complete the transfer

</dd>

<dt><span class="term">Pinging</span></dt>

<dd>

Ping send to target, waiting for reply

</dd>

<dt><span class="term">NoResponse</span></dt>

<dd>

Cell connection to target lost

</dd>

<dt><span class="term">Waiting</span></dt>

<dd>

Waiting for final confirmation from target

</dd>

<dt><span class="term">MovingPin</span></dt>

<dd>

Waiting for pin manager to move pin

</dd>

<dt><span class="term">Cancelling</span></dt>

<dd>

Attempting to cancel transfer

</dd>

<dt><span class="term">Cancelled</span></dt>

<dd>

Task cancelled, file was not copied

</dd>

<dt><span class="term">Failed</span></dt>

<dd>

The task failed

</dd>

<dt><span class="term">Done</span></dt>

<dd>

The task completed successfully

</dd>

</dl>

</div>

</div>

</div>

<div class="refentry" title="migration ls">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-migration-ls"></a>

<div class="refnamediv">

## migration ls

migration ls — Lists all migration jobs.

</div>

<div class="refsynopsisdiv" title="SYNOPSIS">

## SYNOPSIS

<div class="cmdsynopsis">

`migration ls`

</div>

</div>

<div class="refsect1" title="DESCRIPTION"><a name="idp7508736"></a>

## DESCRIPTION

Lists all migration jobs.

</div>

</div>

<div class="refentry" title="migration move">

<div class="refentry.separator">

* * *

</div>

<a name="idp7509968"></a>

<div class="refnamediv">

## migration move

migration move — Moves replicas to other pools.

</div>

<div class="refsynopsisdiv" title="SYNOPSIS">

## SYNOPSIS

<div class="cmdsynopsis">

`migration move` [_<tt><options></tt>_] _<tt><target></tt>_...

</div>

</div>

<div class="refsect1" title="DESCRIPTION"><a name="idp7515856"></a>

## DESCRIPTION

Moves replicas to other pools. The source replica is deleted. Similar to <span class="command">**migration copy**</span>, but with different defaults. Accepts the same options as <span class="command">**migration copy**</span>. Equivalent to: <span class="command">**migration copy**</span> -smode=delete -tmode=same -pins=move

</div>

</div>

<div class="refentry" title="migration suspend">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-migration-suspend"></a>

<div class="refnamediv">

## migration suspend

migration suspend — Suspends a migration job.

</div>

<div class="refsynopsisdiv" title="SYNOPSIS">

## SYNOPSIS

<div class="cmdsynopsis">

`migration suspend` job

</div>

</div>

<div class="refsect1" title="DESCRIPTION"><a name="idp7524048"></a>

## DESCRIPTION

Suspends a migration job. A suspended job finishes ongoing transfers, but is does not start any new transfer.

</div>

</div>

<div class="refentry" title="migration resume">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-migration-resume"></a>

<div class="refnamediv">

## migration resume

migration resume — Resumes a suspended migration job.

</div>

<div class="refsynopsisdiv" title="SYNOPSIS">

## SYNOPSIS

<div class="cmdsynopsis">

`migration resume` job

</div>

</div>

<div class="refsect1" title="DESCRIPTION"><a name="idp7530048"></a>

## DESCRIPTION

Resumes a suspended migration job.

</div>

</div>

</div>

<div class="section" title="PoolManager Commands">

<div class="titlepage">

<div>

[[return to top](#dCacheBook)]

<div>

## <a name="rf-cc-pm"></a>`PoolManager` Commands

</div>

</div>

</div>

<div class="refentry" title="rc ls"><a name="cmd-rc_ls"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**rc ls**</span></span>

<span class="command">**rc ls**</span> — List the requests currently handled by the `PoolManager`

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`rc ls` [_<tt><regularExpression></tt>_] [`-w`]

</div>

</div>

<div class="refsection" title="Description"><a name="idp7541184"></a>

## Description

Lists all requests currently handled by the pool manager. With the option `-w` only the requests currently waiting for a response are listed. Only requests satisfying the regular expression are shown.

</div>

</div>

<div class="refentry" title="cm ls">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-cm_ls"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**cm ls**</span></span>

<span class="command">**cm ls**</span> — List information about the pools in the [_cost module_](#gl-pm-comp-cm) cache.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`cm ls` [-r] [-d] [-s] [_<tt><fileSize></tt>_]

</div>

<div class="variablelist">

<dl>

<dt><span class="term">-r</span></dt>

<dd>

Also list the tags, the [_space cost_](#gl-space_cost), and [_performance cost_](#gl-performance_cost) as calculated by the cost module for a file of size _<tt><fileSize></tt>_ (or zero)

</dd>

<dt><span class="term">-d</span></dt>

<dd>

Also list the [_space cost_](#gl-space_cost) and [_performance cost_](#gl-performance_cost) as calculated by the cost module for a file of size _<tt><fileSize></tt>_ (or zero)

</dd>

<dt><span class="term">-t</span></dt>

<dd>

Also list the time since the last update of the cached information in milliseconds.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7562224"></a>

## Description

A typical output reads

    (PoolManager) admin >

</div>

</div>

<div class="refentry" title="set pool decision">

<div class="refentry.separator">

* * *

</div>

<a name="cmd-set_pool_decision"></a>

<div class="refnamediv">

## <span class="refentrytitle"><span class="command">**set pool decision**</span></span>

<span class="command">**set pool decision**</span> — Set the factors for the calculation of the total costs of the pools.

</div>

<div class="refsynopsisdiv" title="Synopsis">

## Synopsis

<div class="cmdsynopsis">

`set pool decision` [-spacecostfactor=_<tt><scf></tt>_] [-cpucostfactor=_<tt><ccf></tt>_] [-costcut=_<tt><cc></tt>_]

</div>

<div class="variablelist">

<dl>

<dt><span class="term">scf</span></dt>

<dd>

The factor (strength) with which the [_space cost_](#gl-space_cost) will be included in the [_total cost_](#gl-cost).

</dd>

<dt><span class="term">ccf</span></dt>

<dd>

The factor (strength) with which the [_performance cost_](#gl-performance_cost) will be included in the [_total cost_](#gl-cost).

</dd>

<dt><span class="term">cc</span></dt>

<dd>

Deprecated since version 5 of the pool manager.

</dd>

</dl>

</div>

</div>

<div class="refsection" title="Description"><a name="idp7587184"></a>

## Description

</div>

</div>

</div>

</div>

<div class="chapter" title="Chapter 28\. dCache Default Port Values">

<div class="titlepage">

<div>

<div>

## <a name="rf-ports"></a>Chapter 28\. <span class="productname">dCache</span> Default Port Values

</div>

</div>

</div>

You can use the command <span class="command">**dcache ports**</span> to get the list of ports used by <span class="productname">dCache</span>.

<div class="informaltable">

<table border="1"><colgroup><col align="left" class="c1"><col align="left" class="c2"><col align="left" class="c3"></colgroup>

<thead>

<tr>

<th align="center">Port number</th>

<th align="center">Description</th>

<th align="center">Component</th>

</tr>

</thead>

<tbody>

<tr>

<td align="left">32768 and 32768</td>

<td align="left">is used by the NFS layer within <span class="productname">dCache</span> which is based upon rpc. This service is essential for rpc.</td>

<td align="left">NFS</td>

</tr>

<tr>

<td align="left">1939 and 33808</td>

<td align="left">is used by portmapper which is also involved in the rpc dependencies of <span class="productname">dCache</span>.</td>

<td align="left">portmap</td>

</tr>

<tr>

<td align="left">34075</td>

<td align="left">is for postmaster listening to requests for the <span class="productname">PostgreSQL</span> database for <span class="productname">dCache</span> database functionality.</td>

<td align="left">Outbound for `SRM`, PnfsDomain, dCacheDomain and doors; inbound for <span class="productname">PostgreSQL</span> server.</td>

</tr>

<tr>

<td align="left">33823</td>

<td align="left">is used for internal <span class="productname">dCache</span> communication.</td>

<td align="left">By default: outbound for all components, inbound for dCache domain.</td>

</tr>

<tr>

<td align="left">8443</td>

<td align="left">is the `SRM` port. See [Chapter 13, _<span class="productname">dCache</span> Storage Resource Manager_](#cf-srm "Chapter 13\. dCache Storage Resource Manager")</td>

<td align="left">Inbound for `SRM`</td>

</tr>

<tr>

<td align="left">2288</td>

<td align="left">is used by the web interface to <span class="productname">dCache</span>.</td>

<td align="left">Inbound for httpdDomain</td>

</tr>

<tr>

<td align="left">22223</td>

<td align="left">is used for the <span class="productname">dCache</span> admin interface. See [the section called “The Admin Interface”](#intouch-admin "The Admin Interface")</td>

<td align="left">Inbound for adminDomain</td>

</tr>

<tr>

<td align="left">22125</td>

<td align="left">is used for the <span class="productname">dCache</span> `dCap` protocol.</td>

<td align="left">Inbound for `dCap` door</td>

</tr>

<tr>

<td align="left">22128</td>

<td align="left">is used for the <span class="productname">dCache</span> `GSIdCap` .</td>

<td align="left">Inbound for `GSIdCap` door</td>

</tr>

</tbody>

</table>

</div>

</div>

<div class="chapter" title="Chapter 29\. Glossary">

<div class="titlepage">

<div>

<div>

## <a name="rf-glossary"></a>Chapter 29\. Glossary

</div>

</div>

</div>

The following terms are used in <span class="productname">dCache</span>.

<div class="glosslist">

<dl>

<dt><a name="gl-dcacheconf-file"></a>The `dcache.conf` File</dt>

<dd>

This is the primary configuration file of a <span class="productname">dCache</span>. It is located at `<span>/etc/dcache</span>/dcache.conf`.

The `dcache.conf` file is initially empty. If one of the default configuration values needs to be changed, copy the default setting of this value from one of the [_properties files_](#gl-properties-files) in `<span>/usr/share/dcache</span>/defaults` to this file and update the value.

</dd>

<dt><a name="gl-layout-file"></a>The `layout` File</dt>

<dd>

The layout file is located in the directory `<span>/etc/dcache</span>/layouts`. It contains lists of the [_domain_](#gl-domain)s and the services that are to be run within these domains.

</dd>

<dt><a name="gl-properties-files"></a>The `properties` Files</dt>

<dd>

The properties files are located in the directory `<span>/usr/share/dcache</span>/defaults`. They contain the default settings of the <span class="productname">dCache</span>.

</dd>

<dt><a name="gl-chimera"></a>Chimera</dt>

<dd>

The <span class="productname">Chimera</span> namespace is a core component of <span class="productname">dCache</span>. It maps each stored file to a unique identification number and allows storing of metadata against either files or directories.

<span class="productname">Chimera</span> includes some features like [_levels_](#gl-file-level), [_directory tags_](#gl-directory-tag) and many of the [_dot commands_](#gl-pnfs-dot-cmd).

</dd>

<dt><a name="gl-chimera-id"></a>Chimera ID</dt>

<dd>

A [_Chimera_](#gl-chimera) ID is a 36 hexadecimal digit that uniquely defines a file or directory.

</dd>

<dt><a name="gl-domain"></a>Domain</dt>

<dd>

A domain is a collection of one or more [_cell_](#gl-cell)s that provide a set of related services within a <span class="productname">dCache</span> instance. Each domain requires its own Java Virtual Machine. A typical domain might provide external connectivity (i.e., a [_door_](#gl-door)) or manage the [_pools_](#gl-pool) hosted on a machine.

Each domain has at least one cell, called the `System` cell and many tunnel cells for communicating with other Domains. To provide a useful service, a domain will contain other cells that provide specific behaviour.

</dd>

<dt><a name="gl-cell"></a>Cell</dt>

<dd>

A cell is a collection of Java threads that provide a discrete and simple service within <span class="productname">dCache</span>. Each cell is hosted within a [_domain_](#gl-domain).

Cells have an address derived from concatenating their name, the `@` symbol and their containing domain name.

</dd>

<dt><a name="gl-well-known-cell"></a>Well Known Cell</dt>

<dd>

A well-known cell is a [_cell_](#gl-cell) that registers itself centrally. Within the admin interface, a well-known cell may be referred to by just its cell name.

</dd>

<dt><a name="gl-door"></a>Door</dt>

<dd>

Door is the generic name for special [_cell_](#gl-cell)s that provides the first point of access for end clients to communicate with a <span class="productname">dCache</span> instance. There are different door implementations (e.g., `GSIdCap` door and `GridFTP` door), allowing a <span class="productname">dCache</span> instance to support multiple communication protocols.

A door will (typically) bind to a well-known port number depending on the protocol the door supports. This allows for only a single door instance per machine for each protocol.

A door will typically identify which [_pool_](#gl-pool) will satisfy the end user’s operation and redirect the client to the corresponding pool. In some cases this is not possible; for example, some protocols (such as `GridFTP` version 1) do not allow servers to redirect end-clients, in other cases pool servers may be behind a firewall, so preventing direct access. When direct end-client access is not possible, the door may act as a data proxy, streaming data to the client.

By default, each door is hosted in a dedicated [_domain_](#gl-domain). This allows easy control of whether a protocol is supported from a particular machine.

</dd>

<dt><a name="gl-jvm"></a>Java Virtual Machine (JVM)</dt>

<dd>

Java programs are typically compiled into a binary form called Java byte-code. Byte-code is comparable to the format that computers understand native; however, no mainstream processor understands Java byte-code. Instead compiled Java programs typically require a translation layer for them to run. This translation layer is called a Java Virtual Machine (JVM). It is a standardised execution environment that Java programs may run within. A JVM is typically represented as a process within the host computer.

</dd>

<dt><a name="gl-tss"></a>tertiary storage system</dt>

<dd>

A mass storage system which stores data and is connected to the <span class="productname">dCache</span> system. Each <span class="productname">dCache</span> pool will write files to it as soon as they have been completely written to the pool (if the pool is not configured as a [_LFS_](#gl-lfs)). The tertiary storage system is not part of <span class="productname">dCache</span>. However, it is possible to connect any mass storage system as tertiary storage system to <span class="productname">dCache</span> via a simple interface.

</dd>

<dt><a name="gl-tape_backend"></a>tape backend</dt>

<dd>

A [_tertiary storage system_](#gl-tss) which stores data on magnetic tapes.

</dd>

<dt><a name="gl-hsm"></a>Hierarchical Storage Manager (<abbr class="abbrev">HSM</abbr>)</dt>

<dd>

See [tertiary storage system](#gl-tss).

</dd>

<dt><a name="gl-hsm_type"></a>HSM Type</dt>

<dd>

The type of <abbr class="abbrev">HSM</abbr> which is connected to <span class="productname">dCache</span> as a [_tertiary storage system_](#gl-tss). The choice of the HSM type influences the communication between <span class="productname">dCache</span> and the <abbr class="abbrev">HSM</abbr>. Currently there are `osm` and `enstore`. `osm` is used for most HSMs (TSM, HPSS, ...).

</dd>

<dt><a name="gl-hsm_instance"></a>HSM Instance</dt>

<dt><a name="gl-lfs"></a>Large File Store (<abbr class="abbrev">LFS</abbr>)</dt>

<dd>

A Large File Store is the name for a <span class="productname">dCache</span> instance that is acting as a filesystem independent to, or in cooperation with, an [_<abbr class="abbrev">HSM</abbr>_](#gl-hsm) system. When <span class="productname">dCache</span> is acting as an LFS, files may be stored and later read without involving any <abbr class="abbrev">HSM</abbr> system.

Whether a <span class="productname">dCache</span> instance provides an LFS depends on whether there are [_pools_](#gl-pool) configured to do so. The `LFS` option, specified for each pool within the [_`layout` file_](#gl-layout-file), describes how that pool should behave. This option can take three possible values:

<div class="variablelist">

<dl>

<dt><span class="term">`none`</span></dt>

<dd>

the pool does not contribute to any LFS capacity. All newly written files are regarded precious and sent to the <abbr class="abbrev">HSM</abbr> backend.

</dd>

<dt><span class="term">`precious`</span></dt>

<dd>

Newly create files are regarded as precious but are not scheduled for the <abbr class="abbrev">HSM</abbr> store procedure. Consequently, these file will only disappear from the pool when deleted in the [_<span class="productname">Chimera</span>_](#gl-chimera) namespace.

</dd>

</dl>

</div>

</dd>

<dt><a name="gl-store"></a>to store</dt>

<dd>

Copying a file from a <span class="productname">dCache</span> pool to the [_tertiary storage system_](#gl-tss).

</dd>

<dt><a name="gl-restore"></a>to restore</dt>

<dd>

Copying a file from the [_tertiary storage system_](#gl-tss) to one of the <span class="productname">dCache</span> pools.

</dd>

<dt><a name="gl-stage"></a>to stage</dt>

<dd>

See [to restore](#gl-restore).

</dd>

<dt><a name="gl-transfer"></a>transfer</dt>

<dd>

Any kind of transfer performed by a <span class="productname">dCache</span> pool. There are [_store_](#gl-store), [_restore_](#gl-restore), pool to pool (client and server), read, and write transfers. The latter two are client transfers.

See Also [mover](#gl-mover).

</dd>

<dt><a name="gl-mover"></a>mover</dt>

<dd>

The process/thread within a [_pool_](#gl-pool) which performs a [_transfer_](#gl-transfer). Each pool has a limited number of movers that may be active at any time; if this limit is reached then further requests for data are queued.

In many protocols, end clients connect to a mover to transfer file contents. To support this, movers must speak the protocol the end client is using.

See Also [transfer](#gl-transfer).

</dd>

<dt><a name="gl-location-manager"></a>Location Manager</dt>

<dd>

The location manager is a [_cell_](#gl-cell) that instructs a newly started [_domain_](#gl-domain)s to which domain they should connect. This allows domains to form arbitrary network topologies; although, by default, a <span class="productname">dCache</span> instance will form a star topology with the `dCacheDomain` domain at the centre.

</dd>

<dt><a name="gl-pinboard"></a>Pinboard</dt>

<dd>

The pinboard is a collection of messages describing events within <span class="productname">dCache</span> and is similar to a log file. Each [_cell_](#gl-cell) will (typically) have its own pinboard.

</dd>

<dt><a name="gl-breakeven"></a>Breakeven Parameter</dt>

<dd>

The breakeven parameter has to be a positive number smaller than 1.0\. It specifies the impact of the age of the least recently used file on space cost. It the LRU file is one week old, the space cost will be equal to (1 + breakeven). Note that this will not be true, if the breakeven parameter has been set to a value greater or equal to 1.

</dd>

<dt><a name="gl-lru"></a>least recently used (LRU) File</dt>

<dd>

The file that has not be requested for the longest.

</dd>

<dt><a name="gl-file-level"></a>file level</dt>

<dd>

In [_<span class="productname">Chimera</span>_](#gl-chimera), each file can have up to eight independent contents; these file-contents, called levels, may be accessed independently. <span class="productname">dCache</span> will store some file metadata in levels 1 and 2, but <span class="productname">dCache</span> will not store any file data in <span class="productname">Chimera</span>.

</dd>

<dt><a name="gl-directory-tag"></a>directory tag</dt>

<dd>

[_<span class="productname">Chimera</span>_](#gl-chimera) includes the concept of tags. A tag is a keyword-value pair associated with a directory. Subdirectories inherit tags from their parent directory. New values may be assigned, but tags cannot be removed. The [_dot command_](#gl-pnfs-dot-cmd) `.(tag)(_<tt><foo></tt>_)` may be used to read or write tag _<tt><foo></tt>_’s value. The dot command `.(tags)()` may be read for a list of all tags in that file’s subdirectory.

More details on directory tags are given in [the section called “Directory Tags”](#chimera-tags "Directory Tags").

</dd>

<dt><a name="gl-pnfs-dot-cmd"></a>dot command</dt>

<dd>

To configure and access some of the special features of the [_<span class="productname">Chimera</span> namespace_](#gl-chimera), special files may be read, written to or created. These files all start with a dot (or period) and have one or more parameters after. Each parameter is contained within a set of parentheses; for example, the file `.(tag)(_<tt><foo></tt>_)` is the <span class="productname">Chimera</span> dot command for reading or writing the _<tt><foo></tt>_ [_directory tag_](#gl-directory-tag) value.

Care must be taken when accessing a dot command from a shell. Shells will often expand parentheses so the filename must be protected against this; for example, by quoting the filename or by escaping the parentheses.

</dd>

<dt><a name="gl-pnfs-wormhole"></a>Wormhole</dt>

<dd>

A wormhole is a feature of the [_<span class="productname">Chimera</span> namespace_](#gl-chimera). A wormhole is a file that is accessible in all directories; however, the file is not returned when scanning a directory(e.g., using the <span class="command">**ls**</span> command).

</dd>

<dt><a name="gl-p2p"></a>Pool to Pool Transfer</dt>

<dd>

A pool-to-pool transfer is one where a file is transferred from one <span class="productname">dCache</span> [_pool_](#gl-pool) to another. This is typically done to satisfy a read request, either as a load-balancing technique or because the file is not available on pools that the end-user has access.

</dd>

<dt><a name="gl-storage_class"></a>Storage Class</dt>

<dd>

The storage class is a string of the form

<div class="literallayout">

`_<tt><StoreName></tt>_:_<tt><StorageGroup></tt>_@_<tt><type-of-storage-system></tt>_`  

</div>

containing exactly one `@`-symbol.

<div class="itemizedlist">

*   `_<tt><StoreName></tt>_`:`_<tt><StorageGroup></tt>_` is a string describing the storage class in a syntax which depends on the storage system.

*   `_<tt><type-of-storage-system></tt>_` denotes the type of storage system in use.

    In general use `_<tt><type-of-storage-system></tt>_=osm`.

</div>

A storage class is used by a tertiary storage system to decide where to store the file (i.e. on which set of tapes). <span class="productname">dCache</span> can use the storage class for a similar purpose, namely to decide on which pools the file can be stored.

</dd>

<dt><a name="gl-replica"></a>Replica</dt>

<dd>

It is possible that <span class="productname">dCache</span> will choose to make a file accessible from more than one [_pool_](#gl-pool) using a [_pool-to-pool_](#gl-p2p) copy. If this happens, then each copy of the file is a replica.

A file is independent of which pool is storing the data whereas a replica is uniquely specified by the <span class="productname">`pnfs`</span> ID <span class="emphasis">_and_</span> the pool name it is stored on.

</dd>

<dt><a name="gl-precious"></a>Precious Replica</dt>

<dd>

A precious replica is a [_replica_](#gl-replica) that should be stored on tape.

</dd>

<dt><a name="gl-cached"></a>Cached Replica</dt>

<dd>

A cached replica is a [_replica_](#gl-replica) that should not be stored on tape.

</dd>

<dt><a name="gl-replicamanager"></a>Replica Manager</dt>

<dd>

The replica manager keeps track of the number of [_replicas_](#gl-replica) of each file within a certain subset of pools and makes sure this number is always within a specified range. This way, the system makes sure that enough versions of each file are present and accessible at all times. This is especially useful to ensure resilience of the <span class="productname">dCache</span> system, even if the hardware is not reliable. The replica manager cannot be used when the system is connected to a [_tertiary storage system_](#gl-tss). The activation and configuration of the replica manager is described in [Chapter 6, _The `replica` Service (Replica Manager)_](#cf-repman "Chapter 6\. The replica Service (Replica Manager)").

</dd>

<dt><a name="gl-srm"></a>Storage Resource Manager (<abbr class="abbrev">SRM</abbr>)</dt>

<dd>

An SRM provides a standardised webservice interface for managing a storage resource (e.g. a <span class="productname">dCache</span> instance). It is possible to reserve space, initiate file storage or retrieve, and replicate files to another SRM. The actual transfer of data is not done via the SRM itself but via any protocol supported by both parties of the transfer. Authentication and authorisation is done with the grid security infrastructure. <span class="productname">dCache</span> comes with an implementation of an SRM which can turn any <span class="productname">dCache</span> instance into a grid storage element.

</dd>

<dt><a name="gl-billing"></a>Billing/Accounting</dt>

<dd>

Accounting information is either stored in a text file or in a PostgreSQL database by the `billing` [_cell_](#gl-cell) usually started in the `httpdDomain` [_domain_](#gl-domain). This is described in [Chapter 15, _The `billing` Service_](#cf-billing "Chapter 15\. The billing Service").

</dd>

<dt><a name="gl-poolmanager"></a>Pool Manager</dt>

<dd>

The pool manager is the [_cell_](#gl-cell) running in the `dCacheDomain` [_domain_](#gl-domain). It is a central component of a <span class="productname">dCache</span> instance and decides which pool is used for an incoming request.

</dd>

<dt><a name="gl-pm-comp-cm"></a>Cost Module</dt>

<dd>

The cost module is a Java class responsible for combining the different types of cost associated with a particular operation; for example, if a file is to be stored, the cost module will combine the storage costs and CPU costs for each candidate target pool. The pool manager will choose the candidate pool with the least combined cost.

</dd>

<dt><a name="gl-pm-comp-psu"></a>Pool Selection Unit</dt>

<dd>

The pool selection unit is a Java class responsible for determining the set of candidate pools for a specific transaction. A detailed account of its configuration and behaviour is given in [the section called “The Pool Selection Mechanism”](#cf-pm-psu "The Pool Selection Mechanism").

</dd>

<dt><a name="gl-pinmanager"></a>Pin Manager</dt>

<dd>

The pin manager is a [_cell_](#gl-cell) by default running in the `utility` [_domain_](#gl-domain). It is a central service that can <span class="quote">“<span class="quote">pin</span>”</span> files to a pool for a certain time. It is used by the `SRM` to satisfy prestage requests.

</dd>

<dt><a name="gl-spacemanager"></a>Space Manager</dt>

<dd>

The (SRM) Space Manager is a [_cell_](#gl-cell) by default running in the `srm` [_domain_](#gl-domain). It is a central service that records reserved space on pools. A space reservation may be either for a specific duration or never expires. The Space Manager is used by the `SRM` to satisfy space reservation requests.

</dd>

<dt><a name="gl-pool"></a>Pool</dt>

<dd>

A pool is a [_cell_](#gl-cell) responsible for storing retrieved files and for providing access to that data. Data access is supported via [_mover_](#gl-mover)s. A machine may have multiple pools, perhaps due to that machine’s storage being split over multiple partitions.

A pool must have a unique name and all pool cells on a particular machine are hosted in a [_domain_](#gl-domain) that derives its name from the host machine’s name.

The list of directories that are to store pool data are found in definition of the pools in the [_`layout` Files_](#gl-layout-file), which are located on the pool nodes.

</dd>

<dt><a name="gl-sweeper"></a>sweeper</dt>

<dd>

A sweeper is an activity located on a [_pool_](#gl-pool). It is responsible for deleting files on the pool that have been marked for removal. Files can be marked for removal because their corresponding namespace entry has been deleted or because the local file is a [_cache copy_](#gl-cached) and more disk space is needed.

</dd>

<dt><a name="gl-hsm-sweeper"></a><abbr class="abbrev">HSM</abbr> sweeper</dt>

<dd>

The <abbr class="abbrev">HSM</abbr> sweeper, if enabled, is a component that is responsible for removing files from the [_<abbr class="abbrev">HSM</abbr>_](#gl-hsm) when the corresponding namespace entry has been removed.

</dd>

<dt><a name="gl-cost"></a>cost</dt>

<dd>

The pool manager determines the pool used for storing a file by calculating a cost value for each available pool. The pool with the lowest cost is used. The costs are calculated by the cost module as described in [the section called “Classic Partitions”](#cf-pm-classic "Classic Partitions"). The total cost is a linear combination of the performance cost and the space cost. I.e.,

<div class="informalequation">

<pre class="programlisting">	    `cost` = `ccf` * `performance_cost` + `scf` * `space_cost`	  </pre>

</div>

where `ccf` and `scf` are configurable with the command [<span class="refentrytitle"><span class="command">**set pool decision**</span></span>](#cmd-set_pool_decision "set pool decision").

</dd>

<dt><a name="gl-performance_cost"></a>performance cost</dt>

<dd>

See also [the section called “The Performance Cost”](#cf-pm-classic-perf "The Performance Cost").

</dd>

<dt><a name="gl-space_cost"></a>space cost</dt>

<dd>

See also [the section called “The Space Cost”](#cf-pm-classic-space "The Space Cost")..

</dd>

</dl>

</div>

</div>

</div>

</div>

</div>

</div>
