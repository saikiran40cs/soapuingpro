### Script Assertion {#test-case-creation}

---

In this case it is Script.

1. Select Script Assertion and there no sub-types associated with it.
2. Click 'Add'.
3. The Scripting Dialog opens where user will be able to write user defined script to validate the response XML.

4. Now let us write a groovy script to validate the Conversion Rate. The Script is attached below with the comments embedded. It is recommended to have knowledge on JavaScript or Groovy Script before attempting to write your own script.

```
//Define Groovy Utils and holder for validating the XML reponse content

def groovyUtils = new com.eviware.soapui.support.GroovyUtils(context)
def holder = groovyUtils.getXmlHolder(messageExchange.responseContent)

//Define the NameSpace
holder.namespaces["ns"] = "http://www.webserviceX.NET/"

//Get the Value of the Node 'ConversionRateResult' and assign to a variable
def conversionRate = holder.getNodeValue("//ns:ConversionRateResult")

//print the value of the conversion rate in the Output pane
log.info "The conversion value from USD to INR is " + conversionRate

//Comparing the value to print 'Pass' or 'Fail'
if(conversionRate=="63.7854")
{ log.info "Pass" }
else
{ log.info "fail"}
```

Click 'Execute' Button to trigger the execution.

1. The output of the Script is shown in the Output pane. It has printed both, Conversion Value as well as the end result \(Pass or Fail\)
2. The Information is displayed that 'Script Assertion Passed'. Click OK.

**Note:**The final Information pop up will always display with the message '**Script Assertion Passed**' as long as the script is syntactically correct. It has got no correlation with your assertion within the script.

If you want to call a particular groovy script in other test cases. Below is the format to call it

```
context.testCase.testSuite.testCases["<TestCaseName>"].testSteps["<TestStepName>"].run(null,context)
```



