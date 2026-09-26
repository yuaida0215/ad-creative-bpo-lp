# カメラパッケージ 5種 ＋ 外し1種

出典：Promptwise Field Guide 01「5 Camera & Lens Setups for AI Video」（P1〜P5）。
向き・不向き、焦点距離の表、素材の語彙、外し（UGC）は【Snafty】で追加したもの。

各テンプレの `{…}` を差し替えて使う。ルック部分（カメラ名と「狙う見え方」）はなるべく残す。
変えるのは人物・場所・動作・素材・光源を中心にする。

- テンプレは t2v で使う1本の形になっている。i2v では末尾の `{MOVEMENT}` を外して KEYFRAME にし、動きは MOTION に移す。
- 人物がいないカットでは、人物用の語（`natural skin tones` など）を外す。
- 光源（`Soft daylight` など）は、シーンに合わせて差し替えてよい。
- 焦点距離とT値は、各パッケージの表から選ぶ。どの値も実在するレンズラインナップの範囲に収めてある。表にない組み合わせ（Cooke S4/i の T1.5 など）は書かない。
- 「寄り」は、表情にも物の寄りにも使う。質感だけで画面を埋めるときは「ディテール」を使う。

---

## P1 FILM — 質感ルック
**ARRICAM LT + Cooke S4/i ｜ Kodak VISION3 500T**

- **向く**：アパレルの生地感、ライフスタイル、ブランドムービー、手仕事、肌や布の手触りを出したいカット
- **向かない**：色再現を最優先する商品ヒーローカット（→ P2）
- **狙う見え方**：`fine organic grain, visible skin texture and fabric weave, gentle highlight roll-off, detailed shadows`
| 引き | ミディアム | 寄り | ディテール | T値（開放 T2） |
|---|---|---|---|---|
| 25 / 32mm | 40 / 50mm | 75mm | 100mm | 浅く T2 / 標準 T2.8 / 深く T4 |

```text
{SHOT} of {SUBJECT} {ACTION}. ARRICAM LT with a Cooke S4/i {FOCAL}mm lens, Kodak VISION3 500T film look, daylight-corrected color. Fine organic grain, visible {SURFACE_1} and {SURFACE_2}, gentle highlight roll-off, detailed shadows. Soft side light from {SOURCE} shapes {TARGET}. {MOVEMENT}, stable exposure, natural motion blur.
```

- **効かせるコツ**：横から光を当てると、毛穴や織り目が見えるようになる。粒子は質感を足すだけで、フラットな光で撮った顔を救うわけではない。
- **全体がぼやけたら**：「soft image」を消し、`sharp eyes, gentle highlight roll-off and fine grain` に置き換える。明部をやわらかくしても、被写体までボケさせる必要はない。
- **色の注意**：500T はタングステン（電球色）用のフィルム。昼光でニュートラルに見せたいときは `daylight-corrected color` を必ず付ける。
  暖色にしたいときは、意図して `warm tungsten color` と書く。暖色はフィルムの自動効果ではなく、演出の選択。
  昼の屋外なら `Kodak VISION3 250D` に替える手もある。

---

## P2 CLEAN — クリアで自然な解像感
**Sony VENICE 2 ｜ ZEISS Supreme Prime**

- **向く**：商品ヒーロー、コスメ、食品、ガジェット、使用デモ、インテリア。**EC商品の既定パッケージ**
- **向かない**：粒子やフィルムの温度で見せたいブランドムービー（→ P1）
- **狙う見え方**：`natural skin tones, neutral color balance, clearly resolved {surfaces}, gentle transition into a softly defocused background, clean digital rendering with natural edge detail`
| 引き | ミディアム | 寄り | ディテール | T値（開放 T1.5） |
|---|---|---|---|---|
| 25 / 29 / 35mm | 50mm | 65 / 85mm | 100mm | 浅く T2 / 標準 T2.8 / 深く T4 |

```text
{SHOT} of {SUBJECT} {ACTION}. Sony VENICE 2 with a ZEISS Supreme Prime {FOCAL}mm lens at T{STOP}. Soft daylight from {SOURCE}, neutral color balance, natural skin tones. Clearly resolved {SURFACE_1}, {SURFACE_2} and {SURFACE_3} texture, gentle transition into a softly defocused background. Clean digital rendering with natural edge detail. {MOVEMENT}.
```

- **効かせるコツ**：大事な素材を2〜3個だけ名指しする（肌、釉薬のかかった陶器、ヘアラインの金属、木目など）。「全部を超精細に」と頼むより効く。
- **無機質・カタログ調になったら**：`natural edge detail, subtle skin variation and soft side light` を足す。解像感は残したまま、ローカルコントラストの誇張だけを抑えられる。

### 素材の語彙【Snafty】

| 商材 | 名指しする素材の例 |
|---|---|
| コスメ | `frosted glass bottle`, `glossy lipstick bullet`, `creamy texture swatch on skin`, `brushed metal cap` |
| スキンケア | `dewy skin with visible pores`, `translucent gel`, `single drop of serum` |
| 食品 | `glistening sauce`, `crisp golden crust`, `rising steam`, `condensation on a cold glass`, `juice beading at the seam`, `lacy crisp edges`, `glossy glaze` |
| アパレル | `cotton jersey knit`, `denim twill weave`, `ribbed knit cuff`, `stitching along the seam` |
| 革小物 | `full-grain leather`, `edge paint`, `saddle stitching` |
| ガジェット | `anodized aluminum`, `matte soft-touch plastic`, `glass display reflections` |
| 住まい | `oak wood grain`, `linen fabric`, `glazed ceramic`, `brushed stainless steel` |

### 食品を撮るときのコツ【Snafty】

- **湯気**は、暗い背景の前に置き、逆光か半逆光で当てると見える（`backlight rims the steam against the darker wall behind`）。明るい背景の前では消える。
- **ツヤと肉汁**は、後ろから来る光の反射で出る（`light from behind catches the juice with small bright highlights`）。
- **色**は `neutral color balance with a gentle warm tint` まで許容する。美味しそうに見えることを優先してよい。

---

## P3 ANAMORPHIC — 夜・光もの
**RED V-RAPTOR ｜ Laowa Proteus 2x Anamorphic**

- **向く**：夜の街、店舗・イベント照明、ヘッドライト、世界観をつかむ冒頭カット
- **向かない**：昼の商品説明、色再現が必要なカット
- **狙う見え方**：`horizontal flare tied to a light source, vertically oval background highlights, natural facial proportions`
| 引き | ミディアム | 寄り | ディテール | T値（開放 T2） |
|---|---|---|---|---|
| 28 / 35mm | 45mm | 60 / 85mm | 不向き | 浅く T2 / 標準 T2.8 |
- **フレア色**：Proteus には blue / amber / silver のフレア版がある。ブランドカラーに寄せて選ぶ。

```text
{SHOT} of {SUBJECT} {ACTION} at night. RED V-RAPTOR with a Laowa Proteus {FOCAL}mm 2x anamorphic lens, {FLARE_COLOR}-flare version, Super 35 sensor crop. Correctly desqueezed image with natural facial proportions. Distant {SMALL_LIGHTS} form vertically oval bokeh. A bright {PRACTICAL_LAMP} near the frame edge creates a brief horizontal {FLARE_COLOR} flare as the handheld camera shifts sideways. Soft {KEY_LIGHT} keeps the face clearly readable.
```

- **フレアには出る理由を与える**：フレームの端に明るいランプを置き、カメラを少し動かして光の角度を変える。フレアは短くし、顔が読める状態を保つ。
- **楕円ボケが出ないとき**：ピント面の外、遠くに小さな光を置く。「anamorphic」と書くだけでは、レンズの癖をどこに出すかがモデルに伝わらない。
- **【Snafty】縦型の場合**：9:16 では楕円ボケと横フレアの癖だけを借りる。画面比はツールのパラメータに任せる。

---

## P4 PORTRAIT — 瞳にピント、背景は光の粒
**RED V-RAPTOR ｜ Laowa Argus（球面レンズのルック）**

- **向く**：モデルの表情アップ、使用後の感情（満足・安堵）、語りかけの寄り
- **向かない**：手に持った商品を見せるカット（深くして P2 / P5 で撮る）
- **狙う見え方**：`precisely focused eyes, shallow depth of field, predominantly rounded highlights near the center of the frame`
| 引き | ミディアム | 寄り | ディテール | 絞り |
|---|---|---|---|---|
| 不向き | 35mm | 35 / 45mm | 不向き | T値は書かず `wide aperture` と書く（開放 f/0.95） |

```text
Close portrait of {SUBJECT} {ACTION}. RED V-RAPTOR with a Laowa Argus spherical lens look, wide aperture and shallow depth of field. The eyes remain precisely focused. Small {WARM_LAMPS} several meters behind the subject become large, soft, predominantly rounded highlights near the center of the frame. Gentle side light preserves skin texture. Restrained handheld breathing, with the focus following the slight head movement.
```

- **ボケは距離で作る**：人物をカメラの近くに置き、光源をずっと後ろに置く。「背景をぼかして」と頼むより、配置を書くほうが効く。
- **顔や手がボケたら**：何を優先するかを決める。ポートレートなら瞳。商品デモなら被写界深度を深めて、顔と商品の両方を読ませる。

---

## P5 NATURAL DEPTH — 空間ごと見せる（ガイドのボーナス枠）
**ARRI ALEXA Mini LF ｜ ARRI Signature Prime**

- **向く**：生活空間での使用シーン、店舗や空間の紹介、部屋の中で起きる出来事（キャラクター物のシリーズ）
- **向かない**：背景を完全に消して、主役だけを浮かせたいカット（→ P4）
- **狙う見え方**：`natural fine detail, smooth tonal transitions, the room behind remains recognizable but softly separated`
| 引き | ミディアム | 寄り | ディテール | T値（開放 T1.8） |
|---|---|---|---|---|
| 29 / 35mm | 47mm | 58 / 75mm | 95mm | 浅く T2 / 標準 T2.8 / 深く T4 |

```text
{SHOT} of {SUBJECT} {ACTION} in {PLACE}. ARRI ALEXA Mini LF with an ARRI Signature Prime {FOCAL}mm lens at T{STOP}. Soft {SOURCE} light, gently warm skin tones, natural fine detail and smooth tonal transitions. {BACKGROUND_ELEMENT} behind remains recognizable but softly separated. {MOVEMENT}.
```

- **世界を少し残す**：ドア、窓、廊下を画面に入れると奥行きが出る。背景を消さなくても主役は立つ。
- **背景がドロドロに溶けたら**：`Moderate depth of field; the background remains recognizable but softly separated.` を足して、背景を再び役立つ情報にする。

---

## 外し：UGC／スマホルック【Snafty・検証枠】

ガイドにはない、Snafty 独自の検証用の型。フィードに馴染ませたいパフォーマンス広告で、シネマ調と比較するために使う。

- **向く**：レビュー風、開封、ビフォーアフター、語りかけ
- **使い方**：同じ台本で、王道パッケージ版とこの型の版を1本ずつ作り、ABテストに回す。どちらを採用するかは CTR / CVR を見て決める。

```text
Vertical smartphone video of {SUBJECT} {ACTION} in {PLACE}, shot on a recent phone's main camera. Natural indoor light from {SOURCE}, true-to-life colors, crisp everyday detail. Handheld with a small natural wobble, the camera following {TARGET}; brief auto-exposure adjustment as it moves toward the window.
```
