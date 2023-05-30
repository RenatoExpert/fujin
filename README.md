FUJIN SCADA
# Brief
A modern out-of-the-box SCADA system, open source, free to use.

# Architecture
Fujin SCADA is written in Java.
The system may be implemented in three sections: Field, Services and Operational.
## Field
This section holds instrument/transmitters, controllers and flow computers.
Once each equipment may have its own communication protocol, its purposive to use an OPC server.
An OPC server may comunicate with different protocols (fieldbus, modbus, hart) and send in a agnostic manner to SCADA server.
## Services
Services section is responsible to get information from instruments, store data, send commands to instruments.
Runtime subsection is inside this section, along with Storage, Software Repository and Project Repository subsections.
Runtime subsection can be split into Fujin SCADA Server + Redis Cache.
Storage subsection can be split into the following databases: self [security(passwords, logs)] + operational [business(clients: location, equipment info) + measurement(history data) + relatories(eg. montly flow)]
## Operational
A set of interfaces for human use, basically the client software.

# Install

$ ./gradlew build
$ ./gradlew run


# Development
## Dependencies
Open JDK 8
Gradle
Kotlin
## References
Automated Tests https://betterprogramming.pub/how-to-write-automation-tests-with-java-ed468e0af305
Gradle Projects https://docs.gradle.org/current/samples/sample_building_java_applications.html

# Licence

# Contact

# Development Goals
CORE ARCHTECTURE
[ ] Basic project archtecture
[ ] CI process
[ ] Versioning model

TESTS
[ ] Automated tests

COMMUNICATION
[ ] OPC
[ ] Prompt
[ ] Websockets
