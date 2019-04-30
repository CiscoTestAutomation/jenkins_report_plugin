# Report Plugin XML Specification

The XML specification to remotely configure the pyATS Report Plugin (through REST API):

```
<publishers>
    <asg.pyats.plugins.pyatsreport.PyATSReportPublisher plugin="pyats-report-plugin@1.0">
        <zipFile/>
        <uploadS3>true</uploadS3>
        <s3Server>some-server:8088</s3Server>
        <s3RequestId>req001</s3RequestId>
    </asg.pyats.plugins.pyatsreport.PyATSReportPublisher>
</publishers>
```

XML Tag Details:
* zipFile: [Free Style Project] A Cisco test archive file that the user wishes to use for uploading.  
* uploadS3: Option to upload the Cisco test results to the Cisco Xpresso portal.
* s3Server: Xpresso instance URL is required.  
* s3RequestId: The Xpresso request ID. 

To upload to Xpresso, authentication token is required:

```
<properties>
    <hudson.model.ParametersDefinitionProperty>
        <parameterDefinitions>
            <hudson.model.PasswordParameterDefinition>
                <name>xpresso_auth_token</name>
                <defaultValue>{token value}</defaultValue>
            </hudson.model.PasswordParameterDefinition>
        </parameterDefinitions>
    </hudson.model.ParametersDefinitionProperty>
</properties>
```

Details can also be found on the (**?**) help for each configurable item on the Jenkins post-build actions UI.