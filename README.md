# PaymentHub EE / Interledger Protocol 1.0 library publish
This gradle project and repository exists only to publish the interop-ilp-conditions-1.7.1.jar to the Mifos JFrog repository in the correct format

## notes 
- even though there seems to be some ILP code in the maven repositories this library and the source code for it seems to be different and hence the need to have it published. 
- this gradle project exists simply to ensure that the interop-ilp-conditions-1.7.1.jar is published to and available to the mojaloop connector from the Mifos Artifactory repository (see the build.gradle for details of the repo and repo key )
- As there is no source code (which I can find) for this .jar file the only relevant gradle task is artifactoryPublish 
- JFrog authentication is done via JFrog access tokens and the environment variables below must be set  prior to running gradlew          
  - MIFOS_ARTIFACTORY_USER 
  - MIFOS_ARTIFACTORY_TOKEN
- This is not well tested and the contents of this repository are largely for documentation purposes , what really matters is that this ILP library is available to other gradle and maven builds as implementation 'org.mifos:interop-ilp-conditions:1.7.1'
- for further example of accessing this .jar file see the build.gradle in the gazelle-dev1 branch of the ph-ee-connector-mojaloop repo
