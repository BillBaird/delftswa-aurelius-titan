> **Note in advance**
> 
> *This document is part of the [Developer Guide](DeveloperGuide.md)*

# Developing Titan

This document describes how to get started with developing Titan itself. There is a separate page describing how to [build Titan](BuildingTitan.md).

## Finding work to do

First of all you need something to work on! Unless you have found a particular issue you would like to work on, we could use your help solving issues from [Github](https://github.com/thinkaurelius/titan/issues). When you find an issue you would like to work on add a comment to the issue so the core developers and other people looking for work know that someone is already working on it.

## Downloading the source

The source repository uses [Git](http://git-scm.com/) and can be found on [Github](https://github.com/thinkaurelius/titan). Instructions on Git use can be found in the online book [Pro Git](http://git-scm.com/book/). Fork the repository to work on it. 

`https://github.com/thinkaurelius/titan.git`

## Testing

You will find many tests in Titan. There are unit tests for correctness (e.g. check whether a return value equals a certain value). After unit testing there are several integration tests for important interfaces that can be extended when you for instance add a new backend. Besides these tests there is also a performance test which extends the com.tinkerpop.blueprints.TestSuite class that checks whether performance hasn't decreased.  

If at all possible, create or modify a unit test to demonstrate the problem, and then validate your fix. If the problem case can't be set up in the unit tests, add an integration test.

Before submitting a patch, in any case, you should run all of the integration tests. For comprehensive test coverage, execute `mvn clean test -P comprehensive`. This will run additional test covering communication to external storage backends, performance tests and concurrency tests. The comprehensive test suite uses Cassandra and HBase as external databases and requires that Cassandra and HBase are installed. Note, that running the comprehensive test suite requires a significant amount of of time (> 1 hour).

## Creating and submitting your work

When you have either completed an issue or just want some feedback on the work you have done, create a pull request and mention in the title the number of the issue in question. We have a couple of guidelines when creating pull requests:

* Always for the master, not a branch. Otherwise, your repository is outdated the moment you create it and might not be applicable to the development head.
* If this was a new piece of work without an issue, create a new issue for it now
* When finished create a pull request mentioning the number of the issue in question. Shortly after, someone will evaluate the pull request, close the issue and merge the pull request.

## Acceptance criteria

There are a number of criteria that your work will be judged on:

* Whether it works and does what is intended. This one is probably obvious.
* Whether it doesn't degrade performance. This point is explicitely mentioned, because performance is one of the most important elements that distinguishes Titan from other solutions and why people buy in to Titan.
* Whether it fits the spirit of the project. Some work may be rejected as it takes the project in a different direction to than the main developers have outlined. This is usually discussed on an issue well before something is contributed, so if you are unsure, discuss it on [Github](https://github.com/thinkaurelius/titan/issues). Feel free to continue discussing it (with new justification) if you disagree, or appeal to a wider audience on the [mailing list](https://groups.google.com/forum/#!forum/aureliusgraphs).
* Whether it contains tests. It is expected that any pull request relating to functionality will be accompanied by unit tests and/or integration tests. It is strongly desired (and will be requested) for bug fixes too, but will not be the basis for not applying it. At a bare minimum, the change should not decrease the amount of automated test coverage. As a community, we are focusing on increasing the current coverage, as there are several areas that do not receive automated testing.
* Whether it contains documentation. All new functionality needs to be documented for users, even if it is very rough for someone to expand on later. While rough is acceptable, incomplete is not. As with automated testing, as a community we are striving to increase the current coverage of documentation.

**Above all, don't be discouraged. These are the same requirements the current developers should hold each other to as well. And remember, your contributions are always welcome!**
