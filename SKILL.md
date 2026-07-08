---
name: storyboard-amazon-listing-demo
description: Use when a user wants an Amazon product-led, evidence-grounded creative storyboard from a product link, ASIN, product image, product screenshot, ecommerce page, or short product description. The required output format is exactly product image first, then storyboard, then 15-second or 30-second video script text. The storyboard section contains a Creative Film Treatment, a Shooting World Lock, and one storyboard image with 5 numbered 16:9 product-proof keyframes with the product as the main subject.
---

# 故事版的 Amazon 商品展示 Skill

## Purpose

Turn a product into an Amazon-ready product-led, evidence-grounded creative storyboard package with exactly three default sections:

1. 产品图
2. 故事版
3. 15 秒或者 30 秒视频脚本文字

This skill is intentionally narrow. It is copied from the TikTok storyboard skill structure, but adapted for Amazon listing / A+ / StoreClaw product demo work.

The platform difference is only this:

- TikTok version: 9:16 vertical, creator / UGC, phone-video feel.
- Amazon version: 16:9 landscape, product-led, listing / A+ buyer-proof feel, but still social-commerce usable and visually cinematic.

Important: product-led does not mean removing the user. For any product whose value depends on real interaction, the storyboard must include the relevant user, operator, wearer, pet, surface, compatible object, or environment in the relevant panels. The product remains the hero, but real use is part of the product proof.

Do not expand this skill into a long Amazon strategy, claim report, task system, or asset pipeline unless the user explicitly asks. Product behavior selection, product locks, and the cinematic layer live inside `## 2. 故事版`, not as extra default sections.

## When To Use

Use this skill when the user asks for:

- Amazon product-led evidence-grounded creative storyboard.
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

Reference-product rule: if there is no real product image, reliable product page, or clear product screenshot, do not create a final product-containing storyboard. Ask for a product image or label the result as a rough concept reference. Do not create a brief-only product concept and pretend it preserves the SKU.

Internally extract product identity anchors before creating the storyboard: shape, silhouette, color, material, logo/label placement, visible construction details, proportions, scale cues, and what must not change. Do not expose this as an extra default section.

## Product Behavior Adapter

Before choosing a creative direction, infer one primary product behavior and any secondary modifier. Do not expose this as an extra default output section. The adapter decides what must stay locked, which buyer event is supported by evidence, which proof beats are useful, and which scenes are high risk.

Behavior adapters, not product-type defaults:

- Worn / carried / on-body: lock silhouette, color, fit, placement, scale, and contact with the body or carried object. Use only the body crop or context needed to prove use.
- Personalized / configurable: lock one Design Asset, selected option, preview state, placement, and final output. Do not switch between unrelated logos, messages, photos, or layouts.
- Hand-operated / assembled / installed: lock parts, buttons, handles, openings, cords, ports, setup order, and hand operation. Avoid inventing parts or showing impossible use.
- Applied / dispensed / textured: lock packaging, applicator, visible amount, texture, contact surface, and routine step. Avoid medical, before/after, cure, safety, or performance claims without evidence.
- Connected / paired / compatible: lock ports, screen state if visible, cable direction, compatible object, size ratio, and setup state. Avoid fake UI, wrong ports, fake brands, and sci-fi lighting.
- Placed / displayed / stored: lock material, scale, placement, packaging if visible, surface context, and final arrangement. Avoid decorative locations that hide the product.
- Living-subject interaction: lock product shape, material, contact method, and scale against the person, pet, or subject. Avoid unsupported safety, durability, health, or training claims.

Use the lowest-risk camera method that can still carry a real buyer event. Human faces, large groups, dramatic reactions, outdoor lifestyle scenes, readable UI, and perfect model poses are high-risk unless the product evidence or user request specifically requires them, but do not replace the event with a static catalog sequence.

## Product-Led Creative Triage

Borrow the lightweight thinking of TVC creative development without turning this skill into a multi-stage TVC workflow. Internally decide these five items before writing or generating the storyboard:

1. `shopper_question`: what buyer doubt or decision does the video answer?
2. `reason_to_watch`: why this needs a short video instead of only a static product image.
3. `product_entrance`: how and when the product becomes the clear hero in the first 1-2 panels.
4. `buyer_event`: the evidence-supported action or moment that makes the product matter.
5. `visual_proposition`: the simple filming idea that connects product proof with the buyer event.

Do not expose these five items as extra default sections. They only control the Creative Film Treatment, Shooting World Lock, and five keyframes.

The buyer event must come from product evidence, visible function, listing context, or the user's explicit direction. Reject events that add unsupported props, people, emotional stakes, use cases, locations, UI, or claims. If multiple events are possible, choose the one with the lowest visual invention and strongest product proof.

## Creative Proof Balance

The adapter is a guardrail, not the creative idea. Do not let it collapse the storyboard into five inspection shots.

Before generating the storyboard image, choose one buyer event that makes the product matter and is supported by the provided evidence. Common event families include:

- selection / preview / configuration,
- setup / opening / assembly / placement,
- hand operation / use moment / routine step,
- texture / scale / fit / compatibility proof,
- visible result / final state / storage,
- comparison or transformation only when the source evidence supports it.

The five panels should balance proof and story:

1. Product entrance / SKU anchor: exact product identity and the reason to watch.
2. Event setup / shopper question: why the product is being used or inspected now.
3. Tactile proof: material, print, component, operation, scale, or texture.
4. Use / emotional payoff: the product doing its job in a real scene.
5. Purchase confidence: final readable product state, fit, result, setup, or included pieces.

At least two panels must be inspectable product proof, and at least two panels must carry the buyer event. Reject a storyboard that is only flat lay, macro, hanger, pack shot, and CTA unless the user explicitly asks for catalog assets. Also reject a storyboard whose buyer event is more creative than the evidence supports.

## Realism Guard

Realism is a validation layer, not a style word. The storyboard should look like plausible Amazon listing / A+ / brand production footage.

Before final delivery, reject or regenerate if:

- decorative props or locations distract from the buying decision,
- lighting, surfaces, shadows, hands, scale, or product contact look physically implausible,
- the scene feels like a fantasy ad instead of a believable ecommerce / brand proof asset,
- the product is present but not readable enough for a shopper to inspect,
- the storyboard relies on mood, lifestyle, or emotional staging to compensate for weak product proof.

## Storyboard Rules

The storyboard is the most important part of this skill. It must not be a random lifestyle image or a generic ad mood board.

The goal of the storyboard is to make an Amazon product demo visually clear:

- product is the main subject,
- product shape and components are inspectable,
- real user, operator, subject, surface, or compatible object proves use when product behavior requires it,
- social-media usable context, not a dead catalog layout,
- camera distance and angle are clear,
- one useful buyer-proof idea per frame,
- scene supports the product instead of replacing it,
- clean but realistic ecommerce lighting,
- no fake Amazon UI, review stars, badges, coupons, or certifications.

Do not create the storyboard as five unrelated concept images. The storyboard must feel like one product-aware proof sequence with an evidence-supported buyer event. Pick one Creative Film Treatment, one Shooting World Lock, the relevant adapter, one product entrance, and one buyer event first, then vary camera distance, product action, and framing.

Default storyboard format:

- one storyboard/contact-sheet image,
- 5 numbered 16:9 landscape panels inside that one storyboard image,
- each panel is a 16:9 Amazon-style keyframe,
- panels must form one continuous product-led demo sequence,
- product appearance must be copied from the product image.

The `## 2. 故事版` section must include only these internal parts:

```text
创意大片方向: one concise Creative Film Treatment
同一拍摄世界锁: one compact Shooting World Lock
5 格 16:9 连续关键帧: one storyboard/contact-sheet image containing five numbered 16:9 product-proof panels
```

These are subparts of the storyboard section. They do not count as extra output sections.

### Creative Film Treatment

Choose one cinematic direction before generating panels. It must come from product evidence, shopper question, product entrance, buyer event, buyer use case, and risk level, not from random style words.

The treatment must lock:

- visual premise: what buyer event are we filming,
- reason to watch: what the viewer can learn only because this is shown as video,
- product entrance: where the product becomes the clear hero,
- style: ordinary customer video / clean product proof / premium macro detail / hands-on demo / setup sequence / workspace use / home use / outdoor proof / other product-specific direction,
- lighting and mood: soft window light, golden hour, diffused overcast, practical indoor light, cinematic side light, etc.,
- lens and camera language: self-shot, handheld close-up, locked product shot, slow push-in, over-the-shoulder, macro detail,
- color palette: 3-5 grounded colors from the product and scene.

Avoid saying only "cinematic", "premium", or "大片感". Those words are not a treatment unless they specify scene, light, lens, product entrance, product action, buyer event, and why that treatment is safe for the evidence.

### Shooting World Lock

Before writing or generating the 5 keyframes, lock a shared visual theme layer. Continuity is defined first by product truth, then by the behavior adapter, then by the scene:

- same product and same product-state,
- same wearer/user/operator/pet/subject/surface when product behavior needs real use,
- same location or continuous campaign world; process sequences may move from preview to detail to use if the product and behavior locks remain stable,
- same light source and color temperature,
- same camera/lens language,
- same wardrobe, props, surface, and background family,
- same product scale and placement logic,
- same motion language from frame to frame.

Product consistency beats single-frame beauty. Five medium-but-consistent, behavior-safe frames are better than five beautiful mismatched frames.

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
- same product fit, placement, part relationship, or visible customization state where relevant,
- same use state where relevant,
- no scene carried over from previous projects unless the user asks for it.

Product correctness is more important than image beauty. If the generated storyboard changes the product shape, color, label, package, size relationship, button, handle, opening, nozzle, or key structure, regenerate the storyboard before writing the final script.

## Amazon Product-Led Generation Contract

Every storyboard image prompt must include a strict Amazon product-led contract. This contract is mandatory, not optional style guidance.

- The storyboard must look like Amazon listing / A+ product demo frames, not TikTok UGC frames.
- Every panel must be 16:9 landscape.
- All five panels must share one product-proof system: same product locks, same behavior adapter, same design asset when personalized, same material logic, and one coherent campaign visual language.
- Every panel must inherit the Creative Film Treatment and Shooting World Lock.
- The product must enter clearly in the first 1-2 panels.
- The buyer event must be supported by product evidence, visible function, listing context, or explicit user direction.
- Product should usually occupy 45%-70% of each frame.
- Product use must be based on actions the product can visibly support. If the product has no visible physical result, do not invent one.
- At least two panels must show product structure, texture, component, size, or operation close enough for inspection.
- Human or subject presence must match product behavior. Worn or carried products need the relevant body or carrying context; operated products need hands or an operator; compatible products need the compatible object; living-subject products need the subject interaction when value depends on use. Use the smallest necessary human/subject presence that proves the product.
- Backgrounds must be simple and buyer-relevant but socially usable: simple room, street, studio corner, desk, gym, pet area, workspace, kitchen counter, bathroom shelf, outdoor use area, or other product-specific context selected by the adapter. Do not add decorative props or locations that are unrelated to the buying decision.
- Text inside generated images must be avoided unless it is required by the product reference. Add final copy later as design overlay, not as AI-generated fake text.
- The final storyboard must prioritize product proof plus real-use social believability over static catalog layout.

For user-dependent products, default to faceless or partially cropped users when model realism is risky. Show only the body part, hand, operator, wearer, pet, or environment needed to prove use. Avoid generating a new face or identity in every panel.

For high-AI-risk cases, prefer believable filming constraints over over-produced scenes: cropped faces, partial hands, real surface texture, matte material, imperfect framing, lived-in rooms, and motivated light. Product truth and continuity are more valuable than a polished fantasy ad.

Avoid:

- TikTok 9:16 vertical framing,
- creator face dominating the frame,
- product hidden inside lifestyle decor,
- removing the user/wearer when the product needs a user to make sense,
- five unrelated scenes or five different people in one storyboard,
- changing the user, subject, room, lighting, or product fit between panels,
- changing the behavior adapter, Design Asset, print area, interface, part set, or material logic between panels,
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
- product entrance is late or unclear,
- no visible buyer event; five panels are only product inspection or catalog pack shots,
- buyer event is unsupported by the product evidence or user request,
- reason to watch is unclear; the same information would work better as a static product image,
- product geometry or color drift,
- invented packaging, logo, badge, or readable claim,
- decorative props, location, or emotional staging distract from the buying decision,
- person, pet, or room becoming the main subject,
- use-dependent product has no necessary wearer, operator, hand, pet, or context proof,
- storyboard panels do not look like one coherent product-proof sequence,
- personalized product changes its Design Asset between panels,
- user identity, product fit, visible placement, part relationship, or lighting changes between panels,
- 9:16 TikTok framing,
- the scene looks over-staged, physically implausible, or less realistic than a usable ecommerce production asset,
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
- product fit, placement, user/operator crop, and visible customization state where relevant,
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

The script must match the storyboard exactly. Do not introduce new people, rooms, claims, product actions, or a new film treatment that is not in the storyboard. Use natural English listing-demo language, not exaggerated brand-deck language.

The script should follow show-don't-tell: the visuals prove about 60% of the message, and copy only labels or amplifies what is already visible. Do not use the voiceover to compensate for a weak storyboard.

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
- one product-behavior adapter selected before the creative direction
- one Creative Film Treatment selected from product evidence
- one Shooting World Lock for all five panels
- clean realistic ecommerce light
- buyer-relevant background
- product occupies 45%-70% of frame
- user/wearer/operator/subject/context included when product behavior requires real-use proof
- one simple product action per shot

Prefer:

- clean surfaces,
- product close-ups,
- visible components,
- necessary user/operator/wearer/subject/context when the product requires real-use proof,
- social proof scenes that still keep the product readable,
- one relevant user, subject, surface, or location logic across all panels,
- cropped body parts, hands, object scale, or surface details when they reduce fake model risk,
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
- Is there a storyboard after the product image?
- Did you infer and apply one product-behavior adapter?
- Did you identify a shopper question, reason to watch, product entrance, and evidence-supported buyer event internally?
- Did you choose one buyer event and keep it visible inside `## 2. 故事版`?
- Is the buyer event supported by product evidence, listing context, or explicit user direction?
- Does `## 2. 故事版` include a Creative Film Treatment?
- Does `## 2. 故事版` include a Shooting World Lock?
- Is the storyboard one image containing five numbered 16:9 product-proof panels?
- Do all five keyframes feel like one coherent product-proof sequence?
- Do at least two panels carry the buyer event rather than only product inspection?
- Is the product dominant and inspectable?
- Does the storyboard look like plausible ecommerce / brand production footage rather than generic AI lifestyle advertising?
- Is there a 15-second or 30-second script after the storyboard?
- Are all screen subtitles and voiceover lines in English?
- Did you avoid extra sections unless requested?
- Is the demo idea visually doable for Amazon / StoreClaw?
- Are product claims safe and grounded?
- Did the storyboard pass the product-led rejection criteria?
