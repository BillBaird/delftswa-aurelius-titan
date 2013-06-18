> **Note in advance**
> 
> *This document is part of the [Developer Guide](DeveloperGuide.md)*

# Titan Conventions

In order to make sure all development effort fit each other nicely some conventions are drawn up.

## Titan Code Style and Conventions

### Generic code style and convention

All working files (java, xml, others) should respect the following conventions:

* **License Header**: Always add the license header below in all versioned files.

```
Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
```

* **Trailing Whitespaces**: Remove all trailing whitespaces. If your are an Eclipse user, you could use the [Anyedit Eclipse Plugin](http://andrei.gmxhome.de/anyedit/).

and the following style:

* **Indentation**: Never use tabs!
* **Line wrapping**: Always use a 120-column line width.

### Java Code Style

The Titan style for Java is mainly:

* **White space**: One space after control statements and between arguments (i.e. if ( foo ) instead of if(foo)), myFunc( foo, bar, baz ) instead of myFunc(foo,bar,baz)). No spaces after methods names (i.e. void myMethod(), myMethod( "foo" ))
* **Indentation**: Always use 4 space indents and never use tabs!
* **Blocks**: Always enclose with a new line brace.
* **Line wrapping**: Always use a 120-column line width for Java code and Javadoc.
* **Readingness**: Specify code grouping members, if needed.

## Titan Git Convention

Commits should be focused on one issue at a time, because that makes it easier for others to review the commit. A commit message should use this template:

```
[<<Issue Number>>] <<Summary of implementation>>
Submitted by: <<Your name>>

o Comments
```
