### Groovy Request and Response Save {#test-case-creation}

---

Groovy Script to save your request and responses in a particular location.

```
//Get the project path stored in
def projectPath = new com.eviware.soapui.support.GroovyUtils(context).projectPath //gets the path of the project root
log.info projectPath

//Check if there is response
assert context.request, "Request is empty or null"

//Save the contents to a file
def saveToFile(file, content) {
    if (!file.parentFile.exists()) {
         file.parentFile.mkdirs()
         log.info "Directory did not exist, created"
    }
    file.write(content) 
    assert file.exists(), "${file.name} not created"
}
def testCaseName = context.testCase.name.take(10) 
def testStepName = context.testCase.getTestStepAt(context.getCurrentStepIndex()).getLabel() 
def timeZone = TimeZone.getTimeZone("HST")
def dateStamp = new Date().format("yyyyMMdd",timeZone)
def timeStamp = new Date().format("yyyyMMdd_HHmmss",timeZone).toString()
def storageLocation = context.testCase.testSuite.getPropertyValue("XMLReqResLoc")
def requestFile = new File("${storageLocation}/${dateStamp}/Requests/${timeStamp}_${testCaseName}_${testStepName}_Request.xml")
def responseFile = new File("${storageLocation}/${dateStamp}/Response/${timeStamp}_${testCaseName}_${testStepName}_Response.xml")
saveToFile(requestFile, context.requestContent)
saveToFile(responseFile, context.response)

//To call in other scripts place below line
//context.testCase.testSuite.testCases["InitialTC"].testSteps["ScriptAssertion"].run(null,context)
```



