# Authentic Chained Data Containers

## Abstract

Authentic Chained Data Containers (ACDC) let formal assertions about data be chained together such that the derivation of any particular datum is traceable back to its source.

## Motivation

Digital signatures let us prove who said what. This is extremely valuable. However, it is often the case that a party who says something is just repeating data that they themselves received from someone else. This indirection may change the reliability of the data, as well as its effects in complex knowledge graphs. Many real-world use cases require us to model this indirection. For example:

* Supply chain, where a valid transfer of custody downstream depends on the validity of all upstream handoffs.
* Delegation, where a delegate's privileges derive from a chain of authorizations that must extend back to a valid root authority.
* Statistical inference and legal judgements, where multiple sources of data may assert contradictory facts, and the ability to weigh cumulative evidence is vital.
* Citation of sources (in art, in journalism, in academia, or in credential issuance), where an author wants to clarify that a particular assertion originates elsewhere. This allows the assertion to acquire (or lose) gravitas independent of the reputation of the author who repeats it, and it lets reusers of data be held accountable for compliance with data sharing constraints.

The last of these examples deserves special comment. There is a tension between the decentralization that we want in a verifiable data ecosystem, and the way that trust tends to centralize because knowledge and reputation are unevenly distributed. We want anyone to be able to attest to anything they like &mdash; but we know that verifiers care deeply about the reputation of the parties that make those attestations.

We could say that verifiers will choose which issuers they trust. This is exactly what most practitioners of verifiable credentials recommend, and it works fine in early pilots. However, as the complexity of a data ecosystem grows, it doesn't scale; verifiers simply can't afford to vet every potential issuer of credentials they might encounter. (Consider a timely example. Tens of thousands of labs are now issuing COVID test results. No verifier can possibly know them all.) One obvious remedy is to accept credentials only from a short list of issuers, which leads back to centralization. Another remedy is to create a trust registry, where vetted issuers can be looked up. This introduces centralization in a different way.

ACDC solves this problem. If employee credentials include a proof that the name of the employee derived from a government-issued passport, then a tiny startup and a global conglomerate with universal brand recognition can both issue employee credentials of equal gravitas  &mdash; and it will require no special setup by verifiers to trust them equally, because the origin of the trusted data, not its proximate source, is what matters.

## Scope

This document describes a mechanism whereby assertions about data can be provenanced in a provably authentic chain. Evaluating the integrity of the chain is in scope -- and because such chains leads to one or more root sources, the chain provides the raw material for making judgments about the data's utility or probable veracity. However, evaluating the data's utility or veracity is out of scope.

In other words, this standard concerns itself with proving that party C got its data in a valid way from party B, who in turn got it from party A. The degree to which the origin party, A, is trustworthy in their assertions about reality is not our concern.

## Terminology

- `SAID` - Self-Addressing Identifier - any identifier which is deterministaclly generated out of the content, digest of the content


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
       i: "did:1209u091u9012d/attestation/1234",  // SAID
       ti: "did:1209u091u9012d",
       s: 
       [
            id: "attestationID1234", tid: "did:jd892j108jd1029", // attestation id not in namespace of testator
            id: "did:9d9j109j1d902dj19/attestation/3242",  // attestation id in namespace of testator
            id: "did:h78h8d2h8d2h8hd28d/attestation/1234"  // attestation id in namespace of testator
        ],
        x: {}, || SAID
        d: 
        {
           k: v,
           k1: SAID,  // ref1
         }, || SAID
         r: {}  || SAID
     }



- `i` - identifier, which can be designated by Testator to uniquely track specific attestation. ADID is always within namespace of the Testator Identifier making it always globally unique.
- `ti` (optional) - Testator Identifier. Required if the attestation datum id (`i`) is not within the namespace of the testator identifier. Testator is a person who attest to `Datum`. Testator ID is identifier of the Testator. Preferable DID but it can be any type of the identifier which provides possibility to sign digital content.
- `s` (optional) - sources to which attestation is linked to
- `x` (optional) - schema DRI, DRI of the schema describing semantic of the data
- `cd` (optional) - consent schema DRI, schema describing consent data linked to attestation
- `r` (optional) - datum of rules/delegation/consent/license/data agreement under which data are shared.

### ACDC as Verifiable Labeled Property Graph Fragment
The structure of an ACDC may be modeled as a fragment of a Labeled Property Graph. The `s` block is an array of edges and the `d` block is the node. The remainder of the ACDC may be metadata about the node that may also be included as special node properties. Because, the edges in labeled property graphs may also have labeled properties, a more aligned representation would make each source entry a labeled block (or at least as an option). This is illustrated in the following example:

```

    {
       i: "did:1209u091u9012d/attestation/1234",  // SAID
       ti: "did:1209u091u9012d",
       s: 
       [
            {sourcEdgeLabel: {id: "did:kdjflkeje", tid: "did:jd892j108jd1029", ...}}, // attestation id not in namespace of testator
            {anotherSourceEdgeLabel: {id: "did:9d9j109j1d902dj19/attestation/3242", ...}},  // attestation id in namespace of testator
            {yetAnotherSourceEdgeLabel: {id: "did:h78h8d2h8d2h8hd28d/attestation/1234",...}}  // attestation id in namespace of testator
        ],
        x: {}, || SAID
        d: 
        {
           k: v,
           k1: SAID,  // ref1
         }, || SAID
         r: {}  || SAID
     }


```

Because each ACDC thus composed is verifiable, a verifiable graph may be communicated via verifiable graph fragments. Given any starting node or root node in the graph, one may add onto the graph by communicating graph fragments where each fragment includes a new node and the edge or edges that connect it to one or more pre-existing nodes.  The over-the-wire communication of the fragment is secured by the immutability of the ACDC contents (SAIDs) and the signature or committment proofs on the fragment.  This drives the structure of any given ACDC to be a graph fragment not a graph in and of itself.  The semantics of who issues or testates to a fragment and who the fragment is issued to (if any) may vary. With an issuer and isuee then the fragment may be an authorization or delegation. If the isuee is the node itself then the fragment is just provenanced data in a provenanced graph.

### Versioning


## References

- [1] https://github.com/SmithSamuelM/Papers/blob/master/whitepapers/ACDC.web.pdf
- [2] https://github.com/THCLab/keri-python-ffi/tree/supply_chain
- [3] https://hackmd.io/rnY5xiXESWqWBlyDPHDorA?view
- [4] https://github.com/THCLab/keri-python-ffi/tree/supply_chain
- [5] https://github.com/SmithSamuelM/Papers/blob/master/whitepapers/VC_Enhancement_Strategy.md

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
