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
