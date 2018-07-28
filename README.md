
## Setup
Run:
```
cd /path/to/project
mvn compile 
mvn exec:java -Dexec.mainClass="com.vvvtimes.server.MainServer" -Dexec.args="-p 8081"
```
Packing a runnable jar:
```
mvn package
```
then
```
java -jar JrebelBrainsLicenseServerforJava-1.0-SNAPSHOT-jar-with-dependencies.jar -p 8081
```
default port is 8081.
## Docker
Build image
```
mvn package 
docker build -t jrebel-ls .
```

start container
```
docker run -d --name jrebel-ls --restart always -e PORT=9001 -p 9001:9001 jrebel-ls
```
default port is 8081,you can modify it
## Support


## Feedback

+ issue: https://gitee.com/gsls200808/JrebelLicenseServerforJava/issues
+ QQ Group: 527290836
