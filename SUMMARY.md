# Summary: User Stories Workshop

This file summarizes, step by step, how the exercises in this repository were
completed. The scenario was the **Policy Assistant Pilot** from
[05 - Session Handout](05-session-handout.md): an internal AI assistant that
helps support agents find answers in approved policy documents.

The work followed the AI Project Manager role: the PM framed the work and made
every decision; the AI agent (Claude Code) critiqued, drafted, and operated
GitHub only after approval.

## Results at a Glance

| Output | Where | Status |
|---|---|---|
| GitHub Project "User Stories Workshop" | GitHub Project #5 | 6 columns, 3 custom fields, 9 items |
| Backlog issues | Issues #1–#9 | 9 user stories, each with acceptance criteria |
| Story backlog | [story-backlog.md](story-backlog.md) | 9 stories with issue links |
| Acceptance criteria | [acceptance-criteria.md](acceptance-criteria.md) | Checklist per story + cross-cutting criteria |
| Epic map | [epic-map.md](epic-map.md) | 4 epics, dependencies, scope, assumptions |
| Ready and Done agreements | [ready-done-agreements.md](ready-done-agreements.md) | Short DoR and DoD |
| AI collaboration log | [ai-collaboration-log.md](ai-collaboration-log.md) | 8 decisions (accepted, edited, rejected) |

## Step 1: Lessons 01–04 and Review Questions

The four theory modules were read in order, and the "Check Your Understanding"
questions were answered without opening the solutions first. Answers were then
compared with the official solutions.

| Module | Key takeaway |
|---|---|
| 01 – User Stories Foundations | Describe the problem before the solution; name a specific role; AI products also involve reviewers and operators. |
| 02 – INVEST and Acceptance Criteria | A story is a starting point for discussion; criteria must be observable and testable; split large stories by workflow step, role, risk, or deliverable. |
| 03 – Epics, Requirements, and Scope | Epics are large bodies of work; non-functional needs (traceability, privacy, monitoring) decide whether an AI product is acceptable at all; missing scope boundaries cause scope creep. |
| 04 – Ready, Done, and Delivery Quality | DoR is an optional team agreement, DoD is a formal quality commitment; AI outputs are uncertain and source-dependent, so "done" needs evidence. |

## Step 2: Tool Setup

- Installed the GitHub CLI with `brew install gh`.
- Logged in with `gh auth login -s project` (scopes include `repo` and `project`).
- Confirmed the remote points to the PM's own copy: `furkanyurttepe/aipm-user-stories`.

## Step 3: Phase 1 – Manual Warm-Up

Three user stories were written before using the agent, each with two
acceptance criteria, one open question, and one risk or assumption.

- **Story 1 (manual):** a support service manager sees which request categories take longer.
  The first drafts were off-scenario and too broad ("maximize customer satisfaction");
  they were narrowed step by step into an observable need.
- **Story 2 (manual):** a support agent sees the approved source document behind each answer.
- **Story 3 (agent-drafted):** a reviewer reviews flagged answers. The PM chose to copy an
  agent example and recorded this in the log.

## Step 4: Phase 2 – Agent Critique

The agent reviewed the three stories with INVEST using the handout prompt.

- **Edited:** Stories 1–3 were sharpened (comparison with and without the assistant,
  assistant refuses instead of the agent, smaller reviewer story).
- **Accepted:** a new story "Flag an uncertain answer", a missing prerequisite for Story 3.
- **Rejected:** a new story "No approved source found", because Story 2 already covers it.
  The escalation question moved into Story 2's open question.

## Step 5: Phase 3 – GitHub Project

Created the project **User Stories Workshop** from the GitHub web UI.

- Columns: `Backlog → Ready → In progress → Review → Blocked → Done`
- Custom fields: **Work type**, **Story quality**, **Risk area** (single select);
  **Owner** uses the built-in Assignees field.
- "Import items from repository" was turned off so issues could be added manually later.
- Two mistakes were found and fixed: the column order, and field options entered as one
  comma-separated value instead of separate options.

## Step 6: Phase 4 – Agent-Built Backlog

The agent created the remaining workshop files. The prompt was extended by the
PM to keep the approved stories, not re-add the rejected story, and cover legal review.

- Stories 5–9 were added: ask a policy question, keep the source library approved,
  retire outdated documents, approve disclaimer wording, track answer risk.
- All six scenario constraints are now covered by at least one story.
- The PM reviewed the result against the handout checklist and accepted it.

| Epic | Stories |
|---|---|
| E1: Find approved answers | 5, 2 |
| E2: Keep the source library trustworthy | 6, 7 |
| E3: Human and legal review | 4, 3, 8 |
| E4: Prove pilot value | 1, 9 |

## Step 7: Phase 5 – Agent-Operated GitHub

Following [06 - Agent-Operated GitHub Workflow](06-agent-operated-github-workflow.md):

1. The agent prepared a plan (titles, bodies, labels, commands) without executing it.
2. The PM approved the plan.
3. The agent created 5 labels and 9 issues (#1–#9, matching Stories 1–9).
4. Issue URLs were saved in `story-backlog.md`.
5. The PM verified the issues with `gh issue list`.
6. The agent compared GitHub with the backlog: no missing issues, no duplicates,
   every story has acceptance criteria. One title mismatch was found (the agent had
   changed Story 1's capitalization without saying so) and fixed in the local files.

## Step 8: Optional – Issues Added to the Project

After approval, the agent added all 9 issues to Project #5 and set their fields:
Status **Backlog**, Work type **Story**, Story quality **Needs refinement**
(open questions are not answered yet), and a Risk area per story.

## Step 9: Phase 6 – Final Verification

The agent produced an audit summary (files, issues, commands, open assumptions,
weak stories, actions deferred to the PM). All "Done Means" items were confirmed:
the project, the issues, the local backlog files, the log, and an example where the
agent was rejected or corrected.

## Step 10: Bonus – MCP Comparison

No GitHub MCP server was connected, so all GitHub work used `gh`.

| Dimension | `gh` command line | MCP or connected tool |
|---|---|---|
| Visibility | Every command is explicit | Tool calls are more abstract |
| Setup | `gh` install and login | Server registration, token or OAuth, permissions |
| PM duty | Approve commands and verify output | Approve tool access and verify state |

**Key point:** `gh` commands are visible, MCP is more abstract; verification stays with the PM.

## Step 11: Git

The new files were committed and pushed manually by the PM, one command at a time:
`git status` → `git diff` → `git add` → `git commit` → `git push`, then the push was
verified on GitHub. Before committing, files that had been renamed with number prefixes
were renamed back to the names required by the handout.

## Open Items

- All assumptions in the stories still need human validation (see [epic-map.md](epic-map.md)).
- Weak points to revisit: Story 8 may block the pilot if legal review is late;
  Stories 5 and 2 overlap; Story 1 needs baseline data.
- Ask the instructor about the submission format and whether the private repository
  and project need to be shared.

> **Note:** This summary was written by the AI agent at the AI Project Manager's request.
