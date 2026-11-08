# Spanish course public module-description crosswalk

Checked: 2026-11-05

## Scope

The requested task is to align explanations with the user's progress in the Spanish-from-Hungarian Duolingo course while storing only original pedagogical conclusions. Do not archive raw Duolingo exercise text.

## Why we do not call an internal endpoint from the APK

The uploaded APK is a Unity/IL2CPP application package, not a plain Android Java application. The local assets include the course/language catalogue, but do not include a complete course module database.

Duolingo's current Terms and Conditions explicitly prohibit deriving source code from, reverse engineering, decompiling or disassembling the App (Section 9), and prohibit automated data-gathering or extraction methods for Service Content (Section 17):
https://www-prod.duolingo.com/terms

A community-maintained API reference also notes that Duolingo does not provide an official public third-party API and that the community-described REST surface is unsupported:
https://github.com/api-evangelist/duolingo/blob/main/graphql/duolingo-graphql.md

Therefore, this project does not reverse engineer or call undocumented internal endpoints.

## Open source replacement for module descriptions

The public community-maintained Duolingo Data course outline provides:
- all eight Spanish-from-Hungarian section descriptions;
- the CEFR label and number of units per section;
- a topic/learning-objective title for each of the 991 units in the published snapshot;
- a separate index of distinct teaching-objective labels.

Sources:
- Course outline: https://duolingodata.com/dat/esfhu991.html
- Teaching-objective index: https://duolingodata.com/dat/esfhu991-d.html

These are public third-party curriculum maps, not official API responses. The detailed course page identifies its snapshot as 2026-03-02. User-visible course progress in the Duolingo app remains the source of truth if its current rollout differs.

## Current module — Section 2, Unit 22

Public course-map theme: diet / eating habits.

Pedagogical interpretation:
- communicative goal: discuss what and how one eats, dietary preferences, and eating habits;
- likely language functions: describe quantities, ask about food and habits, state preferences, describe routines, and evaluate food choices;
- possible grammar candidates: present indicative; quantity expressions and interrogatives; noun gender/number and noun–adjective agreement; definite/indefinite articles; preference verbs; gustar-type constructions; impersonal se for general eating customs.

Evidence level:
- The diet/eating-habits theme is directly visible in the public Duolingo course map.
- The candidate grammar list is a pedagogical inference, not a verified list of Duolingo's official grammar objectives.

## Thematic reference — Instituto Cervantes AVE Global A1.1, Topic 3: La alimentación

Official topic index:
https://shanghai.cervantes.es/es/cursos_espanol/cursos_en_linea_espanol/cursos_ave.htm

Official topic PDF:
https://shanghai.cervantes.es/imagenes/File/ave/a11_t3.pdf

The A1.1 topic is organized by communicative function, grammar and vocabulary across sessions. Its grammar reference includes:
- indefinite pronouns algo/nada and the interrogative cuánto;
- present indicative of querer and preferir, including e>ie stem change;
- definite/indefinite article contrast;
- present indicative practice;
- poner and irregular -go verbs;
- demonstratives este/ese/aquel;
- agreement in cuánto/-os/-as;
- noun–adjective agreement;
- poner and traer;
- exclamative qué and stress/intonation;
- estar + adjective for evaluation;
- recomendar and poder with stem changes;
- gustar in first and second persons;
- impersonal se + third-person verb.

These are Instituto Cervantes AVE A1.1 topic contents, not Duolingo's official Unit 2.22 syllabus. They provide an excellent level- and theme-matched reference pool.

## Teaching decision for Unit 2.22

Until the user supplies the Hungarian-translated Guidebook page or current exercise examples, teach the following as a theme-based support lesson only:
1. present-tense regular verbs already introduced in the course;
2. quantities and food-related question words;
3. noun gender/number and adjective agreement where needed;
4. preference constructions if they appear in the actual examples;
5. eating habits and general statements only when examples justify impersonal `se`.

Do not introduce an unverified new grammar point as if Duolingo formally teaches it in this unit. If an item is needed to understand the current examples, mark it as supporting grammar.

## Ongoing workflow

1. Ask the user for the current section/unit if progress is not known.
2. Use the public course map to identify its communicative theme.
3. Cross-reference a level-appropriate PCIC/AVE theme.
4. Form a small set of grammar candidates and mark confidence.
5. Confirm only the relevant new rule from the in-app Guidebook or the user's examples when exact sequencing matters.
6. Save only original Hungarian teaching notes and the derived grammar map, never raw lesson text.
