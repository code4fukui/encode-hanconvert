# encode-hanconvert

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

This is the README file for Encode::HanConvert, two encoding formats to facilitate mappings between traditional and simplified Chinese characters.

## Installation

Encode::HanConvert uses the standard perl module install process:

```sh
perl Makefile.PL
make
make test
make install
enc2xs -C	# optional; updates Encode.pm's on-demand loading DB
```

You will need perl 5.7.3 or better, as well as Encode 1.41 or better for Unicode-related functions. Otherwise, Encode::HanConvert::Perl is used automatically, which provides perl-based implementations to big5_to_gb() and gb_to_big5().

Regardless of the implementation, two command-line utilities ('b2g.pl' and 'g2b.pl') are installed for simple conversion between GBK and Big5 encodings.

For this module's typical usage and examples, please consult its POD documentation.

## in JavaScript

- [Live Demo](https://code4fukui.github.io/encode-hanconvert/)
```js
import { Big5 } from "https://code4fukui.github.io/encode-hanconvert/js/Big5.js";

console.log(Big5.encode("元気？"));
```

## License

MIT License — see [LICENSE](LICENSE).