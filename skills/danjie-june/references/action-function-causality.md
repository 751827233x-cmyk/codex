# 动作功能与因果校验系统

Use this reference before writing any beat involving movement, interruption, attack, warning, restraint, exit, pursuit, spell, weapon, door, obstacle, reveal, or environmental force. Its purpose is to prevent a storyboard prompt from turning a character's reaction into a false physical state.

## Core Principle

Do not describe what the audience emotionally understands as if it were a new physical fact.

Example: if a character stops because a sword energy passes close to their face, the fact is `danger passes close -> character chooses/bodily reacts to stop`; the false fact is `the path is blocked`.

## Root Causes To Prevent

- **Outcome-to-object error**: writing `角色停住` as `路被挡住`.
- **Emotion-to-physics error**: writing `角色害怕不敢走` as `不能走`.
- **Warning-to-blockade error**: writing `擦身警告` as `屏障/封锁/覆盖出口`.
- **Reaction-to-restraint error**: writing `本能后退` as `被力量拖住/定住`, unless the source actually says restraint.
- **Metaphor-to-image error**: turning phrases such as `压住他`, `断了退路`, `不让他走` into visible physical objects when the script only implies pressure.
- **Ledger amplification error**: the planning or continuity table overstates an action, and later shot prompts inherit the wrong logic.

## Action Function Taxonomy

Classify the action before writing shots. Use the weakest function that satisfies the source.

| Function | What physically happens | Character reaction | Do not write as |
|---|---|---|---|
| Warning / 威慑 | danger passes near, lands nearby, sounds near, or shows capability | startles, stops, hesitates, changes tone, chooses not to continue | blocked path, sealed exit, trapped body |
| Interruption / 打断 | action forces a pause in timing | hand stops, foot halts, speech breaks | permanent restraint |
| Real blockade / 封锁 | door, object, person, magic, wall, or body physically prevents passage | cannot pass unless obstacle changes | mere hesitation |
| Hit / 击中 | force contacts the body/prop | injury, stumble, dropped item, pain response | near miss |
| Miss / 擦过/落空 | force passes nearby or hits environment | flinch, dodge, delayed fear | direct hit |
| Restraint / 控制 | body or object is held, bound, frozen, pinned | cannot move freely | voluntary fear reaction |
| Signal / 示意 | action communicates intent without force | notices, looks, understands | attack or restraint |
| Reveal / 暴露 | action uncovers information | realizes, reacts | new physical movement not shown |
| Exit / 离场 | character moves toward leaving | path, body orientation, speed change | instant disappearance without route |

## Five-Step Causality Gate

Before drafting a high-risk beat, answer these internally:

1. **Source fact**: What does the source explicitly say happened?
2. **Action function**: warning, interruption, blockade, hit, miss, restraint, signal, reveal, exit, or another concrete function?
3. **Physical mechanism**: What visible force/object/body movement causes the next reaction?
4. **Reaction owner**: Who changes state because of it, and is the change voluntary, reflexive, or physically forced?
5. **Negative boundary**: What did not happen? Did the path remain open, did the body remain unhit, did the effect vanish, did the character choose not to continue?

Only after this gate should you write `本段生成规划`, `场次空间锁定表`, shot lines, and effects.

## Output Mapping Rules

- `本段生成规划` should name the action function, not just the emotional result.
  - Good: `赵烈借口离场，沈寒渊以擦身警告打断离场。`
  - Avoid: `沈寒渊封住赵烈退路。` unless the path is physically sealed.
- `场次空间锁定表` should preserve physical facts.
  - Good: `出口方向仍可见；赵烈因危险太近本能刹停。`
  - Avoid: `出口被剑气挡住。`
- Shot prompts should separate cause, reaction, and aftermath.
  - Cause shot: source action or force starts.
  - Reaction shot: target flinches, stops, dodges, or changes line.
  - Aftermath shot: environment returns, dust settles, path/position remains clear unless changed by source.
- Continuity ledgers carry the character's new state, not an invented obstacle.
  - Good: `赵烈在右端出口边缘刹停，心虚后退。`
  - Avoid: `赵烈被屏障困住。`

## Language Controls

Use precise verbs:

- Warning / near miss: `擦过`, `落在脚前`, `掠近`, `逼近脸侧`, `本能刹停`, `后仰`, `改口`, `不敢继续`.
- Real block: `挡住`, `封住`, `堵住`, `锁死`, `拦腰截住`, `门合上`, `墙升起`; use only when something physically prevents passage.
- Hit: `击中`, `砸中`, `刺中`, `撞上`, `打落`; use only when contact happens.
- Restraint: `缠住`, `按住`, `锁住`, `冻住`, `钉住`; use only when motion is physically restrained.

Avoid ambiguous shorthand such as `压住退路`, `断了去路`, `被拦住`, `被定住`, unless the source and shot show the exact physical mechanism.

## Shot Construction Patterns

Warning / near miss:

```text
2秒 中景 / 直接切动作源 / A中右，B画外右端；A只抬手，冷光从袖前掠出；动作声；[光效]
2秒 中近景 / 快速掠过后急停 / B右端单人；危险从画外擦过B眼前落在脚前，B本能刹住、后仰，脚步断在原地；急促吸气声；[光效]
```

Real blockade:

```text
2秒 中景 / 跟拍 / B冲向出口；门板在B前方合拢，B被迫停在门前；撞门声；[光效]
2秒 中景 / 拉远 / 出口物理关闭；B手按门板无法通过，A在原位看着；环境声压低；[光效]
```

Hit:

```text
2秒 中景 / 快速推进 / 力量击中B肩侧，B身体偏斜；撞击声；[光效]
2秒 中近景 / 后拉 / B扶住肩膀后退，疼痛反应清楚；呼吸声；[光效]
```

## Self-Check

Reject and revise the segment if any answer is "yes":

- Did I write a warning as a blockade?
- Did I write a character's fear, hesitation, or obedience as a physical restraint?
- Did the planning table, spatial ledger, or continuity ledger overstate the actual source action?
- Did I use words like `挡住`, `封住`, `屏障`, `锁死`, `困住`, `压住去路` without a visible physical object or force that persists?
- Did the shot need only a reaction, but I invented an environment change?
- Did the effect's aftermath contradict the next beat's action, such as saying the exit is blocked while the character later escapes through it?
- Did I use a negative prompt inside the shot line instead of describing the desired visible aftermath?

When in doubt, write the visible cause and the character reaction, not an inferred physical state.
