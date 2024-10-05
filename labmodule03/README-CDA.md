# Constrained Device Application (Connected Devices)

## Lab Module 03

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-03-001 - Lab Module 03](https://github.com/orgs/programming-the-iot/projects/1#column-10488379).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 
Implementation is to develop a limited device application with classes that represent the data and tasks of the various sensors and actuators to simulate their interactions. This system's primary components are the simulation of sensor and actuator activities and the management of sensor and actuator data. In order to facilitate coordination amongst sensor and actuator managers and enable them to replicate data collecting and processing, it incorporates a device data manager. In addition, the application offers ways to initiate and terminate the device management process, offering a regulated setting for controlling actuator and sensor simulations.
How does your implementation work?

The approach is built upon establishing an abstract base class, BaseIotData, that defines the data model for IoT devices. Certain sensor, actuator, and system performance classes, like SensorData, ActuatorData, and SystemPerformanceData, extend this class. There are methods in each of these classes for handling and processing the data that they create or gather. Concurrently, BaseSensorSimTask and BaseActuatorSimTask are abstract classes that manage sensor and actuator simulation jobs; actual subclasses of these classes simulate certain device types, such as HVAC actuators or temperature sensors.The DeviceDataManager, which coordinates the sensor and actuator managers (SensorAdapterManager and ActuatorAdapterManager), is the central component of the program. These managers are in charge of adding and overseeing tasks related to actuator and sensor simulation. The DeviceDataManager controls the data flow amongst the managers and guarantees accurate data processing and management. The ConstrainedDeviceApp, which integrates the complete system, manages the simulation's start and stop procedures by calling the required task simulations and managers.
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

BaseIotDataTest
SensorDataTest
ActuatorDataTest
SystemPerformanceDataTest
HumidifierActuatorSimTaskTest
HvacActuatorSimTaskTest
HumiditySensorSimTaskTest
PressureSensorSimTaskTest
TemperatureSensorSimTaskTest
ConfigUtilTest
BaseSensorSimTaskTest
BaseActuatorSimTaskTest
DeviceDataManagerTest
- 
- 

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

SensorAdapterManagerTest
ActuatorAdapterManagerTest
DeviceDataManagerNoCommsTest
ConstrainedDeviceAppTest 
- 

EOF.
