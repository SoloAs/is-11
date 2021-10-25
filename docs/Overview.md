# AMWA IS-11 NMOS Sink Metedata Proccessing Specification: Overview \[Work In Progress\]

{:.no_toc}

- A markdown unordered list which will be replaced with the ToC, excluding the "Contents header" from above
{:toc}

<!-- _(c) AMWA 2017, CC Attribution-NoDerivatives 4.0 International (CC BY-ND 4.0)_  -->

## Introduction

The purpose of AMWA IS-11 is to provide a mechanism by which to configure Sources, Flows and Senders using information from Receivers. Receiver provides Receiver Capabilities and exposes its Outputs each of which may have EDID. Sender has Media Profiles, which restrict media formats allowed for sending, and Inputs each of which may have an effective EDID to present to its upstream media producing unit.

The Specification includes:

- RAML and JSON Schema definitions, with supporting JSON examples
- This documentation set, which provides:
  - An overview of the API and how it is used.
  - Normative requirements in addition to those included in the RAML and JSON schemas specifying the API.
  - Additional details and recommendations for implementers of API providers and clients.
  - Information about compatibility between different API versions.

IS-11 is intended to be used in conjunction with an [IS-04 NMOS Discovery & Registration](https://specs.amwa.tv/is-04) and [IS-05 NMOS Device Connection Management](https://specs.amwa.tv/is-05) deployment; however it has been written in such a way to provide useful functionality even in the absence of such a system.

## Use of Normative Language

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "MAY",
and "OPTIONAL" in this documentation set are to be interpreted as described in [RFC 2119][RFC-2119].

## Definitions

The terms 'Node', 'Device', 'Sender' and 'Receiver' are used extensively in this documenation set. The [NMOS Technical Overview](https://specs.amwa.tv/nmos/main/docs/2.0._Technical_Overview.html) provides an outline of these terms, and IS-04 provides corresponding schema definitions.

### Input

An Input is a unit consuming media data for providing it to Sender(s). Input may present metadata about media consuming capabilities to its upstream counterpart. Input is a resource and based on [Resource Core JSON Schema][Resource-Core-Schema].

### Output

An Output is a unit producing media data provided by Receiver(s). Output may consume metadata about the media consuming capabilities from its downstream counterpart. Output is a resource and based on [Resource Core JSON Schema][Resource-Core-Schema].

### Media Profile

Description of a format that is acceptable for all Receivers implied to be a part of a connection. A Media Profile consists of separate media parameters required to configure Input(s) of a Sender, and, subsequently, a Flow and a Source of the Sender. Media Profiles follow the same EDID mapping as [BCP-005-1 EDID to Receiver Capabilities][BCP-005-1].

[RFC-2119]: https://tools.ietf.org/html/rfc2119 "Key words for use in RFCs"
[BCP-005-1]: https://specs.amwa.tv/bcp-005-01 "AMWA BCP-005-01 NMOS EDID to Receiver Capabilities Mapping"
[Resource-Core-Schema]: https://github.com/AMWA-TV/nmos-discovery-registration/blob/v1.3.x/APIs/schemas/resource_core.json "AMWA NMOS IS-04 v1.3.x Resource Core JSON schema"