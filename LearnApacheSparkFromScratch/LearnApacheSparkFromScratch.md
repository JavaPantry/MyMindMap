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
             then in the Hortonworks vm ’s Bash shell check with printenv you should  should see


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



