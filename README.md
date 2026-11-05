# Duolingo study companion data

A private, multi-course reference repository for preparing Hungarian-language explanations that accompany Duolingo lessons.

## Supported learning directions

| Repository key | Duolingo course ID | Learning language | Base language | Explanation language |
|---|---|---|---|---|
| `es-en` | `DUOLINGO_ES_EN` | Spanish | English | Hungarian |
| `en-hu` | `DUOLINGO_EN_HU` | English | Hungarian | Hungarian |

The two courses are kept separate. The explanation language is Hungarian in both cases.

## Data available now

- Course identifiers and support flags extracted from the uploaded APK's `assets/courses_and_languages.json`.
- Public curriculum snapshots for Spanish from English and English from Hungarian, with source dates and freshness notes.
- The user's screenshot capture for Module 2, Unit 22, stored separately because the screenshot alone does not conclusively identify the course direction.
- A schema and ingestion rules for adding future Guidebook pages, lesson screenshots, examples and verified grammar points.

## Important distinction

The APK does **not** contain the actual language-course lesson corpus. It contains the application and a list of supported course IDs. Lesson paths and Guidebook resources are server-driven. This repository therefore does not claim to contain every exercise, sentence, audio file or official explanation.

Curriculum topic labels are orientation metadata, not proof that a particular grammar rule is taught in that unit. For exact explanations, use the in-app Guidebook and user-provided lesson material as the primary source. Do not invent grammar topics from a unit title.

## Repository layout

- `courses/registry.json` — the two requested course identities and source links.
- `courses/es-en/course.json` — Spanish-from-English course map and unit currently identified.
- `courses/en-hu/course.json` — English-from-Hungarian course map.
- `captures/` — user-provided screenshots transcribed as evidence, with uncertainty labelled.
- `sources/` — APK extraction findings, endpoint notes and source provenance.
- `schemas/` — structure for adding future lesson records.

## Teaching workflow

1. Identify the course by its exact source/target direction.
2. Identify the section/module and unit from the user's current Duolingo screen.
3. Consult the matching curriculum snapshot for orientation only.
4. Prefer the current in-app Guidebook and screenshots for actual grammar content and examples.
5. Separate new grammar from previously encountered grammar.
6. Save only verified information; label uncertain or inferred items explicitly.
7. Explain in Hungarian, regardless of the course's base language.

Last initialized: 2026-11-05.
