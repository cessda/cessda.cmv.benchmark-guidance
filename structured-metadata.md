---
title: How to pass Structured Metadata Validation (F2, structured-metadata)
parent: CESSDA FAIR Benchmark Guidance
has_children: false
is_hidden: false
nav_order: 030
---

# {{ page.title }}

This guidance explains how to pass the Structured Metadata Validation (F2, structured-metadata) FAIR test, which checks whether
the metadata record includes suitable namespace declaration.

## Why

When metadata is based on a discipline-appropriate metadata standard such as DDI (Data Documentation Initiative) it ensures that
research data are described consistently, comprehensively, and in ways that meet the specific needs of the social sciences.
Using DDI improves the interoperability, discoverability, interpretation, and reuse of data across repositories, organizations,
and research infrastructures. DDI Codebook is represented in XML. Using an XML namespace within a DDI record is important
because it uniquely identifies element and attribute names, preventing naming conflicts.

## What

To pass this test there needs to be:

1. Namespace declaration (attribute xmlns) in the codeBook root element
1. The contents of the namespace declaration include either "ddi:codebook:2_5" for DDI Codebook 2.5
   or "ddi:codebook:2_6" for DDI Codebook 2.6


## How

The XML snippets below are provided separately for DDI Codebook 2.5 and 2.6. The XPath apply to both.

### XML example for DDI Codebook 2.5

```xml
<codeBook xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="ddi:codebook:2_5"  version="2.5"
xsi:schemaLocation="ddi:codebook:2_5 http://www.ddialliance.org/Specification/DDI-Codebook/2.5/XMLSchema/codebook.xsd" xml:lang="fi">
```

### XML example for DDI Codebook 2.6

```xml
<codeBook xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns="ddi:codebook:2_6"  version="2.6"
xsi:schemaLocation="ddi:codebook:2_6 http://www.ddialliance.org/Specification/DDI-Codebook/2.6/XMLSchema/codebook.xsd" xml:lang="fi">
```

### XPath for DDI Codebook 2.5 and 2.6

XPath of the xmlns attribute:

```xpath
/codeBook/@xmlns
```

## More information

More information on the use of XML namespaces and xmlns attribute is available in the W3C Recommendation:

- [Namespaces in XML 1.0 Third Edition](https://www.w3.org/TR/xml-names/)
