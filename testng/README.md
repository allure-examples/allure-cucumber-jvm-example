[maven]: http://maven.apache.org/
[git]: http://git-scm.com/

## Allure Cucumber-JVM with TestNG Example

### Getting Started

To run tests you need to install [maven][maven] and [git][git].

To generate Allure Report you should perform following steps:

```bash
$ git clone git@github.com:allure-examples/allure-cucumber-jvm-example.git
$ cd testng
$ mvn clean test
$ mvn site
```

To see a report, run `mvn jetty:run` in current folder and open `http://localhost:8080` in your browser

### More

* [Documentation](https://github.com/allure-framework/allure-core/wiki)
* [Issue Tracking](https://github.com/allure-framework/allure-core/issues?labels=&milestone=&page=1&state=open)
* Mailing list: [allure@yandex-team.ru](mailto:allure@yandex-team.ru)
* Gitter chat room: [https://gitter.im/allure-framework/allure-core](https://gitter.im/allure-framework/allure-core)
* StackOverflow tag: [Allure](http://stackoverflow.com/questions/tagged/allure)
