[comment]: # "Auto-generated SOAR connector documentation"
# Phishing Initiative

Publisher: Splunk  
Connector Version: 2.1.1  
Product Vendor: Phishing Initiative  
Product Name: Phishing Initiative  
Product Version Supported (regex): ".\*"  
Minimum Product Version: 5.3.5  

Implements reputational capabilities for URL by querying the Phishing Initiative web API

### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Phishing Initiative asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**base_url** |  required  | string | Base URL
**api_key** |  required  | password | API Key

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity  
[url reputation](#action-url-reputation) - URL Reputation  

## action: 'test connectivity'
Validate the asset configuration for connectivity

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'url reputation'
URL Reputation

Type: **investigate**  
Read only: **True**

This action runs a URL reputation query to check the connection and credentials.

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**url** |  required  | URL to Query | string |  `url`  `domain` 

#### Action Output
DATA PATH | TYPE | CONTAINS | EXAMPLE VALUES
--------- | ---- | -------- | --------------
action_result.status | string |  |   success  failed 
action_result.parameter.url | string |  `url`  `domain`  |   https://test.com 
action_result.data.\*.tag | numeric |  |   2 
action_result.data.\*.tag_label | string |  |   clean 
action_result.data.\*.url | string |  `url`  `domain`  |   https://test.com 
action_result.summary.tag_label | string |  |   clean 
action_result.message | string |  |   Tag label: clean 
summary.total_objects | numeric |  |   1 
summary.total_objects_successful | numeric |  |   1 