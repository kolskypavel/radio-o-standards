# ARDF XML Schema

ARDF (Radio Orienteering) reuses most structures from the
[IOF XML v3.0 Data Standard](https://orienteering.sport/iof/it/data-standard-3-0/).
The official IOF artifacts and examples are here:
- **IOF XML schema**: https://github.com/international-orienteering-federation/datastandard-v3/blob/master/IOF.xsd  
- **IOF examples**: https://github.com/international-orienteering-federation/datastandard-v3/tree/master/examples

This repository provides a minimal extension for ARDF use cases.

## Files & namespace

- **Schema (XSD)**:  
  `https://raw.githubusercontent.com/kolskypavel/radio-o-standards/main/ardf-xml/ardf_schema.xsd`

- **Namespace (targetNamespace / default xmlns in instances)**:  
  `http://robis.cz/datastandard/ardf/1.0`

> The IOF 3.0 schema is imported; you don’t need to modify the IOF namespace or files.

## How to reference the schema (instance XML) in each XML

**For example in results**
```xml
<ResultList
  xmlns="http://rob-is.cz/datastandard/ardf/1.0"
  xmlns:iof="http://www.orienteering.org/datastandard/3.0"
  xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
  iofVersion="3.0"
  createTime="2024-12-08T16:52:12Z" 
  creator="CREATOR NAME"
  xsi:schemaLocation="
    http://rob-is.cz/datastandard/ardf/1.0 https://raw.githubusercontent.com/kolskypavel/radio-o-standards/main/ardf-xml/ardf_schema.xsd
    http://www.orienteering.org/datastandard/3.0 https://raw.githubusercontent.com/international-orienteering-federation/datastandard-v3/master/IOF.xsd">
</ResultList>
```