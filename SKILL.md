---
name: storyboard-amazon-listing-demo
description: Use when a user wants an Amazon product-led listing storyboard from a product link, ASIN, product image, product screenshot, ecommerce page, or short product description. The required output format is exactly product image first, then storyboard image, then 15-second or 30-second video script text. The storyboard image uses 5 numbered 16:9 landscape panels and keeps the product as the main subject.
---

# 故事版的 Amazon 商品展示 Skill

## Purpose

Turn a product into an Amazon-ready product-led storyboard package with exactly three default sections:

1. 产品图
2. 故事版
3. 15 秒或者 30 秒视频脚本文字

This skill is intentionally narrow. It is copied from the TikTok storyboard skill structure, but adapted for Amazon listing / A+ / StoreClaw product demo work.

The platform difference is only this:

- TikTok version: 9:16 vertical, creator / UGC, phone-video feel.
- Amazon version: 16:9 landscape, product-led, listing / A+ buyer-proof feel, but still social-commerce usable.

Important: product-led does not mean removing the user. For apparel, wearable items, accessories, beauty, fitness, pet products, tools, or any product whose value depends on human/pet interaction, the storyboard must include the user/wearer/operator/pet in the relevant panels. The product remains the hero, but real use is part of the product proof.

Do not expand this skill into a long Amazon strategy, claim report, task system, or asset pipeline unless the user explicitly asks.

## When To Use

Use this skill when the user asks for:

- Amazon product listing storyboard.
- Amazon A+ or listing demo preparation.
- StoreClaw Amazon image-to-video preparation.
- "先产品图，再故事版，再脚本".
- "亚马逊", "Amazon", "A+", "listing demo", "产品为主", "16:9".
- More products from one brand, each with a product image and storyboard.

Do not use this skill for TikTok UGC, Reels, creator scripts, generic marketing copy, product listing copy, or full campaign reports unless the user explicitly asks to expand beyond the three-section output.

## Core Rule

Default output must contain only these three sections for each product:

```text
## 1. 产品图
## 2. 故事版
## 3. 15 秒或者 30 秒视频脚本文字
```

Hard language rule: the third section's script text must be in English. In the script table, all `屏幕字幕` and `旁白 / 口播` values must be natural English, even when surrounding instructions or section labels are Chinese.

Do not include extra sections by default. Do not add FYPro keywords, negative prompts, correction prompts, long platform analysis, source notes, JSON files, or extra recommendations unless the user asks.

If the user asks for Amazon claim analysis, A+ copy, StoreClaw handoff prompts, or image-generation metadata later, provide them as a separate follow-up output.

## No Autonomous Regeneration

Do not generate new images just because the user asks for keywords, scripts, or video prompts.

Only generate or regenerate images when the user explicitly asks for:

- 故事版
- 生图
- 换一个图
- 重画
- 重新生成
- 多给几张图

If a storyboard already exists and the user asks for keywords or video text, write from the existing storyboard. Do not create a new visual direction.

## Product Intake

Accept any of these inputs:

- Amazon ASIN
- Amazon product URL
- Product URL from another ecommerce site
- Product image
- Product screenshot
- Product name and brand
- Ecommerce page
- Chat context that contains a product link or product direction

If the user gives a brand and asks for more products, find 2-3 suitable products from that brand. Choose products that are visually demonstrable for Amazon listing / A+:

- clear product shape and components,
- obvious setup/use/detail/confidence sequence,
- strong visible material, texture, size, or structure,
- low compliance risk,
- easy for image/video generation tools to understand.

## Product Image Rules

The first section must show or link the product image before any storyboard.

Step 1 only needs to extract or select a clear product image. Do not produce long product analysis, claim analysis, FYPro keywords, video prompts, JSON files, or extra notes in this section.

Prefer official product images from Amazon, the brand site, or ecommerce page. Use the clearest available product image, not a small share-card thumbnail. If the image cannot be fetched, use the best available product screenshot or generated reference image, and label it clearly.

Never make the user infer the product from the storyboard alone.

## Storyboard Rules

The storyboard is the most important part of this skill. It must not be a random lifestyle image or a generic ad mood board.

The goal of the storyboard is to make an Amazon product demo visually clear:

- product is the main subject,
- product shape and components are inspectable,
- real user or wearer proves use when the category requires it,
- social-media usable context, not a dead catalog layout,
- camera distance and angle are clear,
- one useful buyer-proof idea per frame,
- scene supports the product instead of replacing it,
- clean but realistic ecommerce lighting,
- no fake Amazon UI, review stars, badges, coupons, or certifications.

Do not create the storyboard as five unrelated concept images. The storyboard must feel like frames from one continuous shoot. Pick one scene and one visual world first, then vary only camera distance, product action, and framing.

Default storyboard format:

- one contact-sheet style image,
- 5 numbered landscape panels,
- each panel is a 16:9 Amazon-style keyframe,
- panels must form one continuous product-led demo sequence,
- product appearance must be copied from the product image.

The 5-frame visual sequence should follow this logic:

1. Product identity: clean hero view showing the exact SKU, shape, color, and included components.
2. Setup / buyer question: show how the product is prepared, opened, placed, worn, installed, selected, or customized.
3. User proof / detail: show a real person, hand, wearer, operator, or pet interacting with the product while preserving product visibility.
4. Use demo: product being used in a realistic social or daily scene while remaining clearly visible.
5. Purchase confidence / social payoff: scale, fit, included components, finished use state, or a clean final product-led social moment.

For every product, derive the visual chain from what the product actually does. Do not reuse a previous room, person, pet, kitchen, or scene from memory unless the current product naturally needs it.

Keep continuity locked inside the current storyboard:

- same product,
- same product color and geometry,
- same accessories or package only if visible in the product image,
- same user/wearer/operator role if the storyboard uses one,
- same person or same cropped body identity across panels,
- same location only within this generated sequence,
- same lighting family,
- same camera language,
- same shirt fit and print placement for apparel,
- same use state where relevant,
- no scene carried over from previous projects unless the user asks for it.

Product correctness is more important than image beauty. If the generated storyboard changes the product shape, color, label, package, size relationship, button, handle, opening, nozzle, or key structure, regenerate the storyboard before writing the final script.

## Amazon Product-Led Generation Contract

Every storyboard image prompt must include a strict Amazon product-led contract. This contract is mandatory, not optional style guidance.

- The storyboard must look like Amazon listing / A+ product demo frames, not TikTok UGC frames.
- Every panel must be 16:9 landscape.
- All five panels must share one continuous visual world: same wearer/user, same product, same room or street, same light, same camera look.
- Product should usually occupy 45%-70% of each frame.
- Product use must be based on actions the product can visibly support. If the product has no visible physical result, do not invent one.
- At least two panels must show product structure, texture, component, size, or operation close enough for inspection.
- Human presence must match the category. Apparel and accessories require a wearer. Tools require hands/operator. Pet products require pet interaction when the value depends on use. Use hands only for products where a full user would distract from proof.
- Backgrounds must be simple and buyer-relevant but socially usable: mirror/selfie room, street, studio corner, desk, gym, pet area, workspace, kitchen counter, bathroom shelf, outdoor use area, or other product-specific context.
- Text inside generated images must be avoided unless it is required by the product reference. Add final copy later as design overlay, not as AI-generated fake text.
- The final storyboard must prioritize product proof plus real-use social believability over static catalog layout.

For apparel, default to a faceless or partially cropped wearer when model realism is risky. Show torso, hands, mirror reflection, shoulder-level crop, hem adjustment, or walking crop. Avoid generating a new face in every panel.

Avoid:

- TikTok 9:16 vertical framing,
- creator face dominating the frame,
- product hidden inside lifestyle decor,
- removing the user/wearer when the product needs a user to make sense,
- five unrelated scenes or five different people in one storyboard,
- changing the wearer, room, lighting, or shirt fit between panels,
- AI-looking perfect faces, plastic skin, extra fingers, impossible hands, or overposed models,
- glossy fake luxury scene,
- floating product,
- magical transformation,
- fake readable labels,
- fake Amazon badges,
- fake review stars,
- fake certification icons,
- unsupported health, safety, durability, performance, or before/after claims.

Reject and regenerate the storyboard before final delivery if it has:

- product not dominant in most panels,
- product geometry or color drift,
- invented packaging, logo, badge, or readable claim,
- person, pet, or room becoming the main subject,
- apparel/accessory storyboard has no wearer or use person,
- storyboard panels do not look like the same shoot,
- wearer identity, shirt fit, print placement, or lighting changes between panels,
- 9:16 TikTok framing,
- a payoff scene that implies medical, health, pet safety, beauty, or performance claims beyond product evidence.

## Storyboard Realism And Continuity

When a storyboard image already exists, treat these as locked for that project:

- product shape and key parts,
- product color and scale,
- visible setup/use action,
- selected hands/person only if present,
- selected location only if present,
- lighting and ecommerce-shot style,
- camera distance progression,
- apparel fit, print placement, and wearer crop,
- object/result continuity.

Do not rewrite prompts as if starting from a blank canvas, and do not reuse a previous storyboard's person or room as a default.

Bad keyword style:

```text
A creator holds the product in a kitchen...
```

Good keyword style:

```text
Use the attached Amazon storyboard as the visual reference. Preserve the current product shape, product action, selected hands/location, lighting, and 16:9 product-led framing from this storyboard. Animate only the small action in this shot...
```

The model should continue the current storyboard, not重新生一个人物/场景, and not copy a remembered scene from a different product.

## 15- or 30-Second Script Rules

The third section should include a concise script table. Use 15 seconds by default; use 30 seconds when the user asks for it.

Language rule: keep the table headers if desired, but write every screen subtitle and voiceover line in English. The `画面` column can be concise Chinese or English, but the actual script text that would appear on screen or be spoken must be English.

For 15 seconds:

```markdown
| 时间 | 画面 | 屏幕字幕 | 旁白 / 口播 |
|---|---|---|---|
| 0-2s | ... | Product-led hero | "Here is the product at a clear angle." |
| 2-5s | ... | Set it up | "Use the included part to get it ready." |
| 5-8s | ... | See the detail | "This close-up shows the main feature." |
| 8-11s | ... | Use it in context | "Now the product is shown in a real use scene." |
| 11-15s | ... | Check the size | "Confirm the size and fit before purchase." |
```

For 30 seconds:

```markdown
| 时间 | 画面 | 屏幕字幕 | 旁白 / 口播 |
|---|---|---|---|
| 0-3s | ... | Product-led hero | "Here is the product at a clear angle." |
| 3-7s | ... | What is included | "These are the visible parts included with it." |
| 7-12s | ... | Set it up | "Use the included part to get it ready." |
| 12-17s | ... | See the detail | "This close-up shows the main feature." |
| 17-23s | ... | Use it in context | "Now the product is shown in a real use scene." |
| 23-30s | ... | Check before purchase | "Confirm the size and details before purchase." |
```

The script must match the storyboard exactly. Do not introduce new people, rooms, claims, or product actions that are not in the storyboard. Use natural English listing-demo language, not exaggerated brand-deck language.

For Amazon-sensitive categories such as pet, baby, beauty, health, supplement, electronic performance, safety, compatibility, or durability, keep script claims factual and visible. Do not promise cure, safety, indestructibility, medical effects, or before/after results unless the evidence explicitly supports it.

## If The User Later Asks For StoreClaw / FYPro Keywords

StoreClaw / FYPro keywords must be written as image-to-video continuation prompts based on the storyboard, not as fresh text-to-image prompts.

Use this structure:

```text
Use the provided Amazon storyboard/reference frame as the visual source. Preserve the current storyboard's product shape, product action, selected hands/location, lighting, object continuity, and 16:9 product-led framing. Only animate: {small action}. Camera: stable ecommerce demo shot with slight natural movement. Do not change the product, action logic, or selected visual setup.
```

For each frame, mention the locked visual details from the current storyboard and one small motion only.

Do not use prompts that invite the model to create a new person, new room, new product package, or new generic location when a storyboard reference already exists.

## Amazon Style Defaults

Default settings:

- 16:9 landscape
- 15 seconds
- product-led Amazon listing demo with social-media usable real-use context
- clean realistic ecommerce light
- buyer-relevant background
- product occupies 45%-70% of frame
- user/wearer/operator included when the category requires real-use proof
- one simple product action per shot

Prefer:

- clean surfaces,
- product close-ups,
- visible components,
- wearer or use person when the product is apparel/accessory/use-dependent,
- social proof scenes that still keep the product readable,
- one wearer and one location across all panels,
- cropped torso/hands/mirror shots when they reduce fake model risk,
- realistic hand scale,
- simple use context,
- real contact shadows,
- easy-to-inspect product geometry.

Avoid:

- TikTok UGC vertical framing,
- creator-first composition,
- glossy studio mood board,
- fake model posing,
- fake readable labels,
- fake reviews or badges,
- floating product,
- magical transformation,
- unsupported claims beyond product evidence.

## Replacement Image Requests

If the user says "换一个图", regenerate or replace the storyboard image unless they specifically say product image.

Keep the same three-section output structure after replacing the image.

After replacing a storyboard image, update all later scripts or keywords to refer to the new storyboard scene and product state.

## Multi-Product Output

For multiple products from the same brand, repeat the three sections per product:

```markdown
## Product A

### 1. 产品图
...

### 2. 故事版
...

### 3. 15 秒或者 30 秒视频脚本文字
...
```

Choose product order by Amazon storyboard readiness:

1. clearest product image,
2. strongest feature proof,
3. lowest claim risk,
4. easiest 16:9 product-led visualization.

## Quality Check Before Final

Before responding, check:

- Does every product have a product image first?
- Is there a storyboard image after the product image?
- Is the storyboard a 5-panel 16:9 landscape contact sheet?
- Is the product dominant and inspectable?
- Is there a 15-second or 30-second script after the storyboard?
- Are all screen subtitles and voiceover lines in English?
- Did you avoid extra sections unless requested?
- Is the demo idea visually doable for Amazon / StoreClaw?
- Are product claims safe and grounded?
- Did the storyboard pass the product-led rejection criteria?
