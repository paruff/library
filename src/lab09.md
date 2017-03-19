# Continuous Database mirgation/deployments - Lab 09
## Flyway

Why [Flyway?]
(https://flywaydb.org/getstarted/why)

How does [Flyway works]
(https://flywaydb.org/getstarted/how)

### GUI
1. Add  flyway and h2 to your pom.xml build section
2. create V1__Create_person_table.sql in src/main/resources/db/migration
3. mvn flyway:migrate
4. mvn flyway:info
5. mvn flyway:validate
6. mvn flayway:clean
7. mvn flyway:info
8. mvn flyway:migrate
9. mvn flyway:info
10. create V2__Add_people.sql
11. mvn info
12. flyway:validate
13. mvn flyway:migrate
14. mvn flyway:info

### Common

Flyway and h2  plugin for build section of pom.xml

```
    <build>
        <plugins>
            <plugin>
                <groupId>org.flywaydb</groupId>
                <artifactId>flyway-maven-plugin</artifactId>
                <version>4.0.3</version>
                <configuration>
                    <url>jdbc:h2:file:./target/foobar</url>
                    <user>sa</user>
                </configuration>
                <dependencies>
                    <dependency>
                        <groupId>com.h2database</groupId>
                        <artifactId>h2</artifactId>
                        <version>1.4.191</version>
                    </dependency>
                </dependencies>
            </plugin>
        </plugins>
    </build>
 
```
  
  V1__Create_person_table.sql  
 
```
 create table PERSON (
    ID int not null,
    NAME varchar(100) not null
);
```

V2__Add_people.sql
```
insert into PERSON (ID, NAME) values (1, 'Axel');
insert into PERSON (ID, NAME) values (2, 'Mr. Foo');
insert into PERSON (ID, NAME) values (3, 'Ms. Bar');
```
