# Spring Serial Port Connector

Is a Spring library to read/write a serial/usb port in your Spring App. Based on 
- Spring Boot
- NeuronRobotic Library https://github.com/NeuronRobotics/nrjavaserial

## Maven Dependency

```
<dependency>
    <groupId>com.github.diegosep</groupId>
    <artifactId>spring-serial-port-connector</artifactId>
    <version>0.0.1-RELEASE</version>
</dependency>
```

###Optional 
Could be needed add this repository in you maven POM file

```
<repositories>
  <repository>
    <id>sonatype</id>
    <url>https://oss.sonatype.org/service/local/repositories/releases/content</url>
  </repository>
</repositories>

```

## How to use it
This library needs two properties

```
springSerialPortConnector.portName= #Serial port name, depends on your operative system
springSerialPortConnector.baudRate= #Baud serial rate transmition 
```
### Implementation
Implement a Spring bean from this class **AbstractSpringSerialPortConnector** and override
the following method

```   
/**
     * This method must implemented with logic that you want execute at the moment to read
     * information from the serial port
     *
     * @param line
     */
    public abstract void processData(String line);
```
### Example

For a Linux System
```
springSerialPortConnector.portName=/dev/ttyACM0
springSerialPortConnector.baudRate=9600
```

## authors
[@colopezfuentes](https://github.com/colopezfuentes)
[@diegosep](https://github.com/diegosep)


