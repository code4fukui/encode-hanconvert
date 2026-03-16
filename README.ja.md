# encode-hanconvert

encode-hanconvertは、中国語の簡体字と繁体字の相互変換を行うためのライブラリです。Perlで実装されており、JavaScriptの実装も提供されています。

## デモ
encode-hanconvertのデモページ: https://code4fukui.github.io/encode-hanconvert/

```js
import { Big5 } from "https://code4fukui.github.io/encode-hanconvert/js/Big5.js";

console.log(Big5.encode("元気？"));
```

## 機能
- 簡体字中国語(GB2312)から繁体字中国語(Big5)への変換
- 繁体字中国語(Big5)から簡体字中国語(GB2312)への変換

## 必要環境
- Perl 5.7.3以上
- Encode 1.41以上

## 使い方
encode-hanconvertはPerlの標準的なモジュールインストール方式に従います:

```sh
perl Makefile.PL
make
make test
make install
```

オプションで`enc2xs -C`を実行することで、Encode.pmのオンデマンドロードDBを更新できます。

コマンドラインツール`b2g.pl`と`g2b.pl`がインストールされ、GBKとBig5エンコーディング間の簡単な変換ができます。

## ライセンス
MIT License — 詳細は [LICENSE](LICENSE) を参照してください。