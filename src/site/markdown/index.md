# Overview

This test suite is based on the OGC WMTS 1.0 Abstract Test Suite ([ATS](ats.html)) and the following specifications:

*   [OpenGIS Web Services Common Specification, Version 1.3 with Corrigendum 1](http://portal.opengeospatial.org/files/?artifact_id=20040) (OGC 06-121r3)
*   [OpenGIS Web Map Tile Service Implementation Standard, Version 1.0.0](http://portal.opengeospatial.org/files/?artifact_id=35326) (OGC 07-057r7)
*   [HTTP 1.1](http://www.ietf.org/rfc/rfc2616) (RFC 2616)
*   [W3C SOAP Version 1.2 Part 1: Messaging Framework, W3C Recommendation 24 June 2003](http://www.w3.org/TR/2003/REC-soap12-part1-20030624/)
*   [W3C SOAP 1.2 Attachment Feature, W3C Working Group Note 8 June 2004](http://www.w3.org/TR/soap12-af/)
*   [W3C Web Services Description Language (WSDL) 1.1, W3C Note 15 March 2001](http://www.w3.org/TR/wsdl)


## What is tested

WMTS Server capabilities are tested. The server under test must support the GetCapabilities operation request in either the _KVP GET_ or _RESTful_ protocol binding, so that the capabilities response XML document may be analyzed during a bootstrap process to determine which protocol bindings are supported and which test prerequisites are met by the server.

The test suite allows selection of tests for any or all of the following protocol binding profiles:

*   _KVP GET_
*   _KVP POST_
*   _XML POST_
*   _SOAP POST_
*   _RESTful_

**Currently, only the KVP GET is required for certification**

Each of these protocol binding profiles includes test groups for the following conformance classes:

*   Common Operations (_Mandatory_)
*   GetCapabilities (_Mandatory_)
*   GetTile (_Mandatory_)

Each of these profiles allows selection of all tests for conformance certification.

To facilitate rapid debugging and correction of software that fails particular tests, each of these profiles also

*   allows selection of conformance class test groups and individual tests
*   allows "Redo using cached values" to reuse the bootstrap capabilities document, and optionally the test selections.

All tests in one or more protocol binding profiles must be selected for conformance certification.

All tests in _Mandatory_ conformance class test groups must be passed for conformance certification. 

<!---

 Tests in _Mandatory If Implemented_ conformance class test groups are skipped if the capabilities they test are not implemented by the server under test. All tests in _Mandatory If Implemented_ conformance class test groups for capabilities that are implemented by the server under test must be passed for conformance class certification.

-->

# What is not tested

* WMTS Client capabilities are not tested
* **Mandatory If Implemented** group of tests


## Test data

Test data consists of one image, [noDataSquare.png](./images/nodataSquare.png). The configuration of the server under test must be modified as described in the release notes so that so that noDataSquare.png is returned in response to a GetTile request for layer TransparentNodata style Default_style format image/png tileMatrixSet TransparentNodata tileMatrix 0 row 0 col 0.

# Release Notes
Release notes are available [here](relnotes.html).
