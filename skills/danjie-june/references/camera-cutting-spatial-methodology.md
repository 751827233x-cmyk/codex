# AI视频切镜、运镜与空间容量方法论

Use this reference with Danjie June storyboard drafts whenever deciding shot cuts, camera movement, and visible subject grouping. It prevents AI video prompts from overloading one shot with impossible spatial information in any story, genre, location, or aspect ratio.

## Failure Pattern To Prevent

Do not combine a close reaction shot and a distant relationship shot in one line.

Wrong pattern:

```text
3秒 中近景 / 缓慢推进 / A中景；A看向画面左侧B与画面右侧C，B/C中景左右未变...
```

Why it fails:

- `中近景` on A can show A's reaction, nearby body/prop relation, and off-screen eye-lines.
- If B and C stand apart in the scene, the current frame may not also carry their medium-shot relationship inside the same close or medium-close shot.
- The prompt asks the AI video model to treat distant characters as both visible medium-shot subjects and off-screen eye-line targets, so space collapses.
- The shot is trying to do two jobs: A reaction + B/C relationship refresh. Split them.

Correct pattern:

```text
3秒 近景 / 轻微推进 / A主可见，B/C均在画外；镜头从A的手部或肩线推进到A转动的眼神，A先看向画外左侧B方向，再扫向画外右侧C方向；A说“原台词/原OS/原VO”；近处呼吸或衣料声；[光效]
2秒 中远景 / 左右平移 / 同轴关系，B左C右，A在后景或画外按上一镜方向保留；镜头从B的身体反应平移到数步外C的反应，两人距离保持打开，空间关系重新清楚；环境声压低；[光效]
```

## Director Decision Order

Before writing any shot, decide in this order:

1. **Beat task**: What changes at this exact moment: action, information, reaction, power, emotion, contradiction, or aftermath?
2. **Attention owner**: Who should the audience watch first in this shot?
3. **Visible subjects**: Who must be visible, who can be partial, who must stay off-screen?
4. **Spatial capacity**: Can this shot size and current aspect ratio physically hold those subjects without flattening distance?
5. **Cut or move**: If the next necessary subject cannot fit, cut directly. Do not pan or push across impossible space.
6. **Camera behavior**: Choose movement only after the shot task and capacity are clear.

Final prompts must show the result, not explain this reasoning.

## Single-Shot Capacity Gate

Every shot has a maximum safe payload. Do not exceed it.

| Shot size | Safe visible payload in the current aspect ratio | Do not use for |
|---|---|---|
| Full / long shot | Spatial map, group lanes, entrances, exits, distance, power layout | Dialogue, OS/VO, micro-expression |
| Medium group shot | 2-4 nearby subjects, or one triangle/group relation if width and depth are clear | Distant opposing sides plus close reaction detail |
| Medium shot | One speaker plus one nearby listener/reaction, or one subject with clear background witness | Far-separated character relationship refresh |
| Medium-close / close | One emotional subject, one partial shoulder/hand/nearby body or prop, off-screen eye-lines | Carrying two distant targets as visible medium subjects |
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
- **不可同框**: too far, blocked, different height/layer, or would break the current frame composition; use a cut.

Do not write a character as detailed visible action and `画外` in the same shot.

## Distance Rules

Use relative distance from the script instead of inventing exact meters.

- **贴身/一臂内**: can share close or medium-close framing.
- **一步到两步**: can share medium shot if screen lane/depth is clear.
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

## Aspect-Ratio Composition Rules

The method must adapt to the user's requested frame. Do not hard-code vertical video when the user asks for horizontal, square, cinematic widescreen, or any other format.

- **Vertical formats, e.g. 9:16 / 3:4**: narrow width, strong center-safe pressure. Use vertical lanes and depth stacking; avoid forcing wide left/right relationships into close shots.
- **Horizontal 16:9 / 2.39:1**: wider lateral capacity, but close/medium-close shots still cannot carry distant detail. Use width for faction layout, entrances, pursuit paths, and multi-person blocking; preserve depth and axis.
- **Square 1:1 / near-square**: balanced but limited. Use center/edge/foreground-background relations rather than wide lateral spread.
- **Any frame**: keep key faces, hands, props, and movement endpoints inside the safe composition area for that format.
- A reaction shot can hold off-screen eye-lines; it does not need to visibly include every target.
- Relationship shots should refresh distance, lanes, depth, and group position only at a shot size that can honestly carry them.
- If two targets are outside the current shot's capacity, write `看向画外左侧/右侧/前方/后方...` or cut to a relationship shot.

## Dialogue, OS, And VO Coverage

- Spoken dialogue belongs on the speaker, the listener's reaction, or a relation shot that can physically hold them.
- OS/VO can stay on the thinking subject's reaction. The objects of thought may be off-screen if the previous or next shot refreshes geography.
- If OS/VO comments on two separated people or places, use either:
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
- Is a rule assuming vertical framing even though the requested frame is horizontal or square?

When in doubt, split the shot.
