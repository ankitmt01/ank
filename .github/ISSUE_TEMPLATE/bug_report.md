---
name: Bug report
about: Create a report to help us improve
title: ''
labels: ''
assignees: ''

---

When reporting a bug, please **try** to provide as much information as possible.

 * Plugin version used.
 * Jenkins version used.
 * Your configuration.
   * Variables configured, names, expressions...
   * Pipeline script (See Pipeline section in README)
 * Build job log
 * Post content received. It can be found in the job execution log. People using GitHub often forget to set the content type in "Manage webhook" when configuring the webhook at GitHub.
 * A `curl` command and its response.
 * Expected result and actual result.

You may also have a look at the test cases as they should answer the most common questions:
 
  https://github.com/jenkinsci/generic-webhook-trigger-plugin/tree/master/src/test/resources/org/jenkinsci/plugins/gwt/bdd

If you are fiddling with expressions, you may want to checkout:

* [This JSONPath site](http://jsonpath.herokuapp.com/)
* [This XPath site](http://www.freeformatter.com/xpath-tester.html)
* [This regexp site](https://jex.im/regulex/)

A Curl command can look something like this:
```
curl -v -H "Content-Type: application/json" -X POST -d '{ "app":{ "name":"GitHub API", "url":"http://developer.github.com/v3/oauth/" }}' http://localhost:8080/jenkins/generic-webhook-trigger/invoke?token=sometoken
```
