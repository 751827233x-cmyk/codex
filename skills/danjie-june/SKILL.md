---
name: danjie-june
description: Generate AI short-drama and short-video storyboard execution drafts from novels, scripts, dialogue scenes, or scene outlines using the Danjie June rules. Use when the user asks for AI短剧分镜, 分镜执行稿, 视频化分镜, 短视频镜头脚本, 运镜提示词, or converting Chinese story/script text into production-ready AI video prompts with strict dialogue preservation, shot timing, movement, lighting, sound effects, anti-axis-crossing rules, vertical 9:16 spatial continuity, and multi-batch consistency constraints.
---

# 丹姐6月

## Core Workflow

1. Read the user's source material, reference images, and any explicit scene requirements before drafting.
2. If producing a full storyboard execution draft, load `references/full-guidelines.md` and `references/axis-continuity.md`; follow both as the authoritative specification.
3. Split by complete dramatic beats. Preserve all original dialogue exactly; never delete, compress, paraphrase, or rewrite dialogue to fit timing.
4. Establish the scene's action line, camera safety side, screen-left/screen-right assignments, and vertical 9:16 lanes before writing shots. Keep this as a production ledger, not repeated as verbose AI-video prompt text.
5. Track each character's position, posture, facing direction, props, visible condition, emotion, eye-line, screen direction, and vertical-frame lane from segment to segment.
6. Draft each segment with the fixed output structure below, keeping each segment prompt under 1900 Chinese characters.
7. Self-check every segment before delivering. Fix violations before output.

## Non-Negotiable Rules

- Dialogue is never deleted. If dialogue exceeds density limits, split the segment; if dialogue is too sparse, merge with adjacent material.
- Keep dialogue density within 20-45 Chinese characters per 15 seconds, excluding punctuation, and add a dialogue count note in the script-content field.
- Each segment should normally contain at least 2 dialogue lines. A 1-line segment may only be 4-6 seconds with no more than 3 shots. Pure action/no-dialogue segments may only be up to 4 seconds with no more than 2 shots.
- Each shot lasts 2-4 seconds. Each segment lasts no more than 15 seconds. The final spoken line must end at least 1 second before the segment ends.
- Cuts are direct cuts only. Camera movement exists only inside one shot; never use movement to transition between shots.
- Every shot must include duration, camera movement, speed, framing, emotion, action, eye-line, spatial relationship, and `[光效]`.
- Do not repeat the same movement style in adjacent shots. Main movement choices should favor left/right pan, rotating tilt up/down, and slow push-in; no single movement type should exceed 30% of shots in a segment.
- Characters cannot stand still and recite lines. Anyone visible must have a relevant facial reaction or body micro-action.
- Position, posture, facing direction, action momentum, and emotion must continue smoothly between segments. Any change requires an explicit transitional action.
- The scene must include a `场次空间锁定表` and every segment must include a compact `连续性承接表`. These ledgers are for continuity control and should not be copied verbosely into every AI video prompt line.
- Never cross the axis accidentally. Define the main action line and camera safety side, then keep every shot on that side unless a visible scripted axis reset happens.
- Lock screen direction in 9:16 vertical video. State who stays screen-left/screen-center/screen-right, who looks screen-left/screen-right, and which vertical lane (left 30%, center 50%, right 70%) each subject occupies.
- Reverse shots must be same-axis or same-side reverse shots. Do not write free "反打" that flips screen direction.
- In close shots and over-shoulder shots, preserve orientation by naming the visible shoulder, off-screen eye-line, screen direction, and vertical-frame lane.
- Use compact shot duration format by default: `2秒`, `3秒`, `4秒`. Do not write timeline ranges like `00:00-00:02` unless the user explicitly asks for timeline editing.
- In AI video prompt lines, include only visually useful continuity words such as `入口侧同轴`, `同侧过肩`, `沈左/陆中/李右`, `前景/中景/后景`. Avoid verbose labels like `轴线：新场景建轴 + 屏幕方向：... + 竖屏构图：...` in every shot.
- Full shots are for spatial reference. Full shots must not contain dialogue, OS, VO, or off-screen narration. Full shots are max 2 seconds and must still include movement.
- Start a new scene with a full shot. End the first segment with a silent full shot after all dialogue. Add a silent full shot after major position/posture/facing changes.
- Ending shots cannot be full shots and must serve the next segment's continuation.
- Use varied shot sizes: full shot, medium shot, medium close shot, close shot. Do not use face close-ups or chest-above close-ups except brief eye/mouth inserts at key emotional explosions.
- If no reference image and no explicit scene requirement is provided, do not invent clothing, appearance, or scene description words. Write only action, emotion, camera movement, lighting, and spatial relationships.
- If a reference image is provided, follow visible clothing, appearance, and scene details strictly. If explicit scene requirements are provided, follow them without adding unmentioned elements.
- Ignore clothing/appearance descriptions inside the script unless they are supported by a provided reference image.
- Preserve script-authored OS/VO exactly when the source script already contains it. Do not invent new OS/VO, narration, or off-screen lines.
- Never include unscripted旁白, black screen, subtitles, text-on-screen, subtitle-like descriptions, BGM, BGM fields, eye catchlights, facial light spots, or random Tyndall light.
- Use Tyndall light only when the scene clearly has light passing through particles such as smoke, dust, mist, or candle smoke.

## Lighting Rules

Use the base lighting vocabulary from `references/full-guidelines.md`. In each segment and shot:

- Use cinematic focal lengths, 8K ultra-realism, HDR, high contrast, rim/back light, shallow depth of field, clean faces, and no text/subtitles.
- Male characters use Rembrandt lighting.
- Female characters use butterfly lighting.
- Atmosphere shots use rim light and backlight.
- Medium-close and close shots must use backlight or side-backlight to create an edge light.
- Match color temperature to genre and keep it consistent within a scene.
- Do not write eye catchlights. Do not write facial speckles, facial light spots, or dirty light patches on faces.

## Visual Style Completeness

- Do not replace the original detailed visual style with vague phrases. Each new scene must include a full `本场画面风格母版` that covers cinematic focal length, 8K ultra-realism, HDR, high contrast, rim/back light, shallow depth of field, clean faces, gender-specific lighting, genre color temperature, no text/subtitles/BGM, no eye catchlights, and no facial light spots.
- For later segments in the same scene, write `沿用本场画面风格母版` plus the segment-specific mood and lighting change. Do not omit the style system entirely.
- Shot lines may use `[光效]` to save space only after the scene style master has been written.
- For female-oriented realistic爽剧, emphasize emotional contrast, clean but high-pressure lighting, restrained romantic rim light, shallow depth of field, and reaction-shot atmosphere without adding decorative text or sticker effects.

## Fixed Output Structure

Use this structure for every segment:

```text
第X段

场景
- 场次编号：
- 地点：
- 时间：
- 内/外景：

实际出场人物
- 人物A
- 人物B

人物站位
- 左侧：
- 中间：
- 右侧：
- 前景：
- 后景：
- 中轴关系：

场次空间锁定表
- 画幅：
- 世界坐标：
- 主轴线：
- 摄影机安全侧：
- 屏幕方向锁：
- 纵深层级：
- 竖屏安全区：
- 允许机位：
- 禁止机位：
- 本场连续性状态：

本场画面风格母版
（首次出现本场时完整写出电影焦段、8K超写实、HDR高对比、浅景深、轮廓光/逆光、男女打光方式、题材色温、无字幕无BGM、禁止眼神光和面部光斑；后续段落可写沿用母版+本段氛围）

人物视线关系位
- 人物A视线朝向：
- 人物B视线朝向：
- 当前是否对视：
- 视线关系是否对上：

人物特殊道具、姿态状态
- 人物A：哪只手拿什么道具 / 姿态 / 动作 / 情绪 / 持续中的外观状态
- 人物B：哪只手拿什么道具 / 姿态 / 动作 / 情绪 / 持续中的外观状态

连续性承接表
- 承接上一段末帧：
- 本段开始状态：
- 本段结束状态：
- 下一段首帧约束：

画面视觉基调
固定光效词组 + 当前剧情专属氛围、光影、空间重点、打光方式、色温基调、近景逆光要求、丁达尔光是否适用；全程无BGM、无字幕。

首帧镜头
第一段直接写本段首帧；第二段起，首帧必须避开上一段最后一个镜头中的人物，优先写其他人物的单人镜头。

剧本内容
严格保留原剧本内容，不漏台词，不删台词；可补动作、情绪、特效过程，但不能改变剧情。
台词字数统计：XX字，段时长XX秒，符合15秒内20字≤台词≤45字。

分秒运镜及切镜视频提示词
2秒 景别 / 运镜方式（速度） / 构图方式 + 简短空间锁定词（如入口侧同轴、沈左陆中李右、同侧过肩、前中后景） + 镜头语言 + 人物表情情绪 + 人物动作 + 视线关系位 + [光效]

特效提示词

音效建议（与运镜联动）
- 环境音：
- 动作音：
- 道具音：
- 特效音：
- 情绪增强音：

主角音色建议
- 主角A：
- 主角B：
```

## Required Self-Check

Before finalizing, check the draft against `references/full-guidelines.md`, especially:

- dialogue completeness and character-count compliance
- direct cuts only
- explicit action line, camera safety side, and stable screen direction
- same-axis or same-side reverse shots only
- vertical 9:16 lane stability and central safe-area framing
- continuity ledger carries previous end state and next first-frame constraints
- shot lines use compact duration format and do not repeat verbose ledger labels
- each new scene has a complete visual style master before `[光效]` shorthand is used
- every shot has movement and `[光效]`
- no BGM/subtitles/black screen/unscripted narration/text-on-screen
- no invented clothing, appearance, or scene words without reference image or scene requirement
- no eye catchlights, facial light spots, or unjustified Tyndall light
- full shots contain no dialogue and are max 2 seconds
- positions, posture, facing direction, visible condition, and emotion continue across segments
- final dialogue leaves at least 1 second of breathing room
