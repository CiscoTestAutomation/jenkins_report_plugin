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

## Feature Highlights
* Extract ResultsDetails.xml results file from a specific archive location(Free Style Project) or from the Jenkins _workspace_ (PyATS Project)
* Provide Test suite, and testcase result details with Trend graphs
* Option to upload the results to Cisco S3 and/or Cisco Trade
* Pointer to direct view from S3 Dashboard


