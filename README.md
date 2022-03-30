# **EEP** 1 - **EpiGraphHub** Enhancement Proposal Template

* **Author** Ivan Ogasawara <ivan.ogasawara at gmail.com>
* **Status**: Accepted
* **Type**: Informational
* **Created**: 2021-01-27
* **Resolution**: None

## Abstract

**EEP** stands for "**EpiGraphHub** Enhancement Proposal". **EEPs** represent a formal
process whereby important changes are proposed and discussed in the **EpiGraphHub**
community.

## What is an EEP?

**EEP** are a formal process whereby important changes are proposed and
discussed. Corresponding to each **EEP** there is a document that outlines the
proposed change(s), the discussion around those changes, and motivation for
that change. This document outlines the details of the **EEP** process and
corresponding documents.

**EEP** are heavely based on [SymPEPs](https://github.com/sympy/SymPEPs), the SymPy Enhancement Proposal process. Also, it is inspired by
[PEP](https://www.python.org/dev/peps/) process, used by the Python language
community, and it takes motivations
from other similar processes in communities adjacent to **EpiGraphHub**, such as the
[NEP](https://numpy.org/neps/nep-0000.html) process for NumPy and the
[MEP](https://matplotlib.org/devel/MEP/index.html) process for Matplotlib.

However, the **EEP** process differs from these processes in many ways, so
those who may already be familiar with similar processes from other
communities should read this document to understand how it works for **EEPs**.

In particular, **EEPs** are significantly less formal than Python PEPs.

## Types

There are three kinds of **EEPs**:

A **Standards Track** **EEP** describes a new feature or important change for
**EpiGraphHub**.

An **Informational** **EEP** describes a **EpiGraphHub** design issue, or provides general
guidelines or information to the Python community, but does not propose a new
feature. Informational **EEPs** do not necessarily represent a **EpiGraphHub** community
consensus or recommendation, so users and implementers are free to ignore
Informational **EEPs** or follow their advice.

A **Process** **EEP** describes a process surrounding **EpiGraphHub**, or proposes a
change to (or an event in) a process. Process **EEPs** are like Standards Track
**EEPs** but apply to areas other than the **EpiGraphHub** library itself. They may
propose an implementation, but not to EEP’s codebase; they require community
consensus. Examples include procedures, guidelines, changes to the
decision-making process, and changes to the tools or environment used in **EpiGraphHub**
development. Any meta-EEP is also considered a Process EEP.

## Purpose

The **EEP** process and corresponding documents serve several purposes:

- To decide, as a community, whether a proposed change should be made.
- To decide on the process by which a change will be implemented, for example,
  whether the change should be implemented in several stages, whether
  intermediate releases are required for things like deprecations, and so on.
- To document the above discussions and decisions for future reference.
- To document the motivations for a change from the perspective of end users
  who may be affected by it. Here "end users" means both users of the **EpiGraphHub**
  library, as well as developers working on parts of **EpiGraphHub** itself which may be
  affected by the change.

Importantly, an **EEP** is not documentation for the proposed change. End
user documentation should be included with the implementation of the feature
in the corresponding **EpiGraphHub** documentation. This also means that other
documentation should not cross-reference an **EEP** as if it were documentation
for a feature. Even technical discussion of a feature should be documented
separately from an EEP. The reason is that **EEPs** will necessarily include
details that are irrelevant to the final implementation, such as discussions
of alternate implementations which were rejected and discussions of
implementation of the change.

## **EEP** Workflow

Discussions around a proposed change may begin informally on the mailing list
or **EpiGraphHub** issue tracker. However, once it is decided that the formal EEP
process is desired for a change, the discussion should move to the
[EEP repository](https://github.com/thegraphnetwork/epigraphhub-enhancement-proposals) on GitHub.

Every **EEP** must have a champion. This is a person who is responsible for
writing the EEP, leads the discussion around it, and tries to create
consensus around it.

The author of an **EEP** should fork the repository and create a pull request
with a new **EEP** document based on the [EEP template][eep-template].
The **EEP** document may be named `eep-YYYYXXX.md` until a number is assigned.

One of the core **EpiGraphHub** developers will then assign a number to the EEP, in
which case `XXX` should be replaced with the number with leading 0s. The
person who assigns the number should also update the
[README](https://github.com/thegraphnetwork/epigraphhub-enhancement-proposals/blob/main/README.md) of the main
[EEP repository](https://github.com/thegraphnetwork/epigraphhub-enhancement-proposals) to list that number.
Numbers should be assigned to **EEPs** as soon as it is determined that they
are a legitimate proposal. If an **EEP** ends up being rejected or postponed, it
keeps its number, as rejection or postponement status is still a discussion
that should be documented in the EEP. **EEP** numbers should generally be
assigned in increasing numeric order.

Discussion on the **EEP** should then continue on the **EEP** pull request.
Discussions may also take place in other places, such as [GitHub
discussions](https://github.com/thegraphnetwork/epigraphhub-enhancement-proposals/discussions) or the [mailing
list](http://groups.google.com/group/**EpiGraphHub**). All discussions should be
cross-referenced in the "Discussions" section of the **EEP** document.

For each EEP, the community should decide whether a draft implementation is
needed before acceptance or not. For instance, if an **EEP** concerns the
details of how a feature is implemented, it should be accepted before that
happens. On the other hand, the community may decide that it cannot come to a
consensus about an **EEP** until a draft implementation is proposed.

Once the community reaches a consensus about an EEP, the status of an EEP
should be updated (see below). This consensus may be to accept or to reject
the EEP, or to defer it. Here the "community" refers to the broader
community that has a stake in the EEP, not just the core **EpiGraphHub** developers.
The purpose of the **EEP** process is not to create a cabal of decision makers,
but rather to enhance the involvement of the broader **EpiGraphHub** community in the
decision making process.

### Status

The **status** section at the top of the **EEP** document (see the
[template](./eeps/__template__.md)) should be updated according to the
current status of the EEP.

All **EEPs** should be created with the **Draft** status. **Draft** status
**EEPs** generally live in a pull request.

Eventually, after discussion, there may be a consensus that the **EEP** should
be accepted–see the next section for details. At this point the status
becomes **Accepted**.

Once an **EEP** has been **Accepted**, the reference implementation must be
completed. When the reference implementation is complete and incorporated into
the main source code repository, the status will be changed to **Final**.

An **EEP** can also be assigned status **Deferred**. The **EEP** author or a core
developer can assign the **EEP** this status when no progress is being made on
the EEP.

An **EEP** can also be **Rejected**. Perhaps after all is said and done it was
not a good idea. It is still important to have a record of this fact. The
**Withdrawn** status is similar—it means that the **EEP** author themselves has
decided that the **EEP** is actually a bad idea, or has accepted that a
competing proposal is a better alternative.

**EEPs** can also be **Superseded** by a different EEP, rendering the
original obsolete.

Process **EEPs** may also have a status of **Active** if they are never meant
to be completed, e.g. **EEP** 1 (this EEP).

### Merging the **EEP** Document Pull Request

Whenever an **EEP** moves from the **Draft** status to one of the other above
statuses, the header should be updated, and the corresponding pull request
should be merged. This way the document lives inside of the **EEP** repository
proper. **EEPs** that are merged are not set in stone, and may be updated by
future pull requests (although **EEPs** that are **Accepted** should generally
not be significantly modified once they have reached that status). The purpose
of merging is simply to make the **EEP** visible in the repository, even if it
isn't yet accepted or rejected. **EEP** discussions that have stalled should
also be merged, so that the **EEP** becomes visible in the **EEP** repository
proper—again, discussion may be picked up again with a new pull request.

## Accepting an EEP

Once an **EEP** is Accepted by consensus of all interested contributors, a
topic should be created to the
[**EpiGraphHubPy** GitHub Discussions](https://github.com/thegraphnetwork/epigraphhub_py/discussions)
or
[**EpiGraphHubR** GitHub Discussions](https://github.com/thegraphnetwork/r-epigraphhub/discussions)
with a subject like:

    Proposal to accept **EEP** #<number>: <title>

In the body of your message, you should:

- link to the latest version of the EEP,

- briefly describe any major points of contention and how they were resolved,

- include a sentence like: “If there are no substantive objections within 7
  days from this message, then the **EEP** will be accepted; see **EEP** 1 for
  more details.”

After you start this discussion, add the GitHub discussion link
to the Discussion section of the EEP, so that people can find it later.

Generally, the **EEP** author will be the one to start this GH Discussion,
but anyone can do it – the important thing is to make sure that everyone
knows when an **EEP** is on the verge of acceptance, and give them a final
chance to respond. If there’s some special reason to extend this final
comment period beyond 7 days, then that’s fine, just say so in the GH Discussion.
It shouldn’t be less than 7 days, because sometimes people are traveling
or similar and need some time to respond.

In general, the goal is to make sure that the community has consensus, not
provide a rigid policy for people to try to game. When in doubt, err on the
side of asking for more feedback and looking for opportunities to compromise.

If the final comment period passes without any substantive objections, then
the **EEP** can officially be marked **Accepted**. A followup message should then
be sent to its GH Discussion thread. Update the **EEP** by setting its **Status** to
**Accepted**, and its **Resolution** header to a link to your GH Discussion thread.
The **EEP** pull request should be merged at this time, if it hasn't been
already, so that it is visible in the **EEP** repository proper.

If there are substantive objections, then the **EEP** remains in Draft state,
discussion continues as normal, and it can be proposed for acceptance again
later once the objections are resolved.

## Discussion

- None

## License

BSD-3-Clause


## Acknowledge

This Enhancement Proposal Template was based other templates, such as:
Arx Enhancement Proposal (ArxEP), Sympy Enhancement Proposal (SymEP),
Numpy Enhancement Proposal (NEP), Python Enhancement Proposal (PEP).


<!-- markdown references -->

[eep-template]: https://github.com/thegraphnetwork/epigraphhub-enhancement-proposals/blob/main/eeps/__template__.md
