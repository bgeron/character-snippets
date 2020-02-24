# Character-snippets

[![Docs.rs link](https://docs.rs/character-snippets/badge.svg)](https://docs.rs/character-snippets)
[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)

A small program that generates a Visual Studio Code snippets file from a TOML input file.

This is particularly useful for a file with snippets for Unicode characters.

The format of the input file should be as follows:

```toml
[Snippets]
    xbrackets = "〚$1〛"
    xcheckbox = "☐ "
    xchecked = "☑ "
    xcheckmark = "✓"
    xch = "✓"
```

Visual Studio Code will interpret variables such as `$1` as placeholders.

Output will be sent to standard output.

TODO document better

# License

This project is licensed under either of

 * Apache License, Version 2.0, ([LICENSE-APACHE](LICENSE-APACHE) or
   http://www.apache.org/licenses/LICENSE-2.0)
 * MIT license ([LICENSE-MIT](LICENSE-MIT) or
   http://opensource.org/licenses/MIT)

at your option.

### Contribution

Unless you explicitly state otherwise, any contribution intentionally submitted
for inclusion in this project by you, as defined in the Apache-2.0 license, shall be
dual licensed as above, without any additional terms or conditions.
