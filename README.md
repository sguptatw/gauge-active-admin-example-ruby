[![Build Status](https://travis-ci.org/getgauge-examples/ruby-selenium.svg?branch=master)](https://travis-ci.org/getgauge-examples/ruby-selenium)

# Gauge example in Ruby

This is an example project for doing web automation testing with [Gauge](http://getgauge.io). This project tests some of the functionalities of the [active admin demo](https://github.com/getgauge/activeadmin-demo) app. This app is hosted as a Java WAR (with embedded Jetty).

## Running this example
The tests are run on Chrome by default.

### Prerequisites

This example requires the following softwares to run.
  * [ruby-2.3.1](https://www.ruby-lang.org/en/news/2016/04/26/ruby-2-3-1-released/) or above
  * [Gauge](https://docs.gauge.org/getting_started/installing-gauge.html)
  * Gauge Ruby plugin
    * can be installed using `gauge install ruby`
  * Chrome

### Setting up the System Under Test (SUT)

* Download [activeadmin-demo.war](https://github.com/getgauge-examples/activeadmin-demo/releases/tag/untagged-f0befd5494efa4baabd2)
* Bring up the SUT by executing the below command
```
java -jar activeadmin-demo.war
```
* The SUT should now be available at [http://localhost:8080/](http://localhost:8080)

## Run specs

You can execute specs as `bundle exec gauge specs`
This runs Gauge specs with [Maven](http://maven.apache.org/index.html).

This uses Chrome as default browser for specs execution. Make sure Chrome is installed in your machine and [chromedriver](https://sites.google.com/a/chromium.org/chromedriver/) is in PATH.

If you want to use Firefox/IE as browser, pass the corresponding argument to set browser environment as follows:

```
bundle exec gauge run specs --env="firefox"
or
bundle exec gauge run specs --env="ie"
```

## Topics covered in the example

- Use [Webdriver](http://docs.seleniumhq.org/projects/webdriver/) as base of implementation
- [Concepts](https://docs.gauge.org/latest/writing-specifications.html#concept)
- [Specification](https://docs.gauge.org/latest/writing-specifications.html#specifications-spec), [Scenario](https://docs.gauge.org/latest/writing-specifications.html#longstart-scenarios) & [Step](https://docs.gauge.org/latest/writing-specifications.html#longstart-steps) usage
- [Table driven execution](https://docs.gauge.org/latest/execution.html#data-driven-execution)
- [External datasource (special param)](https://docs.gauge.org/latest/execution.html#external-csv-for-data-table)
- Using Gauge with [Selenium Webdriver](http://docs.seleniumhq.org/projects/webdriver/)

# Copyright
Copyright 2018, ThoughtWorks Inc.
