# Gateway Device Application (Connected Devices)

## Lab Module 05

Be sure to implement all the PIOT-GDA-* issues (requirements) listed at [PIOT-INF-05-001 - Lab Module 05](https://github.com/orgs/programming-the-iot/projects/1#column-10488421).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
In order to manage sensor and actuator data within the Gateway Device Application (GDA), Java modules must be created and modified. In particular, a base class named BaseIotData is the ancestor of four classes: SensorData, ActuatorData, SystemPerformanceData, and SystemStateData. For consistency and ease of mapping into a cloud-based representation of the device, each of these data classes will have a name and a type value. The SystemPerformanceManager will also be modified to invoke callbacks for new instances and store performance data using SystemPerformanceData. In order to manage device data, the DeviceDataManager class will also be developed. It will be integrated into the GatewayDeviceApp to start and stop data management procedures.

How does your implementation work?
BaseIotData is extended by the SensorData, ActuatorData, SystemPerformanceData, and SystemStateData classes, which guarantee a uniform structure for the data that the GDA processes. To ensure consistency throughout the application, each class will contain properties for the data name and type, which are predefined in the ConfigConst class. Telemetry data will be gathered by the SystemPerformanceManager, which will store it in SystemPerformanceData and alert listeners when new data becomes available. The DeviceDataManager will be instantiated within the GatewayDeviceApp to manage its lifecycle using start and stop methods, and the DataUtil class will be developed to provide utility functions for managing data operations.
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

- DataUtilTest
- ActuatorDataTest
- SensorDataTest
SystemPerformanceDataTest
SystemStateDataTest
### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- GatewayDeviceAppTest
DeviceDataManagerNoCommsTest
- DataIntegrationTest
- SystemPerformanceManagerTest

EOF.
