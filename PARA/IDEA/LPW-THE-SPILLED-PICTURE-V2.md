---
id: LPW-THE-SPILLED-PICTURE-V2
aliases: []
tags: []
---

# The Spilled Picture · v2 prompt pack (bible, world, cast sheet, drawing, 7 scenes)

Rebuilt 2026-10-15 on the One More Game v2 method, then cut to **7 scenes = the 7 timed blocks of the script**
(0:00-0:06, 0:06-0:15, 0:15-0:24, 0:24-0:34, 0:34-0:47, 0:47-0:56, 0:56-1:00). One still and one clip per block; every beat of the block
happens inside its clip. The 14-scene version is in `archive/STILL-PROMPTS-v2-14scenes-20261015.md`.
Extra images that are NOT clips: W00 (empty bakery), W01 and W02 (more angles of it), CAST (character sheet), D1 to D5 (the drawing at each stage).
Diagrams in this folder: `SPILLED-PICTURE-bakery-map.png` (top-down room, cast spots, cameras), `SPILLED-PICTURE-scale-ref.png`
(heights in L, with the table; for checking by eye, do NOT wire it, its text bleeds).

## What v2 fixes from the v1 stills

- The table changed: small round table in S01, long plank table in S02 to S08. v2 = ONE low round table.
- Paws used as hands: Leo holds a glass (S08), paws on the tabletop like elbows. v2 = table top at chest height so everyone stands on four
  feet; a drawer holds the crayon in ONE curled front paw and stands on the other three (Manish, 2026-10-15); big props (the glass) are nudged with the nose.
- The drawing changed shot to shot. v2 = the drawing is made ONCE (D1); every later stage5g is an Image Editor change of the one before.
- Bakery colours/light drifted. v2 = one bible + one W00, sun always from the window on the right-hand wall.

---

## Setup in Spaces (same as One More Game)

1. Shared nodes, made once:
   - Text **bible**: the BIBLE TEXT below.
   - Upload **scale**: `character-refs/toy-scale-ref-CANON.png` (all four at true size, no text).
   - Upload **leo**, **kaya**, **zara**, **biko**: the four `*-canon-ref.jpg` in `character-refs/`.
   - Image Generator **world** ← Text W00 (no references). Run 2-3 times, keep the best.
   - Image Generators **world-left** (W01) and **world-right** (W02): see "World angles" below.
   - Image Generator **cast** ← Text CAST + `scale` + `world`. (Reference only.)
   - Image Generator **D1** ← Text D1. Then Image Editor nodes **D2 → D3 → D4 → D5**, each fed by the one before.
2. **7 scene generators** (S1 to S7), each with its own Text node. Text port ← `bible` + its `Text Sx`;
   image port ← the world node named on its card + `scale` + the characters named on its card (+ a drawing node only where listed).
3. Settings: Nano Banana 2, 9:16, 2K, same seed, inline prompt box empty. Drawing nodes: 4:3.
4. Order: world → world-left, world-right → cast → D1 to D5 → S1. If S1 looks right, run the rest.

Why the drawing is wired on only 2 scenes: it is a top-down image and can pull the camera top-down (the field-plate lesson). Where it is small
in frame the words carry it. If a scene's drawing looks off, wire the matching D node as a fix-up.

---

## BIBLE TEXT

```
Style: high-end 3D animated feature film, Pixar quality, on a bright sunny morning. Vivid, highly saturated colours: fresh mint-green walls, a warm honey-wood floor, bright pastel pinks, yellows and blues. Crisp bright sunshine pours in from a big window on the right side of the frame, warm-white light with soft shadows falling to the left, a gentle rim light on fur and skin, three round pendant lamps glowing softly overhead, shallow depth of field with the background softly blurred. Natural things look real and tactile: fur, skin, wood grain, bread, fruit and plant leaves. Made things are clean, stylised and cheerful. Vertical 9:16, filling the whole tall frame.

World, identical in every shot and matching the attached world image: inside a small, cheerful children's bakery café. The back wall is mint green with a cream lower panel. Along the back wall runs a curved glass display counter full of pink-frosted cupcakes, a strawberry cake, chocolate-chip cookies and golden bread loaves, with a row of pastel triangle bunting along its front. Above the counter hangs a wood-framed chalkboard covered in small colourful chalk pictures of cupcakes and stars, with three round cream pendant lamps hanging in a row in front of it. Wooden shelves of colourful mugs on the left of the back wall, glass jars of sweets on the right. On the left wall, a serving hatch under a mint-and-cream striped awning, and a red coffee machine in the back-left corner. On the right wall, a tall white-framed window full of morning sunshine with green trees outside, a pink cushioned bench under it, and an orange pot with a green plant in the back-right corner between the end of the counter and the bench. Further forward on the same right wall is a white wooden door with a small round window. The floor is warm honey-coloured wooden planks. Two small round café tables, one yellow and one blue, stand in the background on the left and right.

The hero table, in the middle of the room: one low, wide round table with a honey-wood top and a single thick pedestal leg, its top at the height of Leo's chest, open floor all around it. In the middle of the tabletop lies Kaya's drawing, a large sheet of white paper, its picture facing the camera. On the front-left of the table stands one tall clear glass of purple berry juice with a pink-and-white striped paper straw, and beside it a small wooden holder of white paper napkins. On the front-right sits a small wooden tray of chunky wax crayons in purple, blue, red, orange, green and yellow.

Cast: @kaya, a young rhino girl: smooth light-grey skin with small darker freckles, a big curved front horn with a carved zigzag band around its base and a small second horn behind it, three small dark freckle dots on her cheek, pink inner ears with two dark dots, warm amber eyes, a dark tufted tail. @leo, a young lion: golden fur, a big full swept-back mane that is light caramel-brown on top and deep dark brown underneath, a small gold crown nestled in the top of his mane, a red bandana with a patterned border around his neck, small whisker spots on his cheeks, amber eyes, a friendly face. @zara, a young leopard: slender, golden fur with black rosette spots, a cream chest, big green eyes, a gold ring near the tip of her tail. @biko, a young African buffalo: stocky, dark charcoal-grey fur, big curved horns meeting in a heavy boss on his head, a dark maroon band wrapped on each horn, darker swirl marks on his forehead, warm brown eyes.
Only the characters named in the SHOT section appear in this image. They are same-age friends, four-legged animals standing on all four feet on the wooden floor around the table, their chests at the table edge. Leo and Zara have round furry animal paws, Kaya has wide round rhino feet, Biko has hooves. When a friend draws, it stands on three feet and holds one chunky crayon in one front paw, the crayon gripped in the curl of the paw's toes like a toddler's fist grip, the tip on the paper: Leo and Zara curl their furry toes around it, Kaya pinches it between the round toes of her front foot, Biko tucks it into the cleft of his front hoof. The paw stays a round animal paw. Size, matching the attached line-up: @kaya is the biggest, her horn tip 1.4 times Leo's height; @biko's horn tips are 1.2 times Leo; @zara's head reaches only to @leo's shoulder (0.8 times Leo).
```

## W00 TEXT (Text node → `world` only, no references)

```
Style: high-end 3D animated feature film, Pixar quality, on a bright sunny morning. Vivid, highly saturated colours: fresh mint-green walls, a warm honey-wood floor, bright pastel pinks, yellows and blues. Crisp bright sunshine pours in from a big window on the right side of the frame, warm-white light with soft shadows falling to the left, three round pendant lamps glowing softly overhead, shallow depth of field. Vertical 9:16, filling the whole tall frame.
An empty children's bakery café, the establishing view of the whole room. Camera at a child's eye level near the front of the room, looking straight at the back wall. Along the back wall runs a curved glass display counter full of pink-frosted cupcakes, a strawberry cake, chocolate-chip cookies and golden bread loaves, with pastel triangle bunting along its front. Above it a wood-framed chalkboard with small colourful chalk pictures of cupcakes and stars, and three round cream pendant lamps hanging in a row. Shelves of colourful mugs on the left of the back wall, jars of sweets on the right. On the left wall, a serving hatch under a mint-and-cream striped awning and a red coffee machine in the corner. On the right, a tall white-framed window full of sunshine with green trees outside, a pink cushioned bench under it, an orange pot plant in the corner. Warm honey-coloured wooden plank floor. A small yellow café table on the left and a small blue one on the right, in the background.
In the centre foreground stands the hero table: one low, wide round table with a honey-wood top and a single thick pedestal leg, open floor all around it. On it: a tall clear glass of purple berry juice with a pink-and-white striped paper straw on the front-left, a small wooden holder of white paper napkins beside it, and a small wooden tray of chunky wax crayons in purple, blue, red, orange, green and yellow on the front-right. The middle of the tabletop is clear, bare honey wood. The café is quiet and empty, waiting for the friends.
```

Check: window on the RIGHT, table low and round in the middle, glass front-left, crayons front-right, middle of the table bare.
Once approved, rewrite any bible line that disagrees with the image (text must describe the picture or they fight).

## CAST TEXT (character reference sheet · Text → `cast`, image port ← `scale` + `world` · 16:9)

```
Style: high-end 3D animated feature film, Pixar quality, bright clean daylight, vivid saturated colours, soft studio shadows. Wide 16:9 frame.
A character line-up reference sheet, matching the attached line-up image: four young animal friends standing side by side on all four feet in a three-quarter view facing right, all on one flat ground line, at their true relative sizes, in front of a plain soft cream studio wall. From left to right: @kaya the young rhino (the biggest, her horn tip 1.4 times Leo's height), @biko the young buffalo (horn tips 1.2 times Leo), @leo the young lion, @zara the young leopard (her head at Leo's shoulder). On the far right stands the hero table from the attached world image: a low, wide round table with a honey-wood top and a single thick pedestal leg, its top level with Leo's chest, with the tall clear glass of purple berry juice with a striped straw and the small tray of chunky crayons on it. Every character is fully in frame with even space between them, friendly calm faces, mouths closed in soft smiles.
```

Use: a reference to check scale and the table height. Wire it into a scene only if a shot keeps getting sizes wrong.

---

## The drawing (4:3 · D1 is an Image Generator, D2 onward are Image Editor nodes, each on the one before)

Picture order on the paper, left to right: rhino, buffalo, lion, leopard. The juice stain covers the lion,
so later Leo draws himself back in, jumping in the puddle.

**D1 · the finished drawing** (Image Generator, no references)

```
A child's crayon drawing on a large sheet of white paper, seen straight from above, the paper filling almost the whole frame and lying flat on a honey-wood tabletop with a thin border of wood showing around it. Drawn in bright wax crayon with visible waxy strokes, simple and joyful, like a talented young child drew it. Four animal friends play together on a strip of green grass along the bottom with a red ball, under a big round yellow sun in the top-left corner and a few blue scribbled clouds. From left to right: a big grey rhino with a big horn, a black buffalo with curved horns, a golden lion with a brown mane and a tiny yellow crown in the middle of the picture, and a yellow leopard with black spots. Big smiles and round eyes. The drawing is pictures only, with clean white paper around the figures.
```

**D2 · the spill** (edit on D1)

```
A big splash of purple berry juice has spilled across the bottom half of the drawing: a wet, glossy dark purple stain over the green grass and the friends' feet, spreading widest in the bottom centre where it covers the golden lion completely except the tip of his tiny crown, with drips and spatters around it. The paper is darkened and slightly wrinkled where it is wet. Keep everything else exactly the same.
```

**D3 · smeared and torn** (edit on D2)

```
The purple stain has been rubbed with a napkin: the purple now spreads in wide streaky swipes, the crayon greens and yellows of the grass bleed into it, and the wet paper is soggy and crinkled. The bottom-left corner of the paper is torn away: a ragged torn edge, a missing triangle of paper, and the small soggy purple scrap still stuck to the wet wood of the table just below the gap. Keep everything else exactly the same.
```

**D4 · the puddle** (edit on D3)

```
Around the edge of the big purple stain, someone has drawn two wavy purple crayon outline rings, following its shape, so the stain now looks like a big purple rain puddle lying on the green grass. Keep everything else exactly the same, including the torn bottom-left corner.
```

**D5 · finished in the rain** (edit on D4)

```
Add to the drawing, in the same bright wax crayon style: many small blue teardrop raindrops falling across the whole sky; a big red umbrella with a curved handle standing over the rhino and the buffalo; and in the middle of the purple puddle, a golden lion with a brown mane and a tiny yellow crown leaping with all four paws in the air, big orange splash lines bursting around him. Every friend in the picture has a big smile. The yellow sun stays in the corner. Keep everything else exactly the same, including the torn bottom-left corner.
```

In the edit, D3, D4 and D5 are cutaway inserts (slow push, 2 to 3s each) laid over the clip; they never go through Seedance. D1 can open the video as a 1.5s title shot.

---

## World angles W01, W02, W03 (made once, right after W00 is approved; cameras on the bakery map, green)

Why: a scene shot from a new camera spot pulls the room back to the front view if only W00 is attached. Each angle
below is a new picture of the SAME room, so a scene wires the angle that matches its camera INSTEAD of `world`.
For each: Text node → Image Generator (NB2, 9:16, 2K), image port ← `world` (W00). If the result snaps back to the front view,
unwire W00 and run the text alone (the text describes the whole room). Run 2 to 3 times, keep the best. Never attach `scale` or characters.

Which scene uses which: W00 (`world`) = S1, S3, S4, S6. W01 `world-left` = S2, S7. W02 `world-right` = S5.
W03 (`world-side`, further down) is NOT used by the 7 scenes; skip it unless a later shot needs it.

**W01 · front-left, looking diagonally to the back-right** (node `world-left`)

```
Style: high-end 3D animated feature film, Pixar quality, on a bright sunny morning. Vivid, highly saturated colours: fresh mint-green walls, a warm honey-wood floor, bright pastel pinks, yellows and blues. Crisp bright sunshine pours in from the big window on the right-hand wall, warm-white light with soft shadows falling to the left, three round pendant lamps glowing softly overhead, shallow depth of field. Vertical 9:16, filling the whole tall frame.
The same children's bakery café as the attached image, seen from a new camera position. Camera at a child's eye level, a little above the tabletop, standing in the front-left part of the room and looking diagonally across the room toward the back-right corner. The back wall fills the left and centre of the frame and recedes toward the right: mint-green with a cream lower panel, the curved glass display counter full of pink-frosted cupcakes, a strawberry cake, chocolate-chip cookies and golden bread with pastel triangle bunting along its front, above it the wood-framed chalkboard of colourful chalk cupcakes and stars with three round cream pendant lamps hanging in a row. In the back-right corner, where the back wall meets the right-hand wall, stands an orange pot with a green plant. On the right edge of the frame the right-hand wall holds the tall white-framed window full of morning sunshine with green trees outside, the pink cushioned bench under it, and the small round blue café table in front of the bench. Warm honey-coloured wooden plank floor with bright patches of sunlight.
In the middle of the frame stands the hero table: one low, wide round table with a honey-wood top and a single thick pedestal leg, open floor all around it. On the near edge of the tabletop, in the middle of the frame, stand the tall clear glass of purple berry juice with a pink-and-white striped paper straw and, right beside it, the small wooden holder of white paper napkins. On the right half of the tabletop sits the small wooden tray of chunky wax crayons in purple, blue, red, orange, green and yellow. The middle of the tabletop is clear, bare honey wood. The café is quiet and empty.
```

**W02 · front-right, looking diagonally to the back-left** (node `world-right`)

```
Style: high-end 3D animated feature film, Pixar quality, on a bright sunny morning. Vivid, highly saturated colours: fresh mint-green walls, a warm honey-wood floor, bright pastel pinks, yellows and blues. Crisp bright sunshine streams in from behind and to the right of the camera, warm-white light with soft shadows falling forward and to the left, three round pendant lamps glowing softly overhead, shallow depth of field. Vertical 9:16, filling the whole tall frame.
The same children's bakery café as the attached image, seen from a new camera position. Camera at a child's eye level, a little above the tabletop, standing in the front-right part of the room and looking diagonally across the room toward the back-left corner. On the left of the frame is the left-hand wall: mint-green with a cream lower panel, a serving hatch under a mint-and-cream striped awning, wooden shelves of colourful mugs, and in the back-left corner a red coffee machine on a small counter; the small round yellow café table stands in front of the hatch. The back wall fills the centre and right of the frame and recedes to the right: the curved glass display counter full of pink-frosted cupcakes, a strawberry cake, chocolate-chip cookies and golden bread with pastel triangle bunting along its front, above it the wood-framed chalkboard of colourful chalk cupcakes and stars with three round cream pendant lamps hanging in a row. Warm honey-coloured wooden plank floor, lit in bright sunny patches.
In the middle of the frame stands the hero table: one low, wide round table with a honey-wood top and a single thick pedestal leg, open floor all around it. On the near edge of the tabletop, in the middle of the frame, sits the small wooden tray of chunky wax crayons in purple, blue, red, orange, green and yellow. On the left half of the tabletop, further away, stand the tall clear glass of purple berry juice with a pink-and-white striped paper straw and the small wooden holder of white paper napkins beside it. The middle of the tabletop is clear, bare honey wood. The café is quiet and empty.
```

**W03 · from the left side of the room, looking straight across it** (node `world-side`)

```
Style: high-end 3D animated feature film, Pixar quality, on a bright sunny morning. Vivid, highly saturated colours: fresh mint-green walls, a warm honey-wood floor, bright pastel pinks, yellows and blues. Bright morning sunshine glows through the big window straight ahead, long warm beams of light falling across the floor toward the camera, a gentle warm rim light on the table edges, three round pendant lamps glowing softly overhead, shallow depth of field. Vertical 9:16, filling the whole tall frame.
The same children's bakery café as the attached image, seen from a new camera position. Camera at a child's eye level, a little above the tabletop, standing near the left-hand wall of the room and looking straight across the room at the right-hand wall. Straight ahead, the right-hand wall is mint-green with a cream lower panel: in the centre of the frame the tall white-framed window full of bright morning sunshine with green trees outside, the pink cushioned bench under it, the small round blue café table in front of the bench, and on the right of the frame a white wooden door with a small round window. On the left edge of the frame the back wall begins: the end of the curved glass display counter with pastel bunting, the wood-framed chalkboard above it and the three round cream pendant lamps in a row receding into the distance, and in the back-right corner an orange pot with a green plant beside the window. Warm honey-coloured wooden plank floor with bright beams of sunlight.
In the middle of the frame stands the hero table: one low, wide round table with a honey-wood top and a single thick pedestal leg, open floor all around it. On the near right corner of the tabletop stand the tall clear glass of purple berry juice with a pink-and-white striped paper straw and the small wooden holder of white paper napkins beside it; on the far right corner sits the small wooden tray of chunky wax crayons in purple, blue, red, orange, green and yellow. The middle of the tabletop is clear, bare honey wood. The café is quiet and empty.
```

Checks for all three: same mint walls and cream panel? Same cupcake counter, chalkboard and 3 lamps? Orange plant in the back-right corner? Glass, napkins and crayon tray on the right corners of the table? Window and bench on the right-hand wall? Table still low and round?
New in W03: the white door with the round window. It was not in W00, so W03 makes it canon (the bible now mentions it).

---

## The 7 scene texts (one Text node each)

Wire = what goes into the image port besides `scale`. Cameras match `SPILLED-PICTURE-bakery-map.png`.
Staging used in every scene: @leo at the LEFT edge of the table (three-quarter view, by the glass), @kaya behind the table in the middle,
@zara and @biko behind the table on the right. Each still is the START of its block; the clip carries the action.

**S1 · 0:00-0:06 · "Done." / "That's us!" / SPLASH** · wire: `world`, leo, kaya, zara, biko

```
SHOT: camera at a child's eye level at the front of the room, a few body-lengths back from the hero table, looking straight at the back wall: the whole round table and all four friends are in frame, the display counter, chalkboard and pendant lamps behind them. @kaya stands behind the table in the middle, head lowered over the drawing, one front foot on the paper with a purple crayon gripped between its round toes, the tip just finishing the last line of the picture, a proud, shy little smile. @leo stands at the left edge of the table in three-quarter view, close to the tall glass of purple berry juice, leaning in toward the drawing with an excited face, his front paws on the floor. @zara and @biko stand behind the table on the right, smiling at the drawing. The glass of juice stands full and upright on the left part of the tabletop, a paw's reach from Leo, with the drawing just to its right. The drawing is a bright crayon picture of four animal friends playing on green grass under a yellow sun.
```

**S2 · 0:06-0:15 · "Kaya! I'm sorry!" / the wipe / "Leo, stop." / the tear / "I worked so hard on it."** · wire: `world-left`, leo, kaya, zara, biko

```
SHOT: camera at a child's eye level at the front-left of the table, looking diagonally toward the back-right. @leo is the main subject, large in the left foreground at the left edge of the table, in three-quarter view, a crumpled white napkin pressed under one front paw on the table, worried eyebrows up, mouth open to speak. The tall glass lies tipped on its side on the left of the paper, empty, and a wave of glossy purple berry juice has spread across the bottom half of the drawing and drips off the table edge. A few more white napkins lie beside the napkin holder. Behind the table, @kaya stands in the middle, frozen in alarm, eyes wide on her drawing, one front foot lifted off the paper. @zara and @biko stand behind her on the right, shocked, mouths small and round. The counter and chalkboard are softly blurred behind them.
```

**S3 · 0:15-0:24 · "I'm really sorry." and the quiet wait** · wire: `world`, leo, kaya, zara, biko, **D3**

```
SHOT: camera at a child's eye level at the front of the room, looking straight at the back wall, the whole table and all four friends in frame. @leo stands at the left edge of the table, in three-quarter view, a little pile of crumpled napkins pushed beside him, head low and ears drooped, looking up at Kaya with a sorry face, his mouth just starting to open to speak. @kaya stands behind the table in the middle, looking down at the ruined drawing, hurt and quiet, her head slightly lowered. @zara and @biko stand behind the table on the right, very still, glancing at each other with worried faces. The drawing lies in the middle of the table matching the attached drawing image: its bottom half a streaky purple smear, its bottom-left corner torn away. The empty glass lies on its side at the table's left edge.
```

**S4 · 0:24-0:34 · the crayon, "What are you doing?" / "It's a puddle now."** · wire: `world`, leo, kaya

```
SHOT: camera at a child's eye level in front of the table, a medium shot looking straight at the back wall. @kaya stands behind the table in the middle, large in the frame, her head lowered over the drawing, her eyes on the big purple stain across the bottom of the picture, thoughtful, one front foot resting on the table beside the drawing. @leo stands at the left edge of the table, in three-quarter view, watching her with a hopeful, worried face. On the table the drawing's bottom half is a streaky purple smear and its bottom-left corner is torn away; on the right of the table stands the tray of chunky crayons with the purple crayon on top. The counter, chalkboard and pendant lamps are softly blurred behind them.
```

**S5 · 0:34-0:47 · raindrops, umbrella, "And I'm jumping in it!" / "You would." / everyone laughs** · wire: `world-right`, leo, kaya, zara, biko

```
SHOT: camera at a child's eye level, a little above the tabletop, standing in the front-right part of the room and looking diagonally toward the back-left, the whole table and all four friends in frame. @zara stands at the right side of the table in the foreground, leaning over the paper, one front paw on it with a blue crayon curled in her toes, dotting little blue raindrops. @biko stands behind her at the far side, one front hoof on the paper, a red crayon tucked into the cleft of his hoof, drawing the first curve of a big umbrella. @leo stands at the left edge of the table, eager, bouncing on his front paws, an orange crayon lying on the tray in front of him, grinning at the drawing. @kaya stands behind the table in the middle, watching with a softening, almost-smiling face. On the table the drawing has two wavy purple rings around the purple stain, so it looks like a puddle. The counter, chalkboard and the yellow table are softly blurred behind them.
```

**S6 · 0:47-0:56 · "It looks even better!" / "I liked the first one." / "But I like this one too."** · wire: `world`, leo, kaya, zara, biko, **D5**

```
SHOT: camera low at the front edge of the hero table, the lens just above the tabletop, the finished drawing large in the foreground matching the attached drawing image, its picture facing the camera. The four friends stand around the far side of the table with their heads close together over the drawing, from left to right @leo, @kaya, @zara, @biko, all four proud and happy, looking at the picture. Morning sunshine from the window on the right falls across the paper.
```

The script says they "hold up" the drawing. Four-legged friends can't, so they gather over it and present it to the camera. If Radha wants it literally held up, tell me and I will write an upright version.

**S7 · 0:56-1:00 · "This stays here." / "Good idea."** · wire: `world-left`, leo, kaya

```
SHOT: camera at the front-left of the table at Leo's eye level, looking diagonally toward the back-right. @leo is the main subject, large in the left foreground at the left edge of the table, in three-quarter view, his eyes on the tall glass of purple berry juice, which stands upright and half full on the left part of the tabletop beside the finished rainy drawing, a careful, serious little face, his nose a short distance from the glass, all four paws on the floor. Behind the table @kaya watches him, warm and relaxed. The finished drawing lies safe in the middle of the table, its picture showing rain, a red umbrella and a golden lion jumping in a purple puddle.
```

---

## Clips (Seedance 2.0 Mini, 720p, 9:16, sound effects ON, music OFF)

All 7 are dialogue shots: still → REFERENCE port + the in-shot characters + the padded voice file → audio. In every prompt write: "The attached still is the
opening frame; keep its composition, characters and background exactly." Then a speaker block: who speaks, at what second, the quoted words, everyone
else's mouth closed, no other words added. If it still invents words, strip the quotes and keep names + times.

| Block        | Clip | Beats inside the clip (seconds)                                                                                                                                                                                                                                   | Insert in the edit                                                          |
| ------------ | ---- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- | --------------------------------------------------------------------------- |
| S1 0:00-0:06 | 6s   | Kaya lifts the crayon, says "Done." at 0.6. Leo says "That's us!" at 2.2, his paw bumps the glass at 3.4, it tips toward the drawing, juice splashes over it at 3.8, all four freeze 4.5-6                                                                        | none                                                                        |
| S2 0:06-0:15 | 9s   | Leo "Kaya! I'm sorry!" at 0.4, wipes with the napkin 1.5-3.2, the colours smear. Kaya "Leo, stop." at 3.6, Leo freezes. Kaya slides her nose under the paper and lifts it 5.0-6.0, the corner tears at 6.0, her face drops. Kaya "I worked so hard on it." at 6.8 | none                                                                        |
| S3 0:15-0:24 | 6s   | Leo sets the napkins down, says "I'm really sorry." at 0.8. Kaya looks at Leo (2.5), then down at the drawing (3.5), sits quietly. Zara and Biko wait                                                                                                             | **D3** cutaway 3s over the quiet end, makes 9s                              |
| S4 0:24-0:34 | 8s   | Kaya studies the stain 0-1.5, takes the purple crayon in one front paw 1.5-3, draws wavy lines around the stain 3-5. Leo "What are you doing?" at 3.8. Kaya "It's a puddle now." at 5.5. Leo leans in to look 7-8                                                 | **D4** cutaway 2s at the end, makes 10s                                     |
| S5 0:34-0:47 | 12s  | Zara dots raindrops, Biko draws the umbrella 0-3. Leo grabs the orange crayon 3. Leo "And I'm jumping in it!" at 4.2, he draws himself. Kaya smiles 8.0, "You would." at 8.6. All four laugh 9.5-12                                                               | **D5** cutaway 2.5s laid over clip seconds 5-7.5 (hides the drawing action) |
| S6 0:47-0:56 | 9s   | Leo "It looks even better!" at 0.6. Kaya looks at the picture 2-3. Kaya "I liked the first one." at 3.0. Small pause. Kaya "But I like this one too." at 6.0, small smile                                                                                         | none                                                                        |
| S7 0:56-1:00 | 5s   | Leo looks at the glass 0-0.5, nudges it along the table with his nose toward the far right end 0.5-2.5, "This stays here." at 1.0. Kaya smiles, "Good idea." at 3.2                                                                                               | none                                                                        |

Clips total 55s, about 60s with the inserts. Clip prompt rules: one action at a time inside each beat; the glass tips only at the instant Leo's paw touches it;
the drawing paw moves the crayon in small strokes while the other three feet stay planted; no slow motion. Seedance may invent voices on silent stretches,
fixed in assembly. Voices: one ElevenLabs profile per character (Leo `QzTKubutNn9TjrB7Xb2Q`), each line padded with silence so the words land on the seconds above.

## Quick check on every still

Window and sunlight on the RIGHT? One low round honey-wood table? Everyone on four feet, chests at the table edge? Paws look like paws (nothing gripped like a hand)?
Kaya > Biko > Leo > Zara? Leo's crown + bandana? Drawing at the right stage? Leo at the table's left edge?

## Credits (estimate)

NB2 2K = 75 cr each: W00 + W01 + W02 + cast + D1 to D5 + 7 scenes = 16 images, about 1,200 cr before rerolls.
Clips via the MCP: 55s x 140 cr/s = 7,700 cr. On the website, use whatever shows the Unlimited badge.
Balance check at the start and end of each batch.
