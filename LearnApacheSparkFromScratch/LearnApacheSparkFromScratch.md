# Learn Apache Spark From Scratch

## Learning Objective 1

- Clustering [Spark doc: Clustering](https://spark.apache.org/docs/1.1.0/mllib-clustering.html)
- refers to a set of specific  algorithms
- spark most commonly uses k-means
- classes of clustering algorithms
- eg hierarchical clustering
- eg statistical clustering (k-means)
- combination of the two
- visualization tools

### Machine Learning
refers to a set of algorithms and conceptual  frameworks
[algorithms](https://spark.apache.org/docs/1.1.0/mllib-guide.html)
conceptual  frameworks supervised. semi-supervised, …. in the end comes down to a mathematical domain for the conceptual basis of the algorithm.

### Data Science and Analysis
refers to a set of algorithms and conceptual frameworks and tools
Learning objective 1
To be able to describe Apache Spark as a solution in a given context. Clustering, Machine Learning, Data Science and Analysis, …..
1.	Clustering applications, eg remove duplicates
2.	Machine Learning Mlib, training, recommendations
3.	Spark components, Shark, GraphX
4.	Runtime Modes, StandAlone, Yarn Cluster, Mesos Cluster

## Learning Objective 2

1. Installation of the tools
    1.	Virtualisation application VMWare, VirtualBox,  and other virtualization environments.
    2. Hortonworks vm  installed virtual box [Recommended Downloads and guide to install](http://hortonworks.com/hdp/downloads/)
    - [Guide to instal on VmWare](http://hortonworks.com/wp-content/uploads/2016/02/Import_on_VMware_3_1_2016.pdf)
    - Hortonworks Data Platform (HDP™) [Sandbox VM Downloads and guide to install](http://hortonworks.com/products/hortonworks-sandbox/#install)
    - save VM for vmWare in c:\WWWDownload\
    - open VmWare Workstation and just open c:\WWWDownload\Hortonworks_sanbox_with_hdp_2_4_vmware.ova
    - try to open http://192.168.217.129/ in chrome

```
During vm initialization I can see "bringing up interface eth0 device eth0 does not seem to be present delaying initialization" in console.
```

![image](vmWareEth0DeviceError.PNG)


```
I've try 'putty' this address. The result is "Network error: Connection timed out".
```


```
c:\WebstormProjects\LearningD3>ping 192.168.217.129
Pinging 192.168.217.129 with 32 bytes of data:
Request timed out.
Ping statistics for 192.168.217.129:
    Packets: Sent = 4, Received = 0, Lost = 4 (100% loss),
```

- Google: 'can't open hortonworks sandbox url'    

## VirtualBox 
- install Oracle [VirtualBox](https://www.virtualbox.org/wiki/Downloads)    
- ![Hortonworks_sanbox_with_hdp_2_4_virtualboxCapture](Hortonworks_sanbox_with_hdp_2_4_virtualboxCapture.PNG)
- ![hdp_2_4_virtualboxInLocalhost](hdp_2_4_virtualboxInLocalhost.PNG)
- SSH with putty (host 127.0.0.1, port 2222, username root) 
- required by system change password to *alex140839* (original *hadoop*)

- check out [tutorials](http://hortonworks.com/tutorials/)
    
    3. Windows: git bash shell http://git-scm.com/downloads
    4. Windows: a ssh directory browser http://www.swish-sftp.org/
    5. Filezilla https://filezilla-project.org/
    6. 7 zip




2, install the virtual machine [instructions here](http://hortonworks.com/wp-content/uploads/unversioned/pdfs/InstallingHortonworksSandbox2onWindowsusingVB.pdf)
3. Download spark binary. please note over time the versions and download links change. change this is the current compatible jar for the Hortonworks VM
wget http://public-repo-1.hortonworks.com/HDP-LABS/Projects/spark/1.2.0/spark-1.2.0.2.2.0.0-82-bin-2.6.0.2.2.0.0-2041.tgz


4. Set up ssh with HortonWorks VM

1.	connect with filezilla
2.	host 127.0.0.1
port 2222
username root
password hadoop
  5 Set the SPARK_HADOOP_VERSION flag in the  Hortonworks vm  environment variable

ssh root@127.0.0.1 -p 2222
hadoop

             cd /etc/   
             vi bashrc 
then append  
             export SPARK_HADOOP_VERSION=2.2.0
             then  :wq   then init 6
             then in the Hortonworks vm ’s Bash shell check with **printenv** you should  should see


6.Install the Apache Spark Binaries and Example Source Code

chmod -R 4777 spark-1.2.0.2.2.0.0-82-bin-2.6.0.2.2.0.0-2041.tgz
tar xvfz spark-1.2.0.2.2.0.0-82-bin-2.6.0.2.2.0.0-2041.tgz
once unpacked rename the directory to spark1.2.0 or something similar


7.
  cd sp*
./bin/spark-shell

  cd sp*
  sbt/sbt assembly

if the spark build fails or hangs on a resolving ……..  or fails
then delete the following directories in the root folder on the vm
.m2   .ivy     .sbt
see screenshot below in the ssh directory browser with show hidden folders enabled in the windows control panel

8. Running the spark api from the scala interface


## Section: 1 - Introduction To Spark
### Lecture 1: Course Introduction

## Section: 2 - Introduction and Application of Apache Spark
### Lecture 2: Understanding Apache Spark
### Lecture 3: Install Apache Spark on Cluster
### Lecture 4: Apache Spark Scala API
### Lecture 5: Running Apache Spark Code

## Section: 3 - Apache Spark with YARN Cluster
### Lecture 6: Apache Spark in Yarn Context
### Lecture 7: Apache Spark with Yarn
### Lecture 8: Yarn Clusters
#### Setup maven pom file for java and scala projects
- Create fresh maven project in IntelliJ IDE 
![MavenForSparkJavaScalaProject](MavenForSparkJavaScalaProject.PNG)
- build our self 
- git hub __hadoop-common-2.2.0-bin__ as runtime dependency for running example project
- create env var HADOOP_HOME pointing to where you check-out __hadoop-common-2.2.0-bin__ 
- after run as standalone rebuild with flag runOnCluster=false
- deploy on spark root
- run spark-submit with custom parameters
### Lecture 9: Bonus Video - Yarn on Eclipse
- Video&Doc to setup maven for spark project in eclipse

## Section: 4 - Spark Applications
### Lecture 10: Different types of Spark Applications
### Lecture 11: Spark with Gradle
- Gradle build file explanation
- JavaKMeans application
- if you have java 8 installed build with _sourceCompatibility = 1.7_ option set in gradle build file ( **not sure if it apply to latest HDP** )
- if build with IDE set version 1.7 in _options -> Java Compiler -> Project bytecode version -> 1.7_ ( **not sure if it apply to latest HDP** )
### Lecture 12: Spark Applications - SQL Library

## Section: 5 - Apache Spark APIs
### Lecture 13: Spark Streaming Applications
### Lecture 14: Twitter Stream Application
- Twitter Stream Application = EduonixLambdaArchitecture project
- use of _cloudera_ repository ( instead of __hadoop-common-2.2.0-bin__  )
- Use version 3.0.3 of _twitter4j_core_ and _twitter4j_stream_   ( **not sure if it apply to latest HDP** )
- gson (google json library)
### Lecture 15: Lambda Architecture

## Section: 6 - Course Summary
### Lecture 16: Summary 



