# WMTS 1.0 Conformance Test Suite

## Summary

This Executable Test Suite (ETS) checks WMTS implementations for conformance 
against the following specification(s):

* _OpenGIS Web Map Tile Service Implementation Standard_, Version 1.0.0 
  [OGC 07-057r7](http://portal.opengeospatial.org/files/?artifact_id=35326)

  
## License

[Apache 2.0 License](LICENSE.md)


## How to build

[Apache Maven](http://maven.apache.org/) or higher is required to build 
the test suite. Simply run 'mvn package' in the root project directory to 
generate all build artifacts; execute the 'mvn site' phase to generate project 
documentation. The main distribution archive (ets-wmts10-${version}.zip) is 
created in the usual output directory (/target).


## How to run
The official OGC test harness, [TEAM Engine](https://github.com/opengeospatial/teamengine), 
is required to run the test suite. Unpack the archive in the TE_BASE/scripts 
directory. In order to run the suite using the web interface, update the 
appropriate entry in the TE_BASE/config.xml file by copying the <standard> 
element from the config.xml file in the distribution archive.


## Mailing Lists

The [CITE forum](http://cite.opengeospatial.org/forum) is where software developers 
and testers discuss issues and solutions related to OGC test suites.


## More Information

Visit the [CITE website](http://cite.opengeospatial.org/) to for more information 
about OGC compliance program.
