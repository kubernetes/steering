# Onboarding

This document covers steps needed to onboard new Steering Committee
members and off-board emeritus members.

- [ ] All new members must complete the [Inclusive Leadership Training]
      within 30 days from the date of their appointment:
  - [x] New steering member @gh_alias: <link to certificate>
- [ ] Update the following files in the respective repos:
  - [ ] [kubernetes/steering]: `OWNERS_ALIASES` and `README.md`
  - [ ] [kubernetes/community]:
      - [ ] `sigs.yaml` (SC members and liaisons) and auto-generated content
      - [ ] slack usergroup - `communication/slack-config/usergroups.yaml`,
            `communication/slack-config/users.yaml`
  - [ ] [kubernetes/org]: `OWNERS_ALIASES` and the `steering-committee`
        GitHub team
  - [ ] [kubernetes/website]: `OWNERS_ALIASES`
  - [ ] [kubernetes/k8s.io] - Update steering@kubernetes.io,
        steering-private@kubernetes.io, and steering-emeritus@kubernetes.io
        in `groups/groups.yaml`
- [ ] Add new members to the steering-private, steering-gb-rep-private and
      steering-cncf-rep-private slack channels.
- [ ] Remove emeritus members from steering-private, steering-gb-rep-private and
      steering-cncf-rep-private slack channels.
      slack channel and `steering-cncf-rep-private` remove emeritus members.
- [ ] Add new members to the CNCF Service Desk and remove emeritus
      members.
- [ ] Add new members to the [cncf-kubernetes-maintainers] mailing list.
      Use `make MAINTAINERS_LIST=true` [generator] to get updated list.
- [ ] Add new members to the [Public CNCF Maintainer List] and remove emeritus
      members. Use `make MAINTAINERS_LIST=true` [generator] to get updated list.
- [ ] Transfer Community Group [liaison assignments] from emeritus members to
      new members.
- [ ] If a Google Workspace [top-level account] is owned by an emeritus member,
      transfer it to an existing member.
  - [ ] SCx - emeritus steering member: new steering member
  - [ ] Update [top-level account] document, if necessary
- [ ] Reach out to SIG-ContribEx to add new members to 1password and remove
      emeritus members.
- [ ] Set up a private meeting to go over backlog.
- [ ] Update onboarding docs, if necessary.


[Inclusive Leadership Training]: /charter.md#inclusive-leadership-training
[kubernetes/steering]: https://github.com/kubernetes/steering
[kubernetes/community]: https://github.com/kubernetes/community
[kubernetes/org]: https://github.com/kubernetes/org
[kubernetes/website]: https://github.com/kubernetes/website
[kubernetes/funding]: https://github.com/kubernetes/funding
[kubernetes/k8s.io]: https://github.com/kubernetes/k8s.io
[liaison assignments]: https://git.k8s.io/community/liaisons.md
[cncf-kubernetes-maintainers]: https://lists.cncf.io/g/cncf-kubernetes-maintainers
[generator]: https://github.com/kubernetes/community/blob/master/generator/README.md
[Public CNCF Maintainer List]: https://docs.google.com/spreadsheets/d/1Pr8cyp8RLrNGx9WBAgQvBzUUmqyOv69R7QAFKhacJEM/edit
[top-level account]: /README.md#top-level-accounts
