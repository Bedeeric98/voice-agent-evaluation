# Evaluation Method

## 1. The rubric

A voice agent can sound fine and still fail the call. The rubric separates the two.

- **Critical errors.** Borrowed from COPC's critical-error model: some mistakes, like a missed compliance step, fail the call however good the rest is.
- **Conversation quality.** Scored from the audio, not only the transcript: turn-taking, interruptions, silences, repeated lines and how the agent handles objections. The turn-taking criteria draw on published turn-taking research.
- **Compliance.** Based on US call-compliance rules: the AI disclosure, the recording notice and consent, and honouring an opt-out.
- **Grader structure.** The scoring structure follows a published LLM-grader rubric.

## 2. The judge

An audio-capable LLM scores each call from its recording against the rubric. Listening to the audio catches problems a transcript hides, such as the agent talking over the caller or a long silence after a question.

## 3. Calibration

Before the judge's scores were trusted, 10 calls were scored by hand, blind, and compared with the judge's scores.

- The judge and the hand scores agreed on pass or fail for all 10 calls, and disagreed in 6 places.
- The disagreements came from gaps in the rubric and from the judge being lenient on some defects. Fixes included:
  - a "not applicable" path for checks that don't apply to a call, for example the disclosure when the wrong person answered and the lead never came to the phone;
  - splitting conversation flow into near-binary checks, so the judge no longer overlooks named defects such as a repeated greeting;
  - telling a speech-to-text error apart from an agent error.
- All 6 were resolved across 6 rubric versions, re-tested against the hand-scored calls.

## 4. Use

- **SunPath Solar.** The rubric scored SunPath's outbound and inbound test calls, producing 36+ scored reports.
- **Desert Comfort.** The rubric was adapted to review Desert Comfort's LiveKit call recordings.
- **Low scores led to fixes.** Low scores pointed to real bugs in the prompts and the backend. Each was fixed and re-tested.

## 5. Live testing and regression

- 300+ live test calls were run across three builds.
- Bugs found in live test calls became a regression suite of 34 scenarios.

## What is not published

The rubric text, the weights, individual scores, transcripts and recordings stay private.
