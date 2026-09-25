# Keyword research for Jev content

Snapshot 2026-09-20. Volumes are monthly US Google searches from a keyword-data provider called through treg (about $0.001 per call). Live results pages were read through treg's Google SERP endpoint. All 112 keywords found are in [data/keywords.csv](../data/keywords.csv).

## How this was done

1. Started from 20 seed phrases that describe jobs Jev does: routing, classification, judging, guardrails, moderation, spam and triage, plus the company and model names.
2. Asked treg for related keyword ideas for each seed, which returns volume, competition and cost per click.
3. Read the top 10 Google results for five keywords to check what the searcher wants, before deciding what kind of page to write.

## Keywords worth targeting

| Keyword | Monthly searches | Competition | CPC (USD) |
| --- | --- | --- | --- |
| openrouter ai | 12,100 | MEDIUM | $4.21 |
| small language model | 2,900 | LOW | $1.64 |
| claude code router | 2,900 | LOW | $8.53 |
| openrouter free models | 2,400 | LOW | $5.99 |
| llm as a judge | 2,400 | LOW | $12.57 |
| llm gateway | 1,600 | MEDIUM | $15.39 |
| ai guardrails | 1,000 | MEDIUM | $24.64 |
| llm router | 720 | MEDIUM | $7.09 |
| openrouter alternative | 720 | MEDIUM | $11.20 |
| typesafe ai | 320 | LOW | - |
| semantic router | 210 | LOW | $5.34 |
| prompt injection ai | 140 | MEDIUM | $13.48 |
| ai slop detector | 260 | LOW | $3.17 |
| content moderation api | 50 | MEDIUM | $19.36 |
| ai spam filter | 40 | MEDIUM | $22.96 |
| llm classifier | 40 | LOW | - |

## What the search results say

| Keyword | Who ranks now | What it means for a page |
| --- | --- | --- |
| claude code router | A GitHub repo (musistudio/claude-code-router) holds positions 1 and 2, then a Hacker News thread, a vendor guide, a Reddit post | Searchers want a tool to install. A "how to route Claude Code with Jev" tutorial fits. Jev-based routers already exist in this list, such as gargpratyush/jev-router. |
| llm as a judge | An arXiv survey, Langfuse docs, Wikipedia, and guides from Confident AI, Evidently and MLflow | Searchers want an explainer. Jev is a cheap, fast judge that returns a probability, so a comparison "LLM-as-a-judge vs a typed decision model" has a clear angle. |
| ai guardrails | IBM, the Guardrails AI repo, F5, an Australian government page, GeeksforGeeks | Mostly enterprise explainers. The highest cost per click in the set ($24.64) means advertisers pay well. The pi-warden project in this list is a working example. |
| llm router | An academic library (ulab-uiuc/LLMRouter), Braintrust's "best routers in 2026", TrueFoundry, Reddit r/LocalLLaMA, NVIDIA | A roundup page. Jev routers belong in "best LLM routers" lists. |
| typesafe ai | The company's own pages fill positions 1 to 6 | Nothing to win here. Demand is about 320 a month and rising fast, but the company owns the page. |

## Read these numbers with care

- "ai detector" shows about 5,000,000 searches a month because the seed "ai slop detector" surfaced it. That is people checking student essays, not LinkedIn slop. It is not demand for a slop detector. "ai slop detector" itself is about 260 a month.
- "jev" alone is about 4,400 a month, but the word has other meanings, so it does not measure demand for the model.
- Terms with no volume, such as "jev model", "jev api" and "system one model", are too new for the provider. Blank means unknown, not zero.
- Volume is Google US only. It does not include X, Reddit, GitHub or Hacker News, where most Jev discussion happens.

## Where people actually talk about Jev

Search volume undercounts this model because it launched days ago and the conversation is on X and GitHub. Two other signals in this repo:

- GitHub: 150 or more repositories mention Jev or TypeSafe, and 111 of them appeared in a single search sweep. See [data/more-repos.csv](../data/more-repos.csv).
- X: 74 demo posts with video, with the top one at 10,435 likes. See [data/demos.csv](../data/demos.csv).

## Forecast: what happens next, from X and YouTube

Run on 2026-09-20 with the enrich skill's search predictor, a YouTube search through yt-dlp, and the X demo data already in this repo. These are forecasts from early signals, not measurements. Check them against Google data in a few weeks.

### Signals

| Signal | Reading |
| --- | --- |
| YouTube | 65 videos about Jev, published 2026-09-15 to 2026-09-20, with 2.68 million views combined. Largest: Rob Shocks 359,278 views, Greg Isenberg 337,547, Caleb Writes Code 203,281, Sam Witteveen 197,796, Syntax 197,781. Full list in [data/youtube.csv](../data/youtube.csv). |
| X | 74 demo posts with video. The top one has 10,435 likes. Vercel's free-window post has 552,601 views. |
| News | The predictor found 50 articles in 7 days, including TechSpot and 36Kr. |
| Vercel | Reports about 13% of AI Gateway teams tried Jev on day one. This is Vercel's number. |
| Google Autocomplete | 0 suggestions for "jev typesafe" and "typesafe jev". Google has not started suggesting these phrases yet. |
| Google Ads volume | The newest month reported is August 2026, before the launch. September is not in it yet. |

The video counts come from three YouTube searches, so they undercount. The views are lifetime totals for each video, so a video's views are not a daily rate.

### Predictions

1. Search volume for "typesafe ai", "jev ai" and "jev model" jumps in the September and October data. Volume is already rising from a base of about 50 a month in late 2025, and it is the first time the model has had mainstream video and press coverage. The 4,400 a month for "jev" alone is a flat baseline from before launch, so it was some other meaning. If it climbs, that is the model.
2. The next wave is how-to queries. The most-viewed titles say "how to use it", "explained" and "what can you build". The queries that follow are likely "how to use jev", "jev tutorial", "jev vs llm", "jev api" and "jev pricing". Google has no autocomplete for them yet, so a page that exists now can rank before competitors arrive.
3. "jev pricing" and "jev free" spike after Sept 25. Vercel's free window ends that day, and people will look up what it costs.
4. Router and judge content grows. Router repos are the largest group on GitHub, and "claude code router" already has 2,900 a month. A Jev tutorial for it fits both.
5. Roundup lists get crowded fast. At least six other awesome-Jev lists exist. The list that keeps a lead is the one with numbers nobody else has, such as follower counts and reach ratios.

### What could make these wrong

- Launch spikes decay. The videos published on 09-17 and 09-18 hold most of the views, and the 09-20 videos have had less time. If new uploads slow within two weeks, expect volume to fall back.
- The predictor's own "CROWDED" verdict for "jev typesafe" is an artifact. It scored an arbitrary heat input that I typed in, against zero autocomplete data. Ignore it.
- The predictor's Wikipedia check picked the wrong page ("Type safety"), because Jev has no Wikipedia page. Its news check is the signal that worked.
- Google Trends is blocked from this environment, so no trend line is included. Pull one by hand at trends.google.com for "jev" and "typesafe ai" over the past 7 days.

## Suggested content, in order

1. A tutorial for "claude code router", built on a working Jev router from this list.
2. A comparison for "llm as a judge": cost, speed and calibration against a general LLM, using the numbers in the cost table and the limits section.
3. A page for "llm router" that ranks the Jev routers by stars.
4. A guardrails walkthrough that uses pi-warden as the example.

Each page needs a real test run before publishing. This research says what people search for. It does not say Jev beats the alternatives, and the [limits](../README.md#limits-of-jev-113) still apply.
