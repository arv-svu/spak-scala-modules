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

I have added your github accounts to collaborators list. I guess, that should give full access on this repository. \
I have basic knowledge on DevOps. I am thinking of creating a branch for each module change. something like below. \

git checkout -b module-name-<change/feature desc> --> create pull request and merge in github.com \
git checkout -b module-name-<change/feature desc> --> create pull request and merge in github.com

Proposed git workflow with commands is below. for your reference.\
Feel free to suggest if you know something better.

    1.Clone current main branch from GitHub to your machine
    command(s): git clone < repository url >
    example: git clone https://github.com/arv-svu/spark-scala-modules.git
    git log -all --graph
    
    2.Create new branch in your machine and checkout new branch
    command(s): git checkout -b <yourinitials>-mod<100 to 199>-<project-name>
    example1: git checkout -b av-mod100-scala-basics
    example2: git checkout -b av-mod101-spark-basics
    
    3.Below are commands for example1 branch
    
        3.1.Add your module to your project in intellij idea. keep module name same as branch name. 
            Refactor project structure per scala standards
        
        3.2.Start coding and commit locally to new branch as needed.
        command(s): git checkout av-mod100-scala-basics
                    git log --all --graph
    
                    git add .
                    git commit -m "feature1: some desc"
    
                    git add .
                    git commit -m "feature2: some desc"
    
                    git commit .
                    git commit -m "features: all done"
        
        3.3.Push new branch to GitHub
        command(s): git checkout av-mod100-scala-basics
                    git log --all --graph
                    git push origin av-mod100-scala-basics
        
    4.Goto github.com and compare & pull request.
        
    5.In github.com, review code and merge pull request into main branch
        
    6.Update local repository after the merge
    command(s): git checkout main
    git pull origin main
    git log --all --graph
    
    7.Delete local branch safely
    command(s): git branch -d av-mod100-scala-basics
    
    8.Delete remove branch safely
    command(s): git push origin --delete av-mod100-scala-basics



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


