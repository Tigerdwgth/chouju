---
name: chouju
description: Generate a coherent two-image cinematic sequence embodying the Chouju spirit—a visibly weaker subject confronts a much stronger subject, then appears in a continuity-preserving close or medium shot showing fear under control, defiance, and resolve. Use for “丑橘精神”, “我庆幸自己只是弱小，而不是懦弱”, “弱小 vs 强大”, “强弱对峙”, “死战不退”, “不屈”, “弱小但不软弱”, or when image 2 must inherit image 1’s subject identity, scene, lighting, direction, and spatial logic.
---

# Chouju: Weak, Not Cowardly

Create a two-image narrative honoring the Chouju spirit rather than two independent illustrations. Use the first result as the canonical visual state for the second.

Read [references/prompt-templates.md](references/prompt-templates.md) before generating either image.

## Resolve the request

Extract:

- weak subject and strong subject;
- setting, era, weather, and action boundary;
- requested aspect ratio and visual medium;
- any pose/expression reference;
- whether the strong subject may appear in image 2.

If both subjects are named, generate directly. Ask one concise question only when a missing subject or setting would materially change the result. Default to 16:9 landscape and realistic cinematic wildlife/documentary photography when the user does not specify them.

Treat “weak” as a power and scale disadvantage, not as malformed, infantile, comic, or helpless. Keep the scene non-graphic unless the user explicitly requests otherwise.

## Establish reference priority

Apply constraints in this order:

1. explicit user instructions;
2. image 1 for identity, environment, lighting, geometry, and direction;
3. a supplied pose image for posture and emotional semantics only;
4. defaults in this skill.

Never copy social-media interface elements, captions, watermarks, usernames, platform chrome, or the reference animal’s species/background merely because they appear in a pose reference.

## Generate image 1: confrontation

Use the image-generation tool to create a new image. Make the imbalance readable without text:

- show both subjects clearly, preferably with enough of each body to read anatomy and stance;
- establish believable relative scale using the ground plane, distance, shadows, or environmental objects;
- orient the subjects toward one another; do not accidentally make them travel in the same direction;
- place the weak subject at a clear tactical disadvantage while preserving agency;
- use a low or eye-level cinematic camera that lets the strong subject loom without hiding the weak subject;
- preserve realistic anatomy, contact, lighting, depth, and ecology;
- use restrained filmic grading and photographic texture, not illustration, oil painting, glossy CGI, or excessive HDR.

Do not start image 2 until image 1 has been returned and is available as a reference.

## Record the continuity ledger

Inspect image 1 and retain these facts internally:

- exact weak species, body proportions, color and pattern markings, age cues, injuries, and accessories;
- setting, terrain, weather, time of day, light direction, and palette;
- weak subject’s screen side, facing direction, gaze target, body orientation, and distance from the threat;
- camera side, focal character, and dominant depth cues;
- strong subject’s off-screen direction if it will not appear in image 2.

Image 1 overrides the initial text prompt wherever the generated visual has already made a concrete continuity choice, unless that choice violates an explicit user instruction.

## Generate image 2: defiant weak subject

Make a second image-generation call using image 1 as a reference. If a pose reference is also required, include both image 1 and that pose reference in the smallest supported recent-image set.

Default to a three-quarter or medium-close shot from near the strong subject’s side. Keep enough of the weak subject’s body visible to read the stance. Exclude the strong subject from the frame by default, but preserve its presence through the weak subject’s gaze, body angle, eyeline, shadow, or off-screen spatial direction.

Translate “死战不退” into species-correct physical signals:

- lower the center of gravity;
- brace the limbs, paws, fins, wings, roots, or equivalent support structures;
- angle the body against the threat instead of retreating;
- lift or stabilize the head and lock the gaze toward the off-screen opponent;
- convey fear under control, exhaustion, and resolve rather than effortless dominance.

For small animals, keep the mouth closed by default. Express defiance primarily through gaze, posture, muscle tension, and weight distribution. Do not add human eyebrows, fists, smiles, superhero poses, or anatomically impossible snarls.

Maintain the continuity ledger exactly. Do not change species, color pattern, body size, injury state, terrain, weather, lighting direction, or confrontation axis. Do not mirror the scene casually.

## Validate before delivery

Regenerate the affected image when any hard failure occurs:

- the weak subject changes species or recognizable appearance;
- strong/weak scale hierarchy becomes ambiguous or reverses;
- image 2 swaps the background or lighting;
- facing direction or off-screen threat direction flips;
- image 2 copies the pose reference’s UI, text, species, or background;
- the posture reads as fleeing, begging, relaxed, comic, or triumphant rather than cornered but resolute;
- anatomy, ground contact, occlusion, or perspective is physically inconsistent;
- the rendering becomes anime, painting, plastic CGI, over-smoothed, or oily.

Deliver both generated images in order and add only a brief label for each unless the user asks for the prompts.
