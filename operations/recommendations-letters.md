# Process for Contributor Recommendation Letters

The Kubernetes Steering Committee is committed to supporting the dedicated
contributors who drive our project forward. We are often asked to provide
letters of recommendation or statements of contribution for purposes such as
visa applications, immigration proceedings, or professional recognition.

This document outlines a formal, consistent, and scalable process for handling
these requests. Its purpose is to enable the Steering Committee to provide
meaningful support while upholding the integrity and accuracy of any statement
made on behalf of the Kubernetes project.

## Roles and Responsibilities

* **Applicant:** The Kubernetes contributor requesting the letter. They are
  responsible for initiating the request, drafting a letter with claims that are
  demonstrable via project artifacts (e.g., pull requests, design docs, meeting
  notes), and obtaining peer verification.

* **Peer Verifier:** A recognized leader (e.g., chair, tech lead, subproject
owner, or maintainer) from the SIGs, WGs or subprojects where the applicant has
contributed. They are responsible for reviewing the applicant's draft letter for
factual accuracy.

* **Steering Committee:** The committee is collectively responsible for the
process. Members individually review submitted materials, ask for clarification
if needed, and provide their signature to signify approval. The collective
signatures constitute the official endorsement.

## The Process

### Step 1: Request Initiation

The Applicant sends their initial request to the Steering Committee's official
contact point: <steering-private@kubernetes.io>.

### Step 2: Applicant Submits Materials

The Steering Committee responds with this process (see Appendix A for a
template). The Applicant is then responsible for submitting the following
materials to the committee:

1. **A Draft of the Recommendation Letter:** All claims and contributions listed
   in the letter must be demonstrable and verifiable through publicly accessible
   artifacts.

1. **A Peer Verification Document:** : This is a formal document (e.g., a shared
   document or a Markdown file) approved by at least one (ideally two) Peer
   Verifiers that validates the claims made in the draft letter. This document
   must contain:

  * A list of the specific claims or contributions made in the draft letter.
  * For each claim, one or more links to the specific artifacts that support it
    (e.g., pull requests, design documents, mailing list discussions, meeting
    notes).
  * A clear statement from each Peer Verifier confirming they have reviewed the
    claims against the provided artifacts and attest to their accuracy.

### Step 3: Committee Review, Signature, and Delivery

Upon receiving the materials, each committee member individually reviews the
draft letter and the peer verification.

* If a member has questions or requires clarification, they should raise them
directly with the Applicant, by responding to the email with submitted
materials, copying  <steering-private@kubernetes.io>. This ensures the entire
conversation history is maintained in a single thread.

* Members who are satisfied with the letter's accuracy and tone proceed to sign
the document.

* The letter is considered officially approved once the [required majority] has
  signed it.

## Appendix A: Template Response to Inquiries

```text
Subject: Re: Your Request for a Recommendation Letter

Hi [Applicant Name],

Thank you for reaching out to the Kubernetes Steering Committee. We are happy to
support you with your request for a recommendation letter.

To ensure the letter we provide is accurate, we follow a standard process described
in https://github.com/kubernetes/steering/operations/recommendations-letters.md

Please provide us with the following:

1. A Draft Letter: A document containing the specific facts and contributions
you would like us to highlight. All claims in the draft must be demonstrable
through public project artifacts.

2. A Peer Verification Document: To validate your draft, please create a
separate document. This document should list each major claim from your letter
and, next to each one, provide direct links to the artifacts that prove it
(e.g., pull requests, design docs, meeting notes).

Once you have created this verification document, please share it with one or
two recognized leaders from the areas you've contributed to. They will
need to review it and add their name, title, and a statement confirming the
accuracy of the information. This will serve as their official signature.

Please send both the draft letter and the signed Peer Verification Document to
us. The committee will then review them and manage the final approval process.

Best regards,

The Kubernetes Steering Committee
```

[required majority]: /charter.md#routine-business
