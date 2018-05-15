# Release Notes OGC WMTS 1.0 Test Suite

## 1.2 (2018-05)

* [Issue #40](https://github.com/opengeospatial/ets-wmts10/issues/40) - CTL feedback should be more explicit about which particular test failed
* [Issue #42](https://github.com/opengeospatial/ets-wmts10/issues/42) - Test wmts:Server.KVP.GET.GetCapabilities.Response.SchemaReferenced does not detect valid schema reference
* [Issue #36](https://github.com/opengeospatial/ets-wmts10/issues/36) - Update CTL with better information about conformance classes

## 1.1 (2017-10)

* [Issue #38](https://github.com/opengeospatial/ets-wmts10/issues/38) - Test wmts:main fails because of invalid Content-Type

## 1.0 (2016-12)

* [Issue #33](https://github.com/opengeospatial/ets-wmts10/issues/33) - Prepare Tag 1.0 - Test got approved by OGC TC
* [Issue #34](https://github.com/opengeospatial/ets-wmts10/issues/34) - Remove not approved profiles for 1.0  


## 0.7 (2016-09-07)
Note: It requires TEAM Engine 4.8 or newer.

* Integrated Pull Request [PR #28](https://github.com/opengeospatial/ets-wmts10/pull/28) Commented the test which has the type 'MandatoryIfImplemented
* Fix [issue #24](https://github.com/opengeospatial/ets-wmts10/issues/24): Server.RESTful.HTTP.Mandatory  test does not work with self-declaring service
* Fix [issue #13](https://github.com/opengeospatial/ets-wmts10/issues/13): Unsupported image formats cause test failures (wmts:Server.KVP.GET.GetTile.Valid.Tile.Size)


## 0.6 (2015-07-30)

*   Integrated Pull Request [#23](https://github.com/opengeospatial/ets-wmts10/issues/23): rename duplicate function
*   Update pom.xml to build with Maven 2

## 0.5 (2015-03-25)

*   Starting this revision, the revision number will follow the conventions described in the [wiki](https://github.com/opengeospatial/cite/wiki/OGC-Compliance-Testing-Tools)
*   Fix [issue #16](https://github.com/opengeospatial/ets-wmts10/issues/16): Incorrect exceptionCode.
*   Fix [issue #15](https://github.com/opengeospatial/ets-wmts10/issues/15): Test wmts:Server.KVP.GET.GetFeatureInfo.Mandatory uses incorrect format in request.
*   Fix [issue #14](https://github.com/opengeospatial/ets-wmts10/issues/14): image/png8 tests failed in WMTS.
*   Fix [issue #10](https://github.com/opengeospatial/ets-wmts10/issues/10): text\html and text\plain not working in KVP valid infoformat test
*   Fix [issue #8](https://github.com/opengeospatial/ets-wmts10/issues/8): Misspelled exception code in Invalid InfoFormat test


## r4 (2014-11-03)


*   Fix [issue #6](https://github.com/opengeospatial/ets-wmts10/issues/6): Validating exception reports is very slow
*   Fix [issue #5](https://github.com/opengeospatial/ets-wmts10/issues/5): GetFeatureInfo response entity is expected to be an XML resource
*   Integrated Pull Request [#1](https://github.com/opengeospatial/ets-wmts10/pull/1): Modify test coverage such that that only capabilities from the ATS are tested. In particular, the following tests were removed:

    *   GetCapabilities.Response.No.Layers.OtherSource
    *   GetCapabilities.Response.Style.Identifiers.Unique
    *   GetCapabilities.Response.Dimension.Identifiers.Unique
    *   GetFeatureInfo.Invalid.SampleDimension.Name
    *   GetTile.Invalid.SampleDimension.Name
    *   GetFeatureInfo.Invalid.Tile.Row.No.TileMatrixSetLimits
    *   GetFeatureInfo.Invalid.Tile.Col.No.TileMatrixSetLimits
    *   GetFeatureInfo.Missing.Optional
    *   GetTile.Missing.Optional
    *   GetTile.Invalid.Tile.Row.No.TileMatrixSetLimits
    *   GetTile.Invalid.Tile.Col.No.TileMatrixSetLimitsAnd the following tests were simplified:
    *   GetTile (SOAP, REST bindings)
    *   GetTile.Mandatory (KVP, XML bindings)
    *   GetTile.Optional (KVP, XML bindings)
    *   GetTile.Valid.Tile.Format (XML binding)
    *   GetTile.Invalid.Tile.Format (XML binding)
    *   GetTile.Valid.Tile.Size (XML binding)
    *   GetFeatureInfo (KVP, XML, SOAP, REST bindings)   
*   Adopt Apache Maven as the build tool and modify the directory layout accordingly.
*   Add capabilities.url parameter to wmts:main test (display main input form only if this is not set).


## r3 (2013-10-28)


*   [CITE-858] Check Content-Type header in GetCapabilities response for XML media type.
*   [CITE-846] Configuration elements in the  (bootstrap) element written to the test logs have a boolean (text) value.
*   [CITE-830] In owsFunctions:KVP.GetCapabilities.Request.UpdateSequence: Modify the Unicode code point value of the first character in the updateSequence string.
*   Allow upload of capabilities document.


## r2 (2013-06-12)


*   [CITE-781] If TileRow or TileCol is out of range the expected exception code is "TileOutOfRange" (wmtsFunctions.xml).
*   [CITE-777] Allow for ows:Constraint to appear as child of ows:Operation in capabilities document (bootstrap.xml, owsFunctions.xml).
*   Ignore GetEncoding operation constraint as there are no alternatives to KVP (in bootstrap.xml).


## r1 (2013-02-09)

*   Updated config.xml for TEAM-Engine v4.
*   Set wmtsSchemaType = "resource" (classpath reference) instead of "file".
*   Fixed XPath errors reported by Saxon: Cannot compare xs:boolean to xs:string.
*   In wmtsFunctions:printSelected: starts-with() arguments must be string values.
*   Added local copies of WMTS 1.0.1 schemas.
*   Issue "skipped" verdict if profile not supported (otherwise displays empty test selection screen).

