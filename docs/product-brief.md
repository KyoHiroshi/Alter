# Alter — Preliminary Product Brief

Status: initial product foundation, before application implementation.

This document records the supplied product direction. **Confirmed** identifies agreed requirements; **Recommendation** identifies a proposed approach that still needs a decision; **Unresolved** identifies an open question. Recommendations are not implementation commitments. No technology stack has been selected.

## Product vision

**Confirmed.** Alter is a guided GCSE study and mastery platform for UK students. It should reduce the mental load of deciding what to study by providing a structured route, tracking mathematical performance, and prescribing the next appropriate work. Students should understand what to do next, why it matters, and what is required to progress.

The initial subject is AQA GCSE Mathematics (8300), Higher tier, aimed at Year 11 exam-year students. The intended curriculum destination is the complete Higher Maths specification; the amount included in the first MVP remains unresolved.

Longer-term scope includes Biology, Chemistry, Physics and English, followed by other exam boards and student year groups. Teacher and administrator functionality belongs to a future phase.

## Problem statement

**Confirmed product premise.** Students face a planning burden when choosing topics, judging their understanding, and deciding when to revisit material. Completing a lesson does not necessarily demonstrate mastery, and a past success does not guarantee retention. Alter should turn those separate signals into actionable study guidance.

**Recommendation.** Validate this premise with Year 11 students before expanding the product. Research should test whether students understand the prescribed route, can fit required work around school commitments, and can recover from missed deadlines. These are hypotheses to validate, not claims of proven educational impact.

## Target users

**Confirmed.** The primary initial user is a UK Year 11 student studying AQA GCSE Mathematics (8300) at Higher tier. Their principal tasks are to identify gaps, learn or revise material, practise, demonstrate mastery, and retain it through the exam year.

Teachers and administrators are future users rather than MVP users. Other subjects, exam boards and year groups are expansion audiences.

**Unresolved.** The first student cohort, recruitment approach, assumed prior attainment, and support for students whose prerequisite knowledge is substantially below the starting route need definition. Parent or carer involvement has not been specified.

## Product principles

**Confirmed.**

- Prescribe a clear next step through a structured curriculum and evidence of performance.
- Keep curriculum coverage, current mastery, retention, predicted grade, Momentum or consistency, and XP or rewards distinct.
- Base academic marks and mastery on demonstrated mathematical performance. Late submission must not reduce academic marks.
- Require homework before the associated section assessment, and provide targeted remediation and another assessment opportunity after failure.
- Preserve access to previously accessible lessons and revision material.
- Prevent an unmanageable mandatory-work backlog and provide a recovery route for overdue work.
- Treat initial diagnostic topic passes as provisional, subject to confirmation through later mixed assessment.
- Use AI to supplement a defined learning system, with human review before publication of AI-generated persistent curriculum content and separate safeguards for runtime tutoring.
- Consider accessibility from the beginning.

**Recommendation.** Make every recommendation, gate and status understandable to the student. Explain the evidence behind a status and the action needed to change it; avoid presenting uncertain judgments as precise facts.

## Core learning model

**Confirmed.** The core loop is:

1. **Diagnose current knowledge.** Identify strengths and gaps. Diagnostics may provisionally pass topics, but do not establish confirmed mastery on their own.
2. **Recommend the next topic.** Prescribe appropriate work based on the student's current position and performance.
3. **Study lessons and worked examples.** Provide instruction and model mathematical reasoning.
4. **Complete guided practice.** Help students apply the material and identify misconceptions before independent work.
5. **Receive mandatory homework.** Initial homework following first study of a topic is mandatory. Require completion of relevant topic work and required homework before the associated section assessment unlocks.
6. **Assess mastery.** Use timed section assessments to evaluate demonstrated performance, separately from submission timeliness and rewards.
7. **Unlock progression after passing.** If the student fails, assign targeted remedial work and provide another assessment opportunity.
8. **Monitor retention.** After sufficient mastery, additional topic homework may become optional. Reactivate required review or homework when later evidence indicates declining retention or performance, feeding the result back into the next recommendation.

**Recommendation.** Map learning sections to specification content and prerequisite relationships. Use later mixed assessments to check whether students can choose and apply methods without a topic-specific prompt, including confirmation of provisional diagnostic passes.

**Unresolved.** Topic and section granularity, diagnostic length, the recommendation policy, mastery thresholds, reassessment design, and the timing of mixed assessment and retention checks remain open.

## Progress and assessment model

**Confirmed.** A persistent student profile is a central product capability. It retains curriculum status, topic mastery, retention evidence, assessment history, strengths and weaknesses, homework, deadlines, Momentum, rewards, and the evidence behind recommendations. This profile supports continuity across study sessions and informs the next appropriate work.

**Confirmed.** Track the following separately; they must not collapse into one progress score.

| Measure | Meaning and boundary |
| --- | --- |
| Curriculum coverage | Which specification content has been encountered or completed. Coverage alone does not demonstrate mastery. |
| Current mastery | The student's currently demonstrated mathematical performance. Academic marks must not be reduced for lateness. |
| Retention | Evidence that learning persists over time, including later performance that creates a need for review. |
| Predicted GCSE grade | An estimate permitted only when sufficiently broad assessment evidence supports it. Topic completion, XP and isolated assessments are insufficient substitutes. |
| Momentum or consistency | Engagement and regularity of study. Lateness may affect this without changing academic marks. |
| XP and rewards | Motivational recognition, kept separate from academic attainment. Late work may earn less XP. |

**Confirmed.** Initial diagnostics may provisionally pass topics; later mixed assessment should confirm mastery. Assessment failure must lead to targeted remediation and a further assessment opportunity. Declining performance should trigger required review.

**Recommendation.** Retain assessment history alongside the current status so a later review need does not erase previous achievement. Distinguish “insufficient evidence” from low performance. Present provisional, confirmed and review-required statuses clearly, with the supporting evidence and its recency.

**Recommendation.** Withhold a grade prediction until an agreed evidence standard is met, then communicate uncertainty and evidence coverage. A prediction should not be presented as an official result or guarantee.

**Unresolved.** Define sufficient breadth, recency and independence of evidence for mastery and grade prediction; treatment of hints, repeated questions and partial credit; and how supported grade predictions relate to applicable official grade boundaries. Deterministic scoring rules and handling of mathematical working need definition before implementation.

**Confirmed future direction, not an MVP commitment.** Mock-paper and past-paper analysis is an important future capability. Students may eventually record or submit paper results. Alter should map lost marks and question performance to curriculum topics, update the persistent student profile with the resulting evidence, and identify areas requiring work.

**Unresolved.** Copyright, paper ingestion, marking reliability and the weighting of paper evidence alongside other assessment evidence require decisions before this capability is introduced.

## Deadline and progression model

**Confirmed.** Initial homework following first study of a topic is mandatory. After sufficient mastery is demonstrated, additional homework for that topic may become optional. Later evidence of declining retention or performance can reactivate required review or homework.

**Confirmed.** Completing relevant topic work and required homework unlocks the associated timed section assessment. A preparation window and assessment deadline may be used. Passing unlocks further progression; failure produces targeted remediation and a fresh assessment opportunity. Previously accessible lessons and revision material remain available, including when a student is overdue or needs review.

Lateness may reduce XP, damage Momentum, and keep progression gates locked. It must not reduce academic marks or distort mastery. Whether late work meets a progression requirement is a separate decision from the mathematical quality of that work.

The system must prevent an unmanageable backlog of mandatory work and provide a recovery route for overdue work.

**Recommendation.** Limit active mandatory assignments and avoid continuing to add obligations while a student is overwhelmed. A recovery flow should identify outstanding requirements, prioritise essential work, and produce a manageable revised schedule. Any consolidation or replacement of assignments should preserve the learning evidence needed to unlock an assessment.

**Recommendation.** Show students exactly what is blocking progression and how to recover. Completing late homework should satisfy its completion requirement, subject to the same completion standard as on-time work; any additional timing restriction needs an explicit product decision.

**Unresolved.** Define homework completion, thresholds for optional homework and reactivation, assignment rules, deadline setting, workload limits, grace periods, rescheduling, reward penalties, and how retention review interacts with current work and gates. Assessment timing, preparation windows, pass thresholds and reassessment rules remain open. Decide how recovery works near exams and after a prolonged absence.

## AI boundaries

**Confirmed.** AI supplements the learning system rather than defining it. Appropriate uses include alternative explanations, hints, worked examples, misconception analysis, and explanations of lost marks.

Curriculum structure, canonical answers, official mark schemes, grade boundaries and deterministic scoring must not depend solely on AI. AI-generated lessons, questions, examples, canonical answers, mark schemes and other persistent curriculum content require human review before publication. AI-assisted drafting is allowed within that review requirement.

Personalised runtime tutoring responses cannot realistically receive individual pre-publication human review. Runtime AI must not independently change canonical answers, marks, mastery, predicted grades or progression decisions. It would require grounding in approved material, guardrails, monitoring, error reporting and clear boundaries.

User-supplied API keys may be considered later and are not an MVP requirement.

**Recommendation.** Build the initial learning loop around reviewed content and defined scoring. Define and evaluate runtime tutoring safeguards before introducing personalised AI responses to students.

**Unresolved.** Whether runtime AI is included in the MVP remains open. Decide which AI capabilities, if any, are necessary for the first MVP, the detailed runtime boundaries and safeguards, and how errors are reported and corrected.

## Content strategy

**Confirmed.** Use licensed or open educational resources where appropriate, and allow AI-assisted drafting followed by human review. Track content provenance, licence, exam board, tier, specification version, author/reviewer and review status. Alter must not imply affiliation with or endorsement by AQA.

**Recommendation.** Maintain a content register linking each lesson, example, question, answer and assessment item to the relevant curriculum content. Record source references, usage conditions, review history and content revisions so corrections can be traced to affected learning material and assessments.

**Recommendation.** Require a release check for mathematical accuracy, pedagogical clarity, accessibility and permitted use. Assign responsibility for canonical answers and scoring rules. Public availability should not be treated as permission to reproduce a resource.

**Unresolved.** Content suppliers, permissions, reviewer capacity, review criteria, specification-version policy and the process for correcting published errors remain to be established. The exact specification edition and source documents have not yet been selected or verified in this brief.

## Accessibility and platform requirements

**Confirmed.** The initial product is a laptop-optimised responsive web application. Preserve tablet compatibility from the beginning and polish it later. Phones are not an initial full-study target.

Accessibility must be considered from the beginning, including keyboard operation, visible focus, readable contrast, zoom and responsive reflow. Avoid hover-only and drag-only interactions. Mathematical content and inputs need accessible alternatives.

**Recommendation.** Include accessibility in content review and interaction acceptance criteria. Validate the core learning flow with keyboard and assistive technology use, and test touch interactions on tablets. Provide accessible representations and input methods for notation, diagrams and worked reasoning rather than relying solely on visual rendering or pointer gestures.

**Unresolved.** Select a formal accessibility target, supported browser and device baseline, mathematical input approach, and scope of the limited phone experience. A reduced phone scope must not undermine the confirmed reflow and accessibility requirements.

## Initial MVP direction

**Confirmed.** The MVP focuses on Year 11 AQA Higher Maths, the guided learning loop, a persistent student profile, separate progress measures, mandatory homework and progression, recovery, reviewed content, and accessibility. Teacher/admin functionality and user-supplied API keys are outside the MVP. Mock-paper and past-paper analysis is a future capability, not an MVP commitment.

**Recommendation.** Start with a coherent, limited curriculum slice that includes prerequisite relationships and enough assessment material to exercise the complete loop. Validate diagnosis, topic recommendation, lessons, practice, homework, mastery assessment, remediation, mixed confirmation and retention review before expanding curriculum breadth.

**Recommendation.** Include a clear next-work view, understandable progress evidence, and an overdue-work recovery flow. Use a manageable editorial process for review and provenance; a dedicated teacher/admin application is not required for that process. Keep grade prediction unavailable until its evidence requirements are met. AI features can follow once the underlying loop works reliably.

**Unresolved.** The first curriculum slice, pilot size, launch criteria and whether complete specification coverage is required for a public launch need explicit decisions. No implementation technology, architecture or delivery dates are committed.

## Explicit non-goals

**Confirmed for the initial scope.**

- Subjects beyond AQA GCSE Mathematics (8300), Higher tier, and audiences beyond the initial Year 11 focus.
- Teacher or administrator product functionality.
- A full phone study experience.
- A requirement for students to supply their own AI API keys.
- Academic penalties for late submission, or using XP and consistency as substitutes for mastery.
- Grade predictions without sufficiently broad assessment evidence.
- AI as the sole authority for curriculum, canonical answers, official mark schemes, grade boundaries or deterministic scoring.
- Removal of access to previously accessible lessons and revision material as a progression penalty.
- Claims of AQA affiliation or endorsement.

**Confirmed for this foundation stage.** Application scaffolding, dependency installation, technology selection and creation of repository agent instructions are outside this work.

## Risks and unresolved decisions

The following are planning risks, not claims that failures have occurred.

| Risk or open area | Decision or validation needed |
| --- | --- |
| Incorrect mastery judgments | Calibrate diagnostics, pass criteria, question variety and mixed confirmation; distinguish supported practice from independent evidence. |
| Misleading grade predictions | Establish a defensible evidence threshold and uncertainty presentation before enabling predictions. |
| Backlog and disengagement | Validate assignment limits, realistic workload, recovery and deadline policies with exam-year students. |
| Content quality and rights | Secure usable resources and sufficient reviewer capacity; define release and correction processes. |
| AI-generated errors | Review persistent curriculum content before publication; define grounding, guardrails, monitoring, error reporting and boundaries for runtime tutoring. Decide whether runtime AI belongs in the MVP. |
| Mock-paper and past-paper analysis | Resolve copyright, paper ingestion, marking reliability and evidence weighting before using paper results to update profiles and recommendations. |
| Inaccessible mathematics | Validate notation, diagrams, input methods and assessment interactions with relevant users and assistive technologies. |
| Retention versus curriculum pace | Decide how required review is prioritised without creating excessive obligations or preventing useful revision. |
| Student data and safeguarding | Define data collection, retention, account access, age-appropriate protections and any consent requirements before a student pilot. These policies are not settled here. |
| Delivery scope | Decide initial curriculum breadth, staffing, operating costs and success criteria without committing prematurely to full subject expansion. |

**Recommendation.** Evaluate the pilot using evidence of learning, retention, ability to identify the next task, and successful recovery from overdue work. Track engagement separately; XP accumulation alone is not evidence of educational success.

## Phased roadmap

**Recommendation.** The sequence below is proposed; it carries no dates or committed release sizes.

| Phase | Focus and exit evidence |
| --- | --- |
| 1. Product and learning definition | Validate student needs; define the curriculum slice, assessment rules, workload and recovery policies, content review process and accessibility target. Select implementation technology in a later decision. |
| 2. Complete-loop MVP | Deliver a reviewed curriculum slice and the entire learning loop, including remediation, overdue recovery and retention review. Demonstrate usable laptop and compatible tablet flows with distinct progress measures. |
| 3. Pilot and calibration | Test learning and usability with the initial audience; refine assessments, recommendation rules, workload and accessibility from evidence. Establish whether grade prediction is sufficiently supported. |
| 4. Higher Maths coverage | Expand towards the complete Higher specification while maintaining review quality, assessment breadth and retention support. Polish tablet use. |
| 5. Broader product | Develop mock-paper and past-paper analysis as separately scoped future work. Extend to Biology, Chemistry, Physics and English; later add other exam boards and year groups. Consider teacher/admin functionality and optional AI capabilities as separately scoped work. |

**Unresolved.** Expansion order within the broader product, staffing, dates and release criteria require later decisions informed by the earlier phases.
