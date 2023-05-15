This repository is obsolete. 
Current work is happening [here](https://github.com/trustoverip/tswg-acdc-specification)



# ToIP TSS0033: Technology Stack Authentic Chained Data Container (ACDC) Specification
- Authors: [Sam Smith](you@github-email) -- email is optional
- Deliverable Type: *Spec - Technical* 
- Status: [PROPOSED](./process/lifecycle_management.md)
- Since: 2021-02-15
- Status Note: (explanation of current status)  
- Supersedes: (link to anything this ToIP Deliverable  supersedes)
- Start Date: 2020-12-07
- Tags: #spec, #tswg, #acdc

## Summary

The purpose of the Authentic Chained Data Container (ACDC) Task Force  is to draft a TSS (ToIP Standard Specification) that defines the standard requirements for the semantics of Authentic Provenance Chaining of Authentic Data Containers. This semantics include both source provenance and authorization provenance or delegation.  The hypothesis is that the W3C Verifiable Credential standard may be expanded to serve as an Authentic Data Container (ADC) and that the semantics of a VC may be expanded to support an authentic provenance chains (APC) as a super semantic. This may be further expanded to support both a source provenance sub-semantic and a delegated authorization sub-semantic.

## Motivation

```Why are we doing this? What use cases does it support? What is the expected outcome?
Todo
```

## Scope

```
Briefly describe the scope of this document – how it presents the architecture of this particular enabler.  Include an explanation of how this architecture relates to Organization Name activity.  If it adds clarity, also describe what is not in the scope of this architecture.  DELETE THIS COMMENT
```

## References

```diff
Todo
```

### Normative References

```
The policy for reference lists is:
1.	'ORG_NAME' documents listed should have at least one approved version – draft-only docs should not be referenced.  
Exception exists for documents that will be approved with or after the referenced doc is approved (may be
part of same enabler package).  In short – approved docs should not reference unapproved docs.
2.	When a reference is made to an 'ORG_NAME' specification, then Organization Name with the TM symbol (™) should
be used in the description.
3.	The name + version (no date) for 'ORG_NAME' specifications are generally sufficient – dates should be used only
if there is a specific reason to limit the usage.
4.	For references to WAP Forum docs, dates should not be included as DID's for the old WAP Forum specifications
are enough and the reference description should refer to WAP Forum™.
5.	References to other affiliate docs should similarly provide sufficient information to uniquely determine the
needed document and should provide the appropriate source information.
6.	The URL for 'ORG_NAME' material (new 'ORG_NAME' and affiliate) should always be http://www.org_name.org (an exception is Registry that is reached through http://www.org_name.org/tech/)

Models to use
	[REFLABEL]	<General Model> "Ref Title", Ref information (source, date, id), URL:http//<ref-source>/
	['ORG_NAME'DOC]	<'ORG_NAME' Model> "'ORG_NAME' Document Title",{ Version x.y,} Organization Name™, 'ORG_NAME' <docname>{ <version>},
                URL:http//www.org_name.org/

If there are no entries in the table – enter ‘none’ to be clear.

ToDo
```
<table>
  <caption>Normative References </caption>
  <tbody>
    <tr>
      <td><strong>[RFC2119]</strong></td>
      <td>"Key words for use in RFCs to Indicate Requirement Levels", S. Bradner, March 1997, URL:http://www.ietf.org/rfc/rfc2119.txt</td>
    </tr>
    <tr>
      <td><strong>[RFC4234]</strong></td>
      <td>"Augmented BNF for Syntax Specifications: ABNF", D. Crocker, Ed., P. Overell, October 2005, URL:http://www.ietf.org/rfc/rfc4234.txt</td>
    </tr>
    <tr>
      <td><strong>[SCRRULES]</strong></td>
      <td>"SCR Rules and Procedures", Organization Name™, 'ORG_NAME'-ORG-SCR_Rules_and_Procedures, URL:http://www.org_name.org/</td>
   </tr>
  </tbody>
</table>

```
Add/Remove reference rows as needed - DELETE This Row
```

### Informative References

```
Check the version of the Dictionary you are using and update the reference below.  Delete the ['ORG_NAME'DICT] entry if
the dictionary is not used.  In general, use the latest available version unless seeking alignment with an
existing set of specifications.

ToDo
```
<table>
  <caption>Informative References </caption>
  <tbody>
    <tr>
      <td><strong>['ORG_NAME'DICT]</strong></td>
      <td>"Dictionary for 'ORG_NAME' Specifications", Version x.y, Organization Name™, 'ORG_NAME'-ORG-Dictionary-Vx_y, URL:http://www.org_name.org/</td>
    </tr>
  </tbody>
</table>

```
Add/Remove references as needed - DELETE This Row
```

## Terminology and Conventions
```diff
ToDo
```

### Conventions

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC2119].

All sections and appendixes, except "Scope" and "Introduction", are normative, unless they are explicitly indicated to be informative.

```
If needed, describe or declare using appropriate normative references the additional conventions that are used.  DELETE THIS COMMENT
```

### Definitions

```
Add definitions in new rows of the following table as needed.  The following examples show how dictionary references should be made
as well as locally defined terms.  This table should be maintained in sorted alphabetic order based on the labels of the terms.

Examples:
	Entity              Use definition #1 from ['ORG_NAME'DICT]
	Interactive Service Use definition from ['ORG_NAME'DICT]
	Local Term          The definition description would be presented directly

DELETE THIS COMMENT
```
<table>
  <caption>Definitions</caption>
  <tbody>
    <tr>
	<td><strong>LWM2M Bootstrap Server Account</strong></td>
	<td>LWM2M Security Object Instance with Bootstrap Server Resource true</td>
    </tr>
    <tr>
	<td><strong>LWM2M Server Account</strong></td>
	<td>LWM2M Security Object Instance with Bootstrap Server Resource false and associated LWM2M Server Object Instance</td>
    </tr>
  </tbody>
</table>

```
Add/Remove definition rows as needed - DELETE This Row
```

Kindly consult ['ORG_NAME'DICT] for more definitions used in this document.

### Abbreviations

```
Add abbreviations as needed.  No special notation should be made regarding terms copied from the Dictionary.  
The list should be maintained in alphabetic order. DELETE This Row
```

<table>
<caption>Definitions</caption>
<tbody>
  <tr>
    <td>'ORG_NAME'</td>
    <td>Organization Name</td>
  </tr>
</tbody>
</table>

## Introduction

```
From a market perspective...  
* What can you do with this specification?
* What problem does this solve?
* How can this specification be applied?
* Consider the target audience and provide deployment examples as possible.
ToDo
```

### Version 1.0

```
This section provides a high level, concise and informative description of the main functionality supported in the initial version of the specification.  The description should be brief, target length should be a few paragraphs.
When the enabler or reference release is finished, this description should be aligned with the final functionality.

ToDo
```

### Version (x.y)

```
This section should be included for each new major or minor version of the specification.

It should provide a high level, concise and informative description of the new or modified functionality introduced in this version of the specification, compared to the previous version.  The description should be brief, target length should be a few paragraphs.  When the enabler or reference release is finished, this description should be aligned with the final functionality differences.

ToDo
```

#### Version (x.y.z)

```
This section should be included for each new service release of the specification.   It should describe at a high level the main changes made to the specification compared to the previous version.  The description should be brief, target length should be one paragraph.

ToDo
```

## Sections As Needed

```
Sections for the normative specification text.  Fill in as needed.  The following validates the styles used for the headers.  DELETE THIS COMMENT
```

### Example Level 2
(Add text here.)

#### Example Level 3
(Add text here.)

##### Example Level 4
(Add text here.)

```diff
- Gating Criteria requirement
- URL to be defined.
```
<figure>
	<img src="images/fig1_example.svg" alt="Example Figure">
	<figcaption>Example Figure</figcaption>
</figure>


<table>
  <caption>Example Table</caption>
  <thead>
      <tr>
	  <th>Item</th>
	  <th>Function</th>
	  <th>Reference</th>
      </tr>	      
  </thead>	    
  <tbody>
    <tr>
	<td>Row 1</td>
	<td>Grid 1,1 data</td>
	<td>Grid 1,2 data</td>	    
    </tr>
    <tr>
	<td>Row 2</td>
	<td>Grid 2,1 data</td>
	<td>Grid 2,2 data</td>	    
    </tr>
  </tbody>
</table>

```diff
- Gating Criteria
- URL to be defined
```

## Appendix Change History (Informative)

### Approved Version x.y History

<table>
    <caption>Approved Version x.y History</caption>
    <thead>
        <tr>
            <th>Reference</th>
            <th>Date</th>
            <th>Description</th>
        </tr>
    </thead>
    <tbody>    
        <tr>
            <td>n/a</td>
            <td>n/a</td>
            <td>No prior version</td>
        </tr>
    </tbody>
</table>



## Appendix Static Conformance Requirements (Informative)

The notation used in this appendix is specified in [SCRRULES].```Add link```

```
The following is an optional model of a set of SCR tables.  DELETE THIS COMMENT
```

### SCR for XYZ Client
<table>
    <caption>Bootstrap Interface</caption>
    <thead>
        <tr>
            <th>Item</th>
            <th>Function</th>
            <th>Reference</th>
            <th>Requirement</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>XYZ-C-001-M</td>
            <td>Something mandatory</td>
            <td>Section x.y</td>
            <td>(XYZ-C-004-O OR XYZ-C-003-M) AND XYZ-C-002-O</td>
        </tr>
        <tr>
            <td>XYZ-C-002-O</td>
            <td>Something optional</td>
            <td>Section x.y</td>
            <td></td>
        </tr>
        <tr>
            <td>XYZ-C-003-M</td>
            <td>Dependencies on ZYX</td>
            <td>Section x.y</td>
            <td>ZYX:MCF</td>
        </tr>
        <tr>
            <td>XYZ-C-004-O</td>
            <td>Dependencies on ZYX</td>
            <td>Section x.y</td>
            <td>ZYX:OCF</td>
        </tr>
    </tbody>
</table>

### SCR for XYZ Server
<table>
    <caption>Bootstrap Interface</caption>
    <thead>
        <tr>
            <th>Item</th>
            <th>Function</th>
            <th>Reference</th>
            <th>Requirement</th>
        </tr>
    </thead>
    <tbody>
        <tr>
            <td>XYZ-S-001-M</td>
            <td>Something mandatory</td>
            <td>Section x.y</td>
            <td>XYZ-S-004-O OR XYZ-S-002-O OR XYZ-S-003-M</td>
        </tr>
        <tr>
            <td>XYZ-S-002-O</td>
            <td>Something optional</td>
            <td>Section x.y</td>
            <td></td>
        </tr>
        <tr>
            <td>XYZ-S-003-M</td>
            <td>Dependencies on ZYX</td>
            <td>Section x.y</td>
            <td>ZYX:MCF</td>
        </tr>
        <tr>
            <td>XYZ-S-004-O</td>
            <td>Dependencies on ZYX</td>
            <td>Section x.y</td>
            <td>ZYX:OCF</td>
        </tr>
    </tbody>
</table>
