---
name: interaction-design
description: "Design, improve, or review software interactions. Use for UI/UX work that requires decisions about task flows, control behavior, state feedback, or recovery, and for reviews of whether an existing flow is coherent and its timing feels natural."
---

# Interaction Design

This is an English translation of [SKILL.md](SKILL.md). The Chinese original is the primary version for maintenance and validation.

Start with the task the user needs to complete. Consider the existing interface, business rules, and system capabilities. Determine where users enter, what context they bring, and how they know the task is complete. Across pages, make the next step easy to find and let users return to the relevant item to continue their work.

## Connect actions with feedback

For a particular action, work out the current state, available actions, system response, and what the user can do next. Cover waiting, partial completion, failure, retry, or departure as the real task requires. Present feedback where users can connect it to the action they just took. For asynchronous work, distinguish a request acknowledgment, a confirmed result, and a result that is still pending. Make sure the system can support any cancellation, undo, or retry the interface promises.

Use the frequency, consequences, and recoverability of an action to decide when to execute it immediately, offer undo, or ask for confirmation. If saving fails, for example, retain the user's input in place, explain what still needs to be saved, and give them a way to resume the task. When states can coexist, convey their meanings and available actions to visual design. A selected record may also be awaiting review.

Use focus, spatial continuity, and appropriate transitions to express the start and result of an action. During a sequence of actions, watch whether feedback keeps up with input and whether users have to wait for a previous animation after the next step becomes available. Handle keyboard focus, touch, or pointer input as appropriate. Keep state changes recognizable with reduced motion. For chart filters or linked selections, specify what subset of the data changes and what to restore when the selection is cleared.

## Walk through and deliver

When building or improving an interaction, implement the main path and relevant branches in the requested flow design, prototype, or running interface. When there is an interactive artifact, start from the normal entry point and work toward the task goal. Check relevant returns, error recovery, or interruptions, and observe where input, selection, and focus end up.

When reviewing an existing interaction, describe in the conversation the user's starting state, their action, the observed feedback, where the flow is smooth or blocked, and what could improve it. Prioritize problems that affect task completion or repeatedly occur on frequently used paths. Screenshots can support judgments about entry points and visible states. Use a walkthrough or recording as evidence for responses, timing, and recovery. With only static material, mark those judgments as pending verification.
