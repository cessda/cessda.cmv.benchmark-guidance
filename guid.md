---
title: How to pass Globally Unique Identifier Validation (F1, guid)
parent: CESSDA FAIR Benchmark Guidance
has_children: false
is_hidden: false
nav_order: 020
---

# {{ page.title }}

This guidance explains how to pass the Globally Unique Identifier Validation (F1, guid) FAIR test, which checks whether
metadata is accessible through a globally unique identifier. In this case GUID must be a working URL.

## Why

A globally unique identifier for metadata is essential because it allows each metadata record to be identified unambiguously
across repositories, systems, and organizations. It prevents confusion between similar records and enables reliable linking,
referencing, exchange, and automated processing of metadata. Global uniqueness therefore supports interoperability, traceability,
and the long-term management and reuse of metadata.

## What

To pass this test there needs to be:

1. Valid and working GUID (URL) of the metadata record

It would also be good to meet the following criterion to pass other CESSDA FAIR tests even if it is not mandatory for
passing this test:

1. Valid and working GUID (URL) of metadata record in an OAI-PMH endpoint

## How

The GUID (URL) examples below can be applied to both DDI Codebook 2.5 and 2.6. In the case of the DDI Codebook 2.6 the metadataprefix
in the OAI-PMH would be e.g. oai_ddi26.

FSD's OAI-PMH endpoint URL GUID for DDI-C 2.5 record:
<https://services.fsd.tuni.fi/v0/oai?verb=GetRecord&metadataPrefix=oai_ddi25&identifier=oai:fsd.uta.fi:FSD3591>

CESSDA's OAI-PMH endpoint URL GUID for DDI-C 2.5 record:
<https://datacatalogue.cessda.eu/oai-pmh/v0/oai?verb=GetRecord&metadataPrefix=oai_ddi25&identifier=0ef2cc1ccfe41baa40fd3e9affea540264fbdd1de3107c35c276cc90f5d72afa>

URL GUID for metadata record in CDC:
<https://datacatalogue.cessda.eu/detail/0f9126169134685b1e7a5e25a2fdee78e66d468e64dbc3375be55ce821939777?lang=en>

## More information

More information on the use of the OAI-PMH is available in the OAI-PMH Specification and in the documentation of Kuha2 tool:

- [OAI-PMH Specification](https://www.openarchives.org/pmh/)
- [Kuha2](https://kuha2.readthedocs.io/en/latest/)
