# encode-hanconvert

A Perl module and JavaScript library for converting between Traditional and Simplified Chinese characters.

> 日本語のREADMEはこちらです: [README.ja.md](README.ja.md)

## JavaScript Usage

This repository provides a modern JavaScript module for client-side character conversion.

### Live Demo

A simple web interface for real-time character conversion is available:

- **[Live Demo](https://code4fukui.github.io/encode-hanconvert/)**

### Code Example

The ES module can be imported directly from GitHub Pages. The `Big5.encode()` function converts Simplified Chinese (GB2312) characters to their Traditional Chinese (Big5) equivalents.

```js
import { Big5 } from "https://code4fukui.github.io/encode-hanconvert/js/Big5.js";

// Converts Simplified/Japanese characters to Traditional
console.log(Big5.encode("元気？")); // Outputs: 元氣？
console.log(Big5.encode("日本的参与！")); // Outputs: 日本的參與！
```

## Perl Module (Encode::HanConvert)

This is the original Perl module that provides two encoding formats to facilitate mappings between Traditional and Simplified Chinese via Perl's `Encode` module.

### Requirements

- Perl 5.7.3 or later
- Encode 1.41 or later

If the requirements are not met, `Encode::HanConvert::Perl` is used as a fallback, providing pure-Perl implementations.

### Installation

`Encode::HanConvert` uses the standard Perl module installation process:

```sh
perl Makefile.PL
make
make test
make install
enc2xs -C	# Optional: updates Encode.pm's on-demand loading DB
```

The module also installs two command-line utilities, `b2g.pl` and `g2b.pl`, for converting files between GBK and Big5 encodings. For detailed usage and examples, please consult the module's POD documentation.

## Acknowledgements

This project is a fork of the original [encode-hanconvert](https://github.com/audreyt/encode-hanconvert) by Audrey Tang, with an added JavaScript implementation and live demo.

## License

MIT License — see [LICENSE](LICENSE).