# OMF to Data Hub Quick Start Guide

**Version:** 1.0.0

The sample code in this folder demonstrates an example of using OMF to send data into AVEVA Data Hub and the Sequential Data Store (SDS) using Python Jupyter Notebook. In order to run this sample, you need to have [Python](https://www.python.org/downloads/) installed.

### Data Example 
The example in this guide will send data for a drone, including its location, battery, and operating temperature. It will cover how to create the OMF connection along with the appropriate OMF types and containers, and finally send data to an OMF endpoint. Once the data is sent to AVEVA Data Hub it will validate the ingress process by reading the drone data from SDS.

### Application Settings Parameters

- The notebook parameters are configured using the file [appsettings.placeholder.json](appsettings.placeholder.json). Before editing, rename this file to `appsettings.json`. This repository's `.gitignore` rules should prevent the file from ever being checked in to any fork or branch, to ensure credentials are not compromised.
- Populate the values of `appsettings.json` with your value for each parameter.
  For example:

```json
{
    "Resource": "PLACEHOLDER_REPLACE_WITH_RESOURCE",
    "ClientId": "PLACEHOLDER_REPLACE_WITH_CLIENT_ID",
    "ClientSecret": "PLACEHOLDER_REPLACE_WITH_CLIENT_SECRET",
    "TenantId": "PLACEHOLDER_REPLACE_WITH_TENANT_ID",
    "NamespaceId": "PLACEHOLDER_REPLACE_WITH_NAMESPACE_ID",
    "TopicName": "PLACEHOLDER_REPLACE_WITH_TOPIC_NAME",
    "TopicDescription": "PLACEHOLDER_REPLACE_WITH_TOPIC_DESCRIPTION",
    "SubscriptionName": "PLACEHOLDER_REPLACE_WITH_SUBSCRIPTION_NAME",
    "SubscriptionDescription": "PLACEHOLDER_REPLACE_WITH_SUBSCRIPTION_DESCRIPTION"
}
```

| Parameters      | Required | Type           | Description                                                                                                                                                  |
| --------------- | -------- | -------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| Resource        | required | string         | The endpoint for ADH of the namespace. If the namespace is located in NA, it is https://uswe.datahub.connect.aveva.com and if in EMEA, it is https://euno.datahub.connect.aveva.com                                                                                                                                    |
| ClientId | required | string         | The id of the client credentials client to use                                                                                                        |
| ClientSecret    | required | string         | The secret of the client credentials client to use                                                                                                                                                 |
| TenantId    | required | string         | The id of the tenant to use                                                                                                         |
| NamespaceId        | required | string         | The id of the namespace to use                                                                                                                                   |
| TopicName        | required | string         | The name of the OMF topic to create
| TopicDescription        | optional | string         | The description of the OMF topic to create
| SubscriptionName        | required | string         | The name of the OMF subscription to create
| SubscriptionDescription        | optional | string         | The description of the OMF subscription to create
                                           
                              
### Running the Jupyter Notebook

1. Install required modules by running:
    ```bash
    pip install -r requirements.txt
    ```
1. Open a terminal and type in `jupyter notebook`. This will open a browser window. Navigate to the cloned repository and open up `quickstart.ipynb`. Run the cells one by one and you can see the output in browser itself.

## Documentation

The documentation for the various topics and APIs used here can be found at the [AVEVA Data Hub documentation website](https://docs.osisoft.com/category/adh-get-started)

---

For the main OMF basic samples page [ReadMe](https://github.com/osisoft/OSI-Samples-OMF/blob/main/docs/OMF_BASIC.md)  
For the main OMF samples page [ReadMe](https://github.com/osisoft/OSI-Samples-OMF)  
For the main AVEVA samples page [ReadMe](https://github.com/osisoft/OSI-Samples)