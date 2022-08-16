# Kubernetes Steering Committee Elections

This document outlines the process for steering committee elections.

### For the current election, check the [Steering Elections][elections] directory

### Eligibility for voting

Precise eligibility for voting in the current Election is 
[defined in the current year's voter guide][elections]

Eligibility to vote for steering committee members is generally defined by:

* [Kubernetes Org Members][members] who had at least a certain number of 
  contributions to the Kubernetes project over the past year, according to a 
  data snapshot taken shortly before the election starts, based on
  the [devstats developer activity counts dashboard][devstats-dashboard].
  Contributions include GitHub events like creating issues, creating PRs,
  reviewing PRs, commenting on issues, etc. For full details see
  [the SQL query used by devstats for developer activity counts][devstats-sql].
  
* Members of certain committees that involve substantial contributions to
  Kubernetes that are frequently not recorded by DevStats, such as the 
  Security Response Committee and the Code of Conduct Committee.

* People who have submitted the voting exception form and are accepted by
  the election committee. We *explicitly* believe the above heuristic will be
  inaccurate and not represent the entire community. Thus we provide the form
  for those who have contributed to the project but may not meet the above
  criteria.  Acceptance of a form submission will be defined by a simple
  majority vote, and the criteria used during this process will be used to
  help refine further elections.

It is the responsibility of the steering committee to refine these criteria
prior to each election, including setting the number of required contributions,
and adding any additional committee memberships that include eligibility.

### Eligibility for candidacy

Eligibility for candidacy is defined by:

* Acceptance of a nomination, or self-nomination (anyone may nominate, anyone
  may be nominated)
* Endorsement by three eligible voters from three different employers (the
  candidate can self-endorse if they are eligible to vote)

Check the current [election Voters Guide][elections] for the exact
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

### Terms and Election Cycles

Steering committee members are elected to serve one, two year term. Members can
serve two consecutive terms (4 years) and a lifetime of four terms (8 years). 
Bootstrap and terms that result in equal to or less than one year served are 
exempt.   

Election cycles are scheduled such that roughly half of the seats come up for
re-election each year for purposes of continuity.  The exact number of seats
alternates between 3 and 4, with the first 3-seat election taking place in
2018.

## Emeritus Term

Members of the steering committee will graduate to becoming Emeritus members of
the steering committee upon vacating their seat.  This confers honor on the
recipient, acknowledging the significant contributions they have made to the
project. Emeritus members have no binding vote, and no expectation of continued
participation in steering committee affairs.

## Election schedule and operation

The steering committee picks election officers to operate the election and
circulate a timeline for nominations, and the vote. The steering committee
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

The steering committee should choose three election officers, ideally by the
following criteria, so as to promote healthy rotation and diversity:

- election officers must be eligible to vote
- election officers should have been an org member for at least one year
- at least one (ideally two) election officers should have served before
- at least one election officer should have never served before
- each officer should come from a different company to maintain 1/3 maximal
  representation

Election officers follow the [election procedure] to administer the election.  

History of election officers:  
2017: castrojo and parispittman  
2018: castrojo, parispittman, idvoretskyi  
2019: mrbobbytables, castrojo, idvoretskyi  
2020: jberkus, jdumars, idvoretskyi    
2021: jberkus, alisondy, coderanger
2022: coderanger, kaslin, dims

### Vacancies

See [Steering Committee charter](/charter.md).

### Limiting Corporate Campaigning

To reduce size of company advantages, candidates may not use their companies
internal or external brand to campaign.  Their employers cannot solicit votes
on their behalf or endorse candidates from partner organizations.  Simply put,
elections highlight individuals outside of their corporate role and should be
treated as “brand free” activities.

## Steering Committee and Election Officer Recusal

Currently serving steering committee members and the appointed election officers
pledge to recuse themselves from any form of electioneering, including
campaigning, nominating, or endorsing. We would prefer that the community
decide without our heavy influence.

Steering committee members _may_ ask other contributors to consider running,
and they _may_ vote, so long as this information is kept private.

Steering committee members who intend to run for re-election _may_
self-nominate but are otherwise expected to adhere to this recusal.

[Condorcet]: https://en.wikipedia.org/wiki/Condorcet_method

[election procedure]: https://git.k8s.io/community/events/elections/README.md

[devstats-sql]: https://github.com/cncf/devstats/blob/master/metrics/shared/project_developer_stats.sql
[devstats-dashboard]: https://k8s.devstats.cncf.io/d/13/developer-activity-counts-by-repository-group?orgId=1&var-period_name=Last%20year&var-metric=contributions&var-repogroup_name=All

[bootstrap committee member]: https://github.com/kubernetes/steering#initial-bootstrap-committee
[elections]: https://github.com/kubernetes/community/tree/master/elections/steering
[members]: https://github.com/kubernetes/community/blob/master/community-membership.md
