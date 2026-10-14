# Almanca – Linie B1

Personal German course for one learner: Turkish native speaker in Hamburg, German level A2 (Oct 2026), training for the bus licence (Klasse D, IHK Berufskraftfahrer-Grundqualifikation exam in German) and applying to Hamburger Hochbahn as Busfahrer around mid-December 2026. Studies 1 hour/day at 07:00 on a phone.

**Talk to the learner in Turkish.** Use simple Turkish; German examples always with Turkish translation. When practising, correct mistakes briefly in Turkish.

## Layout
- `index.html` – the phone app (single file, vanilla JS). Published as artifact https://claude.ai/artifact/1wvoC5oqL4XYrXkg8n6DQE with capabilities `db` (rule: write owner) and `sample`. Republish with the Artifact tool using `url` and `files` mapping `content/weekN.json` → same path.
- `content/week1.json` … `week8.json` – 5 lessons each (12 words, 6 phrases, dialog, grammar, roleplay). `week9.json` = bonus IHK exam vocabulary. Schema: see any file. Validate with `python3 -c "import json;[json.load(open(f'content/week{n}.json')) for n in range(1,10)]"`.
- `PLAN.md` – the 8-week plan in Turkish (for the learner).
- `reports/` – weekly progress reports (Turkish), one file per week `YYYY-MM-DD.md`.

## Learner progress
Stored in the artifact database, document `progress/main` (read with ArtifactData `get`, collection `progress`, doc_id `main`). Fields: `start` (course start date), `done` {unitId: {score, at}}, `steps` {unitId: [step keys]}, `srs` {"w1d1:3": {b: box 1–5, due}} (word = lesson w1d1, words[3]), `days` [study dates]. Unit ids: `w{week}d{day}` lessons, `w{week}r` weekly review. Box 1 words = currently weak words.

## Reminders
- Google Calendar: daily 07:00–08:00 Europe/Berlin, 56 days from 2026-10-15.
- Weekly Sunday report routine (fresh session) reads progress and writes `reports/`.
