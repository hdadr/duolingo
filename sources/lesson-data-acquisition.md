# Lesson data acquisition and derived teaching map

## Goal

Use the learner's current Duolingo progression to infer what language structures are being introduced, practiced, and reinforced. The repository stores only original Hungarian-language conclusions and teaching notes, not copied lesson or Guidebook text.

## Public course map

- Spanish from English: https://duolingodata.com/dat/esfen991.html
- English from Hungarian: https://duolingodata.com/dat/enfhu1005.html (2026-02-20 snapshot, 1005 units)
- Main course index: https://duolingodata.com/

These are community-maintained curriculum indexes, not official Duolingo APIs. They can help identify broad sections, CEFR bands, unit counts and unit themes. The derived progression in each course file is a teaching hypothesis, not an official grammar syllabus.

## APK/API findings

The uploaded APK contains the supported course catalogue and application models for course paths, lessons and Guidebook resources. It also contains the Android API hostnames. However:

- The local APK does not contain the complete course lesson corpus.
- The app's Guidebook URL is supplied by the server; there is no documented public API to bulk-download all Guidebook pages.
- Community documentation of legacy profile endpoints indicates that course-path data can describe sections, units and level metadata, but this is not the same as a complete text lesson corpus.
- Lesson-session endpoints may create a live lesson session rather than act as read-only course-text export endpoints.

Duolingo's published Terms and Conditions prohibit reverse engineering the app and using automated scraping or similar data-gathering methods to obtain Service Content (Sections 9 and 17): https://www-prod.duolingo.com/terms

For that reason, this project does not bulk-call undocumented app endpoints or crawl every lesson. No login token, cookie, password or bearer credential is requested or stored.

## How to build the teaching map

1. Use the public curriculum index to understand the broad progression and unit themes.
2. Use the learner's current in-app Guidebook/screenshot as the immediate evidence for the unit being studied.
3. Analyze relevant examples transiently in the conversation.
4. Save only derived knowledge: grammar concepts, vocabulary categories, skill progression, common Hungarian-speaker errors, prerequisites, and Hungarian explanations.
5. Mark every claim as confirmed, likely, or unknown. A unit title alone is insufficient to confirm a grammar rule.

## Evidence levels

- `confirmed`: directly shown in the current Guidebook or lesson examples.
- `likely`: a pedagogical hypothesis inferred from multiple public topic descriptions or repeated examples.
- `unknown`: insufficient evidence; do not teach as a new official unit objective.

## Supported study tracks

- Spanish from English: `DUOLINGO_ES_EN`
- English from Hungarian: `DUOLINGO_EN_HU`

Both are explained in Hungarian.
