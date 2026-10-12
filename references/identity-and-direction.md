# 身份提取与跨角度重绘

## 观察卡

每只宠物独立记录，字段无证据时填 unknown。不要把“橘猫”等泛称当身份。

```yaml
subject_id: pet-01
identity_images: []
species: cat_or_dog
breed_hint: unknown
observed:
  head_shape: unknown
  muzzle_length_and_width: unknown
  nose_color_and_shape: unknown
  ears_shape_and_carriage: unknown
  eyes_visible_color_and_spacing: unknown
  coat_base_and_length: unknown
  forehead_cheeks_muzzle_chest_markings: unknown
  asymmetric_marks: unknown
  expression: unknown
source_view: unknown
high_information_anchors: []
unknown_or_occluded: []
target_facing: image_right
pose_change: mild_three_quarter
hat_theme: auto
ear_solution: unknown
background_color: auto
```

这是简报结构，不是生图 API。实际提示词不保留空变量或 unknown 字样，而把不确定事项转换为保守处理。

## 锚点选择

优先能区别于同品种其他宠物的组合：鼻梁偏一侧的白斑、奶油下巴、深色面罩边界、单侧耳色、眼距与吻部长度、眉点、自然卷、垂耳等。可见眼色保留；反光/阴影下无法确认时不猜特定颜色。

照片方向和动物解剖左右分开。记录“原片画面左眼上方深斑”等可核对描述；能确认解剖侧时再写解剖侧。不要为朝向变化镜像整个脸，或把看不见的一侧复制成对称花纹。

不必精准认出品种才能生成。“黑白长毛、细长吻部、半立耳”比不确定品种标签更可靠。不推断姓名、性别、年龄、健康状态。

## 视角转换

| 输入 | 转换方式 | 不得做 |
|---|---|---|
| 正脸 | 轻微转向，双眼保留；优先展现独特斑纹那侧 | 仅倾斜照片冒充 3/4 |
| 已是 3/4 | 保留可信侧面关系，调整裁切和材质 | 无故反转方向与花纹 |
| 完全侧脸 | 同侧转回轻度 3/4；远侧只补最低限度合理结构 | 宣称不可见特殊斑纹已还原 |
| 仰拍/俯拍 | 重绘到接近眼平视，依靠眼距、鼻吻、花纹定位 | 保留夸张透视导致失真 |
| 强遮挡/模糊 | 有足够锚点则保守重绘；否则请求清晰照片 | 仅靠品种想象整张脸 |
| 同宠多图 | 清晰照定身份，侧面照补吻部和耳型 | 把不同光线当作新花纹 |
| 多宠 | 独立绑定身份，按指认或默认分别生成 | 混脸、遗漏目标、串用眼色 |

## 猫狗分流

猫：保留耳间距、腮部、胡须垫、鼻口三角与胡须走向。可适度柔化，但不把长脸猫全变短鼻圆脸猫。

狗：优先保留鼻梁/吻部长度、鼻头体积、额段、眉点、垂耳或立耳、卷毛/直毛差别。贵宾卷毛用细碎纤维小簇表达；长吻犬仍是长吻，不换成猫的粉色小三角鼻。

猫和立耳犬可设帽子开孔；垂耳犬可从帽侧露出或沿脸旁垂下。帽上兔耳/熊耳是缝合装饰，与宠物耳朵分清层次，不长成四只生物耳朵。

仅在用户要求或明确选定表情时闭眼，因为闭眼会损失眼色辨识信息。默认温和清醒，眼睛可略圆润，不用全黑超大玻璃球覆盖虹膜。
