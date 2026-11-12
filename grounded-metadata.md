---
title: How to pass Grounded Metadata Validation (F2, grounded-metadata)
parent: CESSDA FAIR Benchmark Guidance
has_children: false
is_hidden: false
nav_order: 040
---

# {{ page.title }}

This guidance explains how to pass the Grounded Metadata Validation (F2, grounded-metadata) FAIR test, which checks whether
the metadata record includes working schema location web address and a link to the original metadata access point.

## Why

When metadata is based on a discipline-appropriate metadata standard such as DDI (Data Documentation Initiative) it ensures
that research data are described consistently, comprehensively, and in ways that meet the specific needs of the social sciences.
Using DDI improves the interoperability, discoverability, interpretation, and reuse of data across repositories, organizations,
and research infrastructures. DDI Codebook is represented in XML. An XML namespace schema location is important for XML record
because it indicates where the XML Schema (XSD) for a namespace can be found, enabling tools to validate the XML.

When a DDI XML record is harvested by external services, the metadata should include a link to the original metadata access
point to ensure that users can locate and access the associated data.

## What

To pass this test there needs to be:

1. Working namespace schema location (attribute xsi:schemalocation) web address for DDI version 2.5 or 2.6
   depending on the used namespace
1. Working web address pointing to (SPs) study description page


## How

The XML snippets below are provided separately for DDI Codebook 2.5 and 2.6. The XPath apply to both.

### XML examples for DDI Codebook 2.5

Namespace schema location:

```xml
<codeBook xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="ddi:codebook:2_5"  version="2.5" xsi:schemaLocation="ddi:codebook:2_5 http://www.ddialliance.org/Specification/DDI-Codebook/2.5/XMLSchema/codebook.xsd" xml:lang="fi">
```

Link to the original metadata access point (study description page):

```xml
<holdings xml:lang="en" URI="https://doi.org/10.17026/SS/ZSQC1E" ></holdings> 
```



### XML examples for DDI Codebook 2.6

Namespace schema location:

```xml
<codeBook xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="ddi:codebook:2_6"  version="2.6" xsi:schemaLocation="ddi:codebook:2_6 http://www.ddialliance.org/Specification/DDI-Codebook/2.6/XMLSchema/codebook.xsd" xml:lang="fi">
```

Link to the original metadata access point (study description page):

```xml
<holdings xml:lang="en" URI="http://doi.org/10.5255/UKDA-SN-9577-1" ></holdings> 
```

### XPaths for DDI Codebook 2.5 and 2.6

XPath of the xsi:schemalocation attribute:

```xpath
/codeBook/@xsi:schemaLocation
```

XPath of the holdings element:

```xpath
/codeBook/stdyDscr/citation/holdings
```

## More information

More information on the use of XML namespaces and xsi:schemalocation attribute is available in the W3C Recommendations:

- [Namespaces in XML 1.0 Third Edition](https://www.w3.org/TR/xml-names/)
- [XML Schema Part 1: Structures Second Edition](https://www.w3.org/TR/xmlschema-1/#xsi_schemaLocation)
