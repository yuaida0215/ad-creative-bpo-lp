# 出力例

以下は出力の粒度と形式を示すための例。題材は架空のもの。

---

## 例1：スキンケア美容液・15秒・9:16・i2v

## LOOK: P2 CLEAN — Sony VENICE 2 / ZEISS Supreme Prime（理由：液の透明感と肌の質感を、色を転ばせずに見せる）

### Cut 1｜掴み — 狙い：最初のフレームから一滴が落ちている
**KEYFRAME（画像生成用）**
```text
Extreme close-up of a single drop of serum falling from a glass dropper onto the back of a hand, in front of a bright bathroom window in the morning. Sony VENICE 2 with a ZEISS Supreme Prime 100mm lens at T2.8. Soft daylight from the left, neutral color balance, natural skin tones. Clearly resolved translucent serum, glass dropper tip and skin texture; the drop is in sharp focus while the window behind becomes a softly defocused bright field. Clean digital rendering with natural edge detail.
```
**MOTION（i2v用）**
```text
The drop lands and spreads slightly across the skin. Locked camera; focus stays on the drop.
```

### Cut 2｜使用デモ — 狙い：顔と商品の両方を読ませる（T4）
**KEYFRAME（画像生成用）**
```text
Medium close-up of a person holding a frosted glass serum bottle at chest height beside a bathroom window. Sony VENICE 2 with a ZEISS Supreme Prime 50mm lens at T4. Soft daylight from a large window on the left, neutral color balance, natural skin tones. Clearly resolved frosted glass, brushed metal cap and skin texture; both the face and the bottle remain readable, the tiled wall behind softly defocused. Clean digital rendering with natural edge detail.
```
**MOTION（i2v用）**
```text
The person turns the bottle slightly toward the camera and holds it still. The handheld camera makes a small adjustment to follow the hand, then settles as the bottle comes to rest.
```

### Cut 3｜結果 — 狙い：使用後の肌のツヤを表情で見せる（同じパッケージのまま、寄りで浅く）
**KEYFRAME（画像生成用）**
```text
Close-up of the person touching their cheek, a slight smile, face turned toward the window. Sony VENICE 2 with a ZEISS Supreme Prime 85mm lens at T2. Soft side light from the window on the left, neutral color balance. Dewy skin with visible pores, sharp eyes, gentle highlight roll-off on the cheekbone. The window frame behind is softly defocused.
```
**MOTION（i2v用）**
```text
The person turns slightly further into the light. Restrained handheld breathing; the focus follows the slight head movement.
```

> 外し案：同じ台本で「UGC／スマホルック」版を1本作り、ABテストに回しますか？
> 推定で埋めた前提：i2v、9:16、1カット5秒で生成し、編集で詰めて15秒にする。商品ラベルは実物写真から作ったキーフレームで担保し、文字はプロンプトで描かせない。
>
> シリーズ用のルック表（パートナー配布用）も出しますか？

---

## 例2：家の中のキャラクター物シリーズ・夜のキッチン・9:16・i2v

## LOOK: P5 NATURAL DEPTH — ARRI ALEXA Mini LF / ARRI Signature Prime（理由：部屋が読めることが物語の前提になるため）

### Cut 3｜対象物アップ — 狙い：困りごとの中身を一目で伝える
**KEYFRAME（画像生成用）**
```text
Close-up of a glass jar with a tight metal lid on a kitchen counter at night, a person's hands gripping the lid. ARRI ALEXA Mini LF with an ARRI Signature Prime 75mm lens at T2.8. Warm practical light from the under-cabinet lamp falls from above, soft and low. Visible texture on the ribbed metal lid and the glass; the lid is in sharp focus. The tiled backsplash behind remains recognizable but softly separated. Deep charcoal shadows retain subtle texture.
```
**MOTION（i2v用）**
```text
The hands twist the lid hard, then pause as it refuses to turn. As the hands pause, the camera slowly pushes in toward the lid.
```

### Cut 6｜キャラクター登場 — 狙い：止まった画の中で、暗がりから現れる動きだけを際立たせる
**KEYFRAME（画像生成用）** — reference image 1 = キャラクターの identity only
```text
Medium shot of the kitchen counter at night: the jar in the foreground and the dark gap beside the bread bin behind it. The small character from reference image 1 (identity only) stands half inside that shadow. ARRI ALEXA Mini LF with an ARRI Signature Prime 47mm lens at T2.8. Low warm practical light; a thin soft rim of light separates the character's dark silhouette from the shadow. Deep charcoal shadows retain subtle texture. The backsplash remains recognizable but softly separated.
```
**MOTION（i2v用）**
```text
The character glides smoothly out of the shadow and stops beside the jar. Locked camera; as the character comes to rest, focus shifts from the shadow to the jar.
```

> 暗い色のキャラクターや商品を暗部に置くときは、`rim light` と `deep charcoal shadows retain subtle texture` をセットで使う。
> キャラクターの外見は文章で描写し直さず、参照画像に任せる。

---

## 例3：リビール型カット（終了フレームを指定できるツールの場合）

### Cut 2｜見せ場 — 狙い：フライパンを返すと、羽根つき餃子が一枚のまま現れる
**KEYFRAME（画像生成用）**
```text
High-angle close-up of two hands holding a black frying pan upside down over a white plate on a wooden table, the pan just beginning to lift away. Sony VENICE 2 with a ZEISS Supreme Prime 50mm lens at T4. Soft daylight from a large window on the left, neutral color balance with a gentle warm tint. Clearly resolved seasoned iron pan surface and glazed ceramic plate; both the hands and the plate remain readable, the table behind softly defocused. Clean digital rendering with natural edge detail.
```
**END FRAME（画像生成用）** — 実物の商品写真をもとに、見せ場の完成形をここで確定させる
```text
High-angle close-up of a single round disc of winged gyoza on a white plate, a lacy, crisp golden wing joining the browned bottoms of the dumplings, fresh steam rising. Sony VENICE 2 with a ZEISS Supreme Prime 50mm lens at T4. Soft daylight from a large window on the left grazes across the wing, neutral color balance with a gentle warm tint. Clearly resolved lacy golden wing, browned dumpling bottoms and rising steam; the wing is in sharp focus, the table behind softly defocused.
```
**MOTION（i2v用）**
```text
The hands lift the pan up and out of the frame, revealing the golden wing as steam rises from it. As the pan clears the frame, the camera slowly pushes in toward the wing, then settles.
```
