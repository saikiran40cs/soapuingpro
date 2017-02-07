### **Test Case Creation** {#test-case-creation}

You can now click ![http://readyapi.smartbear.com/_media/loadui_ng/getting_started/run_b.png](assets/httpreadyapismartbearcommedi.png)to send individual requests to the service. Ready! API will display the response from the service once it is received.

![http://readyapi.smartbear.com/_media/soapui/getting_started/createdproject.png](assets/httpreadyapismartbearcommedi.png)

To automate your tests, for example to send multiple requests at once or create [data-driven tests](http://readyapi.smartbear.com/soapui/data_driven/start), you need to create a SoapUI NG test:

*   Right-click the REST request and select **Add to TestCase**. ![http://readyapi.smartbear.com/_media/soapui/getting_started/addtotestcase.png?w=400&tok=7273d8](assets/httpreadyapismartbearcommedi.png)
*   Specify the name of the TestSuite and TestCase that will contain the request. SoapUI NG will create a TestSuite and TestCase for the request.
*   Specify the name of the request and leave the rest of the options the same. Click **OK**

![http://readyapi.smartbear.com/_media/soapui/getting_started/addrequest_dialog.png?w=400&tok=2150bf](assets/httpreadyapismartbearcommedi.png)

Ready! API will create a SoapUI NG test.

**Execution in SoapUI NG Pro**

The test execution is SoapUI NG Pro can be performed in three hierarchies(Test case,Test Suite and Project level)

When you run tests from the request window, only the selected request is simulated. This is convenient when you prepare for testing or when you run simple tests, since you can instantly access the response, modify the request or add assertions. In more complex tests the requests often rely on the data from previous TestSteps, these requests will fail. To run the individual request, click ![http://readyapi.smartbear.com/_media/loadui_ng/getting_started/run_b.png](assets/httpreadyapismartbearcommedi.png).![http://readyapi.smartbear.com/_media/soapui/getting_started/runrequest.png](assets/httpreadyapismartbearcommedi.png)

When you run tests from TestCases, all TestSteps in this TestCase are simulated in order. The editor provides a wide variety of possible actions that are not available on TestStep level, such as comparing test runs or viewing test history. To run all TestSteps in the TestCase, click ![http://readyapi.smartbear.com/_media/loadui_ng/getting_started/run_b.png](assets/httpreadyapismartbearcommedi.png).

![http://readyapi.smartbear.com/_media/soapui/getting_started/runtestcase.png](assets/httpreadyapismartbearcommedi.png)