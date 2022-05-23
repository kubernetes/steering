## Annual Report summary 21/22

This is a summary of the Kubernetes project’s contributor community and
activities. This report documents both quantitative measures of community
health (project milestones and snapshot) as well as qualitative measures of the
community as reported by community leaders and contributors to the project.


## Terminology

This report uses the following terminology:

- **Special Interest Group (SIG):** a body of contributors, responsible on an
  ongoing basis for an area of work in the Kubernetes project. They own code,
  docs, and/or policy.
- **Working Group (WG):** a body of contributors, responsible for an area of work
  in the project. Unlike SIGs, WGs dissolve once the scoped work is complete.
  Working groups are cross-functional efforts sponsored by a SIG.
- **Community Groups:** all of our official groups of the upstream project. Special
  Interest Groups + Working Groups + Committees = community groups. For a full
  list, visit the Kubernetes Contributor Site at: https://k8s.dev/groups 
- **Chair and/or Tech Lead:** a contributor who organizes and leads a community group.
- **KEP:** a [Kubernetes Enhancement Proposal][kep]
- **OWNER:** a GitHub user who reviews, approves, and/or merges commits and is listed in an
  [`OWNERS` file]. Maintainer is a good industry synonym.
- **Contributor Ladder:** [member, reviewer, approver, subproject owner].


For the community group mailing list, meeting times, and other contact info visit:
https://k8s.dev/groups


For community groups governance:
  - [SIG governance]
  - [WG governance]


[`OWNERS` file]: https://www.kubernetes.dev/docs/guide/owners/
[member, reviewer, approver, subproject owner]: https://git.k8s.io/community/community-membership.md
[SIG governance]: https://git.k8s.io/community/committee-steering/governance/sig-governance.md
[WG governance]: https://git.k8s.io/community/committee-steering/governance/wg-governance.md


## Data collection

The Kubernetes Steering Committee sent out a survey to all community group
leads to collect data for this report. Each individual group report may be
found in their respective directory inside the [Kubernetes Community repo].

For more, see:
[Program Documentation]

[Program Documentation]: https://github.com/kubernetes/community/blob/master/committee-steering/governance/annual-reports.md

## Contributor snapshot

66000 
contributors all time
TODO: add a contributors for the year

1 
new sig SIG K8s Infra, converted from WG

3 
emeritus leads 
TODO: we need the stat for OWNERs 

1 
new working group

5 
new chairs and tech leads 

10 or less 
unique reviewers in 8 groups

8.29 
average active meeting participants in each group

~70000 
slack members in SIG/WG rooms


[Kubernetes Community repo]: https://github.com/kubernetes/community


### Accolades

On behalf of the project, we'd like to say thanks to the following contributors,
community groups, and ecosystem for the following highlights. As always, give
praise to an effort in `#shoutouts` on Kubernetes slack.


#### Feature Maturity and Stability

Thanks to our groups for continuing the efforts from 2020, many SIGs continue
to drive long standing beta features to graduate to stable.

Several features that graduated to stable or made notable progress include:
- [CSI Plugins on Windows Nodes] graduated to stable in v1.22 (SIG Windows)
- [Generic ephemeral inline volumes] graduated to stable in v1.23 (SIG
  Storage)
- [IPv4/IPv6 dual-stack] graduated to stable in v1.23 (SIG Network)
- [Metrics stability framework] graduated to stable in v1.21 (SIG
  Instrumentation)
- [Server-side Apply] graduated to stable in v1.22 (SIG API Machinery)
- [Client credential plugins] graduated to stable in v1.22 (SIG Auth)
- [Kubetest2] is maturing (SIG Testing)
- [CSI migration] has been an effort that has been going on for several releases.
  It involves SIG Storage, SIG Cloud Provider, and contributors across many
  cloud providers and storage vendors to work together and move in-tree volume
  plugins to out-of-tree CSI drivers.

Other project processes are maturing, too, and not just the code. A new way to
cast votes in elections (like Steering Committee and more) runs via [Elekto].
The [Kubernetes Monthly Community meeting] was rebooted to include discussions
and not just presentations.

[CSI Plugins on Windows Nodes]: https://git.k8s.io/enhancements/keps/sig-windows/1122-windows-csi-support
[Generic ephemeral inline volumes]: https://git.k8s.io/enhancements/keps/sig-storage/1698-generic-ephemeral-volumes
[IPv4/IPv6 dual-stack]: https://git.k8s.io/enhancements/keps/sig-network/563-dual-stack
[kubetest2]: https://git.k8s.io/enhancements/keps/sig-testing/2464-kubetest2-ci-migration
[Metrics stability framework]: https://git.k8s.io/enhancements/keps/sig-instrumentation/1209-metrics-stability
[CSI migration]: https://kubernetes.io/blog/2021/12/10/storage-in-tree-to-csi-migration-status-update/
[Client credential plugins]: https://kubernetes.io/docs/reference/access-authn-authz/authentication/#client-go-credential-plugins
[Server-side Apply]: https://kubernetes.io/docs/reference/using-api/server-side-apply/
[Elekto]: https://elekto.dev/
[Kubernetes Monthly Community meeting]: https://youtube.com/playlist?list=PL69nYSiGNLP1pkHsbPjzAewvMgGUpkCnJ


#### Showing up and sticking around 

Climbing the contributor ladder is a trust-building exercise as much as it is
a skills one. Sticking around, chopping wood, and carrying water is the main
formula for growing OWNERs and leaders on the project.

An example of an intentional contributor ladder growth effort happened in SIG 
Docs by growing its contributor and reviewer base in 2021. They introduced a 
shadow program for PR Wrangling and dedicated more time to being active in 
the `#sig-docs` Slack channel, helping grow the community. SIG Docs also worked on
a leadership transition strategy to bring community members into leadership 
roles via a specialized six-month group mentorship program. They were able to 
cultivate leaders for the SIG and some of its subgroups, adding new co-chairs 
and tech leads.

SIG CLI deserves another great shoutout for having long-standing Chairs and
Tech Leads take the emeritus route while growing new leaders into the roles.
Thanks for your service and great job, team!


#### Amping up Kubernetes security

Every group in Kubernetes has a responsibility to make sure we are putting
our best foot forward with supply chain security. Accolades to all of
SIG Release, SIG Auth, and SIG Security for their sustained efforts in this
area that include: 
- generating SBOMs, 
- compliance with [SLSA 3 standards](https://slsa.dev), 
- artifact signing,
- rearchitecting release process from bash to Go,
- and adding new features, tests and checks to the release process - these were 
  missing from the original anago tooling (binary verification, CVE disclosure, building 
  from custom branches and repositories).

Alongside those improvements specifically to supply-chain security, we've seen:

- improvements to end-user security documentation.
- Pod credentials are auto-revoked when pods complete or are deleted (1.22+)
- CSI drivers can use pod-scoped credentials using [Service Account Token for CSI Driver] (1.22+)
- Certificates can be requested with shorter lifetimes (1.22+)
- Pods can listen on low ports without requiring a root user or expanded capabilities (1.22+)
- [Pod Security admission] has graduated to beta and is enabled by default (1.23+)
  
[Pod Security admission]: https://kubernetes.io/docs/concepts/security/pod-security-admission/
[`CSIServiceAccountToken`]: https://git.k8s.io/enhancements/keps/sig-storage/1855-csi-driver-service-account-token

#### Things that no longer spark joy

There are plenty of processes, tools, and policy that are put 
together in a project lifecycle that eventually need to be phased 
out for whatever reason. A contributor painpoint that we've had with 
a codebase this large is [bazel]. The crews in SIG Testing and 
SIG Release put in a lot of time and attention on removing bazel
from kubernetes/kubernetes. There are some pieces left in 
kubernetes/test-infra but needless to say, we are on the road to 
moving on in our build processes.  

[bazel]: https://github.com/kubernetes/enhancements/issues/2420

#### Growing Windows support 

Thanks to the SIG Windows team and surrounding groups for their efforts 
in growing the support in this space! A true testament to the power of the 
ecosystem. They have more upcoming work to do and we are looking forward 
to seeing their growth in 2022 and beyond. 

Details:
- Implemented hostProcess container support in Kubernetes (now in beta) and
pomoted adoption in multiple open source communities
- Defined the kubectl subcommand for fetching node-level logs.
- Made the developer UX for windows transparent with sig-windows-dev-tools.
- Defined windows operational readiness standards.
- Defined the pod OS field.



### Themes / Trends 


#### Prioritizing Quality

The project saw an increase in regression-related backports in the two most
recent releases (1.22 and 1.23). Many of these regressions were related to a
couple types of changes:
- Changes to add features or fix unrelated bugs in areas that are complex
  and undertested
- Changes that were intended to be mechanical refactors that accidentally
  modified behavior


##### What have we done?

Adjustments are being made in several areas throughout the release cycle to
reverse this trend:
- Encouraging SIG and component leads to
  [track and consider the health of existing code/components] when planning
  and accepting new feature proposals.
- Guiding proposal authors to [provide more specific test plans], and reminding
  them that stabilizing or improving the existing health of the area they want
  to change may be required before their proposal can proceed.
- Clarifying the standards [reviewers and approvers should apply] during
  implementation.
- Improving test signal by cleaning up unowned or permanently failing CI jobs,
  to give better visibility to test flakes or failures introduced during a
  development cycle.
- Adjusting release schedules to ensure time for at least two release candidate
  builds, and giving time for feedback on those builds. Thanks to reports from
  users testing pre-release builds, regressions were fixed before both the
  1.23.0 and 1.24.0 releases!


[track and consider the health of existing code/components]: https://youtu.be/32Sm2bHNnCI
[provide more specific test plans]: https://github.com/kubernetes/enhancements/blob/278a3169457576fcf8ede27df2b2f1902eeea2a1/keps/NNNN-kep-template/README.md?plain=1#L270-L328
[reviewers and approvers should apply]: https://groups.google.com/a/kubernetes.io/g/dev/c/6F3h0Z1QzVg


#### Independent contributors play a critical role on the project

A misconception is that this project is just cloud providers maintaining it;
however, one of our biggest contributor bases are "[independent]" that is, not
affliated with an organization. 

There is space for everyone here. 


[independent]: https://k8s.devstats.cncf.io/d/8/company-statistics-by-repository-group?orgId=1&from=1609480800000&to=1641016800000&viewPanel=1&var-period=d7&var-metric=committers&var-repogroup_name=All&var-repo_name=kubernetes%2Fkubernetes&var-companies=All


##### What have we done?

Connect folks to jobs! While not all indie contributors are looking for
employment, many are. This year we worked with CNCF to add a feature to the
[cncf.jobs.io site], which allows employers to indicate a percentage of time
that they would support upstream activities. The Kubernetes project needs more
contributors with employer-backed time, and this was a great step toward that
goal. Aligning contributors with the right incentives is the sweet spot for
lasting contributions. 

[jobs.cncf.io site]: https://jobs.cncf.io


##### Areas to research?

As part of upcoming surveys, we will poll the indpedenet contributors on various
topics and how we can support them more. As always, we welcome feedback via
[SIG Contributor Experience] or for high level governance matters, the
[Steering Committee].

[SIG Contributor Exerperience]:https://git.k8s.io/community/sig-contributor-experience#contact
[Steering Committee]: https://git.k8s.io/community/committee-steering#contact


#### Niche contributor documentation /help-wanted

With one of the largest decentralized distributed open-source projects out
there, expect our contribution guides to be in-depth and extensive.
[k8s.dev/guide] is our primary guide; no matter where you contribute to the
project, you start there. But because the project is so large, some groups have
other style guides, code review processes, and more that define how they do
business and operationalize. This is an important part of our [values]. Same 
thing at big employers: everyone gets the standard onboarding docs, but 
your department might have an additional "here's how to get work done" 
document floating around. 

Many of our groups reported in that they have a hard time keeping [this
information] up to date, if they even have this kind of documentation at all. This 
is a great way to get involved if you are new to a group! Want to become an OWNER? 
Set someone up for success behind you by creating documentation for your area.

[k8s.dev/guide]: https://k8s.dev/guide
[this information]: https://github.com/kubernetes/community/tree/master/contributors/devel


#### What have we done?

In late 2020, SIG Leads were tasked with [auditing] their area specific
documentation, with many removing out-dated information and creating follow-up
items calling out things things that should be documented. These audits made it
easy for companies to bring on Tech Writers to help shore up this needed
documentation.

Additional processes have been put in place, such as a documentation review as
part of the annual report process should ensure that project contributing docs
remain (relatively) up-to-date.


[auditing]: https://github.com/kubernetes/community/issues/5229


#### Areas to research 

Updating documentation is usually a good onboarding path for interns and 
new contributors but this can get murky with some of the complexities of
the code and doc set. It can take up to 3 months to onboard on to the project
before suggestion and submitting changes. Is there a program that SIGs could
create as an onboarding path towards OWNERship here? 



#### Burnout 

The topics of burnout and workload management are frequent in our Leads and 
group meetings, Steering Committee, and even the growing voices at ecosystem
level during talks and events at KubeCon/CloudNativeCons. This is an industry
wide problem that we need to solve together. With a mix of reasons why 
contributors are burning out, there is no one solve all solution here. 
Aligning incentives to grow OWNERs seems to be one of the main challenges in 
this space. 

#### What have we done
- Reducing the release cadence. While this wasn't the only reason for having 
3 and not 4 releases in a year, 





### Growth Areas

This section represents an area of the project that we've identified as having a growth opportunity or need.



#### What's project health anyway?

Some of the more mature groups like SIG Instrumentation or those with industry
open-source veterans can quickly identify areas of their components that need
help and tell stories about what's flourishing. Yet, it can be challenging to
establish universal indicators of "project health" in a project as large and
diverse as Kubernetes. We need to develop these indicators to provide signal to
the leads so that they may detect, pre-empt, or bubble up this information to
keep their area healthy.


#### Every group needs more reviewers

If you've been watching open source news over the last year, supply chain security has made headlines. According to OpenSSF and other security groups, [insert line about reviewers are important] 
Reviewers are a key part of our success in quality code and documentation changes upstream. Reviewer is the next step on our [contributor ladder](https://github.com/kubernetes/community/blob/master/community-membership.md) post member 
- talk about showing up and sticking around
- talk about chopping wood and carrying water first 
- maybe include the reviewer graph stats 


#### The 9 to 5 contributor is almost over and we have to adjust

Only a handful of our OWNERs, some of our most active contributors, will tell
you that they work 80-100% upstream. These folks know the codebase and docs
extensively and are some of our most experienced reviewer eyes. But anecdotally,
the number of experienced and very active core folks able to contribute has
decreased in recent years. Ensuring continuity and growing more people into
senior roles is becoming critical for the project to continue to deliver a
robust and reliable releases.

In 2022 we have started discussion the CNCF Governing Board to see how we can
tackle long term strategies together.
- How can we incentivize growth in this area of sustainers?
- How can we surface areas of risk that require investment to keep going?
- Are there additional actions we might take in the short term?


#### This reporting process and its summary

This process takes us 6 months. This is both not sustainable and not helpful.
Between our groups being heads down shipping reliable and stable enhancements, 
societal challenges and atrocities that affect us such the war in Ukraine, not to mention
a global pandemic, we have a lot of leniency for groups getting this together.
Our contributors live all over the world, have day jobs, and might have their
own challenges that they are living through. 

With the theme of burnout, how can we support groups without bogging them down
with paperwork? How can we communicate our needs at a level that hears and takes
action on them? We need to build more tooling in this area and will be putting out
a call for interns soon. [Have other advice for us?]


[Have other advice for us?]: https://github.com/kubernetes/steering/issues/242





## Help Wanted

#### [SIG API Machinery](https://git.k8s.io/community/sig-api-machinery/annual-report-2021.md#project-health)

- Client libraries 
- Triage
- Sticking around and growing into contributor ladder roles 


#### [SIG Apps](https://git.k8s.io/community/sig-apps/annual-report-2021.md#project-health)

SIG Apps is looking to grow their pool of [reviewers and appprovers]. Contributors
looking at growing into these roles can join the[SIG Apps / SIG CLI Review club].

[reviewer and appprover]: #OWNERmaintainer
[SIG Apps / SIG CLI Review club]: https://groups.google.com/g/kubernetes-sig-apps/c/aTymvEPd2y0/m/HbqV7NiZBAAJ


#### [SIG Auth](https://git.k8s.io/community/sig-auth/annual-report-2021.md#project-health)

SIG Auth keeps a running list of [KEPs that need help] and tracks their progress
on their [SIG Auth project board]. They are also looking for help in enhancing
their own [onboarding guide and PR review guidance].

Specifically SIG Auth is looking for help in these initatives:
- [KMS-Plugin: Improvements](https://docs.google.com/document/d/1YHzSzITSS3ZNpf63E-rseDo-ocpxexp3ttzjBU2P8Ck/edit?usp=sharing)
- Specifying multiple webhooks in the kube-apiserver authorization chain
- Structured config for OIDC authentication
- Audit logging improvements
- Renaming the `system:masters` group
 

[KEPs that need help]: https://docs.google.com/document/d/1sY8fRyRtk4eG9R439z5ao5i9bFuuxilS03XaNlqoni0/edit
[onboarding guide and PR review guidance]: https://github.com/kubernetes/community/blob/master/sig-auth/CONTRIBUTING.md
[SIG Auth project board]: https://github.com/orgs/kubernetes/projects/54


#### [SIG CLI](https://git.k8s.io/community/sig-cli/annual-report-2021.md#project-health)

SIG CLI has three areas where they're looking for more help:
- Optimizing [kubectl memory usage].
- Contributors that can dedicate time and grow into maintainer roles (reviewer /
  approver) for [Kustomize].
- SIG CLI's docs for both kubectl and kustomize need additional support. They
  are built off [cli-experimental], are outdated, need SEO improvements and
  migrated to the new kustomize.io and kubectl.io domains. Alignment with k8s.io docs
  would be useful too.

[kubectl memory usage]: https://github.com/kubernetes/kubectl/issues/978
[kustomize]: https://github.com/kubernetes-sigs/kustomize
[cli-experimental]: https://github.com/kubernetes-sigs/cli-experimental


#### [SIG Cloud Provider](https://git.k8s.io/community/sig-cloud-provider/annual-report-2021.md#project-health)

SIG Cloud Provider needs more support from cloud providers to
[extract the provider specific code] from the main Kubernetes repo. Spinning
them out will create a smaller and more secure core, while enabling the Cloud
Providers to release and update their components on their own cadence.

[extract the provider specific code]: https://git.k8s.io/enhancements/keps/sig-cloud-provider/2395-removing-in-tree-cloud-providers


#### [SIG Contributor Experience](https://git.k8s.io/community/sig-contributor-experience/annual-report-2021.md#project-health)

The SIG is looking for a full time community manager. Also, there are three
[subprojects][contribex-sp] where [SIG Contributor Experience] could use assistance.

- [GitHub Administration]
  - The GitHub Admin team needs more [new membership coordinators]. These
    coordinators are current contributors that help serve as a friendly face
    to newer, prospective community members, guiding them through the process
    to request membership to a Kubernetes GitHub organization.
- [Community Management Automation]
  - [Auto upload recordings from Zoom to YouTube]
    - Every community group (SG/WG/Committee) records and publishes their meetings
      for transparency. The current process is frought with manual work and toil,
      frequently leading to recordings being published in batches long after the
      meeting was held.
  - [Workspace Automation]
    - The Kubernetes project as a whole relies heavily on Google Workspace, mailing
      lists, calendars and docs. There is an ongoing effort to streamline these
      processes and bring them under a single domain for central management.
 - [Mentoring Program Management and new Roles]
    - [Group Mentoring Coordinator]
      - SIG Contributor Experience facilitates and aids other groups with their
        in-project mentoring initatives. With increased interest in mentoring
        from other SIGs and WGs, there is a need for a dedicated coordinator to
        spin up and manage these initatives.
    - [3rd Party Mentoring Coordinator]
      - SIG Contributor Experiences works with a number of external mentorship
        programs such as Outreachy, Google Summer of Code, LFX and more. As
        there are a number of external parties with a variety of deadlines and
        requirements, the SIG is looking for a dedicated person(s) to manage
        and facilicate working with these external mentorship programs.

[contribex-sp]: https://git.k8s.io/community/sig-contributor-experience/#subprojects
[SIG Contributor Experience]: https://git.k8s.io/community/sig-contributor-experience/
[GitHub Administration]: https://git.k8s.io/community/sig-contributor-experience/#github-management
[new membership coordinators]: https://git.k8s.io/community/github-management#new-membership-coordinator
[Community Management Automation]: https://git.k8s.io/community/sig-contributor-experience/#community-management
[Auto upload recordings from Zoom to Youtube]: https://github.com/kubernetes/community/issues/5201
[Workspace Automation]: https://github.com/kubernetes/steering/issues/213
[Mentoring Program Management and new Roles]: https://git.k8s.io/community/sig-contributor-experience/#mentoring
[Group Mentoring Coordinator]: https://github.com/kubernetes/community/issues/6517
[3rd Party Mentoring Coordinator]: https://github.com/kubernetes/community/issues/6471


#### [SIG Docs](https://git.k8s.io/community/sig-docs/annual-report-2021.md#project-health)

There are two initatives where [SIG Docs] could use assistance.

The [blog subproject] is particularly short on resources and attention. At the
moment a very small pool of active editors are the constraint / most critical
resource for article publication. One editor is involved in the majority of
published articles;  other editors are perhaps even more stretched with other
Kubernetes contributions and involvement with other SIGs.

The Ukrainian localization team is primarily worked on by people based in Ukraine,
where the ongoing and intensifying conflict creates challenges that take priority
over open source contribution.
     
[SIG Docs]: https://git.k8s.io/community/sig-docs/
[Blog subproject]: https://git.k8s.io/community/sig-docs/blog-subproject/


#### [SIG Instrumentation](https://git.k8s.io/community/sig-instrumentation/annual-report-2021.md#project-health)

The [Prometheus Adapter subproject] is in need of additional contributors that
can grow and commit to becoming [reviewer/approvers]. It currently only has one
active approver and is used a number of endusers.


[Prometheus Adapter subproject]: https://github.com/kubernetes-sigs/prometheus-adapter
[reviewer/approvers]: #OWNERmaintainer


#### [SIG K8s Infra](https://git.k8s.io/community/sig-k8s-infra/annual-report-2021.md#project-health)

SIG K8s Infra is looking for engineers to help build tools to automate more of the
project's infrastructure and to help migrate more tests to community owned resources.
Please show up to #sig-k8s-infra on Slack to help with this important group.
(You can get an invitation to Slack from https://slack.k8s.io/)



#### [SIG Release](https://git.k8s.io/community/sig-release/annual-report-2021.md#project-health)

SIG Release is looking for more contributors in a number of subprojects
- [kubernetes-sigs/bom](https://github.com/kubernetes-sigs/bom) - A utility to
  generate SPDX-compliant Bill of Materials manifests
- [kubernetes-sigs/downloadkubernetes](https://github.com/kubernetes-sigs/downloadkubernetes) -
  The tool that generates the site downloadkubernetes.com, making it easier to
  download Kubernetes release artifacts
- [kubernetes-sigs/mdtoc](https://github.com/kubernetes-sigs/mdtoc) - A small
  utility that generates a Table of Contents in Markdown.
- [kubernetes-sigs/release-notes](https://github.com/kubernetes-sigs/release-notes) -
  Generator for Kubernetes release notes
- [kubernetes-sigs/zeitgeist](https://github.com/kubernetes-sigs/zeitgeist) -
  language-agnostic dependency checker
- [kubernetes/repo-infra](https://github.com/kubernetes/repo-infra) - A collection
  of common Kubernetes repo project tools


#### [SIG Scalability](https://git.k8s.io/community/sig-scalability/annual-report-2021.md#project-health)

SIG Scalability is looking to grow their contributors base across all their
[subprojects][scale-sp]. Good entry points for new scalability contributors are
the [Scalability Test Framework] and [Performance Tests & Validaiton subproject].

[scale-sp]: https://git.k8s.io/community/sig-scalability/#subprojects
[Scalability Test Framework]: https://git.k8s.io/community/sig-scalability/#kubernetes-scalability-test-frameworks-1
[Performance Tests & Validaiton subproject]: https://git.k8s.io/community/sig-scalability/#kubernetes-scalability-and-performance-tests-and-validation-1


#### [SIG Scheduling](https://git.k8s.io/community/sig-scheduling/annual-report-2021.md#project-health)

The [Scheduler Simulator], a project that allows for simulating and testing of
scheduling profiles/plugins needs more reviewers and approvers.

[Scheduler Simulator]: https://github.com/kubernetes-sigs/kube-scheduler-simulator


#### [SIG Security](https://git.k8s.io/community/sig-security/annual-report-2021.md#project-health)

The SIG Security [docs subproject] is always looking for security-minded
contributors of all experience levels to share their learning and knowledge
with the community. This subproject has consistently been a place where people
merge their first Kubernetes PRs. There’s always room for continuous improvement
in our documentation, and contributing to this provides an opportunity to
learn more about Kubernetes security while helping everyone run their clusters
more safely. We’re really proud of the way Docs encourages and welcomes new
contributors, and we’d love to encourage you to become a part of it!


[Docs subproject]: https://github.com/kubernetes/sig-security/issues


#### [SIG Storage](https://git.k8s.io/community/sig-storage/annual-report-2021.md#project-health)

SIG Storage is broadly looking for more help [fixing bugs] and growing
reviewers across the board.

Full time contributors in the following areas:
- Write more tests and monitor [test grid health]
- Improve out of tree [test framework]
- Enhance [CSI release tools]
- Improve [docs on CSI] and general storage architecture
- Help with initial PR triage

[fixing bugs]: https://github.com/kubernetes/kubernetes/issues?q=is%3Aissue+is%3Aopen+label%3Asig%2Fstorage+label%3Akind%2Fbug+
[test grid health]: https://testgrid.k8s.io/sig-storage
[CSI release tools]: https://github.com/kubernetes-csi/csi-release-tools
[test framework]: https://github.com/kubernetes-csi/csi-test
[docs on CSI]: https://github.com/kubernetes-csi/docs


#### [SIG Testing](https://git.k8s.io/community/sig-testing/annual-report-2021.md#project-health)

SIG Testing is broadly looking for more contributors that can become
reviewers / approvers.

Looking for help in the following projects:
- [Boskos](https://github.com/kubernetes-sigs/boskos)- Resource management
  service used by Kubernetes CI that provides reservation and lifecycle management
- [Kubetest2](https://github.com/kubernetes-sigs/kubetest2) - Framework for
  launching and running end-to-end tests on Kubernetes.
- [Prow](https://git.k8s.io/test-infra/prow) - Main Kubernetes CI system
  - Cannot continue to maintain https://monitoring.prow.k8s.io due to Grafana
    license change. Kubernetes has switched to using Google Cloud Monitoring,
    but cannot make the dashboards publicly visible.
- [Triage](https://git.k8s.io/test-infra/triage) - Tool for gathering and
  reporting similar test failures across all CI jobs
- [Kettle](https://git.k8s.io/test-infra/kettle) - Tool that collections CI
  job information and loads it into BigQuery for analysis


#### [SIG Windows](https://git.k8s.io/community/sig-windows/annual-report-2021.md#project-health)

SIG Windows has several areas it is looking for support, the largest being related
to [Windows Storage support/CSI Proxy].

Looking for full time contributors to help with:
- Testing hostProcess implementations on several windows apps
- Improving Windows dev tools to help grow the Windows contributor community
- Hardening the CSI proxy and CSI support ecosystem
- Performance testing Kubernetes on Windows

[Windows Storage support/CSI Proxy]: https://github.com/kubernetes-csi/csi-proxy


#### [WG API Expression](https://git.k8s.io/community/wg-api-expression/annual-report-2021.md#project-health)

_No Report_


#### [WG Data Protection](https://git.k8s.io/community/wg-data-protection/annual-report-2021.md#project-health)

- End users come to meetings and contribute to design/implementation of the features we are working on


#### [WG IoT/Edge](https://git.k8s.io/community/wg-iot-edge/annual-report-2021.md#project-health)

Spinning down inside of Kubernetes and heading to CNCF level 


#### [WG Multitenancy](https://git.k8s.io/community/wg-multitenancy/annual-report-2021.md#project-health)

No specific help needed! Contributions are still welcome.


#### [WG Structured Logging](https://git.k8s.io/community/wg-structured-logging/annual-report-2021.md#project-health)

   - Graduate [Contextual Logging](https://github.com/kubernetes/enhancements/issues/3077) to Beta and GA
   - Graduate [Deprecation of klog specific flags](https://github.com/kubernetes/enhancements/issues/2845) to GA
   - Graduated [Structured Logging](https://github.com/kubernetes/enhancements/issues/1602) to GA
   - All code in kubernetes/kubernetes repository is migrated to Structured Logging API



## Initiatives

#### [SIG API Machinery](https://git.k8s.io/community/sig-api-machinery/annual-report-2021.md#current-initiatives)

API Machinery is evaluating the potential for generics in go1.19.
There are a number of [other initiatives].

[Other initiatives]: https://github.com/kubernetes/enhancements/issues?q=is%3Aissue+label%3Asig%2Fapi-machinery+updated%3A%3E%3D2021-01-01+is%3Aopen

#### [SIG Apps](https://git.k8s.io/community/sig-apps/annual-report-2021.md#current-initatives)

- Significant improvements were made to the Job API, along with finally driving CronJobs
  to stable and introduced several long-desired features. This work is expected
  to continue through 2022 to finish rounding out the Job API.
  - [CronJobs promoted to stable (1.21)](https://git.k8s.io/enhancements/keps/sig-apps/19-Graduate-CronJob-to-Stable)
  - [Indexed Job promoted to beta (1.22)](https://git.k8s.io/enhancements/keps/sig-apps/2214-indexed-job)
  - [Suspend Job promoted to beta (1.22)](https://git.k8s.io/enhancements/keps/sig-apps/2232-suspend-jobs)
  - [Job tracking without lingering Pods promoted to beta (1.23)](https://git.k8s.io/enhancements/keps/sig-scheduling/2926-job-mutable-scheduling-directives)
- Stability and availability improvements were made across several controllers,
  with larger improvements being made to both DaemonSets and StatefulSets.
  - [minReadySeconds for StatefulSets promoted to beta (1.22)](https://git.k8s.io/enhancements/keps/sig-apps/2599-minreadyseconds-for-statefulsets)
  - [Allow DaemonSets to surge during update like Deployments promoted to beta (1.22)](https://git.k8s.io/enhancements/keps/sig-apps/1591-daemonset-surge)
- Additional improvements have been made to conformance testing promotions.

Kubernetes Enhancements:
- Stable
  - [19 - CronJob to Stable](https://git.k8s.io/enhancements/keps/sig-apps/19-Graduate-CronJob-to-Stable/) - 1.21
  - [85 - PodDisruptionBudget to GA](https://git.k8s.io/enhancements/keps/sig-apps/85-Graduate-PDB-to-Stable/) - 1.22
  - [592 - TTL After Finished](https://git.k8s.io/enhancements/keps/sig-apps/592-ttl-after-finish/) - 1.23
- Beta
  - [2185 - Random Pod Selection on ReplicaSet Downscale](https://git.k8s.io/enhancements/keps/sig-apps/2185-random-pod-select-on-replicaset-downscale/) - 1.22
  - [1591 - Allow DaemonSets to surge during update like Deployments](https://git.k8s.io/enhancements/keps/sig-apps/1591-daemonset-surge/) - 1.22
  - [2214 - Indexed Job](https://git.k8s.io/enhancements/keps/sig-apps/2214-indexed-job/) - 1.22
  - [2232 - Suspend Job](https://git.k8s.io/enhancements/keps/sig-apps/2232-suspend-jobs/) - 1.22
  - [2255 - ReplicaSet Pod Deletion Cost](https://git.k8s.io/enhancements/keps/sig-apps/2255-pod-cost/) - 1.22
  - [2307 - Job tracking without lingering Pods](https://git.k8s.io/enhancements/keps/sig-scheduling/2926-job-mutable-scheduling-directives/) - 1.23
  - [2599 - minReadySeconds for StatefulSets](https://git.k8s.io/enhancements/keps/sig-apps/2599-minreadyseconds-for-statefulsets/) - 1.23
  - [2926 - Mutable Node Scheduling Directives for Jobs](https://git.k8s.io/enhancements/keps/sig-apps/2599-minreadyseconds-for-statefulsets/) - 1.23
- Alpha
  - [2185 - Random Pod Selection on ReplicaSet Downscale](https://git.k8s.io/enhancements/keps/sig-apps/2185-random-pod-select-on-replicaset-downscale/) - 1.21
  - [1591 - Allow DaemonSets to surge during update like Deployments](https://git.k8s.io/enhancements/keps/sig-apps/1591-daemonset-surge/) - 1.21
  - [2214 - Indexed Job](https://git.k8s.io/enhancements/keps/sig-apps/2214-indexed-job/) - 1.21
  - [2232 - Suspend Job](https://git.k8s.io/enhancements/keps/sig-apps/2232-suspend-jobs/) - 1.21
  - [2255 - ReplicaSet Pod Deletion Cost](https://git.k8s.io/enhancements/keps/sig-apps/2255-pod-cost/) - 1.21
  - [2307 - Job tracking without lingering Pods](https://git.k8s.io/enhancements/keps/sig-apps/2307-job-tracking-without-lingering-pods/) - 1.22
  - [2599 - minReadySeconds for StatefulSets](https://git.k8s.io/enhancements/keps/sig-apps/2599-minreadyseconds-for-statefulsets/) - 1.22
  - [1847 - Auto delete PVCs created by StatefulSet](https://git.k8s.io/enhancements/keps/sig-apps/1847-autoremove-statefulset-pvcs/) - 1.23
  - [2879 - Track ready Pods in Job status](https://git.k8s.io/enhancements/keps/sig-apps/2879-ready-pods-job-status/) - 1.23


#### [SIG Auth](https://git.k8s.io/community/sig-auth/annual-report-2021.md#current-initiatives)

- [Pod Security admission](https://kubernetes.io/docs/concepts/security/pod-security-admission/) has [graduated to beta](https://github.com/kubernetes/kubernetes/pull/106089) and is enabled by default. The admission configuration version has been promoted to `pod-security.admission.config.k8s.io/v1beta1` in v1.23.
- The [PodSecurityPolicy API is deprecated in v1.21](https://github.com/kubernetes/kubernetes/pull/97171), and will no longer be served starting in v1.25.
- Marking `audit.k8s.io/v1[alpha|beta]1` versions as deprecated and warning if a version other than `audit.k8s.io/v1` was passed to the kube-apiserver flags `--audit-log-version` and `--audit-webhook-version` [in v1.21](https://github.com/kubernetes/kubernetes/pull/98858).
- [PodSecurityPolicy only stores "generic" as allowed volume type](https://github.com/kubernetes/kubernetes/pull/98918) if the GenericEphemeralVolume feature gate is enabled
- RunAsGroup feature for Containers in a Pod [graduates to GA in v1.21](https://github.com/kubernetes/kubernetes/pull/94641)
- RootCAConfigMap feature [graduates to GA in v1.21](https://github.com/kubernetes/kubernetes/pull/98033)
- The ServiceAccountIssuerDiscovery feature has [graduated to GA](https://github.com/kubernetes/kubernetes/pull/98553), and is unconditionally enabled in v1.21.
- CSIServiceAccountToken [graduates to GA](https://github.com/kubernetes/kubernetes/pull/103001) in 1.22
- Mark `net.ipv4.ip_unprivileged_port_start` as safe sysctl [in v1.22](https://github.com/kubernetes/kubernetes/pull/103326)
- BoundServiceAccountTokenVolume [graduates to GA in v1.22](https://github.com/kubernetes/kubernetes/pull/101992)
- Kubernetes client [credential plugins](https://kubernetes.io/docs/reference/access-authn-authz/authentication/#client-go-credential-plugins) feature graduates to stable in v1.22. The GA feature set includes improved support for plugins that provide interactive login flows. The in-tree Azure and GCP authentication plugins have been [deprecated](https://github.com/kubernetes/kubernetes/pull/102181) in favor of out-of-tree implementations.
- Kube-apiserver `--service-account-issuer` can be specified multiple times now, to enable non-disruptive change of issuer [starting v1.22](https://github.com/kubernetes/kubernetes/pull/101155)
- The `CertificateSigningRequest.certificates.k8s.io` API supports an optional expirationSeconds field to allow the client to request a particular duration for the issued certificate. The default signer implementations provided by the Kubernetes controller manager will honor this field as long as it does not exceed the `--cluster-signing-duration` flag [starting v1.22](https://github.com/kubernetes/kubernetes/pull/99494).
- Aggregate write permissions on events to edit and admin role [starting v1.22](https://github.com/kubernetes/kubernetes/pull/102858)
- The kubelet now reports distinguishes log messages about certificate rotation for its client cert and server cert separately to make debugging problems with one or the other easier.[starting v1.22](https://github.com/kubernetes/kubernetes/pull/101252)
- A new field `omitManagedFields` has been added to both `audit.Policy` and `audit.PolicyRule` so cluster operators can opt in to omit managed fields of the request and response bodies from being written to the API audit log [starting v1.23](https://github.com/kubernetes/kubernetes/pull/94986)
- Adds `--as-uid` flag to kubectl to allow uid impersonation in the same way as user and group impersonation [starting v1.23](https://github.com/kubernetes/kubernetes/pull/105794)


- Stable
  - [1205-bound-service-account-tokens](https://git.k8s.io/enhancements/keps/sig-auth/1205-bound-service-account-tokens/) - 1.22
  - [1393-oidc-discovery](https://git.k8s.io/enhancements/keps/sig-auth/1393-oidc-discovery/README.md) - 1.21
  - [2907-secrets-store-csi-driver](https://git.k8s.io/enhancements/keps/sig-auth/2907-secrets-store-csi-driver/) - 1.0.0
  - [541-external-credential-providers](https://git.k8s.io/enhancements/keps/sig-auth/541-external-credential-providers/) - 1.22
  - [1687-hierarchical-namespaces-subproject](https://git.k8s.io/enhancements/keps/sig-auth/1687-hierarchical-namespaces-subproject/) - stable
- Beta
  - [2579-psp-replacement](https://git.k8s.io/enhancements/keps/sig-auth/2579-psp-replacement/) - 1.23
  - [2784-csr-duration](https://git.k8s.io/enhancements/keps/sig-auth/2784-csr-duration/) - 1.22



#### [SIG CLI](https://git.k8s.io/community/sig-cli/annual-report-2021.md#current-initiatives)

SIG CLI made progress on a number of initiatives in 2021:
- [kubectl events alpha command](https://github.com/kubernetes/enhancements/blob/master/keps/sig-cli/1440-kubectl-events/README.md).
- [KRM Functions subproject started](https://github.com/kubernetes-sigs/krm-functions-registry).
- New changes to leadership.
  - [@KnVerey](https://github.com/knverey) brought on as new Co-Chair and Tech Lead.
  - [@soltysh](https://github.com/soltysh) stepped down from Co-Chair to focus on Tech Lead.
  - [@pwittrock](https://github.com/pwittrock) moved to emeritus.
  - [@monopole](https://github.com/monopole) moved to emeritus for Kustomize.
- [Started a new monthly Kustomize bug scrub](https://github.com/kubernetes/community/tree/master/sig-cli#meetings).
- [Upgraded the version of Kustomize that ships with kubectl](https://github.com/kubernetes/kubernetes/pull/98946).
- [Implemented native Go shell completions](https://github.com/kubernetes/kubernetes/pull/96087).
- [Replicated](https://www.replicated.com/) donated [kubectl.io](https://kubectl.io) and [kustomize.io](https://kustomize.io) to the project.
- [IBM](https://ibm.com) donated the [Kui](https://github.com/kubernetes-sigs/kui) project.
- [The Kustomize Roadmap](https://github.com/kubernetes-sigs/kustomize/blob/master/ROADMAP.md)
- [Refactoring old kubectl commands](https://github.com/kubernetes/kubectl/issues/1046)

Kubernetes Enhancements
- Stable
  - [KEP-555 - Server-side apply](https://github.com/kubernetes/enhancements/issues/555) - 1.22
- Beta
  - [KEP-1441 - kubectl debug](https://github.com/kubernetes/enhancements/issues/1441) - 1.20, continued to evolve the beta through the year
  - [KEP-859 - kubectl command metadata in http request headers](https://github.com/kubernetes/enhancements/issues/859) - 1.22
- Alpha
  - [KEP-1440 - kubectl events](https://github.com/kubernetes/enhancements/issues/1440) - 1.23
  - [KEP-2227 - Default container annotation to be used by kubectl](https://github.com/kubernetes/enhancements/issues/2227) - 1.21
- Pre-alpha
  - [KEP-2985 - Public KRM functions registry](https://github.com/kubernetes/enhancements/issues/2985)
  - [KEP-2953 - Kustomize Plugin Graduation](https://github.com/kubernetes/enhancements/issues/2953)
- Rejected
  - [KEP-2229 - Use XDG Base Directory Specification](https://github.com/kubernetes/enhancements/issues/2229)


#### [SIG Cloud Provider](https://git.k8s.io/community/sig-cloud-provider/annual-report-2021.md#current-initiatives)

_No Report_


#### [SIG Contributor Experience](https://git.k8s.io/community/sig-contributor-experience/annual-report-2021.md#current-initiatives)

During 2021, SIG Contributor Experience continued to provide a number of
services to the project and it's 75,000 contributors. Some achievements include
the [migration of the large public kubernetes-dev] mailing list to to managed
a project owned Google workspace, [developing Elekto], a replacement for the CIVS
voting system, and the seamless migration of the [CLA system to EasyCLA].

SIG Contributor Experience also ran the [North America Contributor Summit], the
end of year [Contributor Celebration], ran three successful mentoring cohorts,
and the [Contributor Comms team] automated and started using the [@k8scontributors] 
twitter account to reach 5700 follows with a number of them being contributors.

[migration of the large public kubernetes-dev]: https://github.com/kubernetes/community/issues/5877
[developing Elekto]: https://github.com/kubernetes/community/issues/5096
[CLA system to EasyCLA]: https://github.com/kubernetes/org/issues/2778
[North America Contributor Summit]: https://www.kubernetes.dev/events/past-events/2021/kcsna/
[Contributor Celebration]: https://www.kubernetes.dev/events/past-events/2021/kcc2021/
[@k8scontributors]: https://twitter.com/k8scontributors


Contributor Experience (“ContribEx”) is a service and program orientated SIG. Most of its initiatives
cover long term services for the Kubernetes project.

|                                                  **Subproject**                                                 |                                                **Initiative / Program**                                               |
|:---------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------:|
| [Community](https://git.k8s.io/community/sig-contributor-experience#community)                                  | [Community Repo Stewardship](https://git.k8s.io/community)                                                            |
| [Community Management](https://git.k8s.io/community/sig-contributor-experience#community-management)            | Calendar Admin                                                                                                    |
| [Community Management](https://git.k8s.io/community/sig-contributor-experience#community-management)            | Leadership Operations                                                                                             |
| [Community Management](https://git.k8s.io/community/sig-contributor-experience#community-management)            | [discuss.k8s.io End User Forum Admin](https://discuss.k8s.io)                                                         |
| [Community Management](https://git.k8s.io/community/sig-contributor-experience#community-management)            | [Mailing List Admin](https://k8s.dev/docs/comms/moderation/)                                                          |
| [Community Management](https://git.k8s.io/community/sig-contributor-experience#community-management)            | [Slack Admin](https://k8s.dev/docs/comms/slack/)                                                                      |
| [Community Management](https://git.k8s.io/community/sig-contributor-experience#community-management)            | [Zoom](https://k8s.dev/docs/comms/zoom) / [YouTube Admin](https://k8s.dev/docs/comms/youtube/#admin-responsibilities) |
| [Contributor Documentation](https://git.k8s.io/community/sig-contributor-experience#contributors-documentation) | [Contributor Guide Stewardship](https://k8s.dev/guide)                                                                |
| [Contributor Documentation](https://git.k8s.io/community/sig-contributor-experience#contributors-documentation) | [Contributor Site](https://git.k8s.io/contributor-site)                                                               |
| [Contributor Documentation](https://git.k8s.io/community/sig-contributor-experience#contributors-documentation) | [Developer Guide Audit](https://github.com/kubernetes/community/issues/5229)                                          |
| [Contributor Documentation](https://git.k8s.io/community/sig-contributor-experience#contributors-documentation) | [Developer Guide Stewardship](https://github.com/kubernetes/community/tree/master/contributors/devel)                 |
| [Contributor Comms](https://git.k8s.io/community/sig-contributor-experience#contributor-comms)                  | Contributor / SIG Profiling                                                                                           |
| [Contributor Comms](https://git.k8s.io/community/sig-contributor-experience#contributor-comms)                  | SIG Outreach and Support                                                                                              |
| [Contributor Comms](https://git.k8s.io/community/sig-contributor-experience#contributor-comms)                  | Contributor Events Outreach                                                                                           |
| [Contributor Comms](https://git.k8s.io/community/sig-contributor-experience#contributor-comms)                  | [Stewardship of k8scontributors twitter](https://twitter.com/k8scontributors)                                         |
| [Devstats](https://git.k8s.io/community/sig-contributor-experience#devstats)                                    | [Devstats Dashboard Update](https://github.com/cncf/devstats/issues/289)                                              |
| [Events](https://git.k8s.io/community/sig-contributor-experience#events)                                        | Monthly Community Meeting                                                                                             |
| [Events](https://git.k8s.io/community/sig-contributor-experience#events)                                        | Office Hours                                                                                                          |
| [Events](https://git.k8s.io/community/sig-contributor-experience#events)                                        | [Elections](git.k8s.io/community/events/elections)                                                                    |
| [Events](https://git.k8s.io/community/sig-contributor-experience#events)                                        | [Contributor Summits](https://k8s.dev/events/past-events/2021/)                                                       |
| [GitHub Management](https://git.k8s.io/community/sig-contributor-experience#github-management)                  | [GitHub Admin / Moderation](https://git.k8s.io/community/github-management#github-management)                         |
| [GitHub Management](https://git.k8s.io/community/sig-contributor-experience#github-management)                  | [GitHub Master -> Main rename](https://github.com/kubernetes/org/issues/2222)                                         |
| [GitHub Management](https://git.k8s.io/community/sig-contributor-experience#github-management)                  | [GitHub New Membership Coordinator](https://git.k8s.io/community/github-management/README.md#other-roles)             |
| [Mentoring](https://git.k8s.io/community/sig-contributor-experience#mentoring)                                  | [Group Mentoring](https://git.k8s.io/community/mentoring/programs/group-mentoring.md)                                 |
| [Mentoring](https://git.k8s.io/community/sig-contributor-experience#mentoring)                                  | [LFX Mentor Program](https://git.k8s.io/community/mentoring/programs/lfx-mentoring.md)                                |
| [Slack Infra](https://git.k8s.io/community/sig-contributor-experience#slack-infra)                              | [slack-infra](https://sigs.k8s.io/slack-infra)                                                                        |



#### [SIG Docs](https://git.k8s.io/community/sig-docs/annual-report-2021.md#current-initiatives)

- SIG Docs put meaningful effort into growing its contributor and reviewer base
  in 2021, introducing [a shadow program for PR Wrangling] as well as dedicating
  more time to being active via our Slack community channel.
- Ahead of the [dockershim removal] in the Kubernetes 1.24 release, SIG Docs
  has been collaborating with various community members and the CNCF towards
  ensuring updation and creation of content in the form of documentation, blog
  posts etc. With weekly meetings and a [project board] to track progress, this
  enabled SIG Docs to invite contributors across experience levels to help us
  keep the Kubernetes website updated and relevant ahead of the major change.
- Alongside growing our contributor base, SIG Docs also worked on a leadership
  transition strategy to bring community members into leadership roles. Via a
  specialized six month mentorship program expertly led by Steering Committee
  member Paris Pittman, SIG Docs was able to grow its leadership cohort for the
  main SIG, as well as some of its subgroups, adding new co-chairs and tech leads.
  - [SIG Docs google group](https://groups.google.com/g/kubernetes-sig-docs/)
  - [Call for help sent to dev@kubernetes.io, kubernetes-sig-leads, kubernetes-sig-docs](https://groups.google.com/g/kubernetes-sig-docs/c/hspG6mzgkrs)
  - [Announcement of new roles and leadership nominations](https://groups.google.com/g/kubernetes-sig-docs/c/cgrAyDLxydk)
- Localization Subproject: SIG Docs is working on formalizing the localization
  work that has been ongoing for some time, with appointed leads of this
  initiative as well as recognizing the contributions of various community
  members across the different languages the Kubernetes website has been
  translated into. This subproject will be finalized by Q1 2022, with all active
  localizations informed and updated.
- [New Contributor Ambassador Program]: As a continued focus to grow the SIG
  Docs contributor base, they're working on a specalized role that aims to
  support new and would-be contributors get up to speed with our processes
  and workflows. This role would be capped at six months for it to be shared
  amongst the community, with this feeding into a possible reviewer funnel as
  contributors get more comfortable with providing feedback to others.


Kubernetes Enhancements:
- [1326 - Doc policies for third party content](https://git.k8s.io/enhancements/keps/sig-docs/1326-third-party-content-in-docs/)

[a shadow program for PR Wrangling]: https://github.com/kubernetes/website/issues/31956
[dockershim removal]: https://kubernetes.io/blog/2022/02/17/dockershim-faq/
[project board]: https://github.com/orgs/kubernetes/projects/67
[New Contributor Ambassador Program]: https://github.com/kubernetes/website/issues/31946


#### [SIG Instrumentation](https://git.k8s.io/community/sig-instrumentation/annual-report-2021.md#current-initiatives)

SIG Instrumentation had several large accomplishments in 2021.
- Formed WG Structured Logging. Successfully migrated multiple components to
  structured logs and graduated feature to beta
- Added tracing support to the Kubernetes API server and began work on Kubelet
  tracing
- Graduated the metrics stability framework
- Put into practice Bi-weekly triage meeting


Kubernetes Enhancements:
- Stable
  - [1209 - Metrics Stability](https://git.k8s.io/enhancements/keps/sig-instrumentation/1209-metrics-stability) - 1.21
  - [1933 - Prevent logging secrets via static analysis](https://git.k8s.io/enhancements/keps/sig-instrumentation/1753-logs-sanitization) - 1.23
- Beta
  - [1602 - Structured Logging](https://git.k8s.io/enhancements/keps/sig-instrumentation/1602-structured-logging) - 1.23
  - [1748 - Pod resource requests/limits metrics](https://git.k8s.io/enhancements/keps/sig-instrumentation/1748-pod-resource-metrics) - 1.22
- Alpha
  - [2305 - Metrics Cardinality Enforcement](https://git.k8s.io/enhancements/keps/sig-instrumentation/2305-metrics-cardinality-enforcement) - 1.21
  - [647 - API Server Tracing](https://git.k8s.io/enhancements/keps/sig-instrumentation/647-apiserver-tracing) - 1.22
  - [2845 - Deprecate klog-specific flags in k8s components](https://git.k8s.io/enhancements/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components) - 1.23
- Pre-alpha
  - [2831 - Kubelet OpenTelemetry Tracing](https://git.k8s.io/enhancements/keps/sig-instrumentation/2831-kubelet-tracing) - alpha in 1.24


#### [SIG Release](https://git.k8s.io/community/sig-release/annual-report-2021.md#current-initiatives)

After finalizing the rewrite of the release process from bash into golang, the
release engineering team focused its efforts on two main areas:

- Improving the release automation on two fronts:
  - Adding new features, tests and checks to the release process which were
    missing from the original release tooling (binary verification, CVE
    disclosure, building from custom branches and repositories).
  - Consolidating the codebases of new repositories which SIG Release
    brought under its responsibility. The range of new repositories it is
    consolidating go from critical projects (like the image promoter) to less
    important repositories such as https://downloadkubernetes.com.
- Hardening the Kubernetes Supply Chain via key efforts:
  - SBOM Generation
  - SLSA 3 compliance
  - Artifact signing


Kubernetes Enhancements
- Alpha
  - [KEP-3027 - SLSA Level 3 Compliance in the Kubernetes Release Process](https://git.k8s.io/enhancements/keps/sig-release/3027-slsa-compliance) - v1.23


#### [SIG Scalability](https://git.k8s.io/community/sig-scalability/annual-report-2021.md#current-initiatives)

SIG Scalability spent significant effort on validating the scalability and
reliability impact of many Kubernetes features across 2021; growing the
scalability tests of large services to cover 1000+ pods. Additional work
was put into adding support for modules in tests, measuring the availability
of the api-server and adding support for measuring cilium propagation delay &
dns latency.


Kubernetes Enhancements:
- Beta
  - [1040 - Priority and Fairness for API Server Requests](https://git.k8s.io/enhancements/keps/sig-api-machinery/1040-priority-and-fairness/) - 1.23
- Alpha
  - [647 - APIServer Tracing](https://git.k8s.io/enhancements/keps/sig-instrumentation/647-apiserver-tracing/) - 1.22
  - [1669 - Proxy Terminating Endpoints](https://git.k8s.io/enhancements/keps/sig-network/1669-proxy-terminating-endpoints/) - 1.22
  - [2464 - Kubetest2 CI Migration](https://git.k8s.io/enhancements/kepssig-testing/2464-kubetest2-ci-migration/) - 1.21


#### [SIG Scheduling](https://git.k8s.io/community/sig-scheduling/annual-report-2021.md#current-initiatives)

During 2021, SIG Scheduling focused on improving the overall performance of the
scheduler, some highlights include:
- Efficient re-queueing of pods, significantly cutting the number of failed
  scheduling cycles
- Improvements to preemption performance
- Simplified plugin configuration in component config
- Created the [Scheduler simulator]
- Performance improvements and benchmarking
- Code refactorings and cleanups
- Enhancements to node resource-based scoring (see [101946] and [101822])


Kubernetes Enhancements:
- Stable
  - [2249 - Multi-scheduling Profiles](https://git.k8s.io/enhancements/keps/sig-scheduling/1451-multi-scheduling-profiles) - 1.22
  - [1845 - Prioritization on Volume Capacity](https://git.k8s.io/enhancements/keps/sig-storage/1845-prioritization-on-volume-capacity) - 1.22
- Beta
  - [2249 - Namespace Selector for Pod Affinity](https://git.k8s.io/enhancements/keps/sig-scheduling/2249-pod-affinity-namespace-selector) - 1.22
  - [1923 - Prefer Nominated Node](https://git.k8s.io/enhancements/keps/sig-scheduling/1923-prefer-nominated-node) - 1.22   
  - [2458 - Resource Fit Scoring Strategy](https://git.k8s.io/enhancements/keps/sig-scheduling/2458-node-resource-score-strategy) - 1.22
  - [2891 - Simplified Scheduler Config](https://git.k8s.io/enhancements/keps/sig-scheduling/2891-simplified-config/kep.yaml) - 1.22
  - [785 - Scheduler Component Config API](https://git.k8s.io/enhancements/keps/sig-scheduling/785-scheduler-component-config-api) - 1.23
  - [2926 - Job Mutable Scheduling Directives](https://git.k8s.io/enhancements/keps/sig-scheduling/2926-job-mutable-scheduling-directives) - 1.23


[Scheduler simulator]: https://github.com/kubernetes-sigs/kube-scheduler-simulator
[101946]: https://github.com/kubernetes/kubernetes/pull/101946
[101822]: https://github.com/kubernetes/kubernetes/pull/101822



#### [SIG Security](https://git.k8s.io/community/sig-security/annual-report-2021.md#current-initiatives)

Most of SIG Security's initiatives are out of scope for KEPs, and instead
are largelty service and process oriented.

In 2021 they had several notable achievements:
- Kickstarted the [security self-assessment] project aimed at providing guidance
  and a framework for Kubernetes subprojects to perform their own security
  self-assessment.
- Implemented [vulnerability scanning for build-time dependences] in container
  images.
- Scoped the work and went through the RFP process to select a vendor to perform
  the project's [second external third-party audit].
- Bootstrapped the [Security Docs subproject] aimed at improving the security
  content in Kubernetes documentation.


Kubernetes Enhancements:
- Stable
  - [1933 - Defend against logging secrets via static analysis](https://git.k8s.io/enhancements/keps/sig-security/1933-secret-logging-static-analysis/) - 1.23
- Beta
  - [2579 - PSP Replacement Policy](https://git.k8s.io/enhancements/keps/sig-auth/2579-psp-replacement/README.m) - 1.23
  - [1933 - Defend against logging secrets via static analysis](https://git.k8s.io/enhancements/keps/sig-security/1933-secret-logging-static-analysis/) - 1.21
- Alpha
  - [2579 - PSP Replacement Policy](https://git.k8s.io/enhancements/keps/sig-auth/2579-psp-replacement/) - 1.22
- Pre-alpha
  - [2763 - Ambient Capabilities](https://git.k8s.io/enhancements/keps/sig-security/2763-ambient-capabilities/)


[security Self-assessment]: https://github.com/kubernetes/sig-security/issues/2
[vulnerability scanning for build-time dependences]: https://github.com/kubernetes/sig-security/issues/3
[second external third-party audit]: https://git.k8s.io/sig-security/sig-security-external-audit/security-audit-2021/RFP.md
[Security Docs subproject]: https://git.k8s.io/sig-security/sig-security-docs


#### [SIG Storage](https://git.k8s.io/community/sig-storage/annual-report-2021.md#current-initiatives)

In addition to a number of KEPs, SIG Storage has been working on [CBT] (Change
Blocking Tracking)] in conjunction with the Data Protection WG

Kubernetes Enhancements:
- Stable
  - [1412 - Immutable Secrets and ConfigMaps](https://git.k8s.io/enhancements/keps/sig-storage/1412-immutable-secrets-and-configmaps) - v1.21
  - [1682 - Skip Volume Ownership Change](https://git.k8s.io/enhancements/keps/sig-storage/1682-csi-driver-skip-permission) - v1.23
  - [1698 - generic ephemeral inline volumes](https://git.k8s.io/enhancements/keps/sig-storage/1698-generic-ephemeral-volumes) - v1.23
  - [1855 - Service Account Token for CSI Driver](https://git.k8s.io/enhancements/keps/sig-storage/1855-csi-driver-service-account-token) - v1.22
  - [1122 - CSI Windows](https://git.k8s.io/enhancements/keps/sig-windows/1122-windows-csi-support) - v1.22
- Beta
  - [1472 - Storage Capacity Constraints for Pod Scheduling](https://git.k8s.io/enhancements/keps/sig-storage/1472-storage-capacity-tracking) - v1.21
  - [1885 - In-tree Storage Plugin to CSI Migration - Azurefile](https://git.k8s.io/enhancements/keps/sig-storage/1885-csi-migration-azurefile) - v1.21
  - [2317 - Provide fsgroup of pod to CSI driver on mount](https://git.k8s.io/enhancements/keps/sig-storage/2317-fsgroup-on-mount) - v1.23
- Alpha
  - [1432 - Volume Health Monitor](https://git.k8s.io/enhancements/keps/sig-storage/1432-volume-health-monitor) - v1.21
  - [1790 - Recover from volume expansion failure](https://git.k8s.io/enhancements/keps/sig-storage/1790-recover-resize-failure/) - v1.23
  - [2485 - ReadWriteOncePod PersistentVolume AccessMode](https://git.k8s.io/enhancements/keps/sig-storage/2485-read-write-once-pod-pv-access-mode) - v1.22
  - [2589 - In-tree Storage Plugin to CSI Migration - Portworx](https://git.k8s.io/enhancements/keps/sig-storage/2589-csi-migration-portworx) - v1.23
  - [2644 - Honor Persistent Volume Reclaim Policy](https://git.k8s.io/enhancements/keps/sig-storage/2644-honor-pv-reclaim-policy) - v1.23
  - [2923 - In-tree Storage Plugin to CSI Migration - Ceph RBD](https://git.k8s.io/enhancements/keps/sig-storage/2923-csi-migration-ceph-rbd) - v1.23
- Pre-alpha
  - [Object Storage API (COSI)](https://github.com/kubernetes/enhancements/pull/2813)


[CBT]: https://docs.google.com/document/d/1bOXazqAVAi8wtJhVsyNNyxhjWgYFzJSTFub2IxiSqMU/edit#



#### [SIG Testing](https://git.k8s.io/community/sig-testing/annual-report-2021.md#current-initiatives)

SIG Testing is largely service-oriented and their initatives are not often
tracked as KEPs, yet they have had a number of achievements in the past year
improving testing infrastructure and features.

Highlights of some of these initiatives include:
- kubetest2 is feature-complete and stable
- Automated secret syncing for ProwJob secrets
- Developed GitHub App support for Prow
- Improved job config validation (strict field checks, build cluster existence)
- Improved in-repo Prow config support and performance
- Added support for Prow config file sharding to better manage approval permissions
- Developed new monitoring stack solution that doesn’t rely on Grafana (GKE
  Workload Metrics + Cloud Monitoring)
- Added OSS-Fuzz integration
- Developed private repo multitenancy (multiple private front ends)
- Completed the removal of Bazel from kubernetes/kubernetes
- Removed most of Bazel from the kubernetes/test-infra repo


Kubernetes Enhancements
- Stable
     - [KEP 2420 - Reducing Kubernetes Build Maintenance](https://github.com/kubernetes/enhancements/issues/2420) - 1.23
- Beta
     - [KEP 2539 - Continuously Deploy K8s Prow](https://github.com/kubernetes/enhancements/issues/2539) - 1.21
     - [KEP 2464 - kubetest2 CI migration](https://github.com/kubernetes/enhancements/issues/2464) - 1.23


#### [SIG Windows](https://git.k8s.io/community/sig-windows/annual-report-2021.md#current-initiatives)

SIG Windows has made progress on a number of lower level features. They
implemented [`hostProcess`] container support (now in beta) which has now been
adopted by a number of other OSS Projects. Other achievements include better
node-level logging, improving the Windows Kubernetes developer experience with
[sig-windows-dev-tools], defining a set of operational readiness standards,
and removed Dockershim from Windows nodes.


Kubernetes Enhancements
- Stable
  - [1122 - windows-csi-support](https://git.k8s.io/enhancements/keps/sig-windows/1122-windows-csi-supportd) - v1.22
- Beta
  - [1981 - Windows Privileged Container Support](https://git.k8s.io/enhancements/keps/sig-windows/1981-windows-privileged-container-support) - v1.23
  - [2802 -Identify Windows pods at API admission level authoritatively](https://git.k8s.io/enhancements/keps/sig-windows/2802-identify-windows-pods-apiserver-admission) - v1.23
- Alpha
  - [1981 - Windows Privileged Container Support](https://git.k8s.io/enhancements/keps/sig-windows/1981-windows-privileged-container-support) - v1.22
  - [2802 -Identify Windows pods at API admission level authoritatively](https://git.k8s.io/enhancements/keps/sig-windows/2802-identify-windows-pods-apiserver-admission) - v1.23
- Pre-alpha (Targeting 1.24)
  - [2578 - Windows Operational Readiness](https://git.k8s.io/enhancements/keps/sig-windows/2578-windows-conformance/)

[`hostProcess`]: https://git.k8s.io/enhancements/keps/sig-windows/1981-windows-privileged-container-support/
[sig-windows-dev-tools]: https://github.com/kubernetes-sigs/sig-windows-dev-tools


#### [WG API Expression](https://git.k8s.io/community/wg-api-expression/annual-report-2021.md#current-initiatives)

- Server-side Apply went GA in 1.22
- Started new initiatives around OpenAPI v3
- Enum for built-in types in OpenAPI
- Server-side field validation


#### [WG Data Protection](https://git.k8s.io/community/wg-data-protection/annual-report-2021.md#current-initiatives)

The Data Protection WG identified the missing building blocks for supporting
data protection in Kubernetes and published in their [whitepaper]. Features
such as Volume Backups, Change Block Tracking, Volume Populator, Volume Group
Group Snapshot, and Backup Repositories are owned by SIG Storage. Features such
as Quiesce and Unquiesce Hooks are owned by SIG Node, with SIG Storage and SIG
Apps participating. Features such as Application Snapshots and Backups are
owned by SIG Apps, with SIG Storage participating. We will continue to work on
them until all the missing pieces are available in Kubernetes.

The following items have been under development and have not yet been captured
in a KEP:
- [Change Block Tracking (CBT) API design](https://docs.google.com/document/d/15tLCV3csvjHbKb16DVk-mfUmFry_Rlwo-2uG6KNGsfw/edit#heading=h.1olwavha9frv)
- [Volume Replication](https://docs.google.com/document/d/15tLCV3csvjHbKb16DVk-mfUmFry_Rlwo-2uG6KNGsfw/edit#heading=h.pah3yke9ddug)
- [Data Protection for Managed Services Presentation](https://docs.google.com/presentation/d/1IM6d0w3CDdHv1dLaFNXEcxy5fuDTr9LERAdMVkZiK9s/edit#slide=id.p)
- [Snapshot policy (immutable snapshot](https://docs.google.com/document/d/15tLCV3csvjHbKb16DVk-mfUmFry_Rlwo-2uG6KNGsfw/edit#heading=h.gb8m7t8jro1v)
- [Volume Snapshot GA phases](https://docs.google.com/document/d/15tLCV3csvjHbKb16DVk-mfUmFry_Rlwo-2uG6KNGsfw/edit#heading=h.w8v8tpkuw8ac)
- [Kubernetes Data Protection with Velero](https://docs.google.com/document/d/15tLCV3csvjHbKb16DVk-mfUmFry_Rlwo-2uG6KNGsfw/edit#heading=h.iekhl8nl58lo)



[whitepaper]: https://github.com/kubernetes/community/blob/master/wg-data-protection/data-protection-workflows-white-paper.md#what-are-the-missing-building-blocks-in-kubernetes


#### [WG IoT/Edge](https://git.k8s.io/community/wg-iot-edge/annual-report-2021.md#current-initiatives)

The IoT/Edge Working Ground is moving to the CNCF ecosystem. 

#### [WG Structured Logging](https://git.k8s.io/community/wg-structured-logging/annual-report-2021.md#current-initiatives)

In 2021 The structured logging WG migrated kubelet, kube-scheduler, kube-proxy
to the new standard format.

Kubernetes Enhancements
Beta:
- [Structured Logging](https://git.k8s.io/enhancements/keps/sig-instrumentation/1602-structured-logging) v1.23
Alpha:
- [Deprecation of klog specific flags](https://git.k8s.io/enhancements/keps/sig-instrumentation/2845-deprecate-klog-specific-flags-in-k8s-components v1.23









<!-- common shared links -->
[kep]: http://git.k8s.io/enhancements/#is-my-thing-an-enhancement