# Acceptance Criteria: Policy Assistant Pilot

Each story's criteria match the criteria in `story-backlog.md`. If a criterion changes, update both files.

## Story 1: Service speed analysis

- [ ] Each request category shows the average handling time with the assistant and without it.
- [ ] The report covers the pilot period selected by the manager.
- [ ] Requests without a recorded handling time are excluded and counted separately.

## Story 2: Source confirmation

- [ ] Each suggested answer shows its policy document title, section, revision, last-updated date, and document status.
- [ ] Suggested answers based on retired or unapproved documents are not shown.
- [ ] If no approved source is found, the assistant shows "No approved source found" and does not suggest an answer.

## Story 3: Review flagged answers

- [ ] Each flagged answer shows the original question, the suggested answer, its source document, and the flagging agent.
- [ ] A reviewer can mark a flagged answer as "confirmed" or "corrected".
- [ ] The flagging agent can see the reviewer's decision on the flagged answer.

## Story 4: Flag an uncertain answer

- [ ] Each suggested answer has a visible option to flag it for review.
- [ ] A flagged answer appears in the reviewer's list of flagged answers.

## Story 5: Ask a policy question

- [ ] The assistant returns suggested passages only from approved policy documents.
- [ ] Each suggested passage links to its section in the source document.
- [ ] The support agent can ask the question without leaving the support workflow.

## Story 6: Keep the source library approved

- [ ] A policy document becomes searchable only after its status is set to "approved".
- [ ] Each document in the library shows its status, revision, and approver.
- [ ] Unapproved documents never appear in suggested answers.

## Story 7: Retire outdated policy documents

- [ ] A retired document no longer appears in suggested answers.
- [ ] A retired document stays visible to the policy content owner with its retirement date.

## Story 8: Approve disclaimer wording

- [ ] Only disclaimer text marked "legal approved" is shown to support agents.
- [ ] If no approved disclaimer exists, the pilot does not show suggested answers to support agents.
- [ ] Each disclaimer version records who approved it and when.

## Story 9: Track answer risk during the pilot

- [ ] The pilot report shows the number of suggested answers, flagged answers, and corrected answers for the selected period.
- [ ] Each corrected answer links to the reviewer decision.

## Cross-Cutting Criteria (all stories)

These non-functional criteria apply to every story. Targets marked "agreed" are not defined yet and need a human decision.

- [ ] Only approved pilot users can access the assistant.
- [ ] Questions, suggested answers, flags, and reviewer decisions are logged for audit.
- [ ] Pages load within the agreed internal performance target. *(Assumption: target not yet agreed.)*
- [ ] Results are labeled as pilot results, not validated production results.
