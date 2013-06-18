> **Note in advance**
> 
> *This document is part of the [Developer Guide](DeveloperGuide.md)*

# Continuous Integration

For [continuous integration](http://en.wikipedia.org/wiki/Continuous_integration) Travis CI is used. Once a pull request is opened (for the master branch) Travis CI will build Titan and run all tests in order to see if nothing is broken. In this way is made sure the master can always be deployed to users. The settings for Travis CI are specified in the `.travis.yml` file.
