# 書き方の原則・トラブル早見表・動きの語彙

出典：Promptwise Field Guide 01（Practice 01 / 02）。
トラブル表の「言われ方」列、動きの語彙、ツール別メモは【Snafty】で追加したもの。

## 原則A：言葉を「作れる条件」にする（Practice 01）

モデルには、画面として組み立てられる条件を渡す。形容詞を1つ足すより、光源・距離・ピント対象を1つ書くほうが効く。

1. **原因を書く**
   「beautiful bokeh」ではなく、被写体のずっと後ろに小さなランプを置く。
   「dramatic light」ではなく、窓が顔のどちら側を照らしているかを書く。
2. **3種類の「ソフト」を分ける**
   - soft light：影の縁がやわらかい
   - soft background：背景がピンぼけしている
   - soft highlight roll-off：明るい部分へなだらかに移行する

   どれを使っても、瞳までボケさせる必要はない。
3. **ピントを合わせる対象を選ぶ**
   シャープに保つものを名指しする。物を見せるときは、物が止まってからそこへ注意（ピント）を移す。
4. **カメラの動きにきっかけを与える**
   カメラは被写体の動作に反応させる。手持ちや遅れてくるピントは選択肢であって、リアルさのための義務ではない。固定ショットが正解のこともある。

## 原則B：うまくいった部分を保つ（Practice 02）

1. **参照画像ごとに役割を決める**
   「identity 用」と「場所と光の用」を分け、そのことを文章でも明記する。ラベルの呼び方は使うツールに合わせる。
   キャラクターシートの背景やポーズを、意図せず持ち込ませない。
2. **i2v では、開始画像に仕事をさせる**
   書くのは「何が変わるか」だけにする。見えているものを全部書き直すと、動きの指示と競合する。
   アクション → カメラの動き → ピントの移動 → 足りない要素の順で書く。
3. **1回に1つだけ直す**
   肌がのっぺりしていたら、光か肌の記述を直す。ボケが出なければ、ピントと背景の距離を直す。
   比較は同じシーンで行い、1回の結果だけでフレーズの良し悪しを決めない。
4. **使うモデルに合わせて書く**
   ネガティブプロンプトは万能ではない。Runway Gen-4 は肯定形を推奨している（「no camera movement」ではなく「locked camera」）。
   黒つぶれには `deep charcoal shadows retain subtle texture` と書く。

## トラブル早見表（変えるのは1つだけ）

| 症状 | クライアントの言われ方【Snafty】 | 原因の仮説 | 変える1手 |
|---|---|---|---|
| 全体がぼやける | 「ピンボケ」「眠い」 | soft 系の語が被写体にまで効いている | `soft image` を消す → `sharp eyes, gentle highlight roll-off, fine grain` |
| 肌がプラスチックみたい | 「AIっぽい」「のっぺり」「CGっぽい」 | 正面からのフラットな光 | `soft side light from a window on the {left} side of the face` ＋ `visible skin texture` |
| 硬くて無機質 | 「安っぽい」「カタログみたい」「ギラギラ」 | 解像感を求める語の盛りすぎ | `natural edge detail, subtle skin variation, soft side light` |
| ボケが出ない、背景がうるさい | 「ごちゃごちゃ」「主役がわからない」 | 被写体と背景の距離を書いていない | 人物をカメラ寄りに、`small lamps several meters behind` を置く |
| 背景が溶けすぎる | 「どこなのかわからない」 | 被写界深度が浅すぎる | `Moderate depth of field; the background remains recognizable but softly separated.` |
| 顔・手・商品がボケる | 「商品が見えない」 | ピントの対象を書いていない | 対象を名指しする。商品デモなら T4 前後にして、顔と商品の両方を読ませる |
| 黒がつぶれる | 「暗くて見えない」「重い」 | 影の階調を指定していない | `deep charcoal shadows retain subtle texture` |
| カメラが勝手に動く、揺れる | 「酔う」「落ち着かない」 | 動きの指示がない、またはきっかけがない | `locked camera` か、動作に反応する動きを1つだけ書く |
| フレアが顔にかかる | 「見づらい」 | フレアが強すぎる・長すぎる | `brief` にして、光源をフレームの端へ寄せる |
| 楕円ボケが出ない | —— | ピント面の外に小さな光がない | `small, distant lights outside the focus plane` |
| i2v で画像が崩れる、動かない | 「最初の画と違う」 | 画像に写っている内容を全部書き直している | MOTION をアクションとカメラの動きだけにする |
| 見せ場（中身・完成形）の形や色が違う | 「商品と違う」「思ってたのと違う」 | リビール後の姿をモデルに作らせている | 終了フレームに完成形の画像を指定する。指定できなければ、開始フレームを見せ場が一部見えている状態にする |
| カットごとに画が違う | 「統一感がない」 | カメラ名をカットごとに変えている | パッケージを1つに固定し、焦点距離と T 値だけ変える（series-look.md） |

## 動きの語彙（きっかけとセットで書く）【Snafty】

| 意図 | 書き方 |
|---|---|
| 固定 | `Locked camera.` |
| 呼吸程度の手持ち | `Restrained handheld breathing.` |
| 手元を追う | `The handheld camera makes a small adjustment to follow the hand.` |
| 動作のあとに寄る | `After {subject} turns, the shoulder-mounted camera moves slightly closer, then settles.` |
| 動作と同時に寄る | `As {subject} {action}, the camera slowly pushes in.` |
| 商品へピントを移す | `As the {product} comes to rest, focus shifts from {A} to the {product}.` |
| フレアを出す | `The handheld camera shifts sideways, catching the lamp at the frame edge.` |
| 頭の動きにピントを追わせる | `The focus follows the slight head movement.` |

## ツール別メモ【Snafty】

- 縦横比と尺は、各ツールの UI パラメータで指定する。プロンプト内では構図で補う程度にとどめる。
- ネガティブ欄があるツールでも、本文は肯定形で書く。ネガティブ欄は、同じ破綻が何度も出るときの抑えにだけ使う。
- 同じフレーズでも、モデルやバージョンによって効き方が違う。新しいモデルに切り替えたら、量産の前に同じシーンで数本出して確認する。
