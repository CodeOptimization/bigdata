# Environment
  CentOS-7-x86_64-DVD-1611 + JDK 1.8 + Hadoop 2.7.3
  
  ![alt text](https://mir-s3-cdn-cf.behance.net/project_modules/disp/d2be1031126119.5605940d55ff5.jpg)

  
# Java
  * Show which java are you using
  > run command __*which java*__, this could be alias, then you need __*readlink $(which java)*__
  * Installing your own JDK and setting as default one:
  > 1. wget  --no-cookies --no-check-certificate --header "Cookie: gpw_e24=http%3A%2F%2Fwww.oracle.com%2F; oraclelicense=accept-securebackup-cookie" "http://download.oracle.com/otn-pub/java/jdk/8u131-b11/d54c1d3a095b4ff2b6607d096fa80163/jdk-8u131-linux-x64.tar.gz", this command will down load the file to current folder.
  > 2. tar xzf jdk-8u131-linux-x64.tar.gz.
  > 3. alternatives --install /usr/bin/java java /user_installed/jdk1.8.0_131/bin/java 2 (*Installing JDK*).
  > 4. sudo alternatives --config java (*Setting the alias pointing to your own JDK*).
  >> * The out put will be.
  >> * There are 3 programs which provide 'java'.
  >> * Selection   Command.
  >> *----------------------------------------------- *.
  >> * 1           java-1.7.0-openjdk.x86_64 (/usr/lib/jvm/java-1.7.0-openjdk-1.7.0.111-2.6.7.8.el7.x86_64/jre/bin/java).
  >> * *+ 2       java-1.8.0-openjdk.x86_64 (/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.102-4.b14.el7.x86_64/jre/bin/java).
  >> * 3           /user_installed/jdk1.8.0_131/bin/java.
  >> * Enter to keep the current selection[+], or type selection number.
  >> * __*As you can seem the second one is the default one right now, Then you choose 3.*__
  
  > 5. You can also run the command or just set up the ~./bashrc file for the JAVA_HOME.
  >> 1. alternatives --install /usr/bin/jar jar /opt/jdk1.8.0_131/bin/jar 2.
  >> 2. alternatives --install /usr/bin/javac javac /opt/jdk1.8.0_131/bin/javac 2.
  >> 3. alternatives --set jar /opt/jdk1.8.0_131/bin/jar.
  >> 4. alternatives --set javac /opt/jdk1.8.0_131/bin/javac.



  

# Steps
1. Download the release hadoop-X.Y.Z-src.tar.gz from a [mirror site](http://www.apache.org/dyn/closer.cgi/hadoop/common).
  * To perform a quick check using SHA-256:
  * Download the checksum hadoop-X.Y.Z-src.tar.gz.mds from [Apache](https://dist.apache.org/repos/dist/release/hadoop/common/).
  * sha256sum hadoop-X.Y.Z-src.tar.gz(performed on Mac)
2. Edit your *~/.bashrc* file for convenience.
    ###### format:
        export JAVA_HOME="/usr/lib/jvm/java-1.8.0-openjdk-1.8.0.102-4.b14.el7.x86_64/jre"
        export HADOOP_HOME="/home/patrick/software/hadoop/hadoop-2.7.3"
        export PATH="$PATH:$JAVA_HOME/bin"
        export PATH="$PATH:$HADOOP_HOME/bin"
        
# Developing
1. IntelliJ: download and unzip the file. Then run "./idea.sh" in the bin folder. One trick is I have cncountered "intellij tartup Error: Unable to detect graphics environment" problem, it was solved by restarting.
2. 
