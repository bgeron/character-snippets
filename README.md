# Character-snippets

[![Commitizen friendly](https://img.shields.io/badge/commitizen-friendly-brightgreen.svg)](http://commitizen.github.io/cz-cli/)
[![Travis Build Status](https://travis-ci.org/bgeron/character-snippets.svg?branch=master)](https://travis-ci.org/bgeron/character-snippets)
[![AppVeyor Build status](https://ci.appveyor.com/api/projects/status/90nssws7muesco60?svg=true)](https://ci.appveyor.com/project/bgeron/character-snippets)

A small program that generates a Visual Studio Code snippets file, with either builtin snippets (>1000 Unicode characters) or a custom TOML input file.

```sh
# Install with Rust. Alternatively, download a binary from the Releases page.
cargo install character-snippets

# Put a snippets file in a good location for Visual Studio Code on Linux. These
# snippets will be visible in all workspaces.
character-snippets --builtin > ~/.config/Code/User/snippets/chars.code-snippets

# Use a custom snippets file.
character-snippets my-custom-snippets.toml > ~/.config/Code/User/snippets/chars.code-snippets

# To find out where the snippets files are located on your operating system, run
# "Preferences: Configure User Snippets" and create a new global snippets file.
```

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

# Installing

Download binaries:

  from the [GitHub releases page](https://github.com/bgeron/character-snippets/releases)

Or compile from scratch on Unix:

  ```sh
  # 1. Install Rust
  curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
  # 2. Add ~/.cargo/bin to PATH
  source $HOME/.cargo/env # or log in again
  # 3. We need a basic build environment (cc, ld) for a dependency
  apt install build-essential
  # 4. Install character-snippets
  cargo install character-snippets
  # 5. Profit!
  character-snippets --help
  ```

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
