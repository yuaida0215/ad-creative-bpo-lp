# 出力例

以下は出力の粒度と形式を示すための例。題材は架空のもの。

---

## 例1：スキンケア美容液・15秒・9:16・i2v

## LOOK: P2 CLEAN — Sony VENICE 2 / ZEISS Supreme Prime（理由：液の透明感と肌の質感を、色を転ばせずに見せる）

### Cut 1｜掴み — 狙い：最初のフレームから一滴が落ちている
**KEYFRAME**
```text
Extreme close-up of a single drop of serum falling from a glass dropper onto the back of a hand, in front of a bright bathroom window in the morning. Sony VENICE 2 with a ZEISS Supreme Prime 100mm lens at T2.8. Soft daylight from the left, neutral color balance, natural skin tones. Clearly resolved translucent serum, glass dropper tip and skin texture; the drop is in sharp focus while the window behind becomes a softly defocused bright field. Clean digital rendering with natural edge detail.
```
**MOTION**
```text
The drop lands and spreads slightly across the skin. Locked camera; focus stays on the drop.
```

### Cut 2｜使用デモ — 狙い：顔と商品の両方を読ませる（T4）
**KEYFRAME**
```text
Medium close-up of a person holding a frosted glass serum bottle at chest height beside a bathroom window. Sony VENICE 2 with a ZEISS Supreme Prime 50mm lens at T4. Soft daylight from a large window on the left, neutral color balance, natural skin tones. Clearly resolved frosted glass, brushed metal cap and skin texture; both the face and the bottle remain readable, the tiled wall behind softly defocused. Clean digital rendering with natural edge detail.
```
**MOTION**
```text
The person turns the bottle slightly toward the camera and holds it still. The handheld camera makes a small adjustment to follow the hand, then settles as the bottle comes to rest.
```

### Cut 3｜結果 — 狙い：使用後の肌のツヤを表情で見せる（同じパッケージのまま、寄りで浅く）
**KEYFRAME**
```text
Close-up of the person touching their cheek, a slight smile, face turned toward the window. Sony VENICE 2 with a ZEISS Supreme Prime 85mm lens at T2. Soft side light from the window on the left, neutral color balance. Dewy skin with visible pores, sharp eyes, gentle highlight roll-off on the cheekbone. The window frame behind is softly defocused.
```
**MOTION**
```text
The person turns slightly further into the light. Restrained handheld breathing; the focus follows the slight head movement.
```

> 外し案：同じ台本で「UGC／スマホルック」版を1本作り、ABテストに回すか確認する。
> 商品ラベルは、実物写真から作ったキーフレームで担保する。プロンプトで文字は描かせない。

---

## 例2：家の中のキャラクター物シリーズ・夜のキッチン・9:16・i2v

## LOOK: P5 NATURAL DEPTH — ARRI ALEXA Mini LF / ARRI Signature Prime（理由：部屋が読めることが物語の前提になるため）

### Cut 3｜対象物アップ — 狙い：困りごとの中身を一目で伝える
**KEYFRAME**
```text
Close-up of a glass jar with a tight metal lid on a kitchen counter at night, a person's hands gripping the lid. ARRI ALEXA Mini LF with an ARRI Signature Prime 75mm lens at T2.8. Warm practical light from the under-cabinet lamp falls from above, soft and low. Visible texture on the ribbed metal lid and the glass; the lid is in sharp focus. The tiled backsplash behind remains recognizable but softly separated. Deep charcoal shadows retain subtle texture.
```
**MOTION**
```text
The hands twist the lid hard, then pause as it refuses to turn. As the hands pause, the camera slowly pushes in toward the lid.
```

### Cut 6｜キャラクター登場 — 狙い：止まった画の中で、暗がりから現れる動きだけを際立たせる
**KEYFRAME**（reference image 1 = キャラクターの identity only）
```text
Medium shot of the kitchen counter at night: the jar in the foreground and the dark gap beside the bread bin behind it. The small character from reference image 1 (identity only) stands half inside that shadow. ARRI ALEXA Mini LF with an ARRI Signature Prime 47mm lens at T2.8. Low warm practical light; a thin soft rim of light separates the character's dark silhouette from the shadow. Deep charcoal shadows retain subtle texture. The backsplash remains recognizable but softly separated.
```
**MOTION**
```text
The character glides smoothly out of the shadow and stops beside the jar. Locked camera; as the character comes to rest, focus shifts from the shadow to the jar.
```

> 暗い色のキャラクターや商品を暗部に置くときは、`rim light` と `deep charcoal shadows retain subtle texture` をセットで使う。
> キャラクターの外見は文章で描写し直さず、参照画像に任せる。
