# tenhou_prob

麻雀の役「天和」が出現する確率を計算するプログラム  


## 計算手順
* 配牌を乱数でランダムに配る
* 和了判定
  * 和了の場合は牌を出力し、カウントを1増やす


## 和了判定アルゴリズム
1. 国士、七対子チェック
2. 手牌を萬索筒字に分け、その枚数が(3x, 3x, 3x, 3x+2)になっているかチェック
3. 3x枚の牌種に対し、全探索で面子になっているかチェック
4. 3x+2枚の牌種に対しては、「一つ雀頭を固定し、手順(3)の全探索」を繰り返す


## 計算結果
* 確率: 3.0(2)e-6 (=約34万回に1回)
  * 試行回数: 1億回
  * 和了回数: 298回
* 不確かさはポアソン分布を仮定
* [Wiki](https://ja.wikipedia.org/wiki/天和_(麻雀))の記述とも一致
