---
flip: 1
title: FLIP Purpose and Guidelines
status: Living
type: Meta
author: John Plevyak <jplevyak@factland.org>, et al.
created: 2022-03-08
---

## What is an FLIP?

FLIP stands for FactLand Improvement Proposal. A FLIP is a document providing information to the FactLand community, or describing a process or feature of Factland or in relattion to its environment. The FLIP should provide a concise description, (design if applicable) and rationale. The FLIP author is responsible for building consensus within the community and documenting dissenting opinions.

## FLIP Rationale

We intend FLIPs to be the primary mechanisms for proposing changes, for collecting community input, and for documenting the decisions that go into FactLand. Because the FLIPs are maintained as text files in a versioned repository, they are the historical record of FactLand policy.

## FLIP Types

There are four types of FLIP:

- An **Informational FLIP** describes a FactLand issue, or provides general guidelines or information to the FactLand community, but does not propose a new process. Informational FLIPs do not necessarily represent FactLand community consensus or a recommendation, so users and implementers are free to ignore Informational FLIPs.

- A **Standard FLIP** describes any change that affects FactLand features and processes.

- A **Governance FLIP** describes any change that affects Factland governance.

- A **Meta FLIP** describes a process surrounding FactLand or proposes a change to such a process. Meta FLIPs are like Standard FLIPs but apply to areas other than FactLand proper. They may propose an implementation, but outside of the FactLand codebase; they often require community consensus; unlike Informational FLIPs, they are more than recommendations, and users are typically not free to ignore them.

It is highly recommended that a single FLIP contain a single key proposal or new idea.

A FLIP must meet certain minimum criteria. It must be a clear and complete description of the proposed change. The change must represent a net improvement. The proposed implementation, if applicable, must be solid and must not overly complicated.

## FLIP Work Flow

### Shepherding an FLIP

Parties involved in the process are the *FLIP author*, the [*FLIP editors*](#flip-editors), and [*FlatLand Governance*](#flatland-governance).

Before you begin writing a formal FLIP, you should discuss your idea on [Discussions](https://github.com/Factland/FLIPs/discussions).

Once the idea has been vetted, your next responsibility will be to present a FLIP to the reviewers and all interested parties to give feedback.

### FLIP Process 

The following is the standardization process for all FLIPs in all tracks:

**Idea** - This is the state where the idea is presented on [Discussions](https://github.com/Factland/FLIPs/discussions) before it is a FLIP.

**Draft** - The first formally tracked stage of a FLIP in development. A FLIP is merged by a FLIP Editor into the repository when it has been discussed and properly formatted.

**Review** - A FLIP Author marks a FLIP as ready for and requesting Review.

**Last Call** - This is the final review window for a FLIP before moving to `Final`. A FLIP editor will assign `Last Call` status and set a review end date (`last-call-deadline`), typically 14 days later.

If this period results in necessary normative changes it will revert the FLIP to `Review`.

**Final** - This FLIP represents the final standard. A Final FLIP exists in a state of finality and should only be updated to correct errata and add non-normative clarifications.

**Stagnant** - Any FLIP in `Draft` or `Review` or `Last Call` if inactive for a period of 6 months or greater is moved to `Stagnant`. An FLIP may be resurrected from this state by Authors or FLIP Editors through moving it back to `Draft` or it's earlier status. If not resurrected, a proposal may stay forever in this status. 

**Withdrawn** - The FLIP Author(s) have withdrawn the proposed FLIP. This state has finality and can no longer be resurrected using this FLIP number. If the idea is pursued at later date it is considered a new proposal.

**Living** - A special status for FLIPs that are designed to be continually updated and not reach a state of finality. This includes most notably FLIP-1.

## Parts of a FLIP

Each FLIP should have the following parts:

- Preamble - RFC 822 style headers containing metadata about the FLIP, including the FLIP number, a short descriptive title, a short description, and the author details. The title and description should not a FLIP number.
- Abstract - Abstract is a short paragraph summary.
- Motivation - A motivation section should clearly explain why the current situation inadequate and must be addressed.
- Specification - The technical specification should describe the specifics of the change. The specification should be detailed enough to allow the feature or policy to be implemented without ambiguity.
- Rationale - The rationale motivates the specific proposed solution as opposed to the Motivation which motivates solving the problem.
- Compatibility - This section describes any incompatibilities with previous behavior and how they are handled
- Testint - An optional section containing (some representitive) tests. Tests should either be inlined in the FLIP or included in `../assets/flip-###/<filename>`.
- Reference Implementation - An optional section that contains an example implementation.
- Copyright Waiver - Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).

## FLIP Formats and Templates

FLIPs should be written in [markdown](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet) format. There is a [template](https://github.com/factland/FLIPs/blob/master/flip-template.md) to follow.

## FLIP Header Preamble

Each FLIP must begin with an [RFC 822](https://www.ietf.org/rfc/rfc822.txt) style header preamble, preceded and followed by three hyphens (`---`). This header is also termed ["front matter" by Jekyll](https://jekyllrb.com/docs/front-matter/). The headers must appear in the following order.

`flip`: *FLIP number* (this is determined by the FLIP editor)

`title`: *The FLIP title is a few words*

`description`: *Description is one sentence*

`author`: *The list of the author's or authors' name(s) and/or username(s), or name(s) and email(s). Details are below.*

`discussions-to`: *The url pointing to the official discussion thread*

`status`: *Draft, Review, Last Call, Final, Stagnant, Withdrawn, Living*

`last-call-deadline`: *The date last call period ends on* (Optional field, only needed when status is `Last Call`)

`type`: *One of `Informational`, `Standard`, `Governance`, or `Meta`*

`created`: *Date the FLIP was created on*

`requires`: *FLIP number(s)* (Optional field)

`withdrawal-reason`: *A sentence explaining why the FLIP was withdrawn.* (Optional field, only needed when status is `Withdrawn`)

Headers that permit lists must separate elements with commas.

Headers requiring dates will always do so in the format of ISO 8601 (yyyy-mm-dd).

#### `author` header

The `author` header lists the names, email addresses or usernames of the authors/owners of the FLIP. Those who prefer anonymity may use a username only, or a first name and a username. The format of the `author` header value must be:

> Random J. User &lt;address@dom.ain&gt;

or

> Random J. User (@username)

if the email address or GitHub username is included, and

> Random J. User

if the email address is not given.

It is not possible to use both an email and a GitHub username at the same time. If important to include both, one could include their name twice, once with the GitHub username, and once with the email.

At least one author must use a GitHub username, in order to get notified on change requests and have the capability to approve or reject them.

#### `discussions-to` header

While an FLIP is a draft, a `discussions-to` header will indicate the URL where the FLIP is being discussed.

#### `type` header

The `type` header specifies the type of FLIP: Informational, Standards, Governance or Meta.

#### `created` header

The `created` header records the date that the FLIP was assigned a number. Both headers should be in yyyy-mm-dd format, e.g. 2001-08-14.

#### `requires` header

FLIPs may have a `requires` header, indicating the FLIP numbers that this FLIP depends on.

## Linking to External Resources

Links to external resources **SHOULD NOT** be included. External resources may disappear, move, or change unexpectedly.

## Linking to other FLIPs

References to other FLIPs should follow the format `FLIP-N` where `N` is the FLIP number you are referring to.  Each FLIP that is referenced in an FLIP **MUST** be accompanied by a relative markdown link the first time it is referenced, and **MAY** be accompanied by a link on subsequent references.  The link **MUST** always be done via relative paths so that the links work in this GitHub repository, forks of this repository, the main FLIPs site, mirrors of the main FLIP site, etc.  For example, you would link to this FLIP with `[FLIP-1](./flip-1.md)`.

## Auxiliary Files

Images, diagrams and auxiliary files should be included in a subdirectory of the `assets` folder for that FLIP as follows: `assets/flip-N` (where **N** is to be replaced with the FLIP number). When linking to an image in the FLIP, use relative links such as `../assets/flip-1/image.png`.

## FLIP Editors

The current FLIP editors are

- Keith Axline(@kaxline)
- Pam Statz (@pamstatz)
- Evan Hansen (@evnhsn)
- John Plevyak (@jplevyak)

## FLIP Editor Responsibilities

For each new FLIP that comes in, an editor does the following:

- Read the FLIP to check if it is ready: sound and complete. The ideas must make technical sense, even if they don't seem likely to get to final status.
- The title should accurately describe the content.
- Check the FLIP for language (spelling, grammar, sentence structure, etc.), markup (GitHub flavored Markdown), code style

If the FLIP isn't ready, the editor will send it back to the author for revision, with specific instructions.

Once the FLIP is ready for the repository, the FLIP editor will:

- Assign an FLIP number (generally the PR number, but the decision is with the editors)
- Merge the corresponding [pull request](https://github.com/ethereum/FLIPs/pulls)
- Send a message back to the FLIP author with the next step.

Many FLIPs are written and maintained by developers with write access to the Ethereum codebase. The FLIP editors monitor FLIP changes, and correct any structure, grammar, spelling, or markup mistakes we see.

The editors don't pass judgment on FLIPs. We merely do the administrative & editorial part.

## Style Guide

### FLIP numbers

When referring to an FLIP by number, it should be written in the hyphenated form `FLIP-X` where `X` is the FLIP's assigned number.

### RFC 2119

FLIPs are encouraged to follow [RFC 2119](https://www.ietf.org/rfc/rfc2119.txt) for terminology and to insert the following at the beginning of the Specification section:

> The key words “MUST”, “MUST NOT”, “REQUIRED”, “SHALL”, “SHALL NOT”, “SHOULD”, “SHOULD NOT”, “RECOMMENDED”, “MAY”, and “OPTIONAL” in this document are to be interpreted as described in RFC 2119.

## History

This document was derived heavily from [Etherum's EIP-01](https://github.com/ethereum/EIPs) which was derived from [Bitcoin's BIP-0001](https://github.com/bitcoin/bips) written by Amir Taaki which in turn was derived from [Python's PEP-0001](https://www.python.org/dev/peps/). Please direct all comments to the FLIP editors.

## Copyright

Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
