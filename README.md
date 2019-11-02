# Spark_workshop_AnitaB
Set up instructions for Laptop with Mac and Windows 
Install spark-shell on MAC OS:
========================
step1. Install brew. 
 $ /usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"

==> This script will install:
/usr/local/bin/brew
/usr/local/share/doc/homebrew
/usr/local/share/man/man1/brew.1
/usr/local/share/zsh/site-functions/_brew
/usr/local/etc/bash_completion.d/brew
/usr/local/Homebrew

step2:
$ xcode-select --install
You get below if command line tools are already installed , then ignore this and move to step 3 . 
“xcode-select: error: command line tools are already installed, use "Software Update" to install updates”

Step3:  Install Java.
$ brew cask install java
It will ask your password and at the end you get  “ java was successfully installed!”  message.

Step4:Install scala band spark
$ brew install scala
$ brew install apache-spark

Step5:
$ spark-shell
Spark context Web UI available at http://88e9fe767.:4040
Spark context available as 'sc' (master = local[*], app id = local-1572297321573).
Spark session available as 'spark'.
Welcome to
      ____              __
     / __/__  ___ _____/ /__
    _\ \/ _ \/ _ `/ __/  '_/
   /___/ .__/\_,_/_/ /_/\_\   version 2.4.4
      /_/

Using Scala version 2.11.12 (Java HotSpot(TM) 64-Bit Server VM, Java 1.8.0_201)
Type in expressions to have them evaluated.

scala>

This confirms spark-shell installation and configuration is succesfull on Mac OS.
Install Spark-shell on Windows:

Step1: Download & Install Java 8

1.	Download Java JDK 8 from below official oracle website.
https://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html
2.	Set the environment variables
            JAVA_HOME= C:\Program Files\Java\jdk1.8.0_231
             PATH += C:\Program Files\Java\jdk1.8.0_231\bin

Step2: Download & Install Spark

1.	Download spark from below. Choose spark-2.4.4-bin-hadoop2.7.tgz
http://spark.apache.org/downloads.html
2.	Extract the .tgz file into D:\Spark
3.	Set the environment variables
SPARK_HOME = D:\Spark\spark-2.3.0-bin-hadoop2.7
PATH += D:\Spark\spark-2.3.0-bin-hadoop2.7\bin

Step3: Download Winutils.exe

1.	Download winutils from here
 https://github.com/steveloughran/winutils
If you chose the same version as me (hadoop-2.7.1) ,is the direct link: https://github.com/steveloughran/winutils/blob/master/hadoop-2.7.1/bin/winutils.exe

      2.  Move the winutils.exe file to the bin folder inside SPARK_HOME,  D:\Spark\spark-2.3.0-  bin-hadoop2.7\bin
      3. Set the environment variable to be the same as SPARK_HOME:
          HADOOP_HOME = D:\Spark\spark-2.3.0-bin-hadoop2.7

Step4: Install Scala:

1.	Download Scala from their official website
https://www.scala-lang.org/download/
Download the Scala binaries for Windows (scala-2.12.4.msi )
     2.   Install Scala from the .msi file
     3.   Set the environment variables:
   SCALA_HOME = C:\Progra~2\scala
   PATH += C:\Progra~2\scala\bin

Step5: Verify spark-shell is working by navigating to the location where spark binaries are available. D:\Spark\spark-2.3.0-bin-hadoop2.7\bin 
$ spark-shell

Welcome to
      ____              __
     / __/__  ___ _____/ /__
    _\ \/ _ \/ _ `/ __/  '_/
   /___/ .__/\_,_/_/ /_/\_\   version 2.4.4
      /_/

Using Scala version 2.11.12 (Java HotSpot(TM) 64-Bit Server VM, Java 1.8.0_201)
Type in expressions to have them evaluated.

scala>

This confirms spark-shell installation and configuration is succesfull on Widows.






 


