# springboot-kafka-microservices-project
Maven project generated with com.a9ski:quick-start archetype
![img_2.png](readme-pic%2Fimg_2.png)

```bash
bin/zookeeper-server-start.sh config/zookeeper.properties
bin/kafka-server-start.sh config/server.properties
```

# Development guide
1. Install pre-commit (https://pre-commit.com/)
2. Install the pre-commit hook by executing `pre-commit install` inside project directory
3. Run against all files in the project: `pre-commit run --all-files`

# Building
```
mvn clean install
```
produces a jar file with MANIFEST containing main class and classpath.
All dependencies are copied to target/libs directory.

# Runing
```
mvn exec:java
```

or

```
cd target
java -jar xxxx.jar
```
