[maven]: http://maven.apache.org/
[git]: http://git-scm.com/

## Allure Cucumber-JVM Examples

### Getting Started

To run tests you need to install [maven][maven] and [git][git].

To generate Allure Report you should perform following:
* [For Junit](junit/)
* [For TestNG](testng/)

**NOTE: required maven version 3.1.1 or above**


### OnFailureSchedulerCallback
This feature let users to schedule events on test failure.
That's how it works:
* Create callback class which implements OnFailureCallback and add some logic into overriden ```call()``` method:
```java
public class FailureCallback implements OnFailureCallback {
    @Override
    public Object call() {
        return 10;
    }
}
```
* To schedule callback action on test failure just put it into ```@Before``` section.
* To get callback result ask it on ```@After``` stage.

```java
import cucumber.api.java.After;
import cucumber.api.java.Before;
import cucumber.api.java.en.Given;

public calss StepDefinitions {
   @Before
    public void before() {
        AllureReporter.applyFailureCallback(FailureCallback.class);
    }

  @Given("some regex")
  public void someFailedStep(){ /* Some code which leads to error */}

    @After
    public void after() {
        int result = AllureReporter.getFailureCallbackResult();
        Assert.assertEquals(10, result);
    }
}
```

### More

* [Documentation](https://github.com/allure-framework/allure-core/wiki)
* [Issue Tracking](https://github.com/allure-framework/allure-core/issues?labels=&milestone=&page=1&state=open)
* Mailing list: [allure@yandex-team.ru](mailto:allure@yandex-team.ru)
* Gitter chat room: [https://gitter.im/allure-framework/allure-core](https://gitter.im/allure-framework/allure-core)
* StackOverflow tag: [Allure](http://stackoverflow.com/questions/tagged/allure)
