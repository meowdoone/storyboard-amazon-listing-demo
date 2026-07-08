# Storyboard Amazon Listing Demo Skill

Amazon 版沿用 TikTok storyboard skill 的三段式输出结构，只改平台差异，并把第 2 段升级为类目适配的商品证明故事版。

默认只输出：

```markdown
## 1. 产品图

## 2. 故事版

## 3. 15 秒或者 30 秒视频脚本文字
```

关键差异：

- TikTok：9:16 vertical，creator / UGC，手机短视频感。
- Amazon：16:9 landscape，产品为主，listing / A+ 商品展示感，但仍要具备社媒使用语境和类目适配的创意方向。

`产品为主` 不等于删掉使用人。服装、配饰、美妆、工具、宠物用品等依赖真实使用场景的类目，故事版必须出现穿着者、使用人、操作者或宠物互动；只是不能让人物压过商品。

第 2 段 `故事版` 内部固定包含：

```text
创意大片方向
+ 同一拍摄世界锁
+ 5 格 16:9 连续关键帧
```

执行时先做类目适配：

```text
识别品类
+ 锁该品类真正会漂的产品真相
+ 选择低 AI 风险镜头库
+ 再写 5 个 16:9 keyframe
```

默认输出仍然是一张故事版图：图里包含 5 格连续的 16:9 keyframe。类目适配只发生在内部，不作为额外输出段落。

规则来源：

- 参考 [`ai-video-storyboard-skill`](https://github.com/aicontentskills/ai-video-storyboard-skill/blob/main/SKILL.md) 的 shared visual theme：五格必须像同一次拍摄。
- 参考 [`ecommerce-image-workflow`](https://github.com/nexu-io/open-design/blob/main/skills/ecommerce-image-workflow/SKILL.md) 的 reference-product mode：没有真实产品图，不做最终商品故事版。
- 参考 [`film-storyboard-skill`](https://github.com/RainLib/AI-Storyboard/blob/main/.claude/skills/film-storyboard-skill/SKILL.md) 的 film treatment：创意方向必须包含场景、光线、镜头和情绪，而不是只写“大片感”。

不要默认输出 FYPro 关键词、JSON、长平台分析或额外建议。

## Use

```text
用 storyboard-amazon-listing-demo，基于这个 Amazon 商品链接输出产品图、16:9 类目适配故事版、15 秒英文脚本。
```

```text
用这个产品图做 Amazon 版故事版，内部图片尺寸 16:9，产品为主，先识别品类，再锁产品真相、拍摄世界和 5 个连续关键帧。
```
