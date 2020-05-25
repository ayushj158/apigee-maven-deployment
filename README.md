# apigee-maven-deployment

This repo defiens structure to deploy an API proxy or a shared flow bundle to APIGEE. It also lists the necessary maven commands to deploy aritifacts into APIGEE via maven-deploy-plugin

## Deploy API proxy Bundle
``` 
cd api-proxy

__ Build the artifact __
mvn package -P PROFILE_NAME(test/prod) -Dorg=YOUR_ORG_NAME

__ Deploy proxy __
mvn apigee-enterprise:deploy -P PROFILE_NAME(test/prod)  -Dusername=YOUR_USERNAME \
-Dpassword=YOUR_PASSWORD -Dorg=YOUR_ORG_NAME -X
```


## Deploy shared flow bundle
``` 
cd shared-flow

__ Build the artifact __
mvn package -P PROFILE_NAME(test-shared-flow/prod-shared-flow) -Dorg=YOUR_ORG_NAME

__ Deploy proxy __
mvn apigee-enterprise:deploy -P PROFILE_NAME(test-shared-flow/prod-shared-flow)  -Dusername=YOUR_USERNAME \
-Dpassword=YOUR_PASSWORD -Dorg=YOUR_ORG_NAME -X
``` 
