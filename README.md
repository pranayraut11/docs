# Random notes

### Add certificates in java using keytool
```
keytool -import -alias example -keystore  "C:\Program Files\Java\jdk-17\lib\security\cacerts" -file example1.cer
```

### Build docker images for all projects
```
 find . -name "pom.xml" -exec mvn clean install -Dmaven.test.skip=true  jib:build -f '{}' \;
```
### Delete docker images by patter
```
 docker rmi $(docker images | grep pattern | tr -s ' ' | cut -d ' ' -f 3)
```
### If you see errors like

Temporary failure resolving 'download.docker.com'
Ign:2 http://archive.ubuntu.com/ubuntu <br>
or
access related errors <br>
Update file /etc/resolve.conf with following content
```
nameserver 8.8.8.8
nameserver 8.8.4.4  
```
