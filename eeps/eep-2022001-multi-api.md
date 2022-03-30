# EEP 2022001: Multi API - Python and R

<!--
Authors Full Name 1 <full.name1 at organization.com>, Full Name2 <full.name2 at organization.com>
-->
**Authors**: Ivan

<!--
Status [Draft | Accepted | Final | Deferred | Rejected | Withdrawn | Superseded | Active]
-->
**Status**: Draft

<!--
Type: [Standards Track | Informational | Process]
-->
**Type**: Standards Track

**Created**: 2022-03-30

<!--
resolution: url to discussion (required for Accepted | Rejected | Withdrawn)
-->
**Resolution**


## Abstract

**EpiGraphHub** offers libraries for **Python** and **R**, but it is a big challenge
to keep both library synchronized. Additionally, computation power could be a
limitation for the user, and scale the computation to a server would improve
the user experience. This EEP proposes a new architecture where the API client call
will connect to the API server and execute the necessary library (Python or R).
This approach also avoid code replication (between Python or R), and it can be easily
replicated for any other language.

## Motivation

Currently, **EpiGraphHub** offers libraries for **Python** and **R**, two very important
language/communities that could potentially use EpiGraphHub. The initial, approach
aims to replicate the functions from one language to another. This cause a double work,
and maybe it would be hard to replicate some specific algorithms.

Another point about the current implementation is that the algorithms consumes a lot
of machine resources, and that means that it would be executed for minutes or hours.


## Proposal

This EEP proposes a new architecture in order to allow implementations in different languages
without any code replications and offer an API, initially for Python and R, but also
the possibility to have it for any other language.

This new architecture also will allow to process the algorithm locally or remotely,
inside a container (recommended) or on a python environment.

**Key points:**

* Architecture
* Implementation

### Architecture

Some example about this architecture can be checked out in
[this Proof of Concept](https://github.com/osl-incubator/poc-multi-api).

#### Key point 1.1

...

### Key point 2

...

### Examples

...

## Alternatives

<!-- Some alternative proposals-->
...

### Alternative 1

...

## Future works

<!-- Some alternative proposals for the future-->
...


## Copyright

This document has been placed in the public domain.

## References

<!--
links to the references used in the text
note: use markdown references
-->
<!-- example: -->
* [EEP][eep]

## Changelog

- 2022-03-30: Creation of this proposal

<!-- markdown references -->
<!-- example:-->

[eep]: https://thegraphnetwork.github.io/epigraphhub-enhancement-proposals
