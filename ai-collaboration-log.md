# AI Collaboration Log

| Prompt or request | Accepted | Edited | Rejected | Reason |
|---|---|---|---|---|
| Phase 1: Asked the agent to draft Story 3 (reviewer, flagged answers) | ✓ |  |  | Two stories were written manually; Story 3 was drafted by the agent and copied into story-backlog.md by the PM. |
| Phase 2: INVEST critique of Stories 1–3 (handout prompt) |  | ✓ |  | The PM chose to edit all three stories and delegated the edits to the agent, then reviewed and approved the result. Kept from the original drafts: category question (Story 1), "document status" (Story 2), reviewer-availability risk (Story 3). |
| Phase 2: Agent proposed a new story "Flag an uncertain answer" | ✓ |  |  | Missing prerequisite for Story 3: reviewers can only review answers that agents can flag. Added as Story 4. |
| Phase 2: Agent proposed a new story "No approved source found" |  |  | ✓ | Story 2 already covers this case (the assistant shows "No approved source found" and does not suggest an answer). The escalation question was moved into Story 2's open question instead. |
| Phase 4: Agent created the workshop backlog (Stories 5–9, epic-map.md, acceptance-criteria.md, ready-done-agreements.md) | ✓ |  |  | PM reviewed Stories 5–9 against the handout checklist and accepted them. All six scenario constraints are now covered, including legal review (Story 8). Known weak points (Story 8 may block the pilot if legal review is late; Story 5 overlaps with Story 2) were noted but kept. |
| Phase 5: Agent planned and ran `gh label create` (5 labels) and `gh issue create` (9 issues) | ✓ |  |  | PM approved the plan before execution. Issues #1–#9 match Stories 1–9; URLs saved in story-backlog.md. |
| Phase 5: Agent compared GitHub issues with story-backlog.md |  | ✓ |  | No missing issues, duplicates, or stories without acceptance criteria. One title mismatch found: the agent had changed Story 1's title case in the plan without saying so. PM chose to align the local files to the GitHub title ("Service speed analysis"). |
| Optional: Agent added issues #1–#9 to the User Stories Workshop project and set fields | ✓ |  |  | PM approved both the item-add commands and the proposed field values (Status: Backlog, Work type: Story, Story quality: Needs refinement, Risk area per story) and verified the board. "Needs refinement" was chosen because open questions are not yet answered. |
