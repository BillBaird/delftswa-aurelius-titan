> **Note in advance**
>
> *This document is part of the [Developer Guide](DeveloperGuide.md)*

# Building Titan

To build Titan you need [Git](http://git-scm.com/) and [Maven](http://maven.apache.org/). First of all clone the repository to a local directory. 

`https://github.com/thinkaurelius/titan.git`

For building the project [Maven](http://maven.apache.org/), a build automation tool is used. If it is installed you can execute `mvn clean install`. This will build Titan and run the internal test suite. The internal test suite has no external dependencies. Note, that running all test cases requires a significant amount of time. To skip the tests when building Titan, execute `mvn clean install -DskipTests`.
