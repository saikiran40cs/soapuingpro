### Assertions in a NutShell

---

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



