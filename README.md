# Project Description

A multi-module spark scala maven project repository where each module solves a specific etl problem. 

Install and configure [Software Needed](#software-needed) to start developing code.

## Good to know

It would be nice if you know/refresh below topics. We will be using these to build pipelines/etls

Maven, Scala/Java, SQL, Git concepts, Conceptual understanding of big data components (Hadoop, HDFS, Hive, Spark) and Docker/Container concepts


## Project Structure

```
|--project root directory
  |--.idea
  |--pom.xml
  |-- readme.md
  |--.gitignore
  |--data
    |--source                       #all your source files go here
    |--target                       #all your hive, kudo and other databases go here
  |--logs                           #all your logs go here
  |--m-av-spark-etl1                #my project source code lives here. standard is : m-<your initials>-<project name>.
    |--pom.xml
    |--src
      |--main
        |--scala
          |--package.structure      #create packages per main pom
            |--*.scala              #scala files          
      |--test
        |--scala
  
  |--m-av-spark-etl2                #second project source code
    |--structure as above module
  
```

## Git Collaboration

I have added your github accounts to collaborators list. I guess, that should give full access on this repository.

I have basic knowledge on DevOps. I am thinking of creating a branch for each module. You can suggest something better.

git commands are below to clone and create a branch.

$ git clone https://github.com/arv-svu/spark-scala-modules.git \
$ git checkout -b <your module name> #create branch for each module \
start coding in IDE and when you are done, \
$ git add . \
$ git commit -m <your comments> \
$ git pull origin master \
$ git push origin <your module/branch name>

will review pull requests and merge together in our sprint



## Software Needed

### Java JDK 1.8.0_201
Windows x64  - [link to download version 1.8](https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html#license-lightbox)\
Mac Intel - [link to download version 1.8](https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html#license-lightbox)

### IntelliJ IDEA 2022.3.2 (Community Edition)
This is already bundled with bunch of plugins like maven. \
Windows x64 - [link to download](https://download.jetbrains.com/idea/ideaIC-2022.3.2.exe?_gl=1*a0c2yj*_ga*MTY5MDU2NzM1NC4xNjczNDcwMDQw*_ga_9J976DJZ68*MTY3NTI4OTM5NC4xMC4wLjE2NzUyODkzOTQuNjAuMC4w&_ga=2.205203024.1147573084.1675219395-1690567354.1673470040) \
Mac Intel - [link to download](https://download.jetbrains.com/idea/ideaIC-2022.3.2.dmg?_gl=1*hsw65d*_ga*MTY5MDU2NzM1NC4xNjczNDcwMDQw*_ga_9J976DJZ68*MTY3NTI4OTM5NC4xMC4wLjE2NzUyODkzOTQuNjAuMC4w&_ga=2.143278709.1147573084.1675219395-1690567354.1673470040)

### Git
Windows x64 - [link to download](https://github.com/git-for-windows/git/releases/download/v2.39.1.windows.1/Git-2.39.1-64-bit.exe) \
Mac Intel - Install homebrew if you don't already have it, then: $ brew install git

### Spark
Will download using Maven. No installation needed, unless you want to run your cluster all the time. Our goal is start the cluster while running our pipeline and stop it once the job is completed. Everything will be done on your computer.

### Scala 2X
Will download using Maven. No installation is needed unless, you want to code outside of IDE.


