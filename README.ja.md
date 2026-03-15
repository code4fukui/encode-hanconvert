# encode-hanconvert

encode-hanconvertは、従来の中国語と簡体字中国語間の変換を容易にするエンコーディング形式です。

## デモ
[デモページ](https://code4fukui.github.io/encode-hanconvert/)
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
Copyright 2002-2009 by Audrey Tang <cpan@audreyt.org>  
Copyright 2006 by Kuang-che Wu <kcwu@csie.org>

Perlと同じ条件で再配布および変更が可能です。
http://www.perl.com/perl/misc/Artistic.html