# APK extraction findings

Checked: 2026-11-05

## Input APK

- File name: `rg-setup.apk`
- File size: 187,306,110 bytes
- SHA-256: `400fa1acea871bfbb6b3892bf48f47752862364fc02a56d1127363180e49f6f3`
- Extracted asset: `assets/courses_and_languages.json`
- Asset size: 53,617 bytes
- Asset SHA-256: `0fc01fc24543866bc98d7ddcc9a112b65e0d63da8cfaaae289beacbb82d361c6`
- Number of course entries in this APK asset: 301

## Confirmed course records

| Course ID | Learning language | Base language | Mobile supported |
|---|---|---|---|
| `DUOLINGO_ES_EN` | Spanish (`es`) | English (`en`) | Yes |
| `DUOLINGO_EN_HU` | English (`en`) | Hungarian (`hu`) | Yes |
| `DUOLINGO_ES_HU` | Spanish (`es`) | Hungarian (`hu`) | Yes |

## What the APK contains

The asset is a course/language catalogue. It confirms that the requested course pairs exist in the installed app build.

The APK also contains application code and model names for course paths and Guidebook resources. A string search found the Guidebook resource path prefix `rest/guidebooks/resource-` and app models named `CoursePathInfo`, `CoursePathSectionData`, `GuidebookResource` and related classes.

## What it does not contain

There is no offline course database with the full set of unit lesson prompts, example sentences, answer alternatives, or Guidebook explanations in the extracted APK assets. The actual learning-path and Guidebook content is server-driven.

Therefore this extraction must not be described as a full lesson-corpus extraction. Course curriculum maps stored elsewhere in this repository are explicitly attributed to their public third-party source.

## Safety and account handling

No Duolingo password, login token, cookie, JWT, or private account data was extracted or stored. Do not ask the user to paste a password or bearer token into chat or commit credentials to this repository.

The APK references server-side Guidebook resources, but the resource identifier and user-specific path data are not available from the local course catalogue alone.
