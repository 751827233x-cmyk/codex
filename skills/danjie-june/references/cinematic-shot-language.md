# 电影镜头语言系统

Use this reference with Danjie June storyboard drafts whenever writing `分秒运镜及切镜视频提示词`. This system makes each shot carry director-level visual decisions instead of only listing shot size, camera movement, action, and space.

## Core Requirement

Director thinking happens before writing the shot. The final AI-video prompt must not explain the director's reasoning. It must only show the camera behavior and visible result.

Do not write explanatory wording such as `为了表现压迫感`, `用这个镜头表达`, `镜头动机是`, `这个镜头为什么存在`, or `镜头语言：压迫感` in the final shot line. Let camera position, framing, movement, distance, focus, blocking, sound, and reaction do the work.

## Internal Shot Decisions

Before writing a shot, internally choose one primary function:

- **建立关系**: show who controls the space, who is exposed, who is blocked, who is far/near/high/low.
- **压迫推进**: use slow push-in, low angle, narrowed foreground, or reduced negative space to make pressure grow.
- **揭示信息**: reveal hidden person, object, route, lie, reaction, wound, gesture, or power shift.
- **反应承接**: show the person affected by a line/action; convert dialogue into consequence.
- **权力转移**: show who gains or loses control through stance, height, center position, stillness, or gaze.
- **情绪崩裂**: show a mask cracking, breath breaking, hand losing control, or posture changing.
- **悬念保留**: withhold full information through partial framing, foreground occlusion, off-screen eye-line, or sound.
- **动作因果**: show cause -> impact -> reaction -> aftermath in separate controlled shots when load is high.
- **女频爽点**: emphasize being seen through, public pressure, calm counterattack, emotional reversal, or humiliating exposure with restrained but sharp framing.
- **余韵沉降**: after a turn, let breath, silence, distance, or physical settling carry the beat.

## Shot Language Formula

Each shot line should read like a shootable visual instruction, not a rationale:

```text
3秒 景别 / 运镜方式（速度） / 空间锁定词；镜头从[可见起点]沿[路径/焦点/遮挡/高低/距离变化]落到[视觉终点]，[构图结果和人物关系自然呈现]；角色以[动作/表情/台词融合]完成剧情；[声音/物理反馈]；[光效]
```

Do not literally keep bracket labels in final output. Do not add "this expresses..." after the shot.

Good:

```text
3秒 中近景 / 缓慢推进 / 陆左沈中后；镜头从陆清韵攥紧的手推进到她强撑的脸侧，画面逐渐压窄，沈寒渊仍在后景中线不动；她开口前先吞住呼吸，说“原台词”，说完视线不敢离开沈寒渊；衣袖轻响；[光效]
```

Bad:

```text
3秒 中近景 / 缓慢推进 / 陆左沈中后 + 陆清韵说台词 + 表情紧张 + [光效]
```

## Camera Behavior

Translate internal attitude into visible camera behavior:

- **冷静审判**: stable frame, slow push-in, centered pressure, restrained sound.
- **窥探秘密**: foreground occlusion, partial reveal, low sound, slow lateral movement.
- **被压迫**: slight low/high angle depending on power, narrowed headroom, blocked escape path.
- **反击爽感**: still subject vs. moving guilty party; clean centered composition; reaction cut after line.
- **心虚逃避**: drifting lateral movement, broken eye-line, body angled toward exit, more negative space near route.
- **危险逼近**: slow push from distance to mid-close, path remains visible, footsteps or fabric lead the movement.
- **真相揭开**: rack focus, pan from liar to evidence, or reveal by reaction.
- **尴尬暴露**: hold the accused in frame after the line, let silence and others' eye-lines trap them.
- **情绪碎裂**: small unstable movement or breath-like handheld only when emotion genuinely destabilizes.

Use these as cinematic behavior, not as labels. Final shot lines should show the behavior directly.

## Composition Grammar

Use composition to express story:

- **Center frame**: control, judgment, arrival, authority, unavoidable truth.
- **Screen edge**: isolation, retreat, being pushed out, moral instability, hidden threat.
- **Foreground obstruction**: secrecy, spying, blocked desire, unstable trust.
- **Negative space**: fear, loneliness, possible escape, emotional distance.
- **Triangular blocking**: third party pressure, public judgment, divided alliance.
- **Depth stack**: foreground reaction + midground conflict + background witness or threat.
- **High/low relation**: hierarchy, surrender, protection, dominance, exposure.
- **Off-screen gaze**: unseen pressure or future reveal; always name where the target remains.

Do not use decorative composition if it weakens spatial continuity.

## Movement Grammar

Use movement to create meaning:

- **Slow push-in**: pressure, discovery, emotional tightening, lie being cornered.
- **Slow pull-back**: isolation, consequence, someone losing support, aftermath.
- **Lateral move**: compare two sides, expose contradiction, connect speaker and listener, reveal witness.
- **Tilt up**: entry, realization, authority rising, power becoming visible.
- **Tilt down**: defeat, shame, physical evidence, emotional weight.
- **Rack focus / focus shift**: truth moves from one subject to another; use only when depth relationship is clear.
- **Follow movement**: track real physical action; do not use it to hide a cut.
- **Weak motion**: static locked frame, slight handheld breath, or micro push only when stillness itself expresses pressure.

Avoid repeating movement for decoration. If two adjacent shots use similar movement, their motivations must be different and clear.

## Internal Editing Function

Each shot should internally serve one editing function:

- **Set**: establish spatial/power relationship.
- **Drive**: push action or dialogue forward.
- **Reveal**: expose new information.
- **React**: show consequence on another person.
- **Contrast**: compare claim vs. visible truth.
- **Interrupt**: break rhythm for shock, entrance, or realization.
- **Settle**: let the emotional/physical aftermath land.
- **Hook**: end with a frame that demands the next segment.

Vary the functions inside a segment. Do not print `Set`, `Drive`, `Reveal`, etc. in the final shot line.

## Female-Oriented Short-Drama Lens

For realistic female-oriented爽剧, prioritize:

- Calm authority defeating frantic explanation.
- The accused held in frame after being exposed.
- Reaction shots that let the audience enjoy someone being seen through.
- Clean, restrained lighting rather than exaggerated effects.
- Small physical details that show social pressure: breath held, hand freezing, step stopped, gaze unable to escape.
- Public spatial pressure: witnesses in background, factions visible, distance preserved.

Do not turn these into melodramatic overacting. The pleasure comes from controlled pressure and precise reaction.

## Shot-Line Minimum Standard

Reject a shot line if removing the camera movement or framing phrase does not change the visible scene. That means the movement is decorative.

Each shot line must include:

- A visible camera behavior that changes pressure, information, reaction, distance, or rhythm.
- A composition strategy shown through frame position, depth, focus, occlusion, high/low relation, or negative space.
- A shot-size capacity decision: who is visible, who is partial/focus-out, and who stays off-screen by eye-line.
- A movement path or deliberate weak-motion state.
- A story effect: pressure, reveal, reaction, contrast, reversal, aftermath, or hook.
- Character performance fused with dialogue/OS/VO if present.
- Space relation and sound/physical feedback.

## Self-Check

Before finalizing, revise if:

- The shot line only says who speaks, who moves, and where they stand.
- Movement is generic and could be swapped with any other movement without changing meaning.
- Every shot uses the same visual behavior.
- Dialogue does not create a visible reaction or consequence.
- A reveal is described as information instead of being staged through camera/focus/reaction.
- A power shift is stated in planning but not visible in framing, distance, stillness, or eye-lines.
- A female-oriented爽点 is rushed past without reaction, silence, or held pressure.
- Final shot lines contain explanatory phrases like `为了`, `用来表达`, `镜头动机`, or `镜头语言：`.
- A close or medium-close shot tries to carry a far-separated group relationship instead of cutting to a relationship shot.
