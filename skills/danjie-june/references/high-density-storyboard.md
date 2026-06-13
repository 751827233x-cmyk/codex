# 高密度分镜与情节打包规则

Use this reference with `full-guidelines.md`, `axis-continuity.md`, `industrial-control-system.md`, and `cinematic-shot-language.md` when the generated storyboard feels thin, too fragmented, or lacks cinematic information per segment. `industrial-control-system.md` governs plot slicing, load scanning, spatial inheritance, and stability; `cinematic-shot-language.md` governs director-level camera behavior and keeps final shot lines visual instead of explanatory; this file governs how each segment and shot becomes denser without becoming bloated.

## Compatibility Boundaries

- Preserve Danjie rules first: do not delete dialogue, do not invent unscripted OS/VO, no BGM, no subtitles, no black screen, no eye catchlights, no facial light spots, direct cuts only.
- Keep each segment under 1900 Chinese characters whenever the user expects AI-video prompt execution.
- Keep the Danjie dialogue density rule: 20-45 Chinese characters per 15 seconds, excluding punctuation. If a source line is too long, split by natural breath and dramatic beat, not by arbitrary length.
- Do not invent clothing, facial appearance, or scene elements unless the user provides a reference image or explicit scene requirement. If a source text explicitly provides a scene requirement, use only those scene elements.
- Keep the compact shot duration style: `2秒`, `3秒`, `4秒`. Use timeline ranges only when the user asks for editing timecodes.

## Why Thin Segments Happen

Thin output usually comes from these failures:

- Splitting by individual dialogue lines instead of complete story beats.
- Spending too many characters on administrative ledgers while the shot itself only says "who does what".
- Separating dialogue from acting, so the video prompt lacks breathing, eye-line, mouth tension, hand motion, and after-reaction.
- Using only "scene / shot size / camera movement" without explaining the shot's story purpose.
- Hiding spatial continuity in the ledger but not translating it into natural visual language inside each shot.
- Omitting sound, material response, and physical cause-effect, leaving the AI model with static poses.

## Pre-Draft Planning

Before drafting a scene, perform a compact planning pass. Include it in the output only when useful; otherwise keep it internal.

1. **Core conflict**: one sentence: who pressures whom, with what secret, lie, desire, or threat.
2. **Plot slicing**: split only at true boundaries:
   - time/place changes
   - a character with power to change the situation enters or exits
   - the micro-goal changes
   - an action or emotional explosion settles into a new state
3. **Load scan**:
   - **High load**: 3+ active characters, physical contact, fast movement, magic/particle effects, complex group blocking. Use more short 2-3秒 shots.
   - **Medium load**: 2-4 people in tension/dialogue, clear emotional reversals, small movement. Use 3-4秒 shots with reaction coverage.
   - **Regular load**: single-person emotion or calm exchange. Use fewer but denser 3-4秒 shots.
4. **Beat packing**: one segment should usually contain one complete micro-beat, not one isolated sentence. A good segment often contains:
   - setup/action trigger
   - dialogue or OS
   - counter-reaction
   - visual aftertaste or state refresh
5. **Three visual anchors for longer scenes**: identify the opening atmosphere anchor, escalation anchor, and hook/aftermath anchor.

## Segment Density Target

For ordinary dialogue-drama scenes:

- Each segment should usually have 3-5 shots and 10-15 seconds.
- Each segment should cover 2-4 tightly related story actions when dialogue density allows.
- Avoid segments that only contain "one sentence + one reaction" unless the single sentence is a major turn.
- If a segment has low dialogue count, add visual information: reaction shot, physical prop/action, spatial re-confirmation, sound cue, or emotional after-beat.
- If a segment becomes too long, split at a plot boundary, not mid-action or mid-emotion.

## High-Density Shot Formula

Each shot line should be a compact natural-language sentence, not a list of labels. Include these elements:

```text
3秒 中近景 / 缓慢推进 / 入口侧同轴，A左看右、B右看左，前景A中景B后景C；镜头从A的手部紧绷推进到脸侧，A开口前先压住呼吸，台词某词咬重，说完后视线避开B；环境声/动作声；[光效]
```

Mandatory content in each shot:

- **Internal shot function**: decide what the shot must accomplish before writing, then show it through visible blocking, framing, movement, focus, distance, occlusion, held reaction, or sound.
- **Cinematic behavior**: final shot lines must not explain purpose; the camera behavior and character reaction must make the story effect visible.
- **Camera motion**: start point, movement, speed, and end point.
- **Space sentence**: where the key people still are; if no one moved, say the original spatial relationship remains.
- **Performance process**: emotion as a change, not a label. Use "先...随后...说到...时...说完后..." when possible.
- **Dialogue fusion**: if the shot contains dialogue or OS, merge it with breath, mouth tension, pause, eye-line, gesture, and after-reaction.
- **Sound/physical cue**: environment sound, footstep, fabric, water, weapon, breath, impact, or silence.
- **Lighting shorthand**: `[光效]` only after the scene visual style master has been written.

## Expression And Distance Scaling

Do not over-describe micro-expressions when the camera cannot see them.

- **Full shot / far shot / high angle / distance > 5m**: describe macro body state only: shoulders tighten, steps stop, group formation shifts, body leans back. Do not write pupils, eyelashes, sweat beads, or mouth muscle details.
- **Medium shot / 2-5m**: allow larger facial cues: brows press down, mouth corners stiffen, jaw line tightens, breathing pauses, eyes avoid contact.
- **Close shot / under 2m**: allow micro details: eyelids tremble, lips part before speaking, throat swallows, fingers press into fabric or palm.
- If global lighting makes a micro detail physically invisible, do not describe it. Use posture, silhouette, or breath instead.

## Dialogue Fusion Rules

- Do not place dialogue as a bare quote after a shot description.
- For every spoken line, include:
  - pre-speech physical cue
  - voice quality or pause
  - exact dialogue
  - expression/action while speaking
  - after-reaction or silence
- For source-authored OS/VO, preserve the text exactly and pair it with a visible physical reaction. Example: "小七在沈寒渊怀中微微僵住，视线从赵烈逃跑方向滑回陆清韵，OS：..."
- Do not add new OS/VO to fill information density.

## Space In The Foreground Prompt

The ledger can be compact, but shot prompts must still contain natural spatial language.

Good:

```text
陆清韵仍停在中偏左，没有靠近沈寒渊；赵烈留在右后出口前，沈寒渊抱着小七站在后景中线不动。
```

Bad:

```text
空间关系不变。
```

Every close shot or over-shoulder shot must still say where the off-screen target remains.

## Sound And Physical Cause-Effect

Each segment should include sound and physical feedback, not only dialogue:

- Environment: wind, rain, water, insects, hall echo, forest hush.
- Action: footstep, fabric rub, cup touch, sword air-cut, breath catch.
- Material response: dust lift, water ripple, branch tremble, sleeve swing, tea surface tremble.
- Silence can be used as a beat, but do not write BGM.

## Output Structure Upgrade

Use this compact add-on in each segment:

```text
本段生成规划
- 冲突功能：
- 负载：
- 情绪曲线：
- 视觉锚点：
- 打包理由：
```

Then write the usual Danjie fields. The shot list should use high-density natural shot lines. Keep ledgers compact; spend the saved characters on shot content.

## Self-Check

Before finalizing, reject and revise if:

- A segment contains only one thin dialogue beat and no reaction/physical after-beat.
- Shot lines can be reduced to "景别 + 运镜 + 动作" without losing much; this means they are too thin.
- Dialogue appears as naked text without performance, breath, pause, or after-reaction.
- Close shots omit spatial relation to off-screen characters.
- Full shots describe invisible micro-expressions.
- Sound design is absent for a segment with action, tension, or physical movement.
- The segment has no visual anchor or emotional movement.
