# Constrained Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-05-001 - Lab Module 05](https://github.com/orgs/programming-the-iot/projects/1#column-10488421).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
By gathering and storing system performance information, including as CPU, memory, and disk utilization, in the SystemPerformanceData class, the implementation improves SystemPerformanceManager. Every time a new SystemPerformanceData instance is produced, it sets off a callback on the IDataMessageListener to guarantee real-time updates for external components. Furthermore, to handle effective data processing and storage, the DataUtil class is either added or updated, increasing the performance monitoring system's overall robustness and responsiveness.
How does your implementation work?
SystemPerformanceData contains the information that the SystemPerformanceManager gathers from handleTelemetry() to gather performance measurements. In order to enable other system components to respond to the changed data, it first verifies that the IDataMessageListener is set before calling the relevant callback when new data is created. To ensure seamless and effective data processing, the DataUtil class offers utility functions for data handling operations such serialization and transformation.
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
DataUtilTest
- 
- 
- 

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- DataIntegrationTest
- SystemPerformanceManagerTest
- 

EOF.
