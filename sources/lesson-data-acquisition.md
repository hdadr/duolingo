# Lesson data acquisition and provenance

## Current public sources

### Duolingo app course catalogue

- Endpoint: https://www.duolingo.com/api/1/version_info
- Use: confirms which learning/base-language directions are supported.
- It does not provide the complete unit or exercise corpus.

### Community-maintained curriculum index

- Spanish from English: https://duolingodata.com/dat/esfen991.html
- English from Hungarian: https://duolingodata.com/dat/enfhu305.html
- Main course index: https://duolingodata.com/
- Use: unit counts, section/CEFR structure, high-level unit topics and course-version observations.
- It is not an official Duolingo API and can lag the app or show different counts between snapshots.

## Server-driven content

The uploaded APK exposes app code and model names for course paths and Guidebook resources. The exact full course content is not stored locally in the APK.

The app includes the Guidebook resource path prefix:

`rest/guidebooks/resource-`

The user's active course path is represented by app models such as `CoursePathInfo`, `CoursePathSectionData` and Guidebook resource models. A complete, account-specific path or Guidebook export is not available from the APK alone.

## Required source priority when teaching

1. Current in-app Guidebook page for the exact course/module/unit.
2. User-provided screenshot or lesson examples.
3. Verified course path or a legitimate account data export provided by the user.
4. Community curriculum index, for identifying unit names and approximate sequence only.
5. General language knowledge, used to explain verified examples—not to invent the unit's syllabus.

## Future lesson-record workflow

For each lesson, store:
- exact course key and Duolingo course ID;
- section/module and unit number;
- localized unit title and original title when available;
- source type (Guidebook, screenshot, API export, curriculum index);
- date observed;
- exact examples supplied by the user;
- grammar points confirmed by the Guidebook or examples;
- separate fields for new grammar, previously learned grammar, vocabulary, and open questions.

Never mark inferred grammar as officially taught. Use `confidence` or `verification_status` fields when the evidence is incomplete.
