# Environment
  CentOS-7-x86_64-DVD-1611 + Hadoop 2.8.0
  
# Steps
1. Download the release hadoop-X.Y.Z-src.tar.gz from a [mirror site](http://www.apache.org/dyn/closer.cgi/hadoop/common).
  * To perform a quick check using SHA-256:
  * Download the checksum hadoop-X.Y.Z-src.tar.gz.mds from [Apache](https://dist.apache.org/repos/dist/release/hadoop/common/).
  * sha256sum hadoop-X.Y.Z-src.tar.gz(performed on Mac)
2. Edit your *~/.bashrc* filr for convenience.
  > format:
  > export JAVA_HOME="/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.102-4.b14.el7.x86_64/jre"
  
  > export HADOOP_HOME="/home/patrick/software/hadoop/hadoop-2.8.0"

  > export PATH="$PATH:$JAVA_HOME/bin"
  
  > export PATH="$PATH:$HADOOP_HOME/bin"

