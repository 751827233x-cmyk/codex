# 工业级改编控制系统

Use this reference with `full-guidelines.md`, `axis-continuity.md`, and `high-density-storyboard.md` when converting scripts, novels, or scene outlines into Danjie June AI-video storyboard execution drafts. This file extracts the reusable control logic from the user's long-form source rules, while preserving Danjie June constraints.

## Compatibility Filter

These rules override only when they do not conflict with Danjie June:

- Preserve all source dialogue. Do not delete, summarize, paraphrase, or rewrite dialogue unless the user explicitly requests anonymization.
- If the user provides a script with OS/VO, preserve those OS/VO lines exactly. Do not invent new OS/VO to fill density.
- If the user provides prose or novel material, convert inner psychology into visible body action first. Add OS/VO only when the source clearly contains inner speech or the user asks for it.
- Use original character names by default. Anonymous names such as `角色1` are allowed only when the user explicitly asks for anonymization.
- Do not invent appearance, clothing, props, or scene objects unless the user provides a reference image or explicit scene requirement.
- Keep Danjie output compact and execution-oriented. Do not expose backend terms such as XYZ coordinates, vector, state machine, or algorithmic calculations inside AI-video shot lines.
- Use direct cuts only. Do not output English transition labels such as `SMASH CUT TO`, `HARD CUT TO`, or `MATCH CUT ON ACTION`; express the same continuity as direct cut logic in Chinese.

## Priority Stack

When rules compete, resolve them in this order:

1. Safety and prohibited content handling.
2. Source integrity: dialogue, plot causality, OS/VO preservation, and no mid-line truncation.
3. Spatial continuity: axis, screen direction, real distance, height difference, layer, occlusion, and vertical 9:16 lanes.
4. Physical and optical plausibility: visible detail must match shot size, distance, lighting, and material behavior.
5. Editing logic: cuts serve action continuity, emotional turns, reaction, reveal, or physical aftermath.
6. Character consistency: names, identity, behavior logic, established visible state.
7. Density and cinematic texture: performance, sound, lighting, and rhythm.

## Pre-Draft Control Pass

Before writing segments, run a compact control pass. Keep it internal unless the user asks for diagnostics; reflect the results in each `本段生成规划`.

- **Source mode**: script, novel prose, dialogue scene, outline, or mixed material.
- **Name mode**: real-name mode by default; anonymous mode only by explicit user instruction.
- **Scene map**: location, time, interior/exterior, entrance/exit direction, weather or atmosphere if explicit.
- **Plot boundaries**: divide by time/place change, micro-goal change, key power-changing entrance/exit, or emotion/action settling into a new state.
- **Load scan**: classify each beat as high, medium, or regular load based on character count, physical contact, movement, effects, wide environment pressure, or extreme close detail.
- **Space state**: decide whether this is spatial initialization, full inheritance, or relationship re-establishment.
- **Master relationship**: identify any distance, height, layer, occlusion, faction, or power-position relationship that must not be flattened for convenience.
- **Visual anchors**: opening anchor, escalation anchor, hook/aftermath anchor.
- **Dialogue/time estimate**: estimate whether dialogue, action, camera movement, or effects dominate the shot duration.
- **Sound plan**: environment sound, physical SFX, prop/material sound, voice quality, silence or impact contrast.

## Plot Boundary Rules

Cut only at real dramatic boundaries:

- **Time/place break**: new location, indoor/outdoor transfer, day/night switch, or explicit time jump. This triggers spatial initialization.
- **Micro-goal change**: the character's immediate objective changes, e.g. from probing a lie to surviving an attack.
- **Power-changing entrance/exit**: a character enters or exits with enough power to change the pressure relationship.
- **Emotional/action settlement**: after a violent action, collapse, confession, reveal, or emotional explosion, allow the aftermath to land before starting the next beat.
- **Flashback closure**: never split inside a flashback. If source material enters memory, complete the loop: present trigger -> memory beat -> return to present with the resulting emotional/action change.

## Load And Duration Rules

Danjie June uses compact shot durations (`2秒`, `3秒`, `4秒`) and segments under 15 seconds. Adapt the source load rules into this scale:

- **High load**: 3+ active characters, close physical contact, fast action, magic/particle effects, complex blocking, large environment reveal, or extreme close detail. Use more 2秒 shots; separate cause, impact, reaction, and aftermath.
- **Medium load**: 2-4 people in tension, clear emotional reversal, small movement, confrontation, or standard dialogue coverage. Use 2-3秒 reaction coverage and 3-4秒 dialogue shots.
- **Regular load**: calm exchange, single-person emotional beat, simple atmosphere, or low movement. Use fewer 3-4秒 shots with stronger performance and sound detail.
- Never truncate in the middle of an action, breath, OS/VO, or dialogue line. If a beat is too large, split at the next plot boundary.
- If dialogue or camera movement takes longer than the physical action, fill the empty time with motivated micro-action: breath, hand tension, robe/fabric shift, eye-line change, pause, or environmental response.

## Spatial State Machine For Storyboards

Use a simple storyboard-facing state machine:

- **Spatial initialization**: first scene or new location. Start with a silent full shot or wide relationship shot to lock the environment, main axis, screen direction, depth layers, and vertical safe lanes.
- **Full inheritance**: same place and continuous action. Do not repeat a full establishment unless needed; carry every character's position, posture, direction, eye-line, prop, visible condition, and emotion forward.
- **Relationship re-establishment**: same place, but the viewer may misunderstand distance, height, occlusion, faction layout, or pressure relationship. Add a compact relationship shot before close or over-shoulder shots.

Track all entities, not only the speaker:

- Speaking characters.
- Silent characters still physically present.
- Background or out-of-focus characters whose position affects power, threat, or blocking.
- Props or effects that constrain movement.

## Main Spatial Relationship Priority

If the drama depends on distance, height, layer, occlusion, faction line, doorway position, or power position, that relationship beats standard dialogue coverage.

- Do not pull a far, high, hidden, background, or off-axis character into the foreground just to make dialogue or expression clearer.
- Do not flatten height difference or same-plane/different-plane relationships.
- Do not use over-shoulder shots when the bodies are too far apart, at different heights, behind obstacles, or not facing each other.
- In those cases, use relationship shot, single reaction shot, long-lens observation, low/high angle, foreground-background composition, or explicit distance-marked single shot.
- In every shot, translate the relationship into natural language: who is left/right, foreground/midground/background, high/low, near/far, blocked/unblocked, and whether anyone is forbidden to approach or enter foreground.

## Optical And Physical Visibility

Only describe what the lens and lighting can plausibly show:

- **Far/full/wide, over 5m**: body posture, group formation, direction change, step stop, silhouette, large movement. No pupils, mouth muscles, tiny sweat, eyelashes, or bloodshot eyes.
- **Medium, 2-5m**: broad facial and body cues: brows press, jaw tightens, mouth stiffens, breath pauses, eyes avoid contact, shoulders tighten.
- **Close/near, under 2m**: micro details are allowed when lighting supports them: lips part, eyelids tremble, throat swallows, fingers press into fabric.
- If a face is backlit, under top light, hidden, or in shadow, use bounce/reflected light only if the scene lighting logically supports it; otherwise express emotion through posture, breath, outline, or sound.
- Scale physical effects to the shot: macro environment changes in wide shots; visible fabric/prop/body interaction in medium shots; micro material texture only in close shots.

## Editing And Rhythm Rules

Cuts must have a reason:

- **Action continuity**: cut at the peak or middle of a real action, then continue the action from the same screen direction.
- **Reaction**: after a reveal, impact, threat, or lie, include the affected person or environment reaction.
- **Reveal**: use pan, push, tilt, rack focus, or static reframing when the shot has to reveal hidden information.
- **Emotional tension**: vary long/short rhythm. Do not distribute time evenly across all shots.
- **Aftermath**: after high-load action or emotional explosion, include a 2-3秒 reaction, silence, or physical settling shot before pushing into the next action.
- Avoid using action-cut language for tiny slow gestures such as a finger tightening, breath pause, or small head turn. Handle those inside one shot or by direct cut to reaction.

## Dialogue, Voice, And Performance

Every spoken line in a shot must be fused with performance:

- Pre-speech cue: breath, swallowing, hesitation, eye-line, hand tension, mouth set, shoulder movement.
- Voice quality: cold, trembling, low, hoarse, clipped, forced calm, breathy, broken, or paused.
- Exact source line: preserve wording.
- During-speech change: a word is bitten harder, tone drops, eye-line shifts, expression cracks, body leans or freezes.
- After-reaction: silence, breath release, avoidance, stare, hand lowering, fabric sound, step stop.

For OS/VO:

- Preserve source-authored OS/VO exactly.
- Pair OS/VO with visible physical reaction.
- Do not add explanatory narration or background-summary narration.

## Sound System

Each segment should include sound as story information, not decoration:

- **Ambience**: rain, hall echo, forest insects, wind, water, fire, distant footsteps.
- **SFX**: footstep, fabric rub, cup touch, sword air-cut, breath catch, body shift, water ripple.
- **Prop/material**: wood creak, metal tremble, tea surface tremble, dust, sleeve swing, branch movement.
- **Voice**: breath, pause, broken sound, clipped tone, trembling tail, suppressed volume.
- **Silence**: use short silence for shock or pressure, but do not write BGM.

## Front-End Shot Compiler

Shot lines must be natural language, not backend fields. Each shot should contain:

```text
3秒 景别 / 运镜方式（速度） / 空间锁定词；镜头从可见动作或空间锚点开始，按明确路径移动或保持弱运动，落到冲突信息；自然写出谁仍在左/右、前/中/后、高/低、远/近、遮挡关系是否变化；角色以可见表演承载原台词或原OS/VO，并补上说完后的余韵；环境声/动作声/物理反馈；[光效]
```

Hard requirements:

- Every shot has one natural spatial sentence.
- Every shot has either a meaningful camera movement sentence or a deliberate weak-motion sentence such as static locked frame, slight handheld breath, or rack focus.
- Every shot explains its narrative purpose through image, not labels.
- Every close shot or over-shoulder shot still names where the off-screen person remains.
- Do not write placeholder labels like `镜头运动句`, `空间关系句`, `表情变化句`, or `表情-台词融合句` in the final shot.

## What To Reject From The Source Rules

Do not import these parts into Danjie output:

- Mandatory invented appearance/clothing when no reference image or explicit requirement exists.
- Unscripted OS/VO for script scenes.
- BGM, subtitles, black screen, text-on-screen, or non-execution explanations.
- English transition tags in final shot lines.
- Backend algorithm vocabulary in final AI-video prompt lines.
- Overly long all-in-one outputs that exceed the user's requested segment scope or Danjie 1900-character execution limit.

## Comprehensive Self-Check

Before delivering, reject and revise if:

- A plot was split mid-action, mid-line, mid-OS/VO, or inside an unfinished flashback.
- Load classification does not match shot density.
- A high-load beat lacks cause-impact-reaction-aftermath coverage.
- A calm beat has unnecessary rapid cutting.
- Any character physically present disappears from continuity tracking.
- A shot makes a far/high/background/occluded person suddenly near, flat, or foreground without action.
- Dialogue is not fused with breath, voice, expression, and aftermath.
- Sound is absent from a segment with tension, movement, props, weather, or shock.
- Facial details exceed the shot's optical distance or lighting.
- Shot lines expose backend labels instead of natural visual language.
