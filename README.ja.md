# encode-hanconvert

繁体字と簡体字の間で文字を変換するためのPerlモジュールおよびJavaScriptライブラリ。

## JavaScriptでの使用方法

このリポジトリは、クライアントサイドでの文字変換用のモダンなJavaScriptモジュールを提供します。

### ライブデモ

リアルタイムで文字変換を行えるシンプルなWebインターフェースを利用できます。

- **[ライブデモ](https://code4fukui.github.io/encode-hanconvert/)**

### コード例

ESモジュールはGitHub Pagesから直接インポートできます。`Big5.encode()`関数は、簡体字（GB2312）を対応する繁体字（Big5）に変換します。

```js
import { Big5 } from "https://code4fukui.github.io/encode-hanconvert/js/Big5.js";

// 簡体字/日本語の文字を繁体字に変換
console.log(Big5.encode("元気？")); // 出力: 元氣？
console.log(Big5.encode("日本的参与！")); // 出力: 日本的參與！
```

## Perlモジュール (Encode::HanConvert)

これはオリジナルのPerlモジュールであり、Perlの`Encode`モジュールを介して繁体字と簡体字間のマッピングを容易にする2つのエンコーディング形式を提供します。

### 要件

- Perl 5.7.3以降
- Encode 1.41以降

要件を満たしていない場合は、フォールバックとして`Encode::HanConvert::Perl`が使用され、Pure Perlによる実装が提供されます。

### インストール

`Encode::HanConvert`は、標準的なPerlモジュールのインストール手順を使用します。

```sh
perl Makefile.PL
make
make test
make install
enc2xs -C	# オプション: Encode.pmのオンデマンドロードDBを更新
```

また、本モジュールはGBKとBig5エンコーディング間でファイルを変換するための2つのコマンドラインユーティリティ（`b2g.pl`および`g2b.pl`）もインストールします。詳細な使用方法や例については、モジュールのPODドキュメントを参照してください。

## 謝辞

本プロジェクトは、Audrey Tang氏によるオリジナルの[encode-hanconvert](https://github.com/audreyt/encode-hanconvert)をフォークしたものであり、JavaScript実装とライブデモが追加されています。

## ライセンス

MIT License — 詳細は[LICENSE](LICENSE)を参照してください。
