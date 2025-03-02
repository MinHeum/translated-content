---
title: TypedArray.prototype.sort()
slug: Web/JavaScript/Reference/Global_Objects/TypedArray/sort
tags:
  - ECMAScript 2015
  - JavaScript
  - Method
  - Prototype
  - TypedArray
  - メソッド
  - 型付き配列
translation_of: Web/JavaScript/Reference/Global_Objects/TypedArray/sort
---
{{JSRef}}

**`sort()`** メソッドは、型付き配列の要素を*その場で*数値的に並べ替え、その型付き配列を返します。このメソッドは {{jsxref("Array.prototype.sort()")}} と同じアルゴリズムです。 _TypedArray_ は、ここでは[型付き配列型](/ja/docs/Web/JavaScript/Reference/Global_Objects/TypedArray#TypedArray_objects)のうちの一つです。

{{EmbedInteractiveExample("pages/js/typedarray-reverse.html","shorter")}}

## 構文

```
typedarray.sort([compareFunction])
```

### 引数

- `compareFunction` {{optional_inline}}
  - : ソート順を定義する関数を指定します。

### 返値

並べ替えた型付き配列です。

## 例

### sort の使用

他の例は、 {{jsxref("Array.prototype.sort()")}} メソッドです。

```js
let numbers = new Uint8Array([40, 1, 5, 200]);
numbers.sort();
// Uint8Array [ 1, 5, 40, 200 ]
// ふつうの配列とは異なり、数値的に数値を並べ替えるためには
// 比較関数は必要ありません。

// ふつうの配列は数値で並べ替えるために比較関数を必要とします。
numbers = [40, 1, 5, 200];
numbers.sort();
// [1, 200, 40, 5]

numbers.sort((a, b) => a - b); // 数値を比較
// [ 1, 5, 40, 200 ]
```

## 仕様書

| 仕様書                                                                                                               |
| -------------------------------------------------------------------------------------------------------------------- |
| {{SpecName('ESDraft', '#sec-%typedarray%.prototype.sort', 'TypedArray.prototype.sort')}} |

## ブラウザーの互換性

{{Compat("javascript.builtins.TypedArray.indexOf")}}

## 関連情報

- {{jsxref("Array.prototype.sort()")}}
