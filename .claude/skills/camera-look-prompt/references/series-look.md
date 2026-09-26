# シリーズ・ルック表（パートナー配布用）【Snafty】

量産やシリーズ物では、カットごとにルックを考えない。**最初に1枚決めて固定し、パートナーに配る。**

- 目的は、パートナーごとの解釈のブレと、「なんか違う」から始まる修正の往復を減らすこと。
- 決めるのは Snafty 側で1回だけ。パートナーは「変えてよいもの」だけを差し替えて量産する。
- 決める前に、同じシーンを候補パッケージ2つで2〜3本ずつ出し、比べてから固定する。1本だけで決めない。
- 案件固有の表は、このリポジトリ（public）には保存しない。

## 記入式テンプレ

````markdown
# SERIES LOOK — 【シリーズ名】
更新日：【　】 / 決定者：【　】

## 1. カメラパッケージ
- 【P1〜P5】：【カメラ】 + 【レンズ】
- 理由（1行）：【　】

## 2. フォーマット
- 縦横比：【9:16】 / 1カットの尺：【5s】 / 生成方式：【i2v】 / ツール：【　】

## 3. ショット別の焦点距離・T値（この範囲からだけ選ぶ）
| ショット | 焦点距離 | T値 |
|---|---|---|
| 引き・空間 | 【　】mm | T【　】 |
| ミディアム | 【　】mm | T【　】 |
| 寄り・表情 | 【　】mm | T【　】 |
| ディテール | 【　】mm | T【　】 |

## 4. 光と色
- 基本の光源：昼【　】 / 夜【　】（画面内にある光源を使う）
- 当てる方向：【例：主役の顔の左側から】
- 色：【neutral color balance / daylight-corrected color / warm tungsten color】
- 影：【暗部が多いなら deep charcoal shadows retain subtle texture を必須にする】

## 5. 動きの文法
- 基本：【locked camera / restrained handheld breathing】
- 見せ場のカットだけ：【例：動作に反応した slow push-in】
- このシリーズでは使わない動き：【例：高速ドリー → 代わりに locked camera と書く】

## 6. ピントの優先順位
1. 【例：主役の瞳】
2. 【例：解決の対象物（止まってからピントを移す）】

## 7. 参照画像の役割
- reference image 1 = 【identity only（背景・ポーズは使わない）】
- reference image 2 = 【setting & light】

## 8. 共通サフィックス（KEYFRAME の末尾に毎回そのまま付ける）
```text
【カメラ + レンズ {FOCAL}mm at T{STOP}】. 【光と色】. 【質感】. 【影】. 【背景の扱い】.
```

## 9. 変えてよいもの / 変えないもの
- 変えてよい：人物、場所、動作、焦点距離と T 値（3 の範囲内）、光源の位置
- 変えない：1 のパッケージ、4 の色、8 の共通サフィックス
````

## 記入例：家の中で起きる出来事を描くキャラクター物シリーズ（汎用例）

````markdown
# SERIES LOOK — 家の中のキャラクター物（例）

## 1. カメラパッケージ
- P5 NATURAL DEPTH：ARRI ALEXA Mini LF + ARRI Signature Prime
- 理由：部屋という「日常の場所」が読めることが物語の前提になる。背景を溶かしすぎない。

## 2. フォーマット
- 9:16 / 5s / i2v

## 3. ショット別の焦点距離・T値
| ショット | 焦点距離 | T値 |
|---|---|---|
| 引き・空間 | 29mm | T4 |
| ミディアム | 47mm | T2.8 |
| 寄り・表情 | 75mm | T2 |
| ディテール | 95mm | T2.8 |

## 4. 光と色
- 基本の光源：昼は窓からの光、夜は部屋の中の実光源（洗面台の鏡灯、キッチンの手元灯など）
- 色：昼は neutral color balance、夜は gently warm practical light
- 影：deep charcoal shadows retain subtle texture（必須）
- 暗い色のキャラクターを暗部に置くカットは、a thin soft rim of light で輪郭を分ける

## 5. 動きの文法
- 基本：locked camera
- 見せ場のカットだけ：動作に反応した slow push-in
- キャラクターが登場するカットは locked camera にする。止まった画のほうが、現れる動きが際立つ

## 6. ピントの優先順位
1. 主人公の瞳（表情カット）
2. 困りごとの対象物（止まってからピントを移す）

## 7. 参照画像の役割
- reference image 1 = キャラクターの identity only（外見は文章で描写し直さない）
- reference image 2 = 部屋の setting & light

## 8. 共通サフィックス
```text
ARRI ALEXA Mini LF with an ARRI Signature Prime {FOCAL}mm lens at T{STOP}. Soft motivated practical light, gently warm skin tones, natural fine detail and smooth tonal transitions. Deep charcoal shadows retain subtle texture. The room remains recognizable but softly separated.
```
````
