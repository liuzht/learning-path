# Maven

https://maven.apache.org/what-is-maven.html


## Creating an Executable JAR

[maven-assembly-plugin/usage](https://maven.apache.org/plugins/maven-assembly-plugin/usage.html)
1. modify pom.xml
  - **\<archive\>/\<manifest\>** configure the Main-Class
  - **\<appendAssemblyId\>** avoid showing the descriptorRef id in the final jar
```
<build>
  <pluginManagement>
    <plugins>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-assembly-plugin</artifactId>
        <version>3.4.2</version>
        <configuration>
          <archive>
            <manifest>
              <mainClass>com.test.Main</mainClass>
            </manifest>
          </archive>
          <descriptorRefs>
            <descriptorRef>jar-with-dependencies</descriptorRef>
          </descriptorRefs>
          <appendAssemblyId>false</appendAssemblyId>
        </configuration>
        <executions>
          <execution>
            <id>make-assembly</id>
            <phase>package</phase>
            <goals>
              <goal>single</goal>
            </goals>
          </execution>
        </executions>
      </plugin>
    </plugins>
  </pluginManagement>
</build>
```

2. execute maven goal
```
mvn clean compile assembly:single
```
