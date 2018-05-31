# Groovy Request and Response Save

Groovy Script to save your request and responses in a particular location.

```text
//Get the project path storage location
def projectPath = new com.eviware.soapui.support.GroovyUtils(context).projectPath.replace("\\", "/") //gets the path of the project root
//log.info(projectPath)
//Save the request and response in the below location
context.testCase.testSuite.setPropertyValue("XMLReqResLoc",projectPath+"/TestResults/")


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
def timeZone = TimeZone.getTimeZone("PST")
def dateStamp = new Date().format("yyyyMMdd",timeZone)
def timeStamp = new Date().format("yyyyMMdd_HHmmss",timeZone).toString()
def storageLocation = context.testCase.testSuite.getPropertyValue("XMLReqResLoc")
def requestFile = new File("${storageLocation}/${dateStamp}/Requests/${timeStamp}_${testCaseName}_${testStepName}_Request.xml")
def responseFile = new File("${storageLocation}/${dateStamp}/Response/${timeStamp}_${testCaseName}_${testStepName}_Response.xml")
saveToFile(requestFile, context.requestContent)
saveToFile(responseFile, context.response)

//To call in other scripts place below line
//context.testCase.testSuite.testCases["<TestCaseName>"].testSteps["<TestStepName>"].run(null,context)
```

