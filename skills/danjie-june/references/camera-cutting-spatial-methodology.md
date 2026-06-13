# AI视频切镜、运镜与空间容量方法论

Use this reference with Danjie June storyboard drafts whenever deciding shot cuts, camera movement, and visible subject grouping. It prevents AI video prompts from overloading one shot with impossible spatial information, especially in 9:16 vertical scenes.

## Failure Pattern To Prevent

Do not combine a close reaction shot and a distant relationship shot in one line.

Wrong pattern:

```text
3秒 中近景 / 缓慢推进 / 沈中后怀中小七；小七看左侧陆清韵与右侧赵烈，陆赵中景左右未变...
```

Why it fails:

- `中近景` on Xiao Qi in Shen Hanyuan's arms can show Xiao Qi, Shen's holding posture, and off-screen eye-lines.
- If Lu Qingyun and Zhao Lie stand apart across the clearing, vertical 9:16 cannot also carry their medium-shot relationship inside the same frame.
- The prompt asks the AI video model to treat distant characters as both visible medium-shot subjects and off-screen eye-line targets, so space collapses.
- The shot is trying to do two jobs: Xiao Qi reaction + Lu/Zhao relationship refresh. Split them.

Correct pattern:

```text
3秒 近景 / 轻微推进 / 沈中怀中小七，陆赵均在画外；镜头从沈寒渊臂弯里的小七耳尖推进到她转动的眼神，她先看向画外左侧陆清韵方向，再扫向画外右侧赵烈方向；小七OS：“原OS”；沈寒渊呼吸平稳；[光效]
2秒 中远景 / 左右平移 / 入口侧同轴，陆左赵右，沈抱小七在后景中线；镜头从陆清韵绷紧的肩线平移到数步外赵烈冷笑的侧脸，两人距离保持打开，沈寒渊抱着小七在后方不动；风声压低；[光效]
```

## Director Decision Order

Before writing any shot, decide in this order:

1. **Beat task**: What changes at this exact moment: action, information, reaction, power, emotion, contradiction, or aftermath?
2. **Attention owner**: Who should the audience watch first in this shot?
3. **Visible subjects**: Who must be visible, who can be partial, who must stay off-screen?
4. **Spatial capacity**: Can this shot size and vertical frame physically hold those subjects without flattening distance?
5. **Cut or move**: If the next necessary subject cannot fit, cut directly. Do not pan or push across impossible space.
6. **Camera behavior**: Choose movement only after the shot task and capacity are clear.

Final prompts must show the result, not explain this reasoning.

## Single-Shot Capacity Gate

Every shot has a maximum safe payload. Do not exceed it.

| Shot size | Safe visible payload in 9:16 | Do not use for |
|---|---|---|
| Full / long shot | Spatial map, group lanes, entrances, exits, distance, power layout | Dialogue, OS/VO, micro-expression |
| Medium group shot | 2-3 nearby subjects or one triangle if lanes/depth are clear | Distant opposing sides plus close reaction detail |
| Medium shot | One speaker plus one nearby listener/reaction, or one subject with clear background witness | Far-separated character relationship refresh |
| Medium-close / close | One emotional subject, one partial shoulder/hand/holding body, off-screen eye-lines | Carrying two distant targets as visible medium subjects |
| Insert / detail | One object, hand, wound, footstep, gaze direction, weapon, prop | Updating overall geography |
| POV / looking shot | What the subject sees from a fixed side | Replacing the subject's own reaction unless paired with a cut |

If a shot exceeds capacity, split it into:

- reaction shot
- relationship refresh shot
- target shot
- aftermath shot

## Visibility States

Mark each important entity internally as one of these before writing the shot:

- **主可见**: the shot's main subject; camera movement lands here.
- **副可见**: visible but secondary; only use if physically near or in clear depth.
- **局部可见**: shoulder, hand, back, sleeve, weapon, foreground edge.
- **焦外可见**: blurred witness/background; no detailed facial action.
- **画外存在**: not visible; use eye-line direction, sound, or reaction to preserve presence.
- **不可同框**: too far, blocked, different height/layer, or would break vertical composition; use a cut.

Do not write a character as detailed visible action and `画外` in the same shot.

## Distance Rules

Use relative distance from the script instead of inventing exact meters.

- **贴身/怀中/一臂内**: can share close or medium-close framing.
- **一步到两步**: can share medium shot if same vertical lane/depth is clear.
- **数步外/空地两侧/门口到主位/台上台下**: use relationship shot or separate single shots; do not pack into medium-close.
- **不同层级/不同高度/有门框、柱子、桌案、树木遮挡**: preserve depth with foreground/background, or cut between layers.
- **追逃/退场/拦截**: show path in medium/full shot, then cut to reaction or obstacle.

When distance is important to the drama, do not reduce it just to fit a close-up.

## Cut Decision Method

Cut when the audience's attention must change and the current shot cannot honestly hold the next subject.

Use cuts for:

- action impact -> affected person's reaction
- lie/claim -> visible contradiction or witness
- line of pressure -> target being trapped
- entrance cue -> existing characters' reaction -> entrant settling into the axis
- attempted exit -> blocking force/path -> stopped body reaction
- OS/VO reaction -> object/person looked at, only if geography needs refresh
- close reaction -> relationship refresh after distance or lane may become unclear

Do not use a camera move to hide a new shot. Cuts are direct cuts. Movement remains inside one shot.

## Camera Movement Method

Choose movement by what the visible frame must change:

- **缓慢推进**: close distance, narrow escape space, bring pressure onto one subject.
- **轻微推进/弱运动**: hold a reaction while keeping the frame alive.
- **左右平移**: compare nearby sides, reveal a witness/evidence, or refresh a same-axis relationship.
- **旋转摇上/摇下**: reveal height, surrender, authority, entrance, or evidence vertically.
- **拉远**: show isolation, consequence, lost support, or restored spatial relationship.
- **焦点转换**: shift truth between foreground/background only when both are already in one believable depth relationship.
- **跟拍**: follow real walking, retreating, chasing, or blocking; never use it to replace a cut across unrelated positions.
- **急推/急拉**: only for shock, exposure, or abrupt reversal; must land on a clear reaction or object.

If movement would need to travel from a close subject to far separated subjects in 2-4 seconds, cut instead.

## Vertical 9:16 Composition Rules

Vertical frame is a narrow stage. Protect it like this:

- Keep the active subject in the central 70% unless a deliberate edge composition is needed.
- Use lanes (`左30% / 中50% / 右70%`) only when lane precision is important.
- A medium-close vertical shot can show off-screen eye-lines, not a full distant triangle.
- Relationship shots should use depth stacking: foreground partial subject, midground conflict, background witness.
- Do not flatten far left/right characters into one close frame. Use a relation shot, then cut back.
- If two targets are on opposite sides of a vertical frame, a single reaction shot should say `看向画外左侧...再看向画外右侧...`, not pretend both targets are visibly present.

## Dialogue, OS, And VO Coverage

- Spoken dialogue belongs on the speaker, the listener's reaction, or a relation shot that can physically hold them.
- OS/VO can stay on the thinking subject's reaction. The objects of thought may be off-screen if the previous or next shot refreshes geography.
- If OS comments on two separated people, use either:
  - one close reaction with both targets off-screen by direction, or
  - reaction shot + relationship refresh shot.
- Do not attach OS/VO to a full shot.

## Per-Shot Capacity Self-Check

Reject and revise a shot if any answer is "yes":

- Does the shot size focus on one close subject while also claiming far-separated people are visible in medium detail?
- Does the line use `中近景/近景` but try to refresh a full group geography?
- Are two or more distant subjects described with detailed expressions inside a close reaction shot?
- Is a character both visible and off-screen in the same line?
- Would the AI need to shrink the world distance to make the prompt possible?
- Does the movement cross too much space for 2-4 seconds?
- Does the shot rely on vague left/right instead of locked screen direction or off-screen eye-line?
- Is the shot doing more than one major job when a direct cut would be cleaner?

When in doubt, split the shot.
