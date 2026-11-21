# When AI says no: 60 yes-or-no questions for ChatGPT, Gemini and Claude

An open dataset from a small test run on 19 and 20 November 2026. We asked ChatGPT, Gemini and Claude the same 60 yes-or-no questions about apps and phones. Each question was asked in a new chat. We then graded each answer against the truth, which we checked before asking.

Full write-up: https://regga.ai/study

## What is in it

One file: ai-says-no-2026-11.csv, with 60 rows.

| Column | Meaning |
|---|---|
| id | A1-A40, B1-B10, C1-C10 |
| group | new_feature: added between November 2025 and November 2026, true answer yes. niche_product: a small product that exists, true answer yes. control: true answer no |
| question | The exact question, in English |
| true_answer | yes or no |
| truth_note | Short note on the truth: version, date or product names |
| truth_sources | Sites we used to confirm the truth (empty where it was confirmed earlier) |
| chatgpt | Grade for ChatGPT, 19 November |
| chatgpt_rerun | Grade when the wrong answers were asked again on 20 November (empty if not asked again) |
| gemini | Grade for Gemini |
| claude | Grade for Claude |

Grades:
- correct: the answer matches the truth.
- wrong_no: says it can't be done or doesn't exist, but it can.
- self_corrected: starts with no, then fixes itself in the same answer.
- partial: part right, for example a workaround that misses the built-in way.
- wrong_yes: says yes to something that can't be done. This did not happen.

## Main results

- On the 40 new features, ChatGPT said no to 16, Gemini to 4 and Claude to 0.
- None of the three said yes to any of the 10 controls.
- Asked again the next day, ChatGPT gave the same wrong no on 15 of the 16. On the last one it offered a workaround but still missed the built-in setting.

## How we tested

- 60 questions in English, picked by hand: 40 features added in the last 12 months, each confirmed in at least two sources; 10 small products that exist; 10 questions where the true answer is no.
- ChatGPT: Plus account, temporary chat, no memory or custom instructions, default model (Instant).
- Gemini: free account, temporary chat, default mode.
- Claude: Max account, incognito chat, default model (Opus 5.5).

## Limits

- The three setups are not equal: Claude ran on a paid top tier and Gemini on the free tier.
- The questions were picked by hand, so these numbers show how often a confident no appears on fresh features. They are not a general error rate.
- One person graded the answers. The same question can get a different answer on another day.
- The full AI answers are not included, only the grades.

## License

CC BY 4.0. You can use, share and adapt the data with credit to Regga (regga.ai/study).

## About

Made by Regga. When AI say no take a scecond look. https://regga.ai
