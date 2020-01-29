Compile the project:

    mvn package

Add `configuration` in `mule-maven-plugin`.

```xml
    <!-- https://docs.mulesoft.com/mule-runtime/4.2/mmp-concept -->
    <cloudHubDeployment>
        <uri>https://anypoint.mulesoft.com</uri>
        <muleVersion>${app.runtime}</muleVersion>
        <username>${cloudhub.username}</username>
        <password>${cloudhub.password}</password>
        <applicationName>${project.artifactId}</applicationName>
        <environment>Sandbox</environment>
        <workerType>MICRO</workerType>
    </cloudHubDeployment>
```

Deploy using the command line:

    mvn deploy -DmuleDeploy -Dcloudhub.username=<username> -Dcloudhub.password=<password>

