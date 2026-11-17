# workout-log

Training data for the Side by Side app. One JSON file per session under `workouts/`.

Each file:

- `id`, `dayName`, `startedAt`, `endedAt`, `finished`
- `notes[]` — timestamped session notes
- `exercises[]` — each with `name`, `unilateral`, `split`, `repLow`/`repHigh`, `cue`, `note`
  and `sets[]`
- each set has `note` and `values`, a map of side to `{kg, reps, done}`.
  Side keys: `B` both, `L` left, `R` right. Left is always trained first.

Sessions before 13 Nov 2026 were imported from a Hevy export. Hevy had no side field,
so those sets are recorded as `B`.
