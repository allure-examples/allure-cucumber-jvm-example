## Allure Cucumber-JVM Example

To run tests you need to install [maven](http://maven.apache.org/) and [git](http://git-scm.com/).

To generate Allure Report you should perform following steps:
```bash
$ git clone git@github.com:allure-examples/allure-cucumber-jvm-example.git
$ mvn clean test
$ mvn site
```
**Please note:** Report could not be opened by file:// url (AngularJS limitation). To correctly open the report, **site/** directory must be acessible under http(s):// context. Or just use [allure-cli](https://github.com/allure-framework/allure-cli) tool instead for report generation and opening.
