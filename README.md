# Eclipse3-Workbench-Mock-Facade

Now what's this?
This bundle contains "mock" implementations of a number of "org.eclipse.ui*" packages. Yes, it's a stripped-down version of the Eclipse 3.x Workbench, 
that is by no means fully functionable. 
The background why this facade implementation was done is the following requirements:
* A pure E4 Application is the basic requirement
* Need EMF Diff/Merge to run in the E4 Application 
* Need bundle "org.eclipse.compare" (required by EMF Diff/Merge) to run in E4 Application 

To achieve this, I have two forked projects:

* https://github.com/Lulle74/emf.diffmerge.core   (containing a separation of Eclipse3.x Workbench dependent UI and "generic" UI)
* https://github.com/Lulle74/eclipse.platform.team  (the version of "org.eclipse.compare" here uses the "Imported Packages" approach to all things "org.eclipse.ui*"

Having done the work in those two forked projects, it made sense also (for me and my project) to create some kind of stripped-down but
still compiling "mock facade" of the org.eclipse.ui* packages used by the forked "org.eclipse.compare". So that's what this is!
