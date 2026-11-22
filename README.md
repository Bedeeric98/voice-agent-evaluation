# Voice Agent Evaluation

How I test and score AI voice agents: a QA rubric, an audio-based LLM judge calibrated against hand-scored calls, and a regression suite built from bugs found in live test calls.

## At a glance

| | |
|---|---|
| Rubric sources | COPC's critical-error model, a published LLM-grader rubric, turn-taking research, US call-compliance rules |
| Judge calibration | 10 hand-scored calls, 6 disagreements resolved across 6 rubric versions |
| Scored reports | 36+ on SunPath Solar's outbound and inbound test calls |
| Also used on | Desert Comfort's LiveKit call recordings |
| Live test calls | 300+ across three builds |
| Regression suite | 34 scenarios, each from a bug found in a live test call |

## Builds it was used on

- [SunPath Solar speed-to-lead agent](https://github.com/Bedeeric98/sunpath-solar-speed-to-lead-voice-agent)
- [Desert Comfort HVAC receptionist](https://github.com/Bedeeric98/desert-comfort-hvac-receptionist-livekit)

The full method is in [EVALUATION.md](EVALUATION.md).

## License

All rights reserved. Published for viewing only. See [LICENSE](LICENSE).
