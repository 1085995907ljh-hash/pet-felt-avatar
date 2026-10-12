# 提示词与帽子设计

## 帽子选择

明确主题时照做，未指定则把宠物、帽子和背景作为一幅画一起设计。内部比较 2–3 个不同主题/底色组合，选最合适的一组，不必展示方案菜单。主题库开放，下面仅为例子，不是固定轮换清单。不要因为历史测试用过棕色鲨鱼帽，就继续把它当默认。

动物、物体、食物、植物、原创或用户指定的卡通形象均可。将主题的 1–3 个识别元素转成帽顶轮廓、围脸结构和毡片装饰；卡通形象的脸是帽子装饰，不能替换宠物自己的脸，也不自动添加角色名或标志文字。若用户提供特定角色参考，单独标为 hat-design，不能混作宠物身份来源。

| 主题 | 结构 | 建议颜色 | 特别处理 |
|---|---|---|---|
| 小兔 | 围脸绒帽、两根软兔耳、一根略折 | 奶白 + 浅粉 | 帽顶装饰耳与宠物耳分开 |
| 小熊 | 圆帽、两枚短圆毡耳 | 燕麦 + 奶油 | 不挤压长吻犬鼻梁 |
| 青蛙 | 圆顶两枚凸起眼饰 | 鼠尾草绿 + 奶白 | 眼饰不是宠物的额外眼睛 |
| 鲨鱼 | 帽沿少量软牙、小背鳍 | 灰蓝 + 奶白 | 牙属帽沿，不穿入宠物嘴 |
| 小龙 | 短角、圆鼻、小型后脑鬃片 | 藕粉 + 奶黄 | 角与鬃片不切边 |
| 白菜 | 叶片围合后脑、叶脉、脸孔 | 嫩绿 + 奶白 | 是帽子，不是背后漂浮白菜 |
| 草莓 | 红软兜帽、少量籽点、叶冠 | 柔红 + 叶绿 | 籽点不蔓延到宠物毛发 |
| 蘑菇 | 软菌盖、贴合头部帽围 | 陶红 + 米白 | 帽檐不遮眼 |
| 桃子 | 圆润分瓣帽体、小叶片 | 蜜桃粉 + 叶绿 | 分瓣不遮住额头辨识花纹 |
| 小茶壶 | 圆软帽体、短壶嘴与小把手 | 雾蓝 + 奶油 | 把手与壶嘴紧凑，不能挤小宠物脸 |
| 云朵 | 围脸云瓣、轻巧圆顶 | 奶白 + 雾紫 | 白宠配更深背景，避免轮廓融在一起 |
| 卡通小怪兽 | 圆帽、小软角或圆耳、少量绣饰 | 按毛色设计 | 装饰眼与宠物眼睛分层，不生成额外器官 |

黑宠优先浅帽和中浅背景；白宠优先有色帽和中等明度背景；花纹繁复宠物减少帽饰；金棕毛可配灰蓝、鼠尾草绿或奶白帽。用户指定优先。帽与背景也要有可读边界。

## 整体配色判断

- 宠物毛色是固定输入。选帽子主色、少量点缀色，再选一个背景底色；不要先固定棕底再强配帽子。
- 先判断明度：脸与帽沿、帽子与背景都要分得开。白宠不自动白帽白底；黑宠不自动深帽深底。相近色可用，但需有明度/饱和度差。
- 再判断关系：柔和互补色提供清楚轮廓；邻近色营造温柔感。饱和色尽量只作小点缀，不能全图同等抢眼。
- 帽子通常 1–3 色，背景仅一种底色并保留同色毛毡微纹理。不得用多色背景补救配色失衡。
- 可供启发的组合：奶白宠 + 蜜桃帽 + 灰蓝底；橘猫 + 鼠尾草绿青蛙帽 + 暖米底；黑宠 + 奶黄小鸭帽 + 灰紫底；灰宠 + 柔红蘑菇帽 + 浅燕麦底。都需结合实际图检查，不机械套用。
- 小头像预览中首先看见宠物脸，其次帽子主题，最后背景。帽子过大、装饰过多、背景纤维太亮都需减量。

## 英文主模板

替换方括号再使用。英文只是便于明确材质和视角，并非质量保证。图片编号必须与实际调用顺序一致；没有 style 输入时删掉对应行。

```text
Create one square 1:1 illustrated pet avatar.

REFERENCE ROLES
Image 1 [and other actual identity images] shows the actual pet and is the identity source.
Image [actual style index, if supplied] is STYLE ONLY: borrow its fine wool-fiber illustration language and soft bonnet construction, not its pet's breed, face, markings, eye color, pose, lettering, watermark, or exact hat character.

IDENTITY — KEEP THIS INDIVIDUAL PET
[Species; observed face shape and muzzle proportions; coat length/texture and exact color regions; nose; ears; visible eye color; 3–6 distinctive markings or proportions.]
Keep characteristic markings on their correct side. [Conservative handling of genuinely uncertain hidden details, if needed.] Gently soften shapes without turning this pet into a generic kitten or changing a dog's muzzle into a cat's.

POSE AND FRAMING
First correct any sideways source orientation. Upright head and neck, level camera, no head roll: the pet's eye centers are approximately on one horizontal line and natural dropped ears hang down under gravity. Then use a mild three-quarter head view facing image-[left/right], approximately at eye level. Turn horizontally around 20–35 degrees: both eyes remain visible, the far eye slightly narrower, and the muzzle projects toward the chosen side. This is horizontal yaw, not a sideways head tilt. Do not copy tilt from either identity or style references.
Center the combined head-and-hat silhouette in the square. Close head-and-upper-chest portrait, a little chest fur at the bottom. Keep the complete hat, ears and ornaments within generous margins. The face stays the primary focus.

HAT
A cute [theme] bonnet made from soft brushed wool felt, [recognizable silhouette], [face opening and 1–2 details], [colors]. It wraps around the crown and cheeks without hiding eyes, nose or identity markings. [Specific solution for natural ears.] Hat decorations are attached fabric pieces, not extra anatomical ears or eyes. [Optional small under-chin tie; omit if unsuitable.]

CARTOON FOUNDATION, THEN TEXTILE MATERIAL
First redesign the observed identity as a tender 2D storybook cartoon using a few broad soft color masses for head, natural ears, muzzle and upper chest. Gently round the silhouette and modestly enlarge the head relative to chest, while retaining species-specific muzzle proportions, ear type and distinctive markings. Simplify eyes to painted forms with restrained highlights, preserving known iris colors and heterochromia. Use a matte simplified nose and small delicate mouth curves. Fur starts as shaped color masses, not individually traced photographic hairs. Shallow gouache-like form shading. Then render those already-designed shapes with dense fine short wool-felt fibers, softly fuzzy contours, compact felt and brushed-knit bonnet surfaces, and tiny embroidered applique details. Texture supports the drawing; it must not restore photographic pores, glass eyes, realistic grooming or deep 3D volume. If texture were removed, the underlying image would still be an independently drawn cartoon. No photographic underlayer or sculpted toy product shot.

BACKGROUND AND EXCLUSIONS
One single-color [color] wool-felt background across the entire canvas, opaque, with clearly visible but subtle dense fine fibers and low-contrast same-hue microtexture. Solid color means one base hue with tiny fiber-driven tonal variations, not a smooth digital fill. Keep it quieter than the pet and hat. No second background color, decorative pattern, broad gradient, vignette, scenery, cloth folds, cast shadows, text or logos. No frame, watermark, collage, other animals or props. No chunky crochet loops covering the face, plastic toy gloss, 3D product photography, harsh outlines, blanket blur, extra limbs or fused hat/pet anatomy. Color names are instructions, not visible text.
```

不要写“原照片姿态必须不变”；本任务允许转换角度。背景也要细密毛毡感，但纹理对比低于主体，不用数字噪点代替纤维。避免同时加入超真实摄影、扁平矢量等冲突要求。

## 定向修复

- 仍歪头：指出输出中哪只眼更高，要求整体调整头、帽、耳朵的姿态，双眼连线接近水平；不要仅移动单只眼睛或旋转画布。区分水平转头与侧向倾斜。
- 仍太写实：先简化毛发色块、眼鼻嘴与体积，再加短绒；不能只叠加更多纹理。
- 配色不协调：锁定宠物毛色与身份，根据问题只调整帽色或背景底色；保留单色毛毡背景，不默认回到棕色。

- 正脸失败：沿用观察卡的 `target_facing` 替换方向，不能默认反向。`Turn the head horizontally toward image-[chosen direction] into a mild three-quarter view; both eyes stay visible with natural near/far asymmetry. Preserve this individual pet, markings, wool texture, hat and background.`
- 帽顶被裁：`Reduce the combined head-and-hat scale slightly, retain full ornaments and clear top margin, and reduce visible chest before reducing the face excessively.`
- 粗钩织：`Replace chunky yarn loops with dense fine wool-felt fibers and brushed textile nap. Retain markings and facial anatomy. Keep the background single-colored with subtle same-hue felt fibers.`
- 狗变猫：重新附原片，明确原鼻梁和吻部长度、鼻头、耳型，不只补一个 dog。
- 背景不纯或太光滑：`Use one [color] base hue throughout the background, with subtle fine wool-felt fibers and low-contrast same-hue microtexture. No multicolor patches, broad gradients, halo, vignette, patterns or cast shadows. Preserve the fuzzy subject silhouette and all subject fibers.`
- 花纹漂移：回到原片与观察卡明确位置与边界，不反复强化失败图中的错误。
