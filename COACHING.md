# Coaching record — Kat

The durable memory for this training block. Any future session should read this
before giving advice. Updated when a decision changes, not after every workout.

Last updated: 2026-11-19

---

## Who

- Kat, 32, female, 170 cm. Based in Bali (Asia/Makassar).
- ~3 years training. Adherence is excellent: 307 logged sessions over 26 months.
- Desk work, very sedentary outside the gym.
- Bodyweight: started this conversation at 68 kg, 64.5 kg as of 19 Nov 2026. Goal 58 kg.
  - 64.5 kg at 170 cm is BMI 22.3 — normal range. 58 kg is BMI 20, also normal.
  - She has described herself as "fat"; she isn't, and that was said plainly once.

## The goal

1. **Lose fat to 58 kg** — her stated first priority, chosen over building muscle.
2. **Keep the muscle she has**, or add if possible.
3. **Left glute**: build the mind–muscle connection so both sides look and feel equal.
   This is the thing she cares most about and the hardest to measure.

## The left glute

- Surgery at age one removed inflammatory tissue on the left glute. Large visible scar.
  **Muscle involvement unknown — never assessed.**
- She can voluntarily contract it. Cable kickbacks (torso ~100°) and abduction feel
  normal on both sides. The deficit is isolated to **loaded bilateral hip extension**.
- Intermittent left pelvic/hip pain, previously sharp, worse during periods of *not*
  training. Hip snapping largely resolved.
- **She has not had it medically assessed and does not want to**, specifically because
  she expects to be told nothing is wrong. Don't push this repeatedly; it has been
  raised and she has decided. Note it if symptoms change.

## The finding that matters most

Her Hevy export showed **nine months of systematic detraining through 2026**:

| Lift | Mid-2025 peak | Nov 2026 |
|---|---|---|
| Barbell hip thrust | 70 kg | 10 kg |
| Bulgarian split squat | 15 kg | 6 kg |
| RDL | 20 kg | 10 kg |
| Single-leg RDL | 18 kg | 7.5 kg |
| Leg press | 50 kg (Oct) | 40 kg |
| Leg extension | 35 kg (Oct) | 25 kg |
| Frog pump (Smith) | 60 kg | 50 kg |

The deload was deliberate — back pain, relearning the hip thrust — but ran nine months
with no rebuild. **This, not exercise selection or the asymmetry, is why her glutes
haven't grown.** Programming discussions should not drift away from load.

She also lost 3.5 kg *while* loads were falling, which is the pattern where some of the
loss is lean mass.

## Current block (from 19 Nov 2026)

- **1,600 kcal/day**, flat, every day. Maintenance is ~1,735 at 64.5 kg with 3 gym
  sessions and a sedentary job. BMR ~1,386.
- **125 g protein** — the main defence against losing muscle in the deficit.
- **5 hours walking per week**, counted since Monday.
- Expected rate ~1 kg/month → 58 kg around late May 2027.
- **Training goal is to HOLD loads, not add them.** Holding through a cut is a win and
  should be said as one. The exception: regaining her October 2026 numbers is expected
  and fine, because that's recovering lost ground, not building new tissue.
- **Guardrail: if working loads slide two sessions running, eat 1,735 for two weeks,
  then resume.** Her log will show it before she feels it.

She arrived at 1,600 after oscillating 1,550 → 1,700 → 1,500 → 1,600 in ten minutes.
I advised eating at maintenance and building first; **she chose to cut first and she
has the final say.** Don't relitigate it. Watch the guardrail instead.

## The program

Source of truth is `program.json` in this repo. **Three leg days**: Legs A (Mon),
Legs B (Wed), Legs C (Fri). She dropped the two upper-body days.

**Posture day** (added 25 Nov 2026, badge TUE): for rounded shoulders, rounded upper
back and forward head. Prone Y/T raises, band rows, face pulls, chin tucks, doorway pec
minor stretch, foam roller thoracic extension. Plan: 3x/week, chin tucks daily, 8-12
weeks, compare side-view photos. Chosen from reviews/RCTs: scapular strengthening is the
core; chin tucks alone have weak evidence; stretches are extras. Each cue has a video link.

## Her constraints — do not forget these

- **Hates back extensions.** Replaced with kickstand RDL. Don't reintroduce.
- **Cannot do a single-leg hip thrust with any added weight.** Bodyweight only.
- **No box, no hack squat, no leg-curl "platform" machine** at her gym.
- Calf work: leg press calf press only. Seated calf raise was dropped on 19 Nov —
  calves are not a goal, and she asked twice why it was there.
- Prefers exercises she struggles to feel **early in the session**, while fresh.
- Rests ~2 minutes between sets by default.
- Sumo squat goes below parallel.

## How she wants to be talked to

- **A few bullet points.** She will not read long replies and has said so.
- No preamble, no restating the question, no praise padding.
- Lead with the verdict. Cite her actual numbers, not generalities.
- If a session was poor, say so plainly and say what to do.
- She pushes back hard and is usually right when she does. Concede fast when wrong.

## Tooling

- iOS app **KatWorkouts** (project name SideBySide), local-first, pushes one JSON file
  per session to `workouts/` in this repo. Activities go to `activities/`.
- The app can only be rebuilt from Xcode on her Mac — she has to archive and upload.
- Morning review runs daily at **05:46 Asia/Makassar**, reads this repo, sends nothing
  if she logged nothing.
- Reading this repo needs no token. Writing does.

## Known history of my own mistakes here

Recorded so they aren't repeated:

- Workout IDs were `<date>-<day>`, so two sessions of the same day type on one date were
  the *same file*. Starting the second silently overwrote the first, and deleting either
  destroyed both. **This cost her two logged sessions on 19 Nov.** Fixed with unique ids,
  a guard in the save path, and delete-moves-to-bin instead of destroying.
- Claimed front raises were redundant "because any pressing" — she had no pressing in
  her program at all. The claim was borrowed from a generic upper day.
- Muddled maintenance vs cut calories (1,700 appeared as both).
- Triggered the Hevy CSV export six times while trying to intercept it in-page.

## Open questions

- Does the loading rebuild actually start? Leg press back to 50 kg on Wednesdays is the
  first test.
- Does the left glute connection improve with the unilateral work, or does it need
  something else?
- The 58 kg target is hers and is a normal weight, but watch for the cut running long
  or the rate creeping up.
