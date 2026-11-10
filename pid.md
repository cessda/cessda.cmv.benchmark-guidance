---
title: How to pass Persistent Identifier Schema Validation (F1, pid)
parent: Home
has_children: false
is_hidden: false
nav_order: 010
---

# {{ page.title }}

The guidance how to pass Persistent Identifier Schema Validation (F1, pid) which checks if metadata are assigned persistent identifiers of type ARK, DOI, Handle or URN FAIR test.


## Why?

Persistent identifiers (PIDs) are essential because they provide a stable and unambiguous reference to data even when its location, ownership, or technical environment changes. Using an established PID system such as DOI, URN, Handle, or ARK ensures that identifiers follow recognized standards, are supported by sustainable infrastructures, and can be reliably resolved and understood across organizations and systems. This makes data easier to find, cite, link, reuse, and manage over the long term.

## What?

To pass this test there needs to be:
1.    Identifier element (IDNo) for the study in study description
1.    At least one instance of this IDNo element includes persistent identifier of type ARK, DOI, Handle or URN
1.    The type of the identifier (ARK, DOI, Handle or URN) is documented

## How?

Here you may find both the DDI Codebook 2.5 and 2.6 XML snippets and XPaths.

### XML Examples for DDI Codebook 2.5 and 2.6

When the PID is an URN:
```xml
<IDNo agency="URN">urn:nbn:fi:fsd:T-FSD4064</IDNo>
```

When the PID is a DOI:
```xml
<IDNo agency="DOI">10.60686/t-fsd4064</IDNo>
```

### XPaths for DDI Codebook 2.5 and 2.6

XPath of the IDNo element:
```xpath
/codeBook/stdyDscr/citation/titlStmt/IDNo
```

XPath of the agency attribute:
```xpath
/codeBook/stdyDscr/citation/titlStmt/IDNo/@agency
```

## More information

More information on the use of the DDI Codebook IDNo element and agency attribute is available in the DDI Specification: [DDI Codebook 2.5](https://docs.ddialliance.org/DDI-Codebook/2.5/xmlschema/schemas/codebook_xsd/elements/IDNo.html)
and [DDI Codebook 2.6](https://docs.ddialliance.org/DDI-Codebook/2.6/xmlschema/schemas/codebook_xsd/elements/IDNo.html)