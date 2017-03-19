# Static Analysis - lab 07
## Findbugs, PMD, CheckStyle


### GUI
1. in eclipse, open pom.xml
2. view as xml, right most option at bottom of pom window.
3. insert the following toward the bottom just above the last tag


```

  <reporting>
    <plugins>
      <plugin>
        <groupId>org.codehaus.mojo</groupId>
        <artifactId>findbugs-maven-plugin</artifactId>
        <version>3.0.4</version>
      </plugin>
      <plugin>
        <groupId>org.apache.maven.plugins</groupId>
        <artifactId>maven-pmd-plugin</artifactId>
        <version>3.6</version>
      </plugin>
       <plugin>
          <groupId>org.apache.maven.plugins</groupId>
          <artifactId>maven-checkstyle-plugin</artifactId>
          <version>2.17</version>
          <reportSets>
            <reportSet>
              <reports>
                <report>checkstyle</report>
              </reports>
            </reportSet>
          </reportSets>
        </plugin>
    </plugins>
  </reporting>

```

4. Select right click on pom.xml -> Run as -> mvn site
5. in Windows Explorer, open c:\user\{ldapid}\Documents\workspace-sts\hello_world\target\site\index.html
6. 
