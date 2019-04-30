# Quick Start

## Step 1:
Navigate to project configuration, click on "Add post-build action" and select "Publish pyATS Report" from the list.

![](assets/images/config1.png)

## Step 2:
Based on the project type (pyATS Project or Free style Project) the Report plugin interface will have minor differences depending on where the _test result archive (.zip)_ is saved.  The _pyATS Project_  saves the test results archive in Jenkins _workspace_ where as the _Free Styple Project plugin_ saves the Test result archive in user specified location. 

_Free Style project_:

* Specify the absolute path to the Test result archive file.  The file must be accessible from the build node (master/slave).
Report Plugin will validate the specified path, in the event of the file not being found/reachable from the current running node (master node), warning message displays. These warning message should be ignored if a _variable_ is used to specify the path, or the build and the archive file are located on remote/slave node.

![](assets/images/config3.png)


## Step 3:

To upload the archive to the Xpresso portal specify:
* The Xpresso instance URL:
  * http://hostname
  * http://hostname:port
* The Xpresso top level *Request ID*  

![](assets/images/config4.png)


### Xpresso Parameter Configuration

Uploading results to Xpresso requires REST API authentication. This is a mandatory parameter to be granted the uploading permission for Jenkins. The Authentication Token Parameters is specified through Jenkins native _Password Parameter_ component. Other optional Xpresso execution specific Parameters is specified through Jenkins native _String Parameter_ component.

Xpresso specific parameters are prefixed with *xpresso_* such as:  
* **xpresso_auth_token**: Xpresso automation token (mandatory parameter)
* **xpresso_branch**: indicating the image branch for the execution (optional parameter)
* **xpresso_component**: indicating the feature component the sanity job covers (optional parameter)
* **xpresso_group**: indicating the group for the execution (optional parameter, but needed when Xpresso *Request ID* is invalid)
* **xpresso_result_id**: indicating the result id the Xpresso will be using for uploading. Added for Autoeasy uploading support (optional parameter)

![](assets/images/config6.png)

## Execution and Output

To execute the job, click "Build Now" on the project page:

![](assets/images/run.png)

### View Results on Jenkins
As the build is completed go to "Build Result Summary" page, click on Jenkins project *build number* to be redirected to  "build result summary" page.  

Example of "Build Result Summary" output: 

![](assets/images/output1.png)

The general information of the job, the report provides the overall result (pass/fail percentage) of the run. Click the **Build # pyATS report** link to view the details of each Test. 

![](assets/images/output2.png)

### View results from Cisco Xpresso dashboard
Click "Cisco Xpresso Result" will go directly to the Xpresso instance the result is uploaded to.

![](assets/images/s3output1.png)  ![](assets/images/s3output2.png)