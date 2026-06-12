# 轴线、竖屏空间与分段连续性规则

Use this reference with `full-guidelines.md` whenever drafting AI short-drama storyboard execution drafts. These rules solve accidental axis crossing, vertical-video spatial confusion, and multi-batch continuity drift. They override any looser wording about "left/right" or "space relation" in the base rules.

## Root Causes To Prevent

- Do not mix story-world left/right with screen left/right. "人物在左侧" must state whether it means screen-left, world-left, or frame-left from the current camera.
- Do not let each segment start from a new imagined camera side. Multi-batch generation fails when the prior segment's camera side and screen direction are not carried forward.
- Do not rely on full shots alone to preserve space. Full shots help, but vertical 9:16 framing compresses horizontal distance and can make left/right relationships ambiguous.
- Do not write shot-reverse-shot as free "反打" without an axis rule. Reverse angles easily cross the action line and flip eye-lines.
- Do not use over-shoulder or close reaction shots without naming which shoulder/which screen side is visible.
- Do not describe movement only as "left/right" unless the coordinate reference is fixed.

## Scene Space Ledger

Before the first segment of every scene, create a `场次空间锁定表`. Keep it stable for the whole scene and update it only when the script has explicit movement.

Required fields:

```text
场次空间锁定表
- 画幅：9:16竖屏 / 或用户指定画幅
- 世界坐标：上/下/左/右/前/后分别对应什么固定物或方向
- 主轴线：哪两个人或哪条动作方向形成180度轴线
- 摄影机安全侧：摄影机始终停留在主轴线哪一侧
- 屏幕方向锁：人物A保持屏幕左/右，人物B保持屏幕左/右；A看向屏幕左/右，B看向屏幕左/右
- 纵深层级：前景/中景/后景分别是谁或什么
- 竖屏安全区：主体落在画面中线两侧的百分比位置，头顶/脚底/手部动作不可被裁切
- 允许机位：同侧正侧、同侧斜45度、同侧过肩、同侧中轴近景、同侧低角度/高角度
- 禁止机位：跨过主轴线的反打、从对侧拍摄、让人物屏幕左右互换的角度
- 本场连续性状态：上一段末帧每个角色的位置、姿态、朝向、情绪、道具、外观状态
```

## Axis Lock Rules

- Establish the action line before writing any shot. For dialogue, the line usually runs between the two speakers. For chase/movement, the line follows the movement direction.
- Pick one camera side and stay on that side for the entire scene unless the script contains a visible axis-reset action.
- Keep screen direction fixed: if A faces screen-right and B faces screen-left in one segment, preserve that direction in all later shots of the same scene.
- Reverse shots must be same-side reverse shots. Write "同轴反打" or "同侧过肩反打" and name the screen direction.
- If a new character enters, add them to the existing axis as a triangle: define whether they stand screen-left, screen-center, or screen-right without flipping existing characters.
- A full shot does not automatically reset the axis. It only re-confirms the existing axis unless the script visibly changes movement direction.

## Axis Reset Rules

Only reset the axis when the audience sees the reset happen.

Valid resets:

- A character clearly crosses to the other side of the other character.
- The camera visibly tracks around the characters within one shot and lands on the new side.
- Everyone turns and creates a new shared facing direction.
- A new scene starts with a new full shot and a new `场次空间锁定表`.

When resetting, write:

```text
轴线重置说明：因XX动作，主轴线从A-B调整为A-C；摄影机安全侧从XX侧调整为XX侧；屏幕方向从XX调整为XX。
```

Do not reset the axis because the shot "looks better".

## Vertical 9:16 Rules

- Treat vertical video as a narrow stage. Keep the main relationship on three lanes: screen-left 30%, screen-center 50%, screen-right 70%.
- Do not use wide horizontal blocking as the only relationship cue. Add depth cues: foreground shoulder, midground speaker, background reaction, floor/water/table edge, or light direction.
- Keep key faces, hands, and props inside the central 70% safe area unless a shot intentionally uses foreground occlusion.
- For two-person dialogue, prefer same-side over-shoulder, 3/4 profile, and vertical depth stacking over flat left-right spacing.
- Avoid large lateral pans that change who occupies screen-left and screen-right. If panning, state that screen direction remains locked.
- In close shots, preserve orientation with shoulder, profile direction, or off-screen eye-line: "A remains on screen-left side, looking screen-right toward B".

## Per-Segment Continuity Ledger

Every segment must include a `连续性承接表` before the shot list:

```text
连续性承接表
- 承接上一段末帧：角色/位置/姿态/朝向/视线/情绪/道具/外观状态
- 本段开始状态：必须与上一段末帧一致；如不同，写明剧本动作依据
- 本段结束状态：角色/位置/姿态/朝向/视线/情绪/道具/外观状态
- 下一段首帧约束：下一段必须从谁/哪个方向/哪个屏幕侧开始，不能从谁开始
```

For multi-batch production, copy the final `本段结束状态` and `下一段首帧约束` into the next batch before drafting. If the user gives a later script chunk without prior state, ask for the last segment's continuity ledger or infer cautiously from the last available segment.

## Shot-Line Requirements

Each shot line must include:

- `轴线`：同轴 / 同侧过肩 / 轴线重置中 / 新场景建轴
- `屏幕方向`：A屏幕左看右，B屏幕右看左, etc.
- `竖屏构图`：左30% / 中50% / 右70% / 前中后景层级

Shot-line pattern:

```text
00:00-00:xx 景别 / 运镜方式（速度） / 构图方式 + 轴线：同侧不过轴 + 屏幕方向：A屏幕左看右、B屏幕右看左 + 竖屏构图：A左30%、B右70%、前景XX中景XX后景XX + 镜头语言 + 人物情绪动作 + [光效]
```

## Axis And Vertical Self-Check

Reject and revise the draft if any answer is "no":

- Is the scene's main action line explicitly defined?
- Is the camera safety side explicitly defined and unchanged?
- Do all shot-reverse-shot lines say same-side/same-axis?
- Do screen-left/screen-right assignments stay stable after each cut?
- Does every close or over-shoulder shot preserve off-screen eye-line direction?
- In 9:16, are the characters placed on stable lanes rather than vague left/right?
- Does each segment carry a continuity ledger with previous end state and next first-frame constraints?
- If an axis reset appears, is the reset visible in the action and explained?
