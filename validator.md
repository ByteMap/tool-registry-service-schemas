---
layout: page
title: Tool Registry Service Validator
permalink: /Validator/

---
### Tool Registry Service Validator
This tool registry validator checks tool registry service URLs to determine if it conforms to the [ga4gh-tool-discovery.yaml](https://raw.githubusercontent.com/ga4gh/tool-registry-service-schemas/2.0.0-beta.1/src/main/resources/swagger/ga4gh-tool-discovery.yaml) swagger specification.  For each endpoint, the validator checks if:


- the endpoint is reachable
- the header info (such as content-type) is available and correct
- the response objects contain all required properties
- the correct response code is returned

and much more.  The validator provides badges based on the results.

---
#### Validation Server Health
See [health]({{site.validation-server-url}}/health_check) of the validation server.


#### Validation Server Environment
See [environment]({{site.validation-server-url}}/environment) of the validation server.

---
#### Tool Registry Service Validation Status
Below is a list of tool registry services and its validation status:

Dockstore Staging [![Validator Running]({{site.validation-server-url}}/trs/validator?url=https://staging.dockstore.org:8443)]({{site.validation-server-url}}/trs/validator/debug?url=https://staging.dockstore.org:8443) 

Dockstore [![Validator Running]({{site.validation-server-url}}/trs/validator?url=https://dockstore.org:8443)]({{site.validation-server-url}}/trs/validator/debug?url=https://dockstore.org:8443) 


---
#### Validator Info

##### Instructions to add your tool registry service to this validator

Make another entry by copying the placeholder line below and simply changing {placeholder_name} to your service name and {placeholder_url} to your service's URL and then adding it to the above "Tool Registry Service Validation Status" section.

{placeholder_name} [![Validator Running]({{site.validation-server-url}}/trs/validator?url={placeholder_url})]({{site.validation-server-url}}/trs/validator/debug?url={placeholder_url})

##### Description of badges

- Error badge indicates one or more endpoints have errored (possibly because the URL could not be reached)
- Failure indicates that there were no errors but one or more endpoints have failed validation (one of many reasons.  Click on badge for details)
- Warning badge indicates there were no errors or failures, but one or more endpoint was skipped (possibly because there was no tools returned so object definition could not be checked)
- Passing badge indicates all endpoints were successfully validated

In general, click on badge for more details about the result.

##### Additional Notes

If you see "Validator Running", wait or refresh the page in a minute.  Validation for each service is only performed at most once every 5 mins (previous badge is shown otherwise).

