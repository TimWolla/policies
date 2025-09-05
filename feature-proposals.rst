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

******************
 Discussion Phase
******************

Before an RFC may move to the voting phase a cooldown period of 2 weeks (336
hours) MUST have elapsed. The cooldown period starts at the time of the initial
email of the official RFC discussion thread.

When making non-editorial / non-typographical changes to the normative section
of the RFC text (i.e. to the actual proposal, excluding future scope, rejected
features and references) the cooldown period MUST be reset. The cooldown period
MUST be reset to 2 weeks (336 hours) in case of major changes. It MUST be reset
to 1 week (168 hours) in case of minor changes if the current remaining cooldown
period is shorter. When in doubt, the change MUST be treated as a major change.
Major and minor changes MUST be announced in the official discussion thread,
either in a dedicated email summarizing a list of changes or in a reply to
another email that clearly indicates that changes to the RFC text have been made
in response to that email.

As an example: An RFC is announced at 2025-02-01 15:00. The initial cooldown
period ends at 2025-02-15 15:00. On 2025-02-03 16:00 a minor change to the RFC
text is made. The cooldown period is not reset, since the remaining cooldown
period of ~12 days is longer than 1 week. On 2025-02-05 17:00 a major change to
the RFC text is made. The cooldown period is reset to 2025-02-19 17:00. On
2025-02-15 16:00 another minor change is made. The cooldown period is reset to
2025-02-22 16:00. On 2025-02-21 13:00 an obvious typo is fixed. The cooldown
period is not reset.

Major changes to the RFC text include any changes that would lead to a change in
the implementation, particularly any changes to the proposed semantics or
syntax, updating the API stub, adding, changing or removing any voting widget.
Minor changes to the RFC text include adding new examples, updating existing
examples, adding additional explanation or clarification, or any other changes
that are not purely editorial.

The discussion phase MAY be extended beyond the required cooldown period. It
SHOULD appropriately be extended in holiday periods or in cases of significant
activity on the mailing list to allow everyone to catch up with the discussion.

After a period of 6 weeks without any email in the official discussion thread,
the discussion is considered inactive and MUST be restarted with a cooldown
period of 1 week (168 hours) before the RFC may proceed to a vote, since it is
likely that other RFC discussions are at the top of mind of the mailing list
participants. After a period of 3 months without any email in the official
discussion thread, the discussion MUST be restarted with a cooldown period of 2
weeks (336 hours).

This does not preclude discussion on the merits on any idea or proposal on the
list without formally submitting it as a proposal, but the cooldown period is
measured only since the formal discussion announcement as described above.

**************
 Voting Phase
**************

RFC authors MAY start a vote after the cooldown period has elapsed. The
intention of starting the vote MUST be announced at least 2 days (48 hours)
before the start of the vote in the official discussion thread. RFC authors
SHOULD NOT announce the start of the vote when the RFC discussion is still
ongoing and new discussion points are brought forward. Similarly RFC authors
SHOULD NOT proceed with an announced vote if new discussion points are brought
forward after the voting announcement. If major or minor changes to the RFC text
are made after announcing the vote, the cooldown period MUST be reset and a new
vote MUST be announced when the RFC is ready for voting after the new cooldown
period has elapsed.

The actual start of the vote MUST be announced on the mailing list in a separate
thread with a ``[VOTE]`` prefix followed by the RFC title as the Subject. The
email MUST include a link to the Wiki page of the RFC and to the mailing list
archives of the discussion thread. The link to the mailing list archives of the
voting thread MUST be added to the RFC as soon as possible and no later than the
announcement of the results of the vote.

The email MUST furthermore clearly specify the voting formalities, such as the
number of votes that can be cast, the interpretation of the voting results and
the end date of the voting. The end date MUST be specified with
minute-precision. The voting period MUST be open for at least two weeks (336
hours). The voting period MAY be extended as necessary (e.g. to accommodate
holiday periods).

Due to the significance of the end-of-year holidays for a majority of the world,
the voting period MUST NOT start and MUST NOT end in the period between
December, 17th 00:00 UTC and January, 10th 00:00 UTC.

After the voting period started, including after the vote closed and the RFC is
either accepted or declined, there MUST NOT be any further major or minor
changes to the RFC text and making editorial changes SHOULD be avoided for the
avoidance of doubt. The voting formalities (including the voting period) MUST
NOT be changed after the vote opened. The voting period MAY be canceled within
the first 2 days (48 hours) in case of severe issues with the RFC. Canceling a
vote is treated as a major change and a cooldown period of 2 weeks (336 hours)
is required before a new vote may be started. The title of all voting widgets
MUST be changed to invalidate any votes that have been cast (e.g. by adding the
suffix “(Restart)”).

If issues with an accepted RFC are noticed during implementation, an errata
section explaining the necessary changes SHOULD be added.

This section has been amended by:

-  `Abolish Short Votes RFC <https://wiki.php.net/rfc/abolish-short-votes>`_.

*******************
 Required Majority
*******************

All votes in an RFC MUST have an "Abstain" option, which is treated identically
to not casting a vote in terms of calculating results, but is used as a signal
that eligible voters explicitly decline to vote one way or the other on a
question rather than simply not having noticed the RFC.

The primary vote of an RFC, determining overall acceptance of the proposal, MUST
be a clearly phrased binary question with the voting options "Yes", "No", and
"Abstain". The primary vote SHOULD be phrased "Implement $feature as outlined in
the RFC?" to avoid ambiguity. For a primary vote to be accepted a 2/3 majority
of "Yes" votes is required. This means that the number of "Yes" votes must be
greater than or equal to the number of "No" votes multiplied by two.

As an example, an RFC with 8 "Yes", 4 "No", and 9 "Abstain" votes is accepted,
as the number of "Yes" votes is twice the number of "No" votes and "Abstain"
votes do not take part in the calculation. An RFC with 5 "Yes", 3 "No", and 4
"Abstain" votes is not accepted.

Additionally, an RFC MAY have secondary votes, which are used to decide
implementation details. The result of secondary votes is void unless the
corresponding primary vote is accepted. Secondary votes MAY have more than two
voting options and MAY be decided by plurality (meaning that the voting option
with the most votes wins). For secondary votes with two voting options the RFC
author MAY decide on a higher threshold (up to a 2/3 majority) for an individual
option. Secondary votes with more than two voting options MAY also be decided
using the "Single transferable vote" voting system. The voting system used,
necessary threshold(s), and tie-breakers MUST be defined at the start of the
voting period.

As an example, a secondary vote using a plurality and having 5 "Foo", 4 "Bar", 8
"Baz", and 9 "Abstain" votes decided on the "Baz" result, since it has the most
number of votes excluding the "Abstain" option. It is not necessary to reach 50%
of the votes ("simple majority").

For procedural reasons, multiple related proposals MAY be combined into one RFC,
in which case there MAY be multiple primary votes. Combining multiple proposals
into one RFC MUST NOT be used to turn a primary vote into a secondary vote.

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
