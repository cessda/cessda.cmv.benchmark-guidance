---
title: How to pass Searchable Metadata Validation (F4, searchable)
parent: CESSDA FAIR Benchmark Guidance
has_children: false
is_hidden: false
nav_order: 050
---

# {{ page.title }}

This guidance explains how to pass the Searchable Metadata Validation (F4, searchable) FAIR test, which checks whether
the metadata record is available through an OAI-PMH endpoint. It also validates if the OAI-PMH envelope is correctly formed
and includes an identifier.

## Why

For metadata to be easily discovered and harvested, it needs to be available through an OAI-PMH endpoint in a correctly
formed OAI-PMH response. Each record should also include a header with a unique identifier, allowing harvesting services
to reliably identify, retrieve, and manage individual metadata records.

## What

To pass this test there needs to be:

1. The OAI-PMH endpoint where the metadata record is available
1. The OAI-PMH response (envelope) must be correctly formed
1. The OAI-PMH record element must have header with an identifier

## How

The XML snippets and XPaths below apply to all OAI-PMH records, regardless of DDI Codebook version.
DDI is embedded within the OAI-PMH envelope.

### XML example of an OAI-PMH record

```xml
<OAI-PMH xmlns="http://www.openarchives.org/OAI/2.0/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
xsi:schemaLocation="http://www.openarchives.org/OAI/2.0/ http://www.openarchives.org/OAI/2.0/OAI-PMH.xsd">
[...]
<record>
<header>
<identifier>c63266b0a9ba9924b5a8f9b2b98e1570e90bf14d1646e04cab23d147082a4a4c</identifier>
[...]
</header>
<metadata>
[...]
</metadata>
</record>
```

### XPaths for OAI-PMH

XPath of the identifier element:

```xpath
/OAI-PMH/record/header/identifier
```

## More information

More information on the use of the OAI-PMH is available in the OAI-PMH Specification and in the documentation of Kuha2 tool:

- [OAI-PMH Specification](https://www.openarchives.org/pmh/)
- [Kuha2](https://kuha2.readthedocs.io/en/latest/)
