---
title: 'CSP: frame-src'
slug: Web/HTTP/Headers/Content-Security-Policy/frame-src
tags:
  - CSP
  - Content-Security-Policy
  - Directive
  - Frame
  - HTTP
  - Reference
  - Security
  - frame-src
  - source
browser-compat: http.headers.Content-Security-Policy.frame-src
translation_of: Web/HTTP/Headers/Content-Security-Policy/frame-src
---
{{HTTPSidebar}}

HTTP の {{HTTPHeader("Content-Security-Policy")}} (CSP) における **`frame-src`** ディレクティブは、 {{HTMLElement("frame")}} や {{HTMLElement("iframe")}} のような要素を使用した内部の閲覧コンテキストの読み込みに有効なソースを指定します。

<table class="properties">
  <tbody>
    <tr>
      <th scope="row">CSP バージョン</th>
      <td>1</td>
    </tr>
    <tr>
      <th scope="row">ディレクティブ種別</th>
      <td>{{Glossary("Fetch directive", "フェッチディレクティブ")}}</td>
    </tr>
    <tr>
      <th scope="row">代替</th>
      <td>
        このディレクティブがない場合、ユーザーエージェントは {{CSP("child-src")}} ディレクティブを探す (さらにこの代替は {{CSP("default-src")}} ディレクティブである)。
      </td>
    </tr>
  </tbody>
</table>

## 構文

`frame-src` ポリシーには、 1 つ以上のソースが許可されています。

```http
Content-Security-Policy: frame-src <source>;
Content-Security-Policy: frame-src <source> <source>;
```

### ソース

`<source>` は、 [CSP ソース値](/ja/docs/Web/HTTP/Headers/Content-Security-Policy/Sources#ソース)にあるいずれかの値を取ることができます。

なお、この同じ値のセットはすべての{{Glossary("fetch directive", "フェッチディレクティブ")}}（と [他の多くのディレクティブ](/ja/docs/Web/HTTP/Headers/Content-Security-Policy/Sources#関連ディレクティブ)）で使用できます。

## 例

## 違反例

この CSP ヘッダーがある場合、

```http
Content-Security-Policy: frame-src https://example.com/
```

以下の {{HTMLElement("iframe")}} はブロックされ、読み込まれません。

```html
<iframe src="https://not-example.com/"></iframe>
```

## 仕様書

{{Specifications}}

## ブラウザーの互換性

{{Compat}}

## 関連情報

- {{HTTPHeader("Content-Security-Policy")}}
- {{HTMLElement("frame")}} および {{HTMLElement("iframe")}}
