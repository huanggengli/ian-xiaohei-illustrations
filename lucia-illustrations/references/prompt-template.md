# 生图提示词模板

每张单独生成。先查看角色主参考图并作为实际图片输入，不把路径字符串当作已经传入的图片。绝对路径从当前 Skill 所在目录解析，不写死某台机器路径。

输入角色分配：主参考 `assets/ip/lucia-character-sheet.png` 约束人物与受光；用户指定的样图约束构图。若只有主参考为 Image 1；若先传构图图再传角色图，明确写 Image 1 = composition，Image 2 = character。不要混淆。

```text
Generate one standalone 16:9 Chinese article illustration.

References:
{逐一说明实际输入图片的角色：character reference / composition reference / edit target}
Use the supplied Lucía character sheet for identity and warm semi-silhouette rendering, not for copying its standing poses.

Visual setting:
Opaque pure white background, generous negative space, thin slightly irregular black hand-drawn props. Sparse red/orange/blue short handwritten Chinese annotations. One core idea, not a dense presentation slide.

Character:
The same adult woman as the character reference. Natural body proportions, softly rounded facial profile, full cheeks and soft chin, long black hair in {loose / half-up claw clip / low gathered claw-clip long tail}. Deep charcoal and black-brown semi-silhouette, face in shadow without distinct eyes or makeup, restrained warm-brown clothing planes. Relaxed everyday {clothing}. No bag. {Optional simple glasses only if relevant.}

Action and gaze (specify for every image):
Task object: {操作或关注的具体物件及其位置}
Gaze target: {人物实际看向哪里}
Head and neck: {平视／自然转头／轻微低头；仰头时写明高处目标或动作理由}
Body action: {手势、重心、身体朝向如何配合操作}
Use a relaxed neck and task-directed gaze; do not lift the chin to display the profile or face the light. Hairstyle does not dictate pose or props.

Light:
External light direction: {独立于视线指定光源方向}
External warm amber light selectively touches {a few relevant edges or contact areas}. Preserve dark face and body masses. Use minimal soft shading inside the figure, not an orange background wash. No full-body neon tracing, magical orb or self-luminous hands/props.

Theme: {主题}
Core idea: {核心意思}
Composition and action (consistent with the gaze target above): {人物在哪里、动作、道具、信息流向与留白}
Exact Chinese labels: {逐项列出需要显示的文字；没有就明确 no text}

Color roles:
Black lines for props and text, dark brown/charcoal for woman, soft amber for localized light. Orange solid directional arrows for main flow, red for problems or emphasis, blue for feedback or secondary notes. Keep arrows visually separate from soft rim lighting.

Constraints:
Character must perform the conceptual action, not merely stand nearby. Preserve human anatomy; use tools rather than transform the body into a funnel or machine. Leave clear gaps between hands, body and props. Simplify hair strands, folds and shoes for small-scale readability. Usually leave at least 35% white space and keep labels short. Do not add a type title at top left. Invent a new metaphor unless the user explicitly requests adaptation of a supplied example.

Avoid:
handbag, shoulder bag, backpack, chibi, anime doll, white dot eyes, pointed chin, exaggerated model proportions, glamorous makeup, fully illuminated face, unreadable solid-black mass, neon outline, flames, excessive bloom, plastic 3D, cluttered background.
```

## 局部编辑

```text
Edit the supplied image. Change only {specific requested change}. Preserve the other labels, composition, props, aspect ratio, character identity and localized amber lighting. Maintain an opaque white background. Do not introduce bags or extra objects.
```

文字错误先局部改字，明显角色漂移再修人物；不要为了修字重新改变整个构图。多次输出仍有问题时如实报告，不声称稳定复现。
