---
title: How to pass Persistent Identifier Schema Validation (F1, pid)
parent: CESSDA FAIR Benchmark Guidance
has_children: false
is_hidden: false
nav_order: 010
---

# {{ page.title }}

This guidance explains how to pass the Persistent Identifier Schema Validation (F1, pid) FAIR test,
which checks whether metadata are assigned persistent identifiers of type ARK, DOI, Handle or URN.

## Why

Persistent identifiers (PIDs) are essential because they provide a stable and unambiguous reference to data
even when its location, ownership, or technical environment changes.
Using an established PID system such as DOI, URN, Handle, or ARK ensures that identifiers follow recognized standards,
are supported by sustainable infrastructures, and can be reliably resolved and understood across organizations and systems.
This makes data easier to find, cite, link, reuse, and manage over the long term.

## What

To pass this test there needs to be:

1. An identifier element (IDNo) for the study in the study description
1. At least one instance of this IDNo element that includes a persistent identifier of type ARK, DOI, Handle or URN
1. The type of the identifier (ARK, DOI, Handle or URN) documented in the `agency` attribute

## How

The XML snippets and XPaths below apply to both DDI Codebook 2.5 and 2.6.

### XML examples for DDI Codebook 2.5 and 2.6

When the PID is a URN:

```xml
<IDNo agency="URN">urn:nbn:fi:fsd:T-FSD4064</IDNo>
```

When the PID is a DOI:

```xml
<IDNo agency="DOI">10.60686/t-fsd4064</IDNo>
```

When the PID is a Handle:

```xml
<IDNo agency="Handle">20.500.12345/example-study-1</IDNo>
```

When the PID is an ARK:

```xml
<IDNo agency="ARK">ark:/12345/x6example</IDNo>
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

More information on the use of the DDI Codebook IDNo element and agency attribute is available in the DDI Specification:

- [DDI Codebook 2.5](https://docs.ddialliance.org/DDI-Codebook/2.5/xmlschema/schemas/codebook_xsd/elements/IDNo.html)
- [DDI Codebook 2.6](https://docs.ddialliance.org/DDI-Codebook/2.6/xmlschema/schemas/codebook_xsd/elements/IDNo.html)
