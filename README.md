This is the repository for the Diaspoship API backend.

## Build the project with gradle

### Building the sample project

To build the project on unix-based systems:

    ./gradlew build

Windows users: Use `gradlew.bat` instead of `./gradlew`

### Generating the openapi.json file

To generate the required configuration file `openapi.json`:

    ./gradlew endpointsOpenApiDocs

This results in a file in build/endpointsOpenApiDocs/openapi.json

### Deploying the sample API to App Engine

To deploy the sample API:

0. Invoke the `gcloud` command to deploy the API configuration file:

         gcloud service-management deploy build/endpointsOpenApiDocs/openapi.json

0. Deploy the API implementation code by invoking:

         ./gradlew appengineDeploy

0. Wait for the upload to finish.
