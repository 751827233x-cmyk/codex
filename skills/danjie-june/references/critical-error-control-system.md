# 不可容忍错误总控系统

Use this reference as the top-level quality gate for Danjie June storyboard drafts. It is not tied to any genre, scene, weapon, layout, aspect ratio, or plot type. Its purpose is to prevent severe logic errors before they enter planning ledgers, shot prompts, or AI video generation.

## Core Principle

Every segment must be physically, narratively, spatially, temporally, and prompt-semantically true before it becomes visually rich.

Beauty, atmosphere, shot variety, and cinematic language never compensate for a wrong fact, wrong cause, wrong position, wrong time, wrong action function, or wrong AI instruction.

## Severity Levels

Classify every issue before final output:

| Level | Meaning | Action |
|---|---|---|
| S0 Fatal | Contradicts source facts, changes plot meaning, breaks character identity, reverses cause-effect, deletes original dialogue, or makes the AI generate the opposite event | Stop and rewrite the segment |
| S1 Critical | Causes spatial chaos, axis flip, impossible movement, false physical state, character teleport, multi-batch continuity drift, or unusable AI video prompt | Stop and rewrite the affected ledger and shots |
| S2 Major | Weakens professional quality: thin beat, poor entrance, bad shot capacity, unclear reaction, weak aftermath, bad timing, repeated movement | Revise before delivery |
| S3 Minor | Wording can be cleaner but does not threaten story, space, or generation | Polish if time permits |

No S0 or S1 issue may remain in delivered output.

## Error Families To Control

### 1. Source Fidelity Errors

- Dialogue deleted, compressed, paraphrased, or redistributed.
- OS/VO added where source did not provide it.
- Characters, relationships, scene facts, props, or outcomes invented.
- A source action is softened, exaggerated, reversed, or replaced.

Gate: every line in `剧本内容` must trace to source text or a non-plot-changing visual bridge.

### 2. Plot Causality Errors

- Effect appears without cause.
- Cause produces the wrong reaction.
- Emotional meaning is written as a physical fact.
- A later action contradicts an earlier ledger.
- A character behaves with knowledge they have not received.

Gate: every beat must read as `cause -> visible mechanism -> character reaction -> new state`.

### 3. Action Function Errors

- Warning written as blockade.
- Near miss written as hit.
- Fear written as restraint.
- Voluntary stop written as physical control.
- Symbolic pressure written as visible object.

Gate: use `action-function-causality.md` for every movement, attack, warning, interruption, exit, pursuit, restraint, spell, weapon, door, obstacle, or environmental force.

### 4. Spatial And Axis Errors

- Screen-left/screen-right swaps without visible reset.
- Characters crowd together despite established distance.
- Wide relationship is forced into close framing.
- Someone appears in a lane, layer, or side they never moved to.
- A path, door, table, stage, height, or obstacle is ignored after being established.

Gate: scene space ledger must match every shot and every continuity ledger.

### 5. Shot Capacity Errors

- Medium-close/close shot tries to show far-separated targets in detail.
- One shot does close reaction, spatial map, dialogue, and relationship refresh at once.
- Camera movement crosses too much physical space in 2-4 seconds.
- Full shot carries dialogue/OS/VO when the rules forbid it.

Gate: use `camera-cutting-spatial-methodology.md`; split incompatible jobs into cause, reaction, relationship refresh, and aftermath shots.

### 6. Time And Process Errors

- New character appears already in final position.
- Entry, exit, fall, kneel, stand, attack, stop, turn, or retreat lacks process.
- Segment starts from a posture that does not match previous ending.
- Final dialogue hits the segment end with no breathing room.

Gate: every state change needs visible transition or source support.

### 7. Aspect-Ratio Errors

- Vertical frame tries to carry horizontal four-person spacing in close shot.
- Horizontal reference is blindly copied into vertical production.
- Safe zones, headroom, hands, props, movement endpoints, and off-screen eye-lines are not adapted to current frame.

Gate: define the current aspect ratio and only use frame lanes that that format can honestly carry.

### 8. Prompt Semantics Errors

- Prompt words imply the opposite visual: `屏障`, `封住`, `挡住`, `困住`, `覆盖`, `压住去路` when the source only shows warning.
- Negative instructions repeat unwanted imagery and trigger it.
- Ledger wording is copied into shot lines as verbose labels instead of useful visual language.
- Abstract explanation replaces visible action.

Gate: final AI video prompt lines must describe desired visible result, not internal reasoning or unwanted objects.

### 9. Ledger Amplification Errors

- `本段生成规划` exaggerates the source, and every later field inherits it.
- `场次空间锁定表` invents a physical state.
- `连续性承接表` carries a wrong posture, position, prop, effect, or obstacle into the next segment.
- A local fix changes shot lines but leaves wrong facts in planning fields.

Gate: after revising any shot, re-check planning, spatial ledger, character state, continuity ledger, visual baseline, effects, and next-frame constraint.

### 10. Character State Errors

- Silent characters vanish from continuity.
- A visible character has no reaction.
- Emotional state jumps without a carrier.
- Props, wounds, wetness, held animals, restraints, or posture disappear without action.
- A character knows, sees, hears, or reacts to something outside their possible line of sight or hearing.

Gate: every present entity has position, visible state, posture, facing, emotion, and eye-line status.

## Mandatory Control Flow

Use this order on every full storyboard draft:

1. **Source Fact Pass**: extract factual actions, dialogue, OS/VO, location, time, known positions, entrances, exits, and outcome boundaries.
2. **Severe Risk Pass**: mark beats with attack, warning, chase, exit, interruption, reveal, new arrival, group movement, hidden presence, spatial change, or high-density dialogue.
3. **Function And Cause Pass**: for each high-risk beat, classify action function and write the true cause-effect chain.
4. **Spatial Truth Pass**: define world coordinates, screen lanes, axis, safe side, depth, distance, paths, and what cannot be in the same shot.
5. **Segment Planning Pass**: write `本段生成规划` only after the true action function and spatial facts are known.
6. **Shot Capacity Pass**: choose shot size and cut points from the job each shot can honestly do.
7. **Prompt Semantics Pass**: replace abstract, negative, or physically false wording with positive visible actions.
8. **Ledger Consistency Pass**: ensure planning, stand positions, space table, special state, continuity table, effects, and shot lines all say the same physical truth.
9. **S0/S1 Stop Gate**: if any fatal or critical issue remains, rewrite before delivery.

## Segment-Level S0/S1 Checklist

Reject and rewrite a segment if any answer is "yes":

- Did I change what happened in the source?
- Did I preserve dialogue words but change the physical meaning around them?
- Did I write a reaction as a physical obstacle, restraint, hit, or movement?
- Did I invent a position, path, object, effect, injury, or knowledge state?
- Did I put a character in a different lane without an action?
- Did I let a close shot carry a full spatial map?
- Did I use a camera move to cross an impossible distance instead of cutting?
- Did I leave wrong information in planning or continuity after fixing a shot?
- Did I write an AI prompt that could reasonably generate the opposite of what the scene needs?
- Did I solve a local issue by adding a rule that only works for this exact scene, instead of classifying the broader error family?

## Corrective Method

When an S0/S1 issue is found:

1. Name the error family.
2. Identify the exact false assumption.
3. Return to the source fact.
4. Rebuild the cause-effect chain.
5. Rewrite planning fields first.
6. Rewrite shot lines second.
7. Rewrite effect/sound/continuity fields third.
8. Run the S0/S1 checklist again.

Do not patch only the visible shot line if the ledger still contains the wrong logic.

## Generalization Rule

Never add a rule that only works for a specific plot, weapon, character, location, genre, or frame format. Every new rule must be phrased as:

`error family -> root cause -> general decision method -> output constraint -> self-check`

If the rule cannot be generalized, keep it out of the skill and fix only the local script.
