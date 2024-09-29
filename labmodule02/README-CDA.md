# Constrained Device Application (Connected Devices)

## Lab Module 02

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-02-001 - Lab Module 02](https://github.com/orgs/programming-the-iot/projects/1#column-9974938).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
To track system performance metrics on constrained devices, like CPU and memory use, the solution generates a Constrained Device Application (CDA). It makes use of Python modules to package up a number of features, such as scheduling, logging, and system performance management. The program launches a performance manager that records and gathers telemetry data on a regular basis, allowing for real-time system health monitoring. This gives consumers insightful information that enables them to take prompt action based on patterns in resource utilization.

How does your implementation work?
ConstrainedDeviceApp, SystemPerformanceManager, and system utility tasks (CPU and memory monitoring) are the main components of the implementation. A SystemPerformanceManager instance is created by the program upon startup, and it uses APScheduler to build up a scheduler to poll performance metrics at predetermined intervals. The psutil library is used by each utility task to obtain pertinent data. The program records the gathered telemetry data and uses logging to record significant occurrences, like when the program launches or terminates. The architecture's modular design makes maintenance and extension simple, paving the way for the eventual inclusion of more monitoring features.
### Code Repository and Branch

NOTE: Be sure to include the branch (e.g. https://github.com/programming-the-iot/python-components/tree/alpha001).

URL: https://github.com/lohitha0798/Connected_Device_CDA.git

### UML Design Diagram(s)

NOTE: Include one or more UML designs representing your solution. It's expected each
diagram you provide will look similar to, but not the same as, its counterpart in the
book [Programming the IoT](https://learning.oreilly.com/library/view/programming-the-internet/9781492081401/).


### Unit Tests Executed

NOTE: TA's will execute your unit tests. You only need to list each test case below
(e.g. ConfigUtilTest, DataUtilTest, etc). Be sure to include all previous tests, too,
since you need to ensure you haven't introduced regressions.


SystemPerformanceManagerTest
SystemCpuUtilTaskTest
SystemMemUtilTaskTest
ConfigUtil

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

SystemPerformanceManagerTest
ConstrainedDeviceAppTest


EOF.
