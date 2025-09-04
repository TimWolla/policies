###################
 Feature Proposals
###################

**************
 Introduction
**************

This document describes the procedure to propose an idea for adoption by the PHP
community and decide if the community accepts or rejects the idea.

*********************
 Proposal Initiation
*********************

A proposal is formally initiated by creating an RFC on the PHP Wiki and
announcing it on the ``internals@lists.php.net`` mailing list.

The official RFC discussion thread MUST use the prefix ``[RFC]`` followed by the
title of the RFC as the Subject. The email MUST include a link to the Wiki page
containing the RFC. The link to the mailing list archives of the discussion
thread MUST be added to the RFC as soon as possible and no later than the
announcement of the start of the vote.

The discussion thread MUST be initiated by one of the RFC's authors. If the
proposal is a repeated one, re-proposed by somebody else, the proposer MUST
discuss it with the original author and add themselves to the RFC author list
before proposing it. If the original RFC authors do not agree or do not respond,
a new Wiki page containing an RFC with a unique title MUST be created. In this
case the original RFC's title is commonly suffixed with ``v2`` to indicate the
relationship with the original RFC.

*******************
 Discussion Period
*******************

Before an RFC may move to the voting phase a minimum discussion period of 2
weeks (336 hours) MUST have elapsed. The discussion period starts at the time of
the initial email of the official RFC discussion thread.

When making non-editorial / non-typographical changes to the normative section
of the RFC text (i.e. to the actual proposal, excluding future scope, rejected
features and references) the discussion period MUST be extended. The discussion
period MUST be extended by 2 weeks (336 hours) in case of major changes. It MUST
be extended by 1 week (168 hours) in case of minor changes. When in doubt, the
change MUST be treated as a major change. Major and minor changes MUST be
announced in the official discussion thread, either in a dedicated email
summarizing a list of changes or in a reply to another email that clearly
indicates that changes to the RFC text have been made in response to that email.
Extensions of the discussion period are not cumulative. The new minimum
discussion period is the current remaining minimum discussion period or the
extended discussion period calculated from the time of the email announcing the
changes that extend the discussion period.

As an example: An RFC is announced at 2025-02-01 15:00. The initial minimum
discussion period ends at 2025-02-15 15:00. On 2025-02-03 16:00 a minor change
to the RFC text is made. The discussion period is not extended, since the
remaining period of 12 days is longer than the required extension. On 2025-02-05
17:00 a major change to the RFC text is made. The minimum discussion period is
extended to 2025-02-19 17:00. On 2025-02-15 16:00 another minor change is made.
The minimum discussion period is extended to 2025-02-22 16:00. On 2025-02-21
13:00 an obvious typo is fixed. The discussion period is not extended.

Major changes to the RFC text include any changes that would lead to a change in
the implementation, particularly any changes to the proposed semantics or
syntax, updating the API stub, retitling any voting widget, or adding voting
widgets. Minor changes to the RFC text include adding new examples, updating
existing examples, adding additional explanation or clarification, or any other
changes that are not purely editorial.

The discussion period MAY be extended beyond the required minimum discussion
period. It SHOULD appropriately be extended in holiday periods or in cases of
significant activity on the mailing list to allow everyone to catch up with the
discussion.

After a period of 6 weeks without any email in the official discussion thread,
the discussion is considered inactive and MUST be restarted with a minimum
discussion period of 1 week (168 hours) before the RFC may proceed to a vote,
since it is likely that other RFC discussions are at the top of mind of the
mailing list participants. After a period of 3 months without any email in the
official discussion thread, the discussion MUST be restarted with a minimum
discussion period of 2 weeks (336 hours).

This does not preclude discussion on the merits on any idea or proposal on the
list without formally submitting it as a proposal, but the discussion time is
measured only since the formal discussion announcement as described above.

********
 Voting
********

RFC authors MAY start a vote after the minimum discussion period has elapsed.
The intention of starting the vote MUST be announced at least 2 days (48 hours)
before the start of the vote in the official discussion thread. RFC authors
SHOULD NOT announce the start of the vote when the RFC discussion is still
ongoing and new discussion points are brought forward. Similarly RFC authors
SHOULD NOT proceed with an announced vote if new discussion points are brought
forward after the voting announcement. If major or minor changes to the RFC text
are made after announcing the vote, the discussion period MUST be extended and a
new vote MUST be announced when the RFC is ready for voting after the new
minimum discussion period has elapsed.

The actual start of the vote MUST be announced on the mailing list in a separate
thread with a ``[VOTE]`` prefix followed by the RFC title as the Subject. The
email MUST include a link to the Wiki page of the RFC and to the mailing list
archives of the discussion thread. It furthermore MUST clearly specify the
voting formalities, such as the number of votes that can be cast, the
interpretation of the voting results and the end date of the voting. The end
date MUST be specified with minute-precision. The voting period MUST be open for
at least two weeks (336 hours). The voting period MAY be extended as necessary
to accommodate holiday periods. Due to the significance of the end-of-year
holidays for a majority of the world, the voting period MUST NOT end in the
period between December, 17th 00:00 UTC and January, 10th 00:00 UTC. The link to
the mailing list archives of the voting thread MUST be added to the RFC as soon
as possible and no later than the announcement of the results of the vote.

This section has been amended by:

-  `Abolish Short Votes RFC <https://wiki.php.net/rfc/abolish-short-votes>`_.

*******************
 Required Majority
*******************

The primary vote of an RFC, determining overall acceptance of the proposal, may
only have two voting options and requires a 2/3 majority. This means that the
number of Yes votes must be greater than or equal to the number of No votes
multiplied by two.

Additionally, an RFC may have secondary votes, which are used to decide
implementation details. Such votes may have more than two voting options and may
be decided by simple plurality. This means that the voting option with the most
votes wins. If there are multiple options with the most number of votes, it is
left at the discretion of the RFC author to choose one of them.

For procedural reasons, multiple RFCs may be combined into one, in which case
there may be multiple primary votes. Combining multiple RFCs into one does not
allow turning a primary vote into a secondary vote.

This section has been amended by:

-  `Abolish Narrow Margins RFC
   <https://wiki.php.net/rfc/abolish-narrow-margins>`_.

*********************************
 Resurrecting Rejected Proposals
*********************************

In order to save valuable time, it will not be allowed to bring up a rejected
proposal up for another vote, unless one of the following happens:

-  6 months pass from the time of the previous vote, **OR**

-  The author(s) make substantial changes to the proposal. While it's impossible
   to put clear definitions on what constitutes 'substantial' changes, they
   should be material enough so that they'll significantly affect the outcome of
   another vote.

**************
 Who Can Vote
**************

There's no way around this 'small' issue. Changes made to the PHP language will
affect millions of people, and theoretically, each and every one of them should
have a say in what we do. For obvious reasons, though, this isn't a practical
approach.

The proposal here is for two audiences to participate in the voting process:

-  People with php.net VCS accounts that have contributed code to PHP

-  Representatives from the PHP community, that will be chosen by those with
   php.net VCS accounts

   -  Lead developers of PHP based projects (frameworks, cms, tools, etc.)
   -  regular participant of internals discussions

**************
 RFC Proposer
**************

-  Proposers vote with +1 on their own RFC per default if they are allowed to
   vote
