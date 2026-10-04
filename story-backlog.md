## Story 1: Service speed analysis

**GitHub issue:** https://github.com/furkanyurttepe/aipm-user-stories/issues/1

As a customer support service manager,
I want to compare average handling time per request category with and without the policy assistant,
so that I can decide whether the pilot saves time and which categories need attention.

**Acceptance criteria:**
- Each request category shows the average handling time with the assistant and without it.
- The report covers the pilot period selected by the manager.
- Requests without a recorded handling time are excluded and counted separately.

**Open question:** Who defines the request categories, and how many categories keep the analysis meaningful?

**Risk / assumption:** We assume handling time is recorded under the same conditions for every request, and that baseline data from before the assistant exists.

## Story 2: Source confirmation

**GitHub issue:** https://github.com/furkanyurttepe/aipm-user-stories/issues/2

As a support agent,
I want to see the approved policy document behind each suggested answer,
so that I can verify the answer before replying to the customer.

**Acceptance criteria:**
- Each suggested answer shows its policy document title, section, revision, last-updated date, and document status.
- Suggested answers based on retired or unapproved documents are not shown.
- If no approved source is found, the assistant shows "No approved source found" and does not suggest an answer.

**Open question:** Who sets a document's "approved" status, and where is that status stored? What should the agent do next when no approved source is found?

**Risk / assumption:** We assume all policy documents already have revision and date information recorded.

## Story 3: Review flagged answers

**GitHub issue:** https://github.com/furkanyurttepe/aipm-user-stories/issues/3

As a reviewer,
I want to see a list of answers flagged by support agents with their sources,
so that I can decide which answers need correction before they reach customers.

**Acceptance criteria:**
- Each flagged answer shows the original question, the suggested answer, its source document, and the flagging agent.
- A reviewer can mark a flagged answer as "confirmed" or "corrected".
- The flagging agent can see the reviewer's decision on the flagged answer.

**Open question:** Who takes the reviewer role, and how quickly must a flagged answer be reviewed?

**Risk / assumption:** We assume a reviewer is available during support hours; if not, flagged questions may wait too long.

## Story 4: Flag an uncertain answer

**GitHub issue:** https://github.com/furkanyurttepe/aipm-user-stories/issues/4

As a support agent,
I want to flag a suggested answer I am unsure about,
so that a reviewer checks it before I reply to the customer.

**Acceptance criteria:**
- Each suggested answer has a visible option to flag it for review.
- A flagged answer appears in the reviewer's list of flagged answers.

**Open question:** Can a flagged answer be sent to the customer while the review is still pending?

**Risk / assumption:** We assume support agents will flag uncertain answers consistently; this needs validation during the pilot.

## Story 5: Ask a policy question

**GitHub issue:** https://github.com/furkanyurttepe/aipm-user-stories/issues/5

As a support agent,
I want to ask the assistant a customer's policy question in my own words,
so that I can find the relevant approved policy passage without searching documents manually.

**Acceptance criteria:**
- The assistant returns suggested passages only from approved policy documents.
- Each suggested passage links to its section in the source document (see Story 2).
- The support agent can ask the question without leaving the support workflow.

**Open question:** Which support channels and question types are in scope for the four-week pilot?

**Risk / assumption:** Assumption: support agents' questions can be matched to policy passages well enough to be useful; this must be checked against agreed pilot questions, not assumed.

## Story 6: Keep the source library approved

**GitHub issue:** https://github.com/furkanyurttepe/aipm-user-stories/issues/6

As a policy content owner,
I want to add a policy document to the assistant only after it is approved,
so that support agents never receive answers from draft or unapproved content.

**Acceptance criteria:**
- A policy document becomes searchable only after its status is set to "approved".
- Each document in the library shows its status, revision, and approver.
- Unapproved documents never appear in suggested answers.

**Open question:** Who is the policy content owner for the pilot, and which documents are in the first approved set?

**Risk / assumption:** Assumption: an approval process for policy documents already exists outside the assistant.

## Story 7: Retire outdated policy documents

**GitHub issue:** https://github.com/furkanyurttepe/aipm-user-stories/issues/7

As a policy content owner,
I want to retire a policy document when it is replaced or withdrawn,
so that support agents do not answer customers from outdated rules.

**Acceptance criteria:**
- A retired document no longer appears in suggested answers.
- A retired document stays visible to the policy content owner with its retirement date.

**Open question:** Should answers given from a document before it was retired be reviewed again?

**Risk / assumption:** Assumption: the policy content owner learns about policy changes in time to retire documents.

## Story 8: Approve disclaimer wording

**GitHub issue:** https://github.com/furkanyurttepe/aipm-user-stories/issues/8

As a legal reviewer,
I want to approve the disclaimer wording before it is shown with any suggested answer,
so that the pilot does not expose the company to unreviewed legal statements.

**Acceptance criteria:**
- Only disclaimer text marked "legal approved" is shown to support agents.
- If no approved disclaimer exists, the pilot does not show suggested answers to support agents.
- Each disclaimer version records who approved it and when.

**Open question:** Is the disclaimer shown to the support agent only, or also included in the customer answer?

**Risk / assumption:** Assumption: the legal team can review the wording before the pilot starts; if not, the four-week timeline is at risk.

## Story 9: Track answer risk during the pilot

**GitHub issue:** https://github.com/furkanyurttepe/aipm-user-stories/issues/9

As a pilot owner,
I want to see how many suggested answers were flagged and how many of those were corrected,
so that I can show whether the assistant saves time without increasing answer risk.

**Acceptance criteria:**
- The pilot report shows the number of suggested answers, flagged answers, and corrected answers for the selected period.
- Each corrected answer links to the reviewer decision (see Story 3).

**Open question:** What level of corrected answers would make the pilot unacceptable, and who decides?

**Risk / assumption:** Assumption: flagging rates reflect real answer quality; low flagging could also mean agents do not flag consistently (see Story 4).

---

> **Note:** Stories 1–3 were edited and Story 4 was added after an AI review (Phase 2). The AI agent read the original drafts, proposed the changes, and applied them to this file at the AI Project Manager's request. Story 3 was originally drafted by the AI agent and copied into this file by the AI Project Manager. A proposed "No approved source found" story was rejected by the AI Project Manager because Story 2 already covers it. Stories 5–9 were drafted by the AI agent in Phase 4 and were reviewed and accepted by the AI Project Manager. All assumptions still need human validation.
