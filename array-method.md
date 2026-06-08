# 配列メソッド

## 参考

- [https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array](https://developer.mozilla.org/ja/docs/Web/JavaScript/Reference/Global_Objects/Array)

## 全部で何個？

ECMAScript標準だと **約40個前後**（静的メソッド含む）。
バージョンごとに増え続けてるから「ちょうど何個」は言いにくい。

## カテゴリ別まとめ

| カテゴリ | メソッド例 | 個数目安 |
|---------|-----------|---------|
| 変換・生成 | map, flatMap, flat | ~4 |
| 絞り込み・検索 | filter, find, findIndex, findLast | ~6 |
| 集約・判定 | reduce, reduceRight, every, some, includes | ~5 |
| 破壊的操作 | push, pop, shift, unshift, splice, sort, reverse, fill | ~8 |
| 非破壊的操作 | toSorted, toReversed, toSpliced, with | ~4 ← ES2023新顔 |
| 反復 | forEach, entries, keys, values | ~4 |
| 結合・変換 | join, concat, slice, flat | ~4 |
| 静的メソッド | Array.from, Array.of, Array.isArray | ~3 |

## よく使うやつ TOP10（個人的感覚）

```
頻度高 ████████████
map        ★★★★★  配列を別の配列に変換
filter     ★★★★★  条件で絞り込み
forEach    ★★★★☆  ループ（返値不要な時）
find       ★★★★☆  最初にマッチした要素1つ
some       ★★★☆☆  1つでも条件満たすか
reduce     ★★★☆☆  集約・合計・変換
includes   ★★★☆☆  含まれるか bool
flat/flatMap ★★☆☆☆ ネスト解消
slice      ★★★☆☆  部分コピー（非破壊）
sort       ★★☆☆☆  並び替え（比較関数必須）
頻度低 ████
```

## 超よく使う3パターン

```js
// 変換したい → map
[1,2,3].map(x => x * 2)  // [2,4,6]

// 絞りたい → filter
[1,2,3].filter(x => x > 1)  // [2,3]

// 1個探したい → find
[{id:1},{id:2}].find(x => x.id === 2)  // {id:2}
```
