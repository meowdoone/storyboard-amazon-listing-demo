# Storyboard Amazon Listing Demo Skill

Amazon 版沿用 TikTok storyboard skill 的三段式输出结构，只改平台差异，并把第 2 段升级为证据驱动的创意商品证明故事版。

默认只输出：

```markdown
## 1. 产品图

## 2. 故事版

## 3. 15 秒或者 30 秒视频脚本文字
```

关键差异：

- TikTok：9:16 vertical，creator / UGC，手机短视频感。
- Amazon：16:9 landscape，产品为主，listing / A+ 商品展示感，但仍要具备社媒使用语境和产品行为适配的创意方向。

`产品为主` 不等于删掉使用关系。凡是依赖真实交互才能证明价值的产品，故事版必须出现必要的使用人、操作者、佩戴/承载关系、接触表面、兼容对象或互动主体；只是不能让这些元素压过商品。

第 2 段 `故事版` 内部固定包含：

```text
创意大片方向
+ 同一拍摄世界锁
+ 5 格 16:9 连续关键帧
```

执行时先做产品证明判断：

```text
识别产品行为和买家问题
+ 锁真正会漂的产品真相
+ 判断 reason_to_watch
+ 设计 product_entrance
+ 选择证据支持的 buyer event
+ 用低 AI 风险拍法承载这个事件
+ 再写 5 个 16:9 keyframe
```

默认输出仍然是一张故事版图：图里包含 5 格连续的 16:9 keyframe。产品行为判断、买家问题、产品进入方式和 buyer event 只发生在内部，不作为额外输出段落。

低 AI 风险不是最终目标。故事版不能退化成平铺、微距、挂拍、CTA 的目录图；至少两格要承担真实使用事件或结果 payoff，至少两格要能检查商品细节。buyer event 必须来自商品证据、可见功能、listing 语境或用户明确要求，不能为了创意强行加礼物、家庭、户外、剧情化人物或无关道具。

借鉴 [`lala-guantou/tvc-storyboard`](https://github.com/lala-guantou/tvc-storyboard) 的不是五阶段确认流程，而是创意判断骨架：

```text
reason_to_watch
+ product_entrance
+ buyer_event
+ visual_proposition
+ realism_check
```

这几个判断只用于让 5 格图更像真实品牌/商品视频，而不是把 skill 改成 TVC 提案工具。

规则来源：

- 参考 [`ai-video-storyboard-skill`](https://github.com/aicontentskills/ai-video-storyboard-skill/blob/main/SKILL.md) 的 shared visual theme：五格必须像同一次拍摄。
- 参考 [`ecommerce-image-workflow`](https://github.com/nexu-io/open-design/blob/main/skills/ecommerce-image-workflow/SKILL.md) 的 reference-product mode：没有真实产品图，不做最终商品故事版。
- 参考 [`film-storyboard-skill`](https://github.com/RainLib/AI-Storyboard/blob/main/.claude/skills/film-storyboard-skill/SKILL.md) 的 film treatment：创意方向必须包含场景、光线、镜头和情绪，而不是只写“大片感”。

不要默认输出 FYPro 关键词、JSON、长平台分析或额外建议。

## Use

```text
用 storyboard-amazon-listing-demo，基于这个 Amazon 商品链接输出产品图、16:9 产品行为适配故事版、15 秒英文脚本。
```

```text
用这个产品图做 Amazon 版故事版，内部图片尺寸 16:9，产品为主，先识别产品行为和买家问题，再锁产品真相、拍摄世界和 5 个连续关键帧。
```

```text
用这个 Amazon 商品链接做故事版，先判断买家真正要确认的问题和产品如何进入视频；buyer event 必须由商品证据支持，不要添加无关生活方式剧情。
```
