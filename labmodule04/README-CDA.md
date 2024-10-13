# Constrained Device Application (Connected Devices)

## Lab Module 04

Be sure to implement all the PIOT-CDA-* issues (requirements) listed at [PIOT-INF-04-001 - Lab Module 04](https://github.com/orgs/programming-the-iot/projects/1#column-10488386).

### Description

NOTE: Include two full paragraphs describing your implementation approach by answering the questions listed below.

What does your implementation do? 

Using Python, the program simulates sensor and actuator activities for a limited IoT device environment. By creating new Python modules from BaseSensorSimTask and BaseActuatorSimTask, it replicates real-world sensors such  as pressure, humidity, and temperature sensors and actuators like humidifiers, HVAC systems, and LED displays. A complete simulation may be performed without the use of actual hardware  to the implementation's integration with the SenseHAT emulator, which reads sensor data and controls actuators. This method allows the application to collect, process, and react to sensor data or commands as if it were dealing with real hardware, simulating the behavior of IoT devices in real-world circumstances.

How does your implementation work?

The way the implementation functions is by adding additional base simulation tasks for actuators and sensors. For sensors, it uses the SenseHAT emulator to read data by simulating pressure, temperature, and humidity readings from sensors. To control the flow of sensor data within the application, the SensorAdapterManager processes the data after that. Similarly, for actuators, the LED matrix of the SenseHAT allows the BaseActuatorSimTask to be extended to control appliances like the humidifier and HVAC system. These simulated actuators are activated and deactivated by the ActuatorAdapterManager in response to system commands and sensor readings. In order to create a working IoT simulation environment, each task processes its corresponding data, uses logic to control devices, and reports the actions taken.
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

- BaseActuatorSimTaskTest
- SensorAdapterManagerTest
- ActuatorAdapterManagerTest
-BaseSensorSimTaskTest
-ConfigUtilTest

### Integration Tests Executed

NOTE: TA's will execute most of your integration tests using their own environment, with
some exceptions (such as your cloud connectivity tests). In such cases, they'll review
your code to ensure it's correct. As for the tests you execute, you only need to list each
test case below (e.g. SensorSimAdapterManagerTest, DeviceDataManagerTest, etc.)

- ActuatorEmulatorManagerTest
-SensorEmulatorManagerTest
- HumidifierEmulatorTaskTest
-HvacEmulatorTaskTest
-LedDisplayEmulatorTaskTest
- HumidityEmulatorTaskTest
-PressureEmulatorTaskTest
-TemperatureEmulatorTaskTest

EOF.
