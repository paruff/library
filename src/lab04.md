# Automated Acceptance Testing  - Lab 04
## Cucumber 

### gui 
1. in eclipse, open pom.xml
2. view as xml, right most option at bottom of pom window.
2. find the Dependencies section
4. replace it with the following:

```
>	    <dependencies>
>        <dependency>
>            <groupId>info.cukes</groupId>
>            <artifactId>cucumber-java</artifactId>
>            <version>1.1.8</version>
>            <scope>test</scope>
>        </dependency>
>        <dependency>
>            <groupId>info.cukes</groupId>
>            <artifactId>cucumber-junit</artifactId>
>            <version>1.1.8</version>
>            <scope>test</scope>
>        </dependency>
>        <dependency>
>            <groupId>junit</groupId>
>            <artifactId>junit</artifactId>
>            <version>4.11</version>
>            <scope>test</scope>
>        </dependency>
>    </dependencies>
```

5. Select right click on pom.xml -> Run as -> mvn test
6. Create a directory src/test/resources
7. Create directory src/test/resources/cucumber
8. create a file calculator.feature with the following contents:


>  Feature: Calculator
>   As a user
>   I want to use a calculator
>   So that I don't need to calculate myself
> 
>
>  Scenario: Add two numbers
>    Given I have a calculator
>    When I add 2 and 3
>    Then the result should be 5


9. 
### Reference
[Cucumber ](https://cucumber.io/docs/reference)
