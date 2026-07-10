# TRANSITION-001 — Universal AI Video Transition Grammar（通用 AI 视频转场语法）

> Canonical Knowledge Node（官方知识节点）
>
> Category：Transition Language
>
> Version：1.0
>
> Status：Active

---

# Definition（定义）

## 中文

Universal AI Video Transition Grammar 是 TSOS 的通用视频转场语言。

它用于把两个镜头或两个场景连接成一个可信、可生成、可剪辑的连续段落。

转场不是单独的特效。转场必须同时服务：

- 故事节奏
- 角色连续性
- 空间理解
- 情绪推进
- 剪辑落点
- 模型可读 Prompt

## English

Universal AI Video Transition Grammar is the reusable transition language for TSOS video production.

It connects two shots or scenes through a motivated visual, motion, emotional, temporal or editorial bridge.

---

# Source Inspiration（来源启发）

This node was adapted into TSOS from a Douyin note by `末鹿` about AI video transition prompts.

Source note:

```text
https://v.douyin.com/ogjaLe3sFsY/
https://www.douyin.com/note/7657192620547935498
```

Visible source categories included:

```text
light / shadow transitions
action occlusion transitions
camera movement transitions
natural material transitions
emotional flashback transitions
time passage transitions
spatial crossing transitions
classical editing techniques
```

TSOS does not copy the source note as a prompt list.

This node converts the visible category system into reusable TSOS transition grammar for Jump / 跳跳 and other future video projects.

---

# Core Principle（核心原则）

Every transition must answer five questions:

```text
1. What is the outgoing shot?
2. What visible carrier creates the transition?
3. What changes during the transition beat?
4. What is the incoming shot?
5. What must stay continuous?
```

If a transition cannot answer these questions, it is decoration, not production language.

---

# Transition Grammar（转场语法）

Use this structure when writing model-facing prompts:

```text
Transition from [outgoing shot] to [incoming shot] using [transition carrier].
The transition begins when [anchor event].
[Carrier] fills or redirects the frame for [transition duration].
The next shot is revealed through [incoming reveal].
Maintain [identity / outfit / object / lighting / spatial continuity].
```

中文结构：

```text
从 [前一个镜头] 转到 [下一个镜头]。
转场由 [可见转场载体] 触发。
当 [动作或画面锚点] 发生时开始转场。
[转场载体] 在画面中完成遮挡、运动、光影变化或情绪变化。
随后自然揭示 [下一个镜头]。
保持 [角色身份 / 服装 / 道具 / 光线 / 空间关系] 连续。
```

---

# Transition Duration（转场时长）

| Type | Suggested Duration | Best Use |
|---|---:|---|
| Hard editorial cut | 0.1s - 0.3s | Beat cut, joke, surprise, rhythm |
| Occlusion / whip / light wipe | 0.3s - 0.8s | Short-form video, action continuity |
| Cinematic dissolve / emotional bridge | 0.8s - 1.5s | Mood shift, memory, reflection |
| Time passage / spatial crossing | 1.5s - 3.0s | Montage, location jump, day-night change |

For AI video generation, the full clip may be longer, but the transition beat itself should stay clear and short.

---

# Transition Families（转场类型）

## 1. Light / Shadow Transition（光影转场）

Use light, shadow, glow, darkness or exposure changes as the transition carrier.

Best for:

- Work-to-life mood shift
- Evening light changes
- Screen glow to city light
- Door opening into warmer light
- Memory or dreamlike soft transitions

Reusable patterns:

```text
screen glow bloom
lamp flare wipe
passing shadow wipe
darkness swallow and reveal
window light sweep
neon flicker cut
sun flare dissolve
flashlight sweep reveal
```

Model-readable block:

```text
Use a warm light flare as the transition carrier. The outgoing shot ends as the light blooms across the frame. The bloom briefly fills the screen, then fades down to reveal the next location. Keep the character identity, clothing and emotional tone consistent.
```

Avoid:

- Overexposed white screen with no reveal logic
- Random neon effects that break the brand mood
- Horror-style high-contrast shadows unless explicitly approved

Jump rule:

```text
Light may hide Jump briefly, but the reveal must keep Jump as a real dog-form character wearing clothes.
```

---

## 2. Action Occlusion Transition（动作遮挡转场）

Use a body, hand-free dog action, prop, door, cloth, bag, foreground object or passing object to cover the frame.

Best for:

- Natural short video transitions
- Character-led continuity
- Moving between desk, hallway, street and shop
- Hiding a scene change behind a motivated action

Reusable patterns:

```text
backpack passes close to lens
door closes to black and opens to new scene
coat or scarf sweeps across frame
foreground passerby wipes the frame
shopping bag crosses lens
elevator door wipe
curtain sweep reveal
table edge or laptop lid close cut
```

Model-readable block:

```text
Use an action occlusion transition. As the character moves past the camera, the backpack briefly fills the frame. Cut during the full occlusion, then reveal the next shot as the backpack exits frame. Preserve the same character, outfit, backpack color and direction of movement.
```

Avoid:

- Human hands appearing to create the wipe for Jump
- Occlusion without a clear incoming reveal
- Objects changing color or shape across the cut

Jump rule:

```text
The occluding action must be possible for a real dog-form character wearing clothes. Do not create human arms, human hands or a bipedal human pose.
```

---

## 3. Camera Movement Transition（镜头运动转场）

Use camera movement as the transition carrier.

Best for:

- Energy shift
- Location move
- Matching screen direction
- Linking two action beats
- Making AI shots feel edited instead of disconnected

Reusable patterns:

```text
whip pan
push-in match cut
pull-back reveal
tilt to sky then tilt down
tilt to ground then lift up
orbit handoff
rack focus handoff
tracking move continuation
foreground parallax wipe
```

Model-readable block:

```text
Use a fast but realistic whip pan transition. The outgoing shot pans right until motion blur fills the frame. The incoming shot continues the same rightward motion and resolves into the new scene. Keep the motion direction continuous and avoid impossible camera paths.
```

Avoid:

- Unmotivated drone-like spins
- FPS-game camera motion
- Physics-breaking camera teleportation
- Extreme wide-angle distortion

Relationship:

```text
Use SHOT-001 for companion tracking movement.
Use SHOT-002 when the same scene must remain locked while the camera angle changes.
Use TRANSITION-001 when moving from one shot or scene into another.
```

---

## 4. Natural Material Transition（自然材质转场）

Use water, rain, smoke, fog, dust, snow, steam, leaves, petals, sparks or clouds as the transition carrier.

Best for:

- Outdoor life montage
- Restaurant steam / street snack moments
- Rainy evening atmosphere
- Soft emotional changes
- Magical but grounded transitions

Reusable patterns:

```text
steam fills frame
rain streak wipe
water ripple dissolve
smoke drift reveal
dust cloud wipe
falling leaves wipe
snow drift dissolve
spark burst cut
cloud cover reveal
```

Model-readable block:

```text
Use rising steam as the transition carrier. Steam from the food gradually fills the frame, softening the outgoing shot. As the steam clears, reveal the next shot in a warm evening location. Keep the color palette natural and cinematic.
```

Avoid:

- Material effects that become fantasy magic unless approved
- Particles hiding identity errors
- Overly dense smoke that prevents review

Jump rule:

```text
Natural material can pass in front of Jump, but the next reveal must preserve dog anatomy, clothing and accessories.
```

---

## 5. Emotional Flashback Transition（情绪闪回转场）

Use memory, blur, exposure pulse, color drain, photo match or sound bridge to connect present emotion with memory or reflection.

Best for:

- Reflection moments
- Before / after work contrast
- Emotional realization
- Gentle nostalgia
- Creator-life montage

Reusable patterns:

```text
soft blur into memory
photo frame match cut
color drains then returns
heartbeat exposure pulse
slow dissolve through eye-line
sound bridge before visual cut
screen reflection flashback
```

Model-readable block:

```text
Use an emotional flashback transition. The outgoing shot softens into a brief warm blur as the character looks toward the light. The blur dissolves into the next shot, revealing a calmer after-work moment. Keep the mood warm, gentle and grounded.
```

Avoid:

- Overly tragic mood
- Random dream imagery that changes canon
- Flashback that changes Jump into a different species or body type

---

## 6. Time Passage Transition（时间流逝转场）

Use visible time markers or environmental change to move time forward.

Best for:

- Workday ending
- Sunset to night
- Waiting, walking, commuting
- Montage compression
- Production sequences

Reusable patterns:

```text
day-to-night timelapse
clock hand match cut
calendar flip
screen time change
street light turning on
crowd flow blur
weather shift
shadows lengthening
coffee cup lowering from full to empty
```

Model-readable block:

```text
Use a time-passage transition. The camera holds on the same window as daylight fades into warm evening light. The changing light bridges the cut and reveals the next shot after work. Preserve the same world, style and emotional direction.
```

Avoid:

- Time jumps that confuse the story
- Changing outfit or identity without reason
- Day-night shift that reverses established light direction inside a locked scene

---

## 7. Spatial Crossing Transition（空间穿越转场）

Use thresholds, doors, windows, mirrors, screens, elevators, vehicles or corners to move from one space to another.

Best for:

- Office to street
- Street to shop
- Studio to cinema
- Real-world location changes
- Social short video transitions

Reusable patterns:

```text
doorway threshold
window reflection reveal
mirror pass-through
elevator door open
subway / car window cut
turning a street corner
screen-to-real-world match
map or phone screen portal
aisle shelf wipe
```

Model-readable block:

```text
Use a spatial crossing transition. The character moves through a doorway; the door frame briefly fills both sides of the image. As the camera follows through the threshold, reveal the next location. Keep the character scale and movement direction consistent.
```

Avoid:

- Literal fantasy portals unless the project asks for them
- Unexplained teleportation
- Scene change that breaks geography or character scale

---

## 8. Classical Editing Transition（经典剪辑技法）

Use established editing logic instead of a visible effect.

Best for:

- Clean storytelling
- Rhythm and pacing
- Comedy or surprise
- Music-driven montage
- Professional continuity

Reusable patterns:

```text
match cut
graphic match
action match
cut on beat
smash cut
jump cut
dissolve
crossfade
L-cut sound bridge
J-cut sound bridge
eyeline match
shot-reverse-shot bridge
```

Model-readable block:

```text
Use a match cut transition. End the outgoing shot on a circular object in the center of frame. Begin the incoming shot with another circular object in the same position and scale, then continue the action naturally. Keep the edit clean and motivated.
```

Avoid:

- Cuts that feel random
- Graphic match that changes the story object without clarity
- Jarring music cuts unless intentionally comedic

---

# Storyboard Annotation Rule（分镜标注规则）

Storyboards must remain:

```text
black-and-white rough pencil line art
```

Colored annotations may describe transitions:

```text
Purple = continuity / transition path
Red = camera movement
Blue = character / dog movement
Yellow = prop / occlusion carrier
Green = lighting / mood / time change
```

Transition notes should be placed beside the cut between shots:

```text
Shot 2 -> Shot 3:
Purple arrow: backpack occlusion wipe
Yellow mark: backpack fills frame
Red arrow: camera continues rightward
```

---

# Prompt Runtime Rule（提示词运行规则）

Internal TSOS references may use:

```text
TRANSITION-001
Universal AI Video Transition Grammar
```

Model-facing prompts must translate this into natural language.

Do not write only:

```text
use TRANSITION-001
apply transition language
```

Write:

```text
Use a warm light flare transition. The outgoing shot ends as the lamp glow expands across the frame, briefly filling the image, then fades down to reveal the next shot. Keep the same character identity, clothing, backpack and gentle after-work mood.
```

---

# Jump Runtime Rule（跳跳运行规则）

When used for Jump / 跳跳, every transition must preserve:

```text
Jump remains a real dog-form character wearing clothes.
```

Transitions must not create:

- humanoid body
- human hands
- human arms
- human legs
- bipedal human standing pose
- unclothed ordinary pet dog
- species change
- outfit loss
- backpack or accessory drift without reason

---

# Selection Guide（选择指南）

| Story Need | Preferred Transition Family |
|---|---|
| Warm mood shift | Light / Shadow |
| Natural scene change | Action Occlusion |
| Energetic rhythm | Camera Movement |
| Food, street, weather, atmosphere | Natural Material |
| Memory or reflection | Emotional Flashback |
| Montage or waiting | Time Passage |
| Location change | Spatial Crossing |
| Clean professional edit | Classical Editing |

---

# Model-Readable Check（模型可读检查）

Before using a transition prompt, check:

```text
[ ] The outgoing shot is named in natural language.
[ ] The incoming shot is named in natural language.
[ ] The transition carrier is visible or editorially clear.
[ ] The transition has an anchor event.
[ ] The transition duration is reasonable.
[ ] Continuity locks are stated.
[ ] Model-facing text does not rely on raw internal IDs.
[ ] For Jump, dog-form identity and clothing are preserved.
[ ] Storyboard notes keep black-and-white rough pencil line art.
[ ] Colored transition annotations use purple and supporting colors correctly.
```

---

# COMMAND-005 Review Requirements（COMMAND-005 审查要求）

COMMAND-005 must check transitions for:

```text
[ ] Whether the transition is motivated by story, action, light, time, space or edit rhythm.
[ ] Whether the transition carrier is legible.
[ ] Whether the incoming shot reveal is clear.
[ ] Whether the transition preserves character identity and outfit continuity.
[ ] Whether Jump remains a real dog-form character wearing clothes.
[ ] Whether transition notes are model-readable natural language.
[ ] Whether storyboard transition annotations use the colored annotation system correctly.
[ ] Whether the transition avoids raw internal IDs in model-facing prompt sections.
```

---

# Relationship With Other Knowledge（与其他知识节点关系）

```text
SHOT-001 = companion tracking movement
SHOT-002 = same-scene camera consistency
MOTIONLANG-001 = believable character motion
TRANSITION-001 = bridge between shots or scenes
```

TRANSITION-001 can combine with:

- SHOT-001 for moving with Jump through a transition
- SHOT-002 for locking a scene before changing camera angle
- MOTIONLANG-001 for preserving believable motion across cuts
- STYLE-001 and COLOR-001 for keeping cinematic warmth

---

# Changelog（更新记录）

| Version | Date | Changes |
|---|---|---|
| 1.0 | 2026 | Initial universal AI video transition grammar adapted from verified Douyin source categories |
