# Architectural Recommendations ![Titan logo](diagrams/titan-kneeling-small.png)

The following recommendations came to mind while writing the various parts of the documentation.

## On the basis of the [Developer Guide](devguide/DeveloperGuide.md)

* Try to really work with contributors to get their code up to the right standard instead of the Titan team rewriting it manually and saying it is implemented, this doesn't really credit the contributors and doesn't give them much incentive to contribute again. 
* Also adhere to the [acceptance criteria](devguide/DevelopingTitan.md#acceptance-criteria) and [conventions](devguide/Conventions.md) yourself to set a good example for contributors and to have credibility.
* Add license information above every file, see the [Apache Software Foundation's website](http://www.apache.org/dev/apply-license.html#license-include) for the explanation why this improves your legal basis.
* Remove the part about the Titan snapshots from the current documentation about [building titan](https://github.com/thinkaurelius/titan/wiki/Building-Titan#depending-on-titan-snapshots). We found out it is [not used anymore](https://groups.google.com/forum/#!msg/aureliusgraphs/k4CVITBtmYc/-6V1c3mTQGsJ), because Titan is now synced to Maven central. This can lead to unnecesarry confusion.

## On the basis of the [Development Viewpoint](Development.md)

* In-memory backend and basic indexing modules are by default part of the core while you would expect this to be a different module in order not to pollute your code unnecessarily.
* Some circular dependencies are discovered between the packages, which reduces or makes it impossible to separate or re-use single module and makes it prone to errors like infinite recursions, memory leaks or other unexpected failures.
* Make guidelines for logging. Several inconsistencies were found throughout the code on where logging is used and where not. Besides the debug and trace levels are not always preceded by an `if()` statement. We recommend to do this in order not to waste resources on writing things to the log that are not displayed.
