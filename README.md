# prepare to oca examination

### Installation
- [Install JDK 8u91 (packages and resources) including JRE (virtual machine, sandbox to compile code)](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html).

- [Install Maven build management system](https://maven.apache.org/download.cgi).

- Update user or system environment variables
```bash
# /etc/environment
# ~/.bashrc
MAVEN_3=/opt/apache-maven-3.3.9
export MAVEN=$MAVEN_3
JAVA_8=/usr/jdk/jdk1.8.0_91
export JAVA_HOME=$JAVA_8
export PATH="$PATH:$JAVA_HOME/bin:$MAVEN/bin"
# $source /etc/environment
```

### Deploy
- import maven dependencies onto target project
```bash
$mvn clean install
```

### Collaboration by private branches
```bash
# Fork private repository and create branch for yourself
git clone https://github.com/[username]/oca.git
git remote add upstream https://github.com/MallorcaRocks/oca.git
git checkout -b [oca-username]

# Commit on your branch (own test Chapters)
git checkout [oca-username] && git add --ignore-removal --all && git commit -m "new example"

# Commit on master (general purpose)
git checkout master && git add --ignore-removal --all && git commit -m "new example"

# sync collaborator knowledge
git pull --all

# check collaborator knowledge
git branch -a
git checkout [oca-username]

# Push changes
git push origin [oca-username]
# create pull request to upstream [oca-username] branch
# auto merge
# send mail to collaborators, PR url
```

### Exam Documentation
- [**Study tips**](https://drive.google.com/drive/folders/0BxsVbGnLpHpAbTBGRC1MMV9aS2c?usp=sharing)
- [**Calendar Program**](https://calendar.google.com/calendar/embed?src=1u3knnhn0enc6gsacndr7acbm4%40group.calendar.google.com&ctz=Europe/Madrid)
