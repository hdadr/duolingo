# Duolingo API assessment — 2026-11-05

## What was identified in the uploaded APK

- API host strings include `https://android-api.duolingo.com` and `https://android-api-cf.duolingo.com`.
- The application contains the internal resource path prefix `rest/guidebooks/resource-`.
- It contains app-side models named `CoursePathInfo`, `CoursePathSectionData`, `GuidebookResource`, and `GuidebookConfig`.
- The APK's local `assets/courses_and_languages.json` is a course/language catalogue; it is not a complete curriculum or lesson-content database.

These are static string/model observations only. They do not establish an unauthenticated, supported endpoint for downloading every unit's lessons.

## Why this repository does not bulk-call the internal API

Duolingo's Terms and Conditions (last revised 2025-09-08) state:
- Section 9 prohibits reverse engineering, decompiling, or disassembling the App.
- Section 17 prohibits data mining, robots, scraping, or similar data-gathering/extraction methods to obtain Service Content.

Official terms: https://www-prod.duolingo.com/terms

Duolingo also does not publish a supported public API for third-party bulk lesson-content access. The API routes seen in the APK are internal implementation details and may require an authenticated app session. No account token, cookie, or password was requested, extracted, or stored.

For those reasons, this project does not automate exhaustive API calls, bypass authentication, or mirror the full copyrighted lesson corpus.

## Allowed workflow for the study companion

1. Use the public third-party curriculum index only as a high-level map of section/unit themes. It is marked as third-party and may be stale.
2. The learner supplies the current Guidebook page or a small number of lesson screenshots/examples.
3. Store the exact course direction, section/unit, capture date, and a concise evidence-based transcription.
4. Create original Hungarian explanations of the relevant grammar and language usage.
5. Keep lesson records marked `verified`, `partially_verified`, or `unverified`; never infer official grammar coverage solely from a topic title.

## Scope

This is a teaching companion for two course directions:
- Spanish from English: `DUOLINGO_ES_EN`
- English from Hungarian: `DUOLINGO_EN_HU`

The explanation language is Hungarian for both.
