# Kubernetes Steering Committee Charter

## Overview

This document describes the bootstrapping process for the Kubernetes Steering
Committee. It describes the formation of the initial steering committee and its
core responsibilities. This includes its governance processes and processes to
reform itself as necessary.

## Goals

The initial role of the steering committee is to instantiate the formal process
for Kubernetes governance. In addition to defining the initial governance
process, the bootstrap committee strongly believes that it is important to
provide a means for iterating the processes defined by the steering committee.
We do not believe that we will get it right the first time, or possibly ever,
and won’t even complete the governance development in a single shot. The role
of the steering committee is to be a live, responsive body that can refactor
and reform as necessary to adapt to a changing project and community.

## Scope
The Steering Committee has a set of rights and responsibilities including the
following:

* Decide which project subgroups are responsible for each area of the project
  and to delegate appropriate authority those groups.
* Define, evolve, and defend the vision, values, mission, and scope of the
  project - to establish and maintain the soul of Kubernetes
* Charter and refine policy for defining new community groups (including
  Special Interest Groups, Working Groups, and Committees), and establish
  transparency and accountability policies for such groups
* Define, evolve, and defend a Code of Conduct, which must include a neutral,
  unbiased process for resolving conflicts
* Define and evolve project governance structures and policies, including how
  contributors become committers/maintainers, approvers, reviewers, members,
  etc.
* Decide, for the purpose of elections, who is a member of standing of the
  Kubernetes project, and what privileges that entails
* Decide which sub-projects are part of the Kubernetes project, including
  accepting new sub-projects and pruning existing sub-projects to maintain
  community focus
* Decide how and when official releases of Kubernetes artifacts are made and
  what they include
* Control access to, establish processes regarding, and provide a final
  escalation path for any Kubernetes repository, which currently includes all
  repositories under the github organizations kubernetes, kubernetes-incubator,
  kubernetes-security, and kubernetes-client, and is expected to expand in the
  future
* Control and delegate access to and establish processes regarding other
  project resources/assets, including artifact repositories, build and test
  infrastructure, web sites and their domains, blogs, social-media accounts,
  etc.
* Define what a conformant Kubernetes cluster is as part of any certification
  process
* Manage the Kubernetes brand to decide which things can be called “Kubernetes”
  and how that mark can be used in relation to other efforts or vendors.
* Declare a release, so that the committee can ensure quality/feature/other
  requirements are met.
* Request funds and other support from the CNCF (e.g. marketing, press, etc.)

## Committee Structure

### Establishment of a steering committee

To bootstrap the process of Kubernetes governance, seven individuals (Joe Beda,
Brendan Burns, Clayton Coleman, Brian Grant, Tim Hockin, Sarah Novotny and
Brandon Philips) were identified to be the Bootstrap Committee, to provide the
initial process that can bootstrap the remainder of the process.

The Bootstrap Committee will be replaced by the Kubernetes Steering Committee.
Ultimately, the Kubernetes Steering Committee will consist of 7 members of the
community elected for 2 year terms.  The terms will be staggered with 1 year
elections (alternating 4 seats and 3 seats).

To provide a level of continuity as this process is established, the initial
committee will include continuity members, expanding the size to 13 members,
which will be eliminated after the first two years. 

This year (2017) as this proposal is enacted, the committee will consist of the
members of the bootstrap committee (Joe Beda, Brendan Burns, Clayton Coleman,
Brian Grant, Tim Hockin, Sarah Novotny, Brandon Philips) plus 6 positions to be
elected from the community. Of the 6 members that are elected, 3 will have a 2
year term and 3 will have 1 year term. 

One year later (in 2018) there will be an election of the 3 people serving a
one year term. The continuity members of the original bootstrap committee will
continue to serve.

One year after that (2019), the continuity positions will be eliminated and the
committee will shrink to the final size of 7.  There will be an election to
fill the 4 open seats on the steering committee. The previous continuity
members are eligible to run for these seats.

The committee will continue to iterate with alternating elections of three and
four members each year. 

For clarity, a table describing this process is given below:

| Year	| Continuity	| Cohort 1		| Cohort 2		|
|----	|----		|----			|----			|
| 2017	| 7 people	| 3 people (2yr term)	| 3 people (1yr term)	|
| 2018	| -		| -			| 3 people (2yr term)	|
| 2019	| 0 people	| 4 people (2yr term)	| -			|
| 2020	| -		| -			| 3 people (2yr term)	|
| 2021	| -		| 4 people (2yr term)	| -			|

## Elections

Special note: The bootstrap committee pledges to recuse itself from any direct
election activities while they serve as continuity members. Members of the
bootstrap committee will refrain from endorsing or otherwise advocating for any
candidate (with the exception that the members of the bootstrap committee may
vote in the elections, and may choose to run in the 2019 election).

### Members of Standing

Initial standing in the Kubernetes community will be defined by the union of:
* SIG leads
* Approvers and reviewers in any Kubernetes owned repositories
* Anyone with write access to a Kubernetes owned repository

The bootstrap committee *explicitly* believes that this heuristic will be
inaccurate and not represent the entire community. An exception form will be
provided for people who have contributed to the project but may not meet these
criteria. Exception applications will be approved by the bootstrap committee
will vote on this eligibility, with simple majority determining eligibility.
The exception process will be used as data points for refining the criteria for
the future.

Within its first year, the Steering Committee will redefine these criteria
around a more robust idea of community membership.

### Eligibility for candidacy

Anyone may nominate either themselves or someone else to be a candidate in the
election. To be ratified as a candidate, the nominee must accept the nomination
and three Members of Standing (including the nominator, if she/he has standing)
from three different employers, must endorse the nomination.  

Nominators are free to nominate as many people as they wish to. Members of
Standing may endorse multiple nominees, but we expect endorsements to be be in
good faith.  If this turns out to be a problem, this will be reconsidered.

### Eligibility for voting

All Members of Standing are eligible to vote for the steering committee
members. 

### Election process

Elections will be held using time-limited Condorcet ranking on CIVS. The top
vote getters will be elected to the respective positions. 

### Maximal representation

To encourage diversity there will be a maximum of one-third representation on
the Steering Committee from any one company at any time. If the results of an
election result in greater than 1/3 representation, the lowest vote getters
from any particular company will be removed until representation on the
committee is less than one-third.

If percentages shift because of job changes, acquisitions, or other events,
sufficient members of the committee must resign until max one-third
representation is achieved. If it is impossible to find sufficient members to
resign, the entire company’s representation will be removed and new special
elections held. In the event of a question of company membership (for example
evaluating independence of corporate subsidiaries) a majority of all
non-involved Steering Committee members will decide. 

### Initial Election

Because of the need to bootstrap a staggered election cycle, some of the
initial committee members will only serve a single year term. These three
people will be the lowest vote getters from the top six in the initial
election.

The bootstrap committee will operate the election and circulate a timeline for
nominations, and the vote.

### Vacancies

In the event of a resignation or other loss of a steering committee member, the
candidate with the next most votes from the previous election will be offered
the seat.  This process will continue until the seat is filled.  In case this
fails to fill the seat, a special election for that position will be held as
soon as possible. The same group of people as described in “eligibility for
voting” will vote in the special election. A committee member elected in a
special election will serve out the remainder of the term for the person they
are replacing, regardless of the length of that remainder. If a continuity
member resigns or otherwise is lost from the Committee, that position will not
be filled.

### Limiting Corporate Campaigning

To reduce size of company advantages, candidates may not use their companies
internal or external brand to campaign.  Their employers cannot solicit votes
on their behalf or sponsor candidates from partner organizations.  Simply put,
elections highlight individuals outside of their corporate role and should be
treated as “brand free” activities.

## Refactoring or reforming the steering committee

At any time the steering committee may vote, via super majority (greater than
two-thirds of votes), to rewrite or remove any part of this charter. Beyond
small tweaks, this should be used sparingly, if ever, and in the presence of
clear failures of the process. We explicitly do not allocate a role for the
broader community in reformulating governance, we believe that in such a case
the community will “vote with their feet” by either leaving or forking the
project.

## Emeritus Term

Members of the steering committee will graduate to becoming Emeritus members of
the steering committee.

## Steering Committee Meetings

Regular steering committee meetings will be held, at least once per month. The
entire steering committee is generally expected to attend every meeting, but
quorum is met with 2/3 attendance. If a member misses more than 50% of all
meetings held within a six month period then they will be removed from the
committee and a special election will be held. Recorded videos of the meetings
will be made publicly available in a timely manner.

Non-recorded, closed meetings are reserved for confidential matters (for
example code of conduct issues) which are not appropriate to be shared with the
broader community. Steering committee meetings can be made closed by a simple
majority vote of the steering committee members, but closed meetings do not
count towards the required meeting frequency. The steering committee will
inform the community if a particular meeting is closed, as well as the general
reasons for this, prior to the meeting taking place.
