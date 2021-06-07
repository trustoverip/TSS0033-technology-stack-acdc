# Authentic Chained Data Containers

## Abstract

Authentic Chained Data Containers (ACDC) Standard Specification provides semantic of authentic provenance chaining of authentic data containers. This semantics include both source provenance and authorization provenance or delegation.

TODO: short motivation

## Scope

TODO

## Terminology

- `SAI` - Self-Addressing Identifier - any identifier which is deterministaclly generated out of the content, digest of the content


## Specification



### Overview

An ACDC may be built up from an authentic data container (ADC) that contains an authentic provenance chain (APC). The term authentic data container (ADC) is an important abstract concept that hopefully may leverage a pre-existing open concrete
implementation standard specification. The current targeted concrete implementation specification is the W3C Verifiable Credential (VC) standard. We believe that authentic data containers (ADCs) with authentic provenance chains (APCs) that together compose an authentic chained data container (ACDC) are essential components of verifiable or authentic data supply chains which in turn are essential to what may be called the authentic data economy

TODO: mention about informative example used across whole spec

### Security guaranties

### Privacy guaranties

### Normative model

### Informative Example


    {
       id: "did:1209u091u9012d/attestation/1234",  // SAI
       tid: "did:1209u091u9012d",
       s: 
       [
            id: "attestationID1234", tid: "did:jd892j108jd1029", // attestation id not in namespace of testator
            id: "did:9d9j109j1d902dj19/attestation/3242",  // attestation id in namespace of testator
            id: "did:h78h8d2h8d2h8hd28d/attestation/1234"  // attestation id in namespace of testator
        ],
        schema: {}, || SAI
        d: 
        {
           k: v
           k1: #ref1
         }, || SAI
         r: {}  || SAI
     }



- `id` - identifier, which can be designated by Testator to uniquely track specific attestation. ADID is always within namespace of the Testator Identifier making it always globally unique.
- `tid` (optional) - Testator Identifier. Required if the attestation datum id (`id`) is not within the namespace of the testator identifier. Testator is a person who attest to `Datum`. Testator ID is identifier of the Testator. Preferable DID but it can be any type of the identifier which provides possibility to sign digital content.
- `s` (optional) - sources to which attestation is linked to
- `dd` (optional) - Datum DRIs (Decentralized Resource Identifier). An array of objects identifiers which refers to Datum Decentralized Identifiers - unique identifier of immutable datum and schema DRI.
- `schema` (optional) - schema DRI, DRI of the schema describing semantic of the data
- `cd` (optional) - consent schema DRI, schema describing consent data linked to attestation
- `r` (optional) - datum of rules/delegation/consent/license/data agreement under which data are shared.

### Versioning


## References

- [1] https://github.com/SmithSamuelM/Papers/blob/master/whitepapers/ACDC.web.pdf
- [2] https://github.com/THCLab/keri-python-ffi/tree/supply_chain
- [3] https://hackmd.io/rnY5xiXESWqWBlyDPHDorA?view
- [4] https://github.com/THCLab/keri-python-ffi/tree/supply_chain

## Apendix




### Examples

TODO: provide more examples
#### Security considerations

#### Privacy consideration



### Benefits

TODO:
- focus on generic problem of authentic data
- do not relay on any specific network nor implementation

ACDC focus on the base semantic specification to address core properties of authentic data flows. ACDC provides semantic allowing to express:
- authenticity for any data flow
- self-describing mechanism to understand the context of data
- chaining mechanism (including delegation)
- increasing interoperability by not relaying on any specific use case and implementation


### Motivation/Problem statement

TODO:

- Arguments why existing solutions are not good enough.
- What is the problem


### Example of similar construct

TODO:

- VC Data Model
- ZCap-LD
- ...
