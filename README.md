[comment]: # "Auto-generated SOAR connector documentation"
# Phishing Initiative

Publisher: Splunk  
Connector Version: 2\.0\.2  
Product Vendor: Phishing Initiative  
Product Name: Phishing Initiative  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 4\.9\.39220  

Implements reputational capabilities for URL by querying the Phishing Initiative web API

### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a Phishing Initiative asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**api\_key** |  required  | password | API Key

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

This action runs a URL reputation query to check the connection and credentials\.

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**url** |  required  | URL to Query | string |  `url`  `domain` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.data\.\*\.tag | numeric | 
action\_result\.data\.\*\.url | string |  `url`  `domain` 
action\_result\.data\.\*\.tag\_label | string | 
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.summary\.tag\_label | string | 
action\_result\.parameter\.url | string |  `url`  `domain` 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 