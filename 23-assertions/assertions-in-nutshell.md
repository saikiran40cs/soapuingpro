### Assertions in a NutShell

---

&lt;!--  
 /\* Font Definitions \*/  
 @font-face  
	{font-family:"Cambria Math";  
	panose-1:2 4 5 3 5 4 6 3 2 4;  
	mso-font-charset:1;  
	mso-generic-font-family:roman;  
	mso-font-format:other;  
	mso-font-pitch:variable;  
	mso-font-signature:0 0 0 0 0 0;}  
@font-face  
	{font-family:Calibri;  
	panose-1:2 15 5 2 2 2 4 3 2 4;  
	mso-font-charset:0;  
	mso-generic-font-family:swiss;  
	mso-font-pitch:variable;  
	mso-font-signature:-536859905 -1073732485 9 0 511 0;}  
 /\* Style Definitions \*/  
 p.MsoNormal, li.MsoNormal, div.MsoNormal  
	{mso-style-unhide:no;  
	mso-style-qformat:yes;  
	mso-style-parent:"";  
	margin-top:0in;  
	margin-right:0in;  
	margin-bottom:8.0pt;  
	margin-left:0in;  
	line-height:107%;  
	mso-pagination:widow-orphan;  
	font-size:11.0pt;  
	font-family:"Calibri",sans-serif;  
	mso-ascii-font-family:Calibri;  
	mso-ascii-theme-font:minor-latin;  
	mso-fareast-font-family:Calibri;  
	mso-fareast-theme-font:minor-latin;  
	mso-hansi-font-family:Calibri;  
	mso-hansi-theme-font:minor-latin;  
	mso-bidi-font-family:"Times New Roman";  
	mso-bidi-theme-font:minor-bidi;}  
.MsoChpDefault  
	{mso-style-type:export-only;  
	mso-default-props:yes;  
	font-family:"Calibri",sans-serif;  
	mso-ascii-font-family:Calibri;  
	mso-ascii-theme-font:minor-latin;  
	mso-fareast-font-family:Calibri;  
	mso-fareast-theme-font:minor-latin;  
	mso-hansi-font-family:Calibri;  
	mso-hansi-theme-font:minor-latin;  
	mso-bidi-font-family:"Times New Roman";  
	mso-bidi-theme-font:minor-bidi;}  
.MsoPapDefault  
	{mso-style-type:export-only;  
	margin-bottom:8.0pt;  
	line-height:107%;}  
@page WordSection1  
	{size:8.5in 11.0in;  
	margin:1.0in 1.0in 1.0in 1.0in;  
	mso-header-margin:.5in;  
	mso-footer-margin:.5in;  
	mso-paper-source:0;}  
div.WordSection1  
	{page:WordSection1;}  
--&gt;  


| **Asserting Mechanism** | **Description** |
| :--- | :--- |
| **PROPERTY CONTENT** |  |
| Contains | Searches for the existence of the specified string. It also supports regular expression. |
| Not Contains | Searches for the Non-existence of the specified string. It also supports regular expression. |
| XPath Match | Uses XPath expression to select the target node and its values. |
| XQuery Match | Uses an Xquery expression to select content from the target property. |
| **Compliance , Status, Standards** |  |
| HTTP Download all resource | Validates the HTML Document after downloading and it holds good to any property containing HTML. |
| Invalid HTTP Status Codes | Verifies if the HTML response contains a status code that is not in the list of defined codes. |
| Not SOAP Fault | Verifies if the last received message is not a SOAP Fault. It is very obvious that it is applicable only for SOAP Test Steps. |
| Schema Compliance | Verifies if the last received message is compliant with the WSDL or WADL standard schema definition. Holds good for SOAP and REST Test Steps. |
| SOAP Fault | Verifies if the last received message is a SOAP Fault. It is the inverse of 'NOT SOAP' Fault Assertions. |
| SOAP Response | Verifies if the last received response is a valid SOAP Response and holds good for SOAP Test Request Steps only. |
| Valid HTTP Status Codes | Verifies if the HTML response contains a status code that is in the list of defined codes. It is the inverse of 'Invalid HTTP Status Codes' Assertion. |
| WS-Addressing Request | Verifies if the last received request contains appropriate WS-Addressing Headers. |
| WS-Addressing Response | Verifies if the last received response contains appropriate WS-Addressing Headers. |
| WS-Security Status | Validates if the last received message contains valid WS-Security headers and holds good only for SOAP Requests. |
| **Script** |  |
| Script Assertion | Allows users to execute a custom script to perform user defined validations. |
| **SLA** |  |
| Response SLA | Validates if the response time of the last received response was within the defined limit. |
| **JMS** |  |
| JMS Status | Verifies if the JMS request of the Test Step has executed successfully and holds good for Test Steps with a JMS endpoint. |
| JMS Timeout | Verifies if that the JMS response of a test step did not took longer than the specified duration. |
| **Security** |  |
| Sensitive Information Exposure | Verifies if the response message does not expose sensitive information about the target system. We can use this assertion for REST, SOAP and HTTP Test Steps. |





