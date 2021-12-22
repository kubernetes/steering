# Kubernetes Community Annual Report, 2020

This is a summary of the Kubernetes project's contributor community and
activities. This report documents both quantitative measures of community health
(project milestones and snapshot) as well as qualitative measures of the
community as reported by community leaders and contributors to the project.
Please see Appendices for full reports and program goals.

This report is a snapshot of the community as of December 2020. 

1. [Terminology](#terminology)
2. [Contributor Snapshot](#contributor-snapshot)
3. [Community Milestones](#community-milestones)
4. [Governance](#governance)
5. [Accolades](#accolades)
6. [Themes](#themes)
7. [Growth Areas](#growth-areas)
8. [/help-wanted](#/help-wanted)
9. [Current Initiatives](#current-initiatives)
10. [Appendices](#appendices)

### Terminology

This report uses the following terminology:

- **Special Interest Group (SIG)**: a body of contributors, responsible on an
  ongoing basis for an area of work in the Kubernetes project. They own code,
  docs, and/or policy.
- **Working Group (WG)**: a body of contributors, responsible for an area of
  work in the project. Unlike SIGs, WGs dissolve once the scoped work is
  complete. Working groups are cross-functional efforts sponsored by a SIG. 
- **Chair and/or Tech Lead**: a contributor who organizes and leads a community
  group.
- **KEP**: [Kubernetes Enhancement Proposal][kep]
- **OWNER/maintainer**: a GitHub user who reviews, approves, and/or merges commits. 

For more on SIG and WG governance, see:

- [SIG governance]
- [WG governance]

For a list of all SIGs and WGs, their charters, meet times, ownership, and more,
see: 

- [SIG list]
- [WG list]

[SIG governance]: https://git.k8s.io/community/committee-steering/governance/sig-governance.md
[WG governance]: https://git.k8s.io/community/committee-steering/governance/wg-governance.md
[SIG list]: https://www.kubernetes.dev/community/community-groups/#special-interest-groups
[WG list]: https://www.kubernetes.dev/community/community-groups/#working-groups


### Data Collection

The Kubernetes Steering Committee sent out a survey to all contributor group
chairs and leads to collect data for this report.

For more, see: 

- [Appendix A: Program Documentation](#Appendix-Program-documentation)
- [Appendix B: Survey Questions](#Appendix-B-Survey-Questions)
- [Appendix C: All SIG and WG Reports](#Appendix-C-All-SIG-and-WG-Reports)


## Contributor Snapshot

As recorded in [devstats] and [sigs.yaml changes], in 2020 the
Kubernetes project had:

- `52,000` Contributors
- `24` Special Interest Groups (SIGs)*
- `9` Working Groups (WGs)*
- `30` New Leaders (Chairs, Tech Leads, Organizers, and Committee Members)
- `14` Emeritus Members of various roles

*Welcome SIG Security and Working Groups: API Expression, Naming, and 
Reliabilty!*

[devstats]: http://k8s.devstats.cncf.io/
[sigs.yaml changes]: https://github.com/kubernetes/community/commits/master/sigs.yaml


## Community Milestones

- `100,000` Issues/pull requests in the `kubernetes/kubernetes` repository 
- `50000` Contributors mark
- `75%`of [API Endpoints included in Conformance]
- `43` Subproject additions or movements
- `35` Stable graduations (KEPs that moved from beta to stable and were 
completed)
- `66` KEPs reviewed by the new Production Readiness Review team

[API Endpoints included in Conformance]: https://apisnoop.cncf.io/conformance-progress?stablechart=percentage

## Governance

At the time of this survey, [all WGs and SIGs] have:

- Up to date READMEs available in the `kubernetes/community` repository
- Up to date group charters 
- Publicly listed meeting times and minutes

[all WGs and SIGs]: https://k8s.dev/groups

## Accolades

The Kubernetes project has achieved major goals and milestones every year. As we
look back, the following accolades paint a picture of our journey in 2020:

### Consistent Feature Graduation to Stable Status

Kubernetes had an issue with features remaining in beta for far
longer than planned. During 2020, many SIGs started driving these long-
standing beta features to completion, and collectively paying down some of their
associated technical debt.

A few features of note that graduated to stable status or made significant
progress include:

- Driving [`CronJobs`] and [`PodDisruptionBudgets`] (SIG Apps)
- [Moving `kubectl` to a staging repo] (SIG CLI)
- [containerd] and [Cluster API support for Windows] (SIG Windows)
- [Ingress API] (SIG Network)

SIG Architecture implemented [a new policy], and this resulted in many SIGs
pushing features to completion. As a result, the project now has less tech debt
and is more stable for end consumers.


[a new policy]: https://kubernetes.io/blog/2020/08/21/moving-forward-from-beta/
[`CronJobs`]: https://git.k8s.io/enhancements/keps/sig-apps/19-Graduate-CronJob-to-Stable
[`PodDisruptionBudgets`]: https://git.k8s.io/enhancements/keps/sig-apps/85-Graduate-PDB-to-Stable
[Moving `kubectl` to a staging repo]: https://git.k8s.io/enhancements/keps/sig-cli/1020-kubectl-staging
[containerd]: https://git.k8s.io/enhancements/keps/keps/sig-windows/1001-windows-cri-containerd
[Cluster API support for Windows]: https://sigs.k8s.io/cluster-api/docs/proposals/20200804-windows-support.md
[Ingress API]: https://git.k8s.io/enhancements/keps/keps/sig-network/1453-ingress-api

### Issue Triage Improvements 

The [kubernetes/kubernetes] repository has over 100,000 issues and pull requests at any time.
To manage this, the community adopted [new triage workflows]. Several SIGs, such
as SIG Node, SIG Network, and SIG API Machinery established their own triage
processes and structure. This resulted in a noticeable reduction in 
[Inactive Issues] and [Inactive Pull Requests] open for 30 days or more.

As SIGs improve their processes with the new workflow, many are having dedicated
triage meetings. Those who have started triage meetings noted they serve as an
excellent engagement point for new contributors.

[kubernetes/kubernetes]: https://github.com/kubernetes/kubernetes
[new triage workflows]: https://git.k8s.io/enhancements/keps/sig-contributor-experience/1553-issue-triage
[Inactive Issues]: https://k8s.devstats.cncf.io/d/77/inactive-issues-by-sig-and-repository?viewPanel=11&orgId=1&from=1577854800000&to=1609390800000
[Inactive Pull Requests]: https://k8s.devstats.cncf.io/d/78/inactive-prs-by-sig-and-repository?viewPanel=11&orgId=1&from=1577854800000&to=1609390800000

### Testing, Continuous Integration, and Scalability

SIG Testing improved the project's testing frameworks and infrastructure. Along
with improvements to scalability tests and other test suites, the Kubernetes
project has experienced significant improvements in CI Signal and general
contributor experience. For example, the [5,000 node] scalability test went from
14 hours to completion to less than 5 hours, roughly 3x faster. The new test
suite and infrastructure is less burdensome on maintainers, ensuring ongoing
project stability.

In addition to the speed improvements, this reduces the compute cost for testing
Kubernetes patches and releases drastically. Thank you to [Google Cloud][credits]
for both [funding][credits] and [staffing] such a critical piece of the project.

[5,000 node]: https://kubernetes.io/docs/setup/best-practices/cluster-large/
[credits]: https://cloud.google.com/blog/products/containers-kubernetes/google-cloud-credits-support-cncf-work-on-kubernetes
[staffing]: https://k8s.devstats.cncf.io/d/8/company-statistics-by-repository-group?orgId=1&var-period=d7&var-metric=contributions&var-repogroup_name=SIG%20Testing&var-repo_name=kubernetes%2Fkubernetes&var-companies=All&from=1577854800000&to=1609390800000

### Localization and Globalization 

The Kubernetes project community is distributed around the world, and there the
end user community is the same. Over the past year, the number of international
contributors has grown, as have initiatives to support localizations of the
project. 

SIG Docs hosts all localizations of the documentation, but each localization
has its own group of maintainers and leads. To manage the growing number of
localizations, SIG Docs started the Localization subproject. Aditionally, SIG
UI added support for several new localizations of the Kubernetes dashboard. 

### Fostering Inclusivity

The Kubernetes [core values] are critical to the success of project.
In 2020 we reinforced our focus on inclusivity by [requiring our community 
leaders]
to further their education on recognizing unconscious bias and working towards
creating a more welcoming environment for every contributor. In addition to
requiring our current leaders to take these steps, it is now a prerequisite for
any future leads before they take a leadership position.

Our talented moderation teams continue to ensure that all our communication
channels are safe and inclusive spaces for our contributor base.

During the Black Lives Matter protests in 2020, the project was introspective in
how it's values intersected with a global movement around equality. We decided
to make a statement about the importance of inclusivity to where the Kubernetes
project is today, and how racism doesn't have a place in our project.

[core values]: https://www.kubernetes.dev/community/values/
[requiring our community leaders]: https://groups.google.com/u/1/g/kubernetes-dev/c/5gRUxPi5XxY/m/1Ollffx4CQAJ

### #shoutouts

A meta accolade.

The #shoutouts channel on the [Kubernetes slack](slack.k8s.io) and highlights
on [@k8scontributors] in the last year has kept us going. Thank a member of the
community here and read the past achievements of many. 

[@k8scontributors]: https://twitter.com/K8sContributors

### Remembering Dan Kohn

In [November of 2020, Dan Kohn], the former director of the CNCF sadly passed
away from complications with Colon Cancer. Dan was instrumental in shaping both
the Kubernetes project, the CNCF, and the Cloud Native community as a whole. He
understood that a foundation built on a vibrant and diverse community was a
requirement to be successful, and the project would not be what it is today
without him. 

[November of 2020, Dan Kohn]: https://kubernetes.io/blog/2020/11/02/remembering-dan-kohn/


## Themes

The following themes emerged from multiple community groups reporting in with 
similar experiences - whether positive or challenging - and areas of research to
explore more in the future. 

### Project Communication Strategy 
  
During periods of significant contributor growth, [community groups were
reporting internally and externally] regularly with the group's members, the 
project at large, and at KubeCons. This made sense as the project scaled ten thousand 
casual and active contributors, but it's resulted in
duplicate meetings and too many update slides. The COVID-19 pandemic and an 
increase in contributors outside of the North America Pacific Timezone made 
regular meetings difficult. Chairs and other project leads asked for a more 
streamline and consistent reporting and feedback mechanism. 
    
#### What We've Done

- Changed [Community Meeting] cadence from weekly to monthly, and changed 
meeting style from a "read out" of updates to more discussion oriented.
- Encouraged groups to use asychronous methods for delivering updates and 
gathering feedback. For example: Slack "standup" theads which feed into larger 
scale reporting to a group on a mailing list.
- Created an internal marketing group under SIG Contributor Experience to help
  facilitate community communication.


[Community Meeting]: https://k8s.dev/events/community-meeting/
[community groups were reporting internally and externally]: https://git.k8s.io/community/committee-steering/governance/sig-governance.md
[Governance requirements]: https://git.k8s.io/community/committee-steering/governance/sig-governance.md#chair
    
#### Areas of Research 

- Review SIG charters to re-focus goals of each group at the current state of
  maturity
- Expand on async meeting adoption and establish best practices 
- Improving subproject communication and connective glue back to the sponsoring
  SIG
- Clarify conditions for archiving or putting a subproject in maintenance mode
- Connecting with the end user community and understanding what they want to
  hear from upstream
  
    
### Refining the Contributor Lifecycle

There are a number of ways to define membership to the Kubernetes project
and its community groups. The project's community groups must define
their own membership terms and any other roles within their group.

Membership drives:

- Kubernetes GitHub Organization membership 
- Consensus 
- Voting

The project defines [membership] as contributors added to to one of the four GitHub 
organizations. Membership grants a contributor access to test their pull 
requests, among other benefits. Membership also defines a member's role within 
the project based on their place on the [Contributor Ladder][ldr]. Membership 
does not grant voting rights for Steering Committee and governance matters; 
there is a separate set of criteria for [elections].

These are guidelines for the project as a whole but do not translate to SIG or
WG based membership, with each group defining membership in their own way.
These methods vary widely and are often founded in the group's specific
workflows. However, there is a common pattern throughout all of them, and that
is the two types of members that are considered early membership (onboarding)
and sustainable membership (ongoing contributor activity).

**Voting and Consensus with Members**

Voting typically doesn't happen in the project unless it's for a Committee role.
Technical and nontechnical decisions are driven mostly by 
consensus of the maintainers in OWNERs files in the code, doc, or policy area of
maintenance. However, in some cases, particularly SIG leadership transitions, 
there have been cases were voting was elected but defining membership and 
reaching out to those members outside of GitHub is difficult. 

#### What we've done

**Sustainable Membership**

While onboarding new contributors is a critical part of a sustainable open
source project, contributors shift focus, change jobs, or
step away from the project for a variety of other reasons. In late 2019, 
Steering Committee updated the project's guidelines to introduce an [emeritus status]. 
Emeritus community members have stepped away from the project, but are still 
recognized for their work. Giving people the ability to step away gracefully 
helps ensure an overall healthy and active community.

In 2020, 185 members stepped down or were removed for inactivity (18
months with 0 activity across any GitHub organization). The Kubernetes project 
has around 1300 active members at any given time.   

[elections]: https://github.com/kubernetes/steering/blob/master/elections.md#eligibility-for-voting
[membership]: https://git.k8s.io/community/community-membership.md#member
[emeritus status]: https://k8s.dev/docs/guide/owners/#emeritus
[achievement for climbing the ladder]: https://github.com/kubernetes/test-infra/issues/11994
[charter process]: https://github.com/kubernetes/community/blob/master/committee-steering/governance/sig-charter-template.md


#### Areas of Research

- Automation around suggesting when contributors may be ready to move to the
  next step in the lifecycle
- Ways to promote a sustainable flow through the various stages of the lifecycle
- Clarifying and/or simplifying definitions around the stages of the lifecycle
- Prompts to assist contributors in knowing what they need to do to 'level up'
  to the next stage in the lifecycle (e.g. prompts when you join a mailing list)
- Joining the project's GitHub organizations is celebrated, but
there are no regular means of celebration or recognition for those that join a
SIG, community group, or [achievement for climbing the ladder].


### Growing a Diverse Group of OWNERs

Moving up the contributor ladder – from contributor, to reviewer, to approver – involves work 
on the part of the contributor. Building trust is a key part of our values and is a
step in the "contributor journey", called the Kubernetes [contributor
ladder][ldr]. 

The Kubernetes project needs more diverse, trusted people from all backgrounds to grow
as contributors. Balancing being welcoming and identifying contributors to
encourage to stick around at scale is difficult, especially with tens of
thousands of casual contributors, and many cultures that come
together. 30 new leaders have stepped up to Chair and other roles in 2020, but
bandwidth for the reviewers and approvers in many subprojects remains a
challenge as does the diversity of those contributing.

#### What We've Done

- Applied consistent labeling of issues with `good-first-issue` and 
`help-wanted`. This was reported as the most successful way of landing new 
contributors.
- Intentionally creating space at meetings for new contributors to get involved
  and/or a dedicated triage meeting that provide an overview of current 
  priorities
- Continued programs such as:
    - [Meet Our Contributors], an Office hours like space where aspiring and 
    experienced contributors can ask questions live
    - Contributor Summits with new contibutor workshops, or Maintainer focused 
    sessions at KubeCon.
- Facilitated One-on-One sessions for dedicated contributors that have 
demonstrated a vested interest in contributing and climbing the contributor 
ladder and sticking around.
- Created Group study groups for reviewers, approvers, and Chairs


[Meet Our Contributors]: https://www.kubernetes.dev/events/meet-our-contributors/


#### Areas of Research

- Specific outreach to new contributors from backgrounds that are
  underrepresented in the community, such as BIPOC contributors
- GitHub automation that will suggest contributors to SIG leadership who are 
making steady contributions to the project that may not have visibility, direct
access to OWNERs, or may feel ackward asking about maintainership
- Encouraging regular review of who is actively reviewing in subprojects
- Scaling the [group contributor ladder program]


[group contributor ladder program]: https://git.k8s.io/community/mentoring/programs

## Growth Areas

### Focus on Reliability

The community is excited to welcome the new lens on reliability through
Production Readiness Reviews, KEPs, and the new Working Group for Reliability.
This effort continues to increase confidence for end users use Kubernetes to
manage production workloads by ensuring the core is stable and reliable.  

This means the features are:  

- Observable: you can tell that it is in use and working properly, and are
  able to define reasonable service level objectives for the feature.
- Supportable: the feature is well documented with a playbook covering failure
  modes, dependencies and what happens when those fail or degrade, and a
  troubleshooting guide.
- Scalable: the feature does not introduce scaling issues.
- Recoverable: the feature can be disabled or rolled back easily and without
  data loss
        
### The Words We Use

The Naming Working Group was spun up to undergo research and create decision
making frameworks around the terminology we use in the technical components and
the documentation.


GitHub has also stepped up to help the open source community at large create a
smooth path for `master->main` branch renaming. We discovered some gaps in our
tooling and automation around this as well, but now have a [clear path]. A
number of repos have already started this migration, and we will continue to 
roll
it out to the remainder of the org.
   

Not only is this a WG Naming initiative, but several parts of the project 
reported in ways they are examining the words we use. For example, SIG 
Contributor Experience's slack-infra team implemented a [new bot] for inclusive 
language. SIG Testing has made a significant effort to eliminate [`blacklist`] 
from the code base.
   
There is still plenty of work however in evaluating further language,
implementing changes to code and documentation, as well as the testing and
validation that related code changes don't introduce unexpected regressions.
  
[new bot]: https://sigs.k8s.io/slack-infra/slack-moderator-words
[clear path]: https://www.kubernetes.dev/resources/rename/
[`blacklist`]: https://github.com/kubernetes/community/pull/5341


### All eyes on SECURITY.md

This year brought the creation of [SIG Security], in response to the greater
community and industry focus on the security of critical pieces of software
like Kubernetes. This new SIG grew out of the previous Security Audit Working
Group, and is designed to be a clear home for security-focused discussions
across the project.

This new group, partnering with the existing Product Security Committee, will
focus on horizontal security initiatives for the Kubernetes project, including
regular security audits, the vulnerability management process, cross-cutting
security documentation, and security community management.

The Product Security Committee is also currently discussing a
[name change to "Security Response Committee"] to better reflect the role they
play in security response.

[SIG Security]: https://git.k8s.io/community/sig-security/charter.md
[name change to "Security Response Committee"]: https://github.com/kubernetes/community/pull/5597


### Improving Kubernetes Enhancements

Kubernetes Enhancement Proosals, the process by which the community proposes and
 approves new features, continues to evolve and mature. As we use and iterate on
  the process, we are consistently learning better ways to communicate, debate, 
  and ultimately grow ideas within the project.

In 2020, KEPs around process and policies have become a focus, and an area of 
future growth for KEPs themselves. For example, a KEP changing the 
[release cadence] of the Kubernetes project garnered attention from the 
community.

[release cadence]: https://git.k8s.io/enhancements/keps/sig-release/2572-release-cadence

## /help-wanted

The community groups report that they need to grow more contributors into 
maintainer-like roles of Reviewers, Approvers, and Subproject OWNERs. 

Below is list of specific contribution needs, special projects, roles available,
and more. Building trust is key and we need folks to stick around. There are
other ways of contributing outside of commits and you'll see those in the
[Other Types of Upstream Contributions] section.

Check out the contributor guide for a comprehensive guide to getting started:
https://k8s.dev/guide.

[Other types of upstream contributions]: #Other-types-of-upstream-contributions

**SIG API Machinery**:
- Performing triage (go to a triage meeting and you'll see it first hand)
- Contributors to the Client Libraries like client-go, python-client

**SIG Architecture**:
- Site Reliability Engineers to review KEPs, Production Readiness Reviews,
  and API Reviewers
- Contributors to help curate a mentoring program for people to work across SIGs

**SIG Auth**:
- Audit logging and testing contributors
- KMS-Plugin contributors

**SIG Autoscaling**:
- Creating and running of a triage program

**SIG CLI**:
- A Product/Feature Manager

**SIG Cloud Provider**:
- More contributors from every cloud to form teams for triage and support, 
- Cloud Engineers at service providers to help run the cloud provider extraction
 working group:
  kubernetes/kubernetes "cluster" directory and resolving how we properly test
  kubernetes/kubernetes in the absence of a cloud provider

**SIG Cluster Lifecycle**:
Code contributors to:  
- Etcdadm
- Cluster-addons
- Kubeadm  

**SIG Contributor Experience**: 
- Full-time (or part-time) community managers 
- Automation Engineers: zoom to youtube automation, github automation, slack
  infrastructure, and more
- Program Manager types for recognition and contributor ladder mentoring 
programs

**SIG Instrumentation**:
- Structured logging
- promq contributors

**SIG Node**:
- Sustaining CI

**SIG Scalability**:
- Scalability Test Frameworks and Scalability and Performance tests and
  validation with a deep understanding of Kubernetes 

**SIG Scheduling**:
- Docs for scheduler internals, cluster-admin best practices; standardize triage
  process

**SIG Security**:
- Future Tech Leads

**SIG Storage**:
- Reviewers
- Issue triage (creating and running a program)
- Feature work for things that are co-owned by sig-node, sig-apps, and 
sig-scheduling (ContainerNotifier, Volume expansion for stateful set, and more)

**SIG Testing**:
- Many more companies to invest in this area heavily and bring steady 
contributors to grow the contributor ladder in areas that are crucial to the 
projects infrastructure

**SIG UI**:
- Contributors who will stick around with AngularJS, golang, and knowledge of
  Kubernetes client-go package

**SIG Usability**:
- We are currently working on a jobs to be done study and an effort to define
  universal personas for the upstream project. 
- Any one is welcome to join and participate in these efforts, especially any 
user researchers, designers, and new contributors

**SIG Windows**: 
- e2e test coverage and API reviewers

**WG K8s Infra**
- Help with migrating resources from Google owned infrastructure to community 
owned 
- At the time of this report, only 288 of the current 1780 prow jobs have 
been migrated

**WG Multitenancy** 
- We have three main projects: Hierarchical Namespace, Virtual Cluster Project,
  and Multi-tenancy Profiles (think conformancy but for secure multi-tenant
  clusters). Contributors and interested parties welcome! 

### Other Types of Upstream Contributions

The above list is good for contributors who have the time or
support from their employer to submit patches and participate in other upstream activities. 
Below are areas of the project that need help but require less dedicated time.

- Comment on [KEPs][kep] with your use case (this is helpful from end users
  too!)
- Tag `sig/security` on issues and pull requests that you review and have security
  concerns
- [SIG Multicluster] needs use cases and validating our approaches for different
  environments and deployment models 
- [SIG Usability] would like more participants for their [Job Study] and many
  other studies that are going on.
- [SIG Contributor Experience] would welcome part-time and full time contributor
  community managers; will mentor and grow dedicated contributors in a large
  environment
- [SIG Architecture] would like cluster operators to take a 
[production readiness survey]


[SIG Multicluster]: https://git.k8s.io/community/sig-multicluster
[SIG Usability]: https://git.k8s.io/community/sig-usability
[Job Study]: https://docs.google.com/document/d/1lkPQdBEw-Xb5GEZ48WnpBgQdZ01EmTBhjcxJBlu5qJs/edit#heading=h.xsg4f6e6yk0p
[SIG Contributor Experience]: https://git.k8s.io/community/sig-contributor-experience
[SIG Architecture]: https://git.k8s.io/community/sig-architecture
[production readiness survey]: https://docs.google.com/forms/d/e/1FAIpQLSc-J-Ydu5vp5G9vdvV5gBcraEDN_Bl-HSkVm15vAlU_orDvoA/viewform

## Current Initiatives 

This section summarizes current initiatives from each SIG and WG. Click on the 
group for reported projects completed in 2020 and granular information for each 
initiative with supporting links to KEPs and more. 

- [SIG API-Machinery](https://git.k8s.io/community/sig-api-machinery/annual-report-2020.md#current-initiatives-and-project-health)
    - Mitigating the impact of removing beta APIs in 1.22
    - Server-side-apply to stable
    - Server-side-apply client
    - Optionally skip backend TLS verification
    - Namespace labels
    - CRD and admission webhook v1beta1 API removal: reminder on kubernetes-dev.
    - Immutable fields API
    - API unions
    - Warnings to stable
    - apiserver network proxy to beta
    - Priority and fairness to stable

- [SIG Apps](https://git.k8s.io/community/sig-apps/annual-report-2020.md#current-initiatives-and-project-health)
    - Promoting CronJobs to GA
    - Promoting PodDisruptionBudgets to GA

- [SIG Architecture](https://git.k8s.io/community/sig-architecture/annual-report-2020.md#current-initiatives-and-project-health)
    - Increased coverage of stable endpoints by conformance tests
    - Coordinating dependency updates across projects
    - Production Readiness Review process was made mandatory in 1.21, improving 
    scalability, supportability, monitoring, and correct feature enablement
    - Set up cross-project policies to move features towards stable ([conformance without beta](https://git.k8s.io/enhancements/keps/sig-architecture/1333-conformance-without-beta), [preventing "permabeta"](https://git.k8s.io/enhancements/keps/sig-architecture/1635-prevent-permabeta))
    - Enhancements subproject is working with sig-release to assist SIGs in 
    taking greater ownership of their KEPs during the release cycle

- [SIG Auth](https://git.k8s.io/community/sig-auth/annual-report-2020.md#current-initiatives-and-project-health)
    - BoundServiceAccountToken
    - CSR v1
    - Token Request / bound SA token admission
    - client-go auth plugins
    - external kubelet credential providers
    - New features in Secrets Store CSI driver
    - Pod Security Policy Replacement
    - Several other KEPs going to General Availability on the report

- [SIG Autoscaling](https://git.k8s.io/community/sig-autoscaling/annual-report-2020.md#current-initiatives-and-project-health)
    - Promoting HPA v2 to stable
    - Promoting HPAScaleToZero to beta
    - Vertical pod autoscaler adding support for customized recommenders
    - Cluster autoscaler adding support for gRPC custom cloud providers
 
- [SIG CLI](https://git.k8s.io/community/sig-cli/annual-report-2020.md#current-initiatives-and-project-health)
    - Moving kubectl package code to staging
    - Our multi-year effort to split out of the main kubernetes repository.
    - kubectl debug (beta)
    - Several smaller efforts to unify code across all the commands, and 
    removing technical debt

- [SIG Cloud Provider](https://git.k8s.io/community/sig-cloud-provider/annual-report-2020.md#current-initiatives-and-project-health)
    - Feature: implement the BackendManager list
    - Fix flag passing in CCM
    - Extending Apiserver Network Proxy to handle traffic originated from Node 
    network

- [SIG Cluster Lifecycle](https://git.k8s.io/community/sig-cluster-lifecycle/annual-report-2020.md#current-initiatives-and-project-health)
    - Standard for communicating a local registry
    - Several KEPs in a separate KEP process https://github.com/kubernetes-sigs/cluster-api/tree/master/docs/proposals

- [SIG Contributor Experience](https://git.k8s.io/community/sig-contributor-experience/annual-report-2020.md#current-initiatives-and-project-health)
  - Community Management
  - Contributor Documentation
  - Contributor Comms
  - Devstats
  - Events
  - GitHub Management
  - Mentoring
  - Slack Infra 
  - KEP for revamping the prow approval plugin
  - Migrating the default branch on GitHub from master to main

- [SIG Docs](https://git.k8s.io/community/sig-docs/annual-report-2020.md#current-initiatives-and-project-health)
    - Coordination with WG naming for things like removing the word “slave” 
    (and other problematic terms) from docs
    - Publishing better information about releases
    - Docsy theme work as well as the reference documentation generation
    - Doc policies for third party content

- [SIG Instrumentation](https://git.k8s.io/community/sig-instrumentation/annual-report-2020.md#current-initiatives-and-project-health)
    - Reducing metrics exposed by the kubelet
    - Tracing
    - Structured Logging
    - and many other KEPs listed in the report

- [SIG Multicluster](https://git.k8s.io/community/sig-multicluster/annual-report-2020.md#current-initiatives-and-project-health)
    - Cluster ID for ClusterSet identification 
    - Multi Cluster Services API
    - Kubefed - support for pull-based reconciliation 
    - Work API - road to alpha

- [SIG Network](https://git.k8s.io/community/sig-network/annual-report-2020.md#current-initiatives-and-project-health)
    - No report

- [SIG Node](https://git.k8s.io/community/sig-node/annual-report-2020.md#current-initiatives-and-project-health)
    - cgroups v2
    - Topology manager/device alignment 
    - Many KEPs listed in their report

- [SIG Release](https://git.k8s.io/community/sig-release/annual-report-2020.md#current-initiatives-and-project-health)
    - Release cadence 
    - North Star Vision Roadmap
    - Enhancing tooling
    - New Program Manager role

- [SIG Scalability](https://git.k8s.io/community/sig-scalability/annual-report-2020.md#current-initiatives-and-project-health)
    - Reduced time for 5k scalability tests from 14 hours to < 5 hours
    - Improved testing frameworks and extended scalability test coverage 
    - [Efficient Watch Resumption](https://github.com/kubernetes/enhancements/issues/1904)
    - [Immutable Secrets and ConfigMaps](https://github.com/kubernetes/enhancements/issues/1412)

- [SIG Scheduling](https://git.k8s.io/community/sig-scheduling/annual-report-2020.md#current-initiatives-and-project-health)
    - Continuing to refactor the core code around the scheduling framework
    - Graduating the scheduler's ComponentConfig to stable
    - Scheduler into a pluggable framework outside of the main repo
    - More alpha and beta features listed in the report

- [SIG Security](https://git.k8s.io/community/sig-security/annual-report-2020.md#current-initiatives-and-project-health)
    - Kubernetes Hardening Guide
    - Third Party Security Audit
    - PodSecurityPolicy replacement: PodSecurity admission 
    - Support for Windows privileged containers
    - Run control-plane as non-root in kubeadm
    - Defend against logging secrets via static analysis
    - More KEPs listed in their report

- SIG Service Catalog
    - No report

- [SIG Storage](https://git.k8s.io/community/sig-storage/annual-report-2020.md#current-initiatives-and-project-health)
    - Container Object Storage Interface
    - Generic Ephemeral Volumes
    - CSI Support for Windows
    - Volume Snapshots stable
    - and other beta, alpha, road to alpha, and stable KEPs listed in the report

- SIG Testing
    - No report

- [SIG UI](https://git.k8s.io/community/sig-ui/annual-report-2020.md#current-initiatives-and-project-health)
    - Ongoing maintenance 
    - Real time dashboard
    - New language translations

- [SIG Usability](https://git.k8s.io/community/sig-usability/annual-report-2020.md#current-initiatives-and-project-health)
    - Jobs-to-be-done research proposal 

- [SIG Windows](https://git.k8s.io/community/sig-windows/annual-report-2020.md#current-initiatives-and-project-health)
    - Privileged containers
    - Network Policy Support

- [WG API Expression](https://git.k8s.io/community/wg-api-expression/annual-report-2020.md#current-initiatives-and-project-health)
    - Server Side Apply landing stable in 1.21; will complete the groups mission

- WG Component Standard
    - n/a

- [WG Data Protection](https://git.k8s.io/community/wg-data-protection/annual-report-2020.md#current-initiatives-and-project-health)
    - Volume Backups
    - Backup Repositories
    - Data Populator
    - Quiesce and Unquiesce Hooks
    - CBT
    - Volume Group and Group Snapshot
    - Application Snapshots and Backups

- WG IoT/Edge
    - n/a

- [WG K8s Infra](https://git.k8s.io/community/wg-k8s-infra/annual-report-2020.md#current-initiatives-and-project-health)
    - Ensure SIG ownership of all infra and services
    - Migrate .deb/.rpm package building/hosting to community
    - stop using google-containers, k8s-prow, k8s-prow-build, k8s-gubernator, kubernetes-jenkins,  GCP project
    - Migrate images used by CI jobs and test-infra components

- [WG Multitenancy](https://git.k8s.io/community/wg-multitenancy/annual-report-2020.md#current-initiatives-and-project-health)
    - [Multi-Tenancy Benchmarks](https://sigs.k8s.io/multi-tenancy/benchmarks)
    - [Virtual Cluster Project](https://sigs.k8s.io/multi-tenancy/incubator/virtualcluster)
    - [Hierarchical Namespace Controller](https://sigs.k8s.io/multi-tenancy/incubator/hnc)


## Appendices


## Appendix A: Program documentation 

[Program Documentation](https://git.k8s.io/community/committee-steering/governance/annual-reports.md)

## Appendix B: Survey questions 

Operational

* How are you doing with operational tasks in SIG-governance.md?
* Is your README accurate? have a CONTRIBUTING.md file?
* All subprojects correctly mapped and listed in sigs.yaml?
* What’s your meeting culture? Large/small, active/quiet, learnings? Meeting 
notes up to date? Are you keeping recordings up to date/trends in community 
members watching recordings?
* How does the group get updates, reports, or feedback from subprojects? Are 
there any springing up or being retired? Are OWNERS.md files up to date in these
 areas?
* Same question as above but for working groups.
* When was your last public community-wide update? (provide link to deck and/or 
recording)

Membership
  
* Are all listed SIG leaders (chairs, tech leads, and subproject owners) active?
* How do you measure membership? By mailing list members, OWNERs, or something 
else?
* How does the group measure reviewer and approver bandwidth? Do you need help 
in any area now? What are you doing about it?
* Is there a healthy onboarding and growth path for contributors in your SIG? 
What are some activities that the group does to encourage this? What programs 
are you participating in to grow contributors throughout the contributor ladder?
* What programs do you participate in for new contributors?
* Does the group have contributors from multiple companies/affiliations? Can end
 users/companies contribute in some way that they currently are not?

Current initiatives and project health
  
* What are some initiatives that should be highlighted, lauded, shoutouts, that 
your group is proud of? Currently underway? What are some of the longer tail 
 projects that your group is working on?
* Year to date KEP work: What's now stable? Beta? Alpha? Road to alpha?
* What initiatives are you working on that aren't being tracked in KEPs?
* What areas and/or subprojects does the group need the most help with?
* What metrics/community health stats does your group care about and/or measure?
 Examples?



<!-- common shared links -->

[ldr]: https://git.k8s.io/community/community-membership.md
[kep]: http://git.k8s.io/enhancements/#is-my-thing-an-enhancement
