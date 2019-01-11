# pyATS Report Plugin ![](guide/assets/images/r_jenkins.png)

The pyATS Report Plugin is a Post Build plugin to display Cisco test automation 
test results within Jenkins, with options to upload the archives to Cisco Self Serve Services(S3) portal. 
The Report Plugin is designed to work with pyATS Project (for pyATS based scripts), 
as well as Jenkins Free Style project(for TCL based scripts).


## Table Of Content
- [Feature Highlights](#feature-highlights)
- [Installation](guide/installation.md)
- [Quick Start](guide/quick_start.md)
- [XML Spec](guide/spec.md)

## Related pyATS Plugins
- [pyATS Jenkins Project Plugin](https://github.com/CiscoTestAutomation/jenkins_project_plugin)
- [S3 Executor Plugin](https://github.com/CiscoTestAutomation/jenkins_executor_plugin)

## Feature Highlights
* Extract ResultsDetails.xml results file from a specific archive location(Free Style Project) or from the Jenkins _workspace_ (pyATS Project)
* Provide Test suite, and testcase result details with Trend graphs
* Upload the results to Cisco S3
* Pointer to direct view from S3 Dashboard

## Workflow

For the complete workflow of how this plugin can be used for, refer to:
https://github.com/CiscoTestAutomation/jenkins_project_plugin/blob/master/README.md#workflow-diagram

## ChangeLog

* [2018](changelog/2018/CHANGELOG.md)
* [2019](changelog/2019/CHANGELOG.md)
