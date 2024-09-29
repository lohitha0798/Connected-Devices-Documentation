# Gateway Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-02-001 - Lab Module 02](https://github.com/orgs/programming-the-iot/projects/1#column-9974938).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Connected devices' system performance measurements are gathered and managed centrally by the Gateway Device Application (GDA). It incorporates a number of system utility functions, such memory and CPU utilization monitoring, to guarantee the IoT environment runs smoothly. The GDA continuously collects telemetry data, processes it, and offers insights into the system's health through the use of a scheduled task runner. Additionally, the program controls its lifetime, enabling appropriate startup and shutdown procedures, which include initiating and terminating the tasks related to performance monitoring.
How does your implementation work?
The Gateway Device Application (GDA) is intended to effectively supervise and manage the connected Internet of Things devices' system operation. The application starts up by creating an instance of the SystemPerformanceManager, which is in charge of organizing several system utility jobs. This manager runs activities at predetermined intervals using Java's ScheduledExecutorService, which enables continuous monitoring of system metrics like CPU and memory use.the SystemPerformanceManager's startManager() method is called by the GDA's startApp() method, which is called by the GDA itself. This function starts the scheduled tasks, which run the utility tasks' getTelemetryValue() methods on a regular basis to gather telemetry data. Every task logs the results for later study after obtaining pertinent performance statistics using the Java Management API. The GDA records all of its operations while it is in operation, including the telemetry data it has acquired and the successful starting and shutdown routines. The stopManager() method is called when the application terminates, causing the stopApp() method to be called as well. This ensures that all resources are released in an orderly manner and ends the scheduled tasks.
### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/lohitha0798/Connected-Devices-GDA.git

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.

ConfigUtilTest
SystemPerformanceManagerTest
SystemCpuUtilTaskTest
SystemMemUtilTaskTest
- 
- 

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

GatewayDeviceAppTest
SystemPerformanceManagerIntegrationTest
SystemCpuUtilTaskIntegrationTest
SystemMemUtilTaskIntegrationTest
- 
- 

EOF.
