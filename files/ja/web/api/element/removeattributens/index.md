---
title: Element.removeAttributeNS()
slug: Web/API/Element/removeAttributeNS
page-type: web-api-instance-method
tags:
  - API
  - DOM
  - Element
  - Method
  - NeedsSpecTable
  - Reference
browser-compat: api.Element.removeAttributeNS
translation_of: Web/API/Element/removeAttributeNS
l10n:
  sourceCommit: 196cc4ff3068a59b962a3fe1cbb960eb72ef542b
---
{{ APIRef("DOM") }}

**`removeAttributeNS()`** は {{domxref("Element")}} インターフェイスのメソッドで、要素から指定された属性を取り除きます。

## 構文

```js
removeAttributeNS(namespace, attrName)
```

### 引数

- `namespace` は文字列で、属性の名前空間を示します。
- `attrName` は文字列で、現在のノードから取り除く属性の名前を示します。

### 返値

なし ({{jsxref("undefined")}})。

### 例

```js
// Given:
//   <div id="div1" xmlns:special="http://www.mozilla.org/ns/specialspace"
//     special:specialAlign="utterleft" width="200px" />
d = document.getElementById("div1");
d.removeAttributeNS("http://www.mozilla.org/ns/specialspace", "specialAlign");
// Now: <div id="div1" width="200px" />
```

## メモ

{{ DOMAttributeMethods() }}

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}

Firefox 3 以降では、このメソッドは DOM 値を既定値にリセットします。
