# Kubernetes Steering Committee Elections

This document outlines the process, for Steering Committee elections.

### For the 2021 election check the [2021 Kubernetes Election Voter's Guide][voter-guide]

### Eligibility for voting

Eligibility for voting in the 2021 Election is [defined in this year's voter guide][voter-guide]

Eligibility to vote for Steering Committee members for prior years is defined by:

* People who had at least 50 contributions to the Kubernetes project over
  the past year, according to a snapshot taken 2021-09-15 of the data driving
  the [devstats developer activity counts dashboard][devstats-dashboard].
  Contributions include GitHub events like creating issues, creating pr's,
  reviewing PR's, commenting on issues, etc. For full details see
  [the SQL query used by devstats for developer activity counts][devstats-sql].

* People who have submitted the [voting exception form] and are accepted by
  the election committee. We *explicitly* believe the above heuristic will be
  inaccurate and not represent the entire community. Thus we provide the form
  for those who have contributed to the project but may not meet the above
  criteria.  Acceptance of a form submission will be defined by a simple
  majority vote, and the criteria used during this process will be used to
  help refine further elections.

It is the responsibility of the Steering Committee to refine these criteria
prior to each election.

### Eligibility for candidacy

Eligibility for candidacy is defined by:

* Acceptance of a nomination, or self-nomination (anyone may nominate, anyone
  may be nominated)
* Endorsement by three eligible voters from three different employers (the
  candidate can self-endorse if they are eligible to vote)

Check the [2021 Kubernetes Election Voter's Guide][candidacy] for the exact
nomination procedure.

Nominators are free to nominate as many people as they wish to. Eligible
voters may endorse multiple nominees, but we expect endorsements to be in
good faith.  If this turns out to be a problem, this will be reconsidered.

### Election process

Elections will be held using an online preference election system which 
supports [Condorcet] elections. The most preferred candidates will be elected to 
the open seats.

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

### Committee Conflict of Interest

As project committees have unique charters, there is a possibility
for a conflict of interest to arise.  While multiple scenarios may
be possible now or in the future, one known example of such conflict
of interest is where a member of the Code of Conduct Committee is
elected to the Steering Committee.

Such conflict will be resolved by the applicable election committee
reaching out to the newly-elected member and facilitating a decision
regarding on which committee the individual will continue.  The
committee where that individual vacated their seat will fill that
vacancy as per existing election or committee vacancy rules.

### Terms and Election Cycles

Steering Committee members are elected to serve one, two year term. Members can
serve two consecutive terms (4 years) and a lifetime of four terms (8 years). 
Bootstrap and terms that result in equal to or less than one year served are 
exempt.   

Election cycles are scheduled such that roughly half of the seats come up for
re-election each year for purposes of continuity.  The exact number of seats
alternates between 3 and 4, with the first 3-seat election taking place in
2018.

## Emeritus Term

Members of the Steering Committee will graduate to becoming Emeritus members of
the Steering Committee upon vacating their seat.  This confers honor on the
recipient, acknowledging the significant contributions they have made to the
project. Emeritus members have no binding vote, and no expectation of continued
participation in Steering Committee affairs.

## Election schedule and operation

The Steering Committee picks election officers to operate the election and
circulate a timeline for nominations, and the vote. The Steering Committee
should consider the following rough schedule:

- End of July
  - Election officers
  - Voter eligibility criteria
  - Election preparation
- September   
  - Nomination period and election
- October  
  - Conclusion of Election
  - Results announced at first community meeting after the election concludes

The election officers will choose exact dates for each step and propose the
final schedule to steering per the [election procedure].

### Election officer selection

The Steering Committee should choose three election officers, ideally by the
following criteria, so as to promote healthy rotation and diversity:

- election officers must be eligible to vote
- two election officers should have served before
- one election officer should have never served before
- each officer should come from a different company to maintain 1/3 maximal
  representation

Election officers follow the [election procedure] to administer the election.  

History of election officers:  
2017: castrojo and parispittman  
2018: castrojo, parispittman, idvoretskyi  
2019: mrbobbytables, castrojo, idvoretskyi  
2020: jberkus, jdumars, idvoretskyi    
2021: jberkus, alisondy, coderanger

### Vacancies

In the event of a resignation or other loss of a [bootstrap committee member],
the position will not be refilled.

In the event of a resignation or other loss of an elected Steering Committee
member, the candidate with the next most votes from the previous election will
be offered the seat.  This process will continue until the seat is filled.

In case this fails to fill the seat, a special election for that position will
be held as soon as possible. Eligible voters from the most recent election
will vote in the special election (ie: eligibility will not be redetermined
at the time of the special election). A committee member elected in a special
election will serve out the remainder of the term for the person they are
replacing, regardless of the length of that remainder.

### Limiting Corporate Campaigning

To reduce size of company advantages, candidates may not use their companies
internal or external brand to campaign.  Their employers cannot solicit votes
on their behalf or endorse candidates from partner organizations.  Simply put,
elections highlight individuals outside of their corporate role and should be
treated as “brand free” activities.

## Steering Committee and Election Officer Recusal

Currently serving Steering Committee members and the appointed election officers
pledge to recuse themselves from any form of electioneering, including
campaigning, nominating, or endorsing. We would prefer that the community
decide without our heavy influence.

Steering Committee members _may_ ask other contributors to consider running,
and they _may_ vote, so long as this information is kept private.

Steering Committee members who intend to run for re-election _may_
self-nominate but are otherwise expected to adhere to this recusal.

[Condorcet]: https://en.wikipedia.org/wiki/Condorcet_method

[election procedure]: https://git.k8s.io/community/events/elections/README.md

[devstats-sql]: https://github.com/cncf/devstats/blob/master/metrics/shared/project_developer_stats.sql
[devstats-dashboard]: https://k8s.devstats.cncf.io/d/13/developer-activity-counts-by-repository-group?orgId=1&var-period_name=Last%20year&var-metric=contributions&var-repogroup_name=All

[bootstrap committee member]: https://github.com/kubernetes/steering#initial-bootstrap-committee
[voter-guide]: https://github.com/kubernetes/community/tree/master/events/elections/2021
[candidacy]: https://github.com/kubernetes/community/tree/master/events/elections/2021#candidacy-process
[voting exception form]: https://elections.k8s.io/app/elections/2021/exception
