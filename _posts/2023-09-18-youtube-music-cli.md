---
layout: post
slug: Youtube Music Cli Terminal Arch
---


kalo pake aplikasi source memori yang dipake boros palagi dipake seharian, padalan butuh banget music untuk temen nugas maupun liat market. Searching di google nemu paket git bagus "ytui-music"

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/ytui-music.png" />


#### installasi & build

sumber paket : https://github.com/sudipghimire533/ytui-music
paket rustup : https://archlinux.org/packages/extra/x86_64/rust/

didalam panduan installasi, butuh "rustup", dikarenakan bisa di install dari pacman, saya install dari pacman saja.

```
[tama@tamaoksa ~]$ sudo pacman -S rustup
[sudo] password for tama: 
resolving dependencies...
looking for conflicting packages...

Packages (1) rustup-1.26.0-3

Total Download Size:   2,48 MiB
Total Installed Size:  6,98 MiB

:: Proceed with installation? [Y/n] 
:: Retrieving packages...
 rustup-1.26.0-3-...     2,5 MiB   610 KiB/s 00:04 [######################] 100%
(1/1) checking keys in keyring                     [######################] 100%
(1/1) checking package integrity                   [######################] 100%
(1/1) loading package files                        [######################] 100%
(1/1) checking for file conflicts                  [######################] 100%
:: Processing package changes...
(1/1) installing rustup                            [######################] 100%
You may need to run rustup update stable
and possibly also rustup self upgrade-data
Optional dependencies for rustup
    lldb: rust-lldb script
    gdb: rust-gdb script
:: Running post-transaction hooks...
(1/1) Arming ConditionNeedsUpdate...
```


```
[tama@tamaoksa ~]$ rustup --help
rustup 1.26.0 (2023-05-04)
The Rust toolchain installer

USAGE:
    rustup [OPTIONS] [+toolchain] <SUBCOMMAND>

ARGS:
    <+toolchain>    release channel (e.g. +stable) or custom toolchain to
                    set override

OPTIONS:
    -v, --verbose    Enable verbose output
    -q, --quiet      Disable progress output
    -h, --help       Print help information
    -V, --version    Print version information

SUBCOMMANDS:
    show           Show the active and installed toolchains or profiles
    update         Update Rust toolchains and rustup
    check          Check for updates to Rust toolchains and rustup
    default        Set the default toolchain
    toolchain      Modify or query the installed toolchains
    target         Modify a toolchain's supported targets
    component      Modify a toolchain's installed components
    override       Modify directory toolchain overrides
    run            Run a command with an environment configured for a given
                       toolchain
    which          Display which binary will be run for a given command
    doc            Open the documentation for the current toolchain
    man            View the man page for a given command
    self           Modify the rustup installation
    set            Alter rustup settings
    completions    Generate tab-completion scripts for your shell
    help           Print this message or the help of the given subcommand(s)

DISCUSSION:
    Rustup installs The Rust Programming Language from the official
    release channels, enabling you to easily switch between stable,
    beta, and nightly compilers and keep them updated. It makes
    cross-compiling simpler with binary builds of the standard library
    for common platforms.

    If you are new to Rust consider running `rustup doc --book` to
    learn Rust.
```



update pake rustup

```
[tama@tamaoksa ~]$ rustup update
info: no updatable toolchains installed
info: cleaning up downloads & tmp directories
info: self-update is disabled for this build of rustup
info: any updates to rustup will need to be fetched with your system package manager
```

>rustup is available on the Arch Linux software repository. Note that rustup self update will not work when installed this way, the package needs to be updated by pacman.





```
[tama@tamaoksa ~]$ rustup default stable
info: syncing channel updates for 'stable-x86_64-unknown-linux-gnu'
info: latest update on 2023-09-19, rust version 1.72.1 (d5c2e9c34 2023-09-13)
info: downloading component 'cargo'
  7.9 MiB /   7.9 MiB (100 %)   1.4 MiB/s in  6s ETA:  0s
info: downloading component 'clippy'
  2.5 MiB /   2.5 MiB (100 %)   1.2 MiB/s in  1s ETA:  0s
info: downloading component 'rust-docs'
 13.7 MiB /  13.7 MiB (100 %)   1.1 MiB/s in 11s ETA:  0s 
info: downloading component 'rust-std'
 26.9 MiB /  26.9 MiB (100 %)   2.2 MiB/s in 15s ETA:  0s
info: downloading component 'rustc'
 64.2 MiB /  64.2 MiB (100 %)   1.8 MiB/s in 38s ETA:  0s
info: downloading component 'rustfmt'
  2.5 MiB /   2.5 MiB (100 %)   2.5 MiB/s in  1s ETA:  0s
info: installing component 'cargo'
info: installing component 'clippy'
info: installing component 'rust-docs'
 13.7 MiB /  13.7 MiB (100 %)   7.1 MiB/s in  1s ETA:  0s
info: installing component 'rust-std'
 26.9 MiB /  26.9 MiB (100 %)  12.9 MiB/s in  3s ETA:  0s
info: installing component 'rustc'
 64.2 MiB /  64.2 MiB (100 %)  14.4 MiB/s in  5s ETA:  0s
info: installing component 'rustfmt'
info: default toolchain set to 'stable-x86_64-unknown-linux-gnu'

  stable-x86_64-unknown-linux-gnu installed - rustc 1.72.1 (d5c2e9c34 2023-09-13)
```



clone paket dari G1t

```
[tama@tamaoksa Downloads]$ git clone https://github.com/sudipghimire533/ytui-music
Cloning into 'ytui-music'...
remote: Enumerating objects: 1146, done.
remote: Counting objects: 100% (65/65), done.
remote: Compressing objects: 100% (48/48), done.
remote: Total 1146 (delta 22), reused 36 (delta 12), pack-reused 1081
Receiving objects: 100% (1146/1146), 5.50 MiB | 1.50 MiB/s, done.
Resolving deltas: 100% (636/636), done.
```



build paket

```
[tama@tamaoksa ytui-music]$ cargo build --all --release
warning: some crates are on edition 2021 which defaults to `resolver = "2"`, but virtual workspaces default to `resolver = "1"`
note: to keep the current resolver, specify `workspace.resolver = "1"` in the workspace root's manifest
note: to use the edition 2021 resolver, specify `workspace.resolver = "2"` in the workspace root's manifest
    Updating crates.io index
    Updating git repository `https://github.com/sudipghimire533/libmpv-rs`
  Downloaded tinyvec_macros v0.1.0
  Downloaded matches v0.1.9
  Downloaded fallible-streaming-iterator v0.1.9
  Downloaded num_cpus v1.13.1
  Downloaded parking_lot v0.12.1
  Downloaded want v0.3.0
  Downloaded http-body v0.4.5
  Downloaded openssl-probe v0.1.5
  Downloaded cfg-if v1.0.0
  Downloaded tower-service v0.3.2
  Downloaded scopeguard v1.1.0
  Downloaded time-core v0.1.1
  Downloaded serde_urlencoded v0.7.1
  Downloaded version_check v0.9.4
  Downloaded tokio-macros v1.8.0
  Downloaded hyper-tls v0.5.0
  Downloaded futures-sink v0.3.21
  Downloaded paste v1.0.14
  Downloaded try-lock v0.2.3
  Downloaded pin-project-lite v0.2.9
  Downloaded log v0.4.17
  Downloaded instant v0.1.12
  Downloaded foreign-types-shared v0.1.1
  Downloaded foreign-types v0.3.2
  Downloaded pin-utils v0.1.0
  Downloaded openssl-macros v0.1.0
  Downloaded httpdate v1.0.2
  Downloaded fnv v1.0.7
  Downloaded autocfg v1.1.0
  Downloaded percent-encoding v2.1.0
  Downloaded num_threads v0.1.6
  Downloaded base64 v0.13.0
  Downloaded cassowary v0.3.0
  Downloaded itoa v1.0.3
  Downloaded ipnet v2.5.0
  Downloaded form_urlencoded v1.0.1
  Downloaded rand_core v0.6.3
  Downloaded dirs-sys v0.3.7
  Downloaded quote v1.0.21
  Downloaded unicode-width v0.1.9
  Downloaded hashlink v0.8.1
  Downloaded ppv-lite86 v0.2.16
  Downloaded dirs v4.0.0
  Downloaded lazy_static v1.4.0
  Downloaded indoc v2.0.3
  Downloaded signal-hook-mio v0.2.3
  Downloaded bitflags v1.3.2
  Downloaded adler v1.0.2
  Downloaded mime v0.3.16
  Downloaded ahash v0.7.6
  Downloaded signal-hook-registry v1.4.0
  Downloaded futures-core v0.3.21
  Downloaded tokio-native-tls v0.3.0
  Downloaded once_cell v1.13.0
  Downloaded pkg-config v0.3.25
  Downloaded rand_chacha v0.3.1
  Downloaded futures-channel v0.3.21
  Downloaded fallible-iterator v0.2.0
  Downloaded slab v0.4.7
  Downloaded parking_lot_core v0.8.5
  Downloaded smallvec v1.9.0
  Downloaded unicode-bidi v0.3.8
  Downloaded unicode-ident v1.0.3
  Downloaded futures-task v0.3.21
  Downloaded signal-hook v0.3.14
  Downloaded tinyvec v1.6.0
  Downloaded deranged v0.3.7
  Downloaded ryu v1.0.11
  Downloaded socket2 v0.4.4
  Downloaded parking_lot v0.11.2
  Downloaded parking_lot_core v0.9.3
  Downloaded getrandom v0.2.7
  Downloaded httparse v1.7.1
  Downloaded lock_api v0.4.7
  Downloaded indexmap v1.9.1
  Downloaded native-tls v0.2.10
  Downloaded miniz_oxide v0.5.3
  Downloaded crc32fast v1.3.2
  Downloaded bitflags v2.4.0
  Downloaded proc-macro2 v1.0.43
  Downloaded serde_derive v1.0.142
  Downloaded bytes v1.2.1
  Downloaded serde v1.0.142
  Downloaded tracing-core v0.1.29
  Downloaded url v2.2.2
  Downloaded async-compression v0.3.14
  Downloaded flate2 v1.0.24
  Downloaded cc v1.0.73
  Downloaded mio v0.7.14
  Downloaded tracing v0.1.36
  Downloaded memchr v2.5.0
  Downloaded openssl-sys v0.9.75
  Downloaded mio v0.8.4
  Downloaded rand v0.8.5
  Downloaded tokio-util v0.7.3
  Downloaded http v0.2.8
  Downloaded hashbrown v0.12.3
  Downloaded crossterm v0.26.1
  Downloaded unicode-normalization v0.1.21
  Downloaded time v0.3.25
  Downloaded crossterm v0.20.0
  Downloaded unicode-segmentation v1.10.1
  Downloaded serde_json v1.0.83
  Downloaded reqwest v0.11.11
  Downloaded futures-util v0.3.21
  Downloaded h2 v0.3.13
  Downloaded rusqlite v0.28.0
  Downloaded hyper v0.14.20
  Downloaded ratatui v0.22.0
  Downloaded openssl v0.10.41
  Downloaded vcpkg v0.2.15
  Downloaded idna v0.2.3
  Downloaded syn v1.0.99
  Downloaded tokio v1.20.1
  Downloaded libc v0.2.127
  Downloaded encoding_rs v0.8.31
  Downloaded libsqlite3-sys v0.25.2
  Downloaded 117 crates (13.0 MB) in 12.04s (largest was `libsqlite3-sys` at 4.8 MB)
   Compiling libc v0.2.127
   Compiling cfg-if v1.0.0
   Compiling autocfg v1.1.0
   Compiling proc-macro2 v1.0.43
   Compiling unicode-ident v1.0.3
   Compiling quote v1.0.21
   Compiling syn v1.0.99
   Compiling log v0.4.17
   Compiling once_cell v1.13.0
   Compiling smallvec v1.9.0
   Compiling lock_api v0.4.7
   Compiling cc v1.0.73
   Compiling pkg-config v0.3.25
   Compiling scopeguard v1.1.0
   Compiling getrandom v0.2.7
   Compiling signal-hook-registry v1.4.0
   Compiling parking_lot_core v0.9.3
   Compiling mio v0.8.4
   Compiling version_check v0.9.4
   Compiling ahash v0.7.6
   Compiling pin-project-lite v0.2.9
   Compiling futures-core v0.3.21
   Compiling parking_lot v0.12.1
   Compiling memchr v2.5.0
   Compiling bytes v1.2.1
   Compiling bitflags v1.3.2
   Compiling openssl-sys v0.9.75
   Compiling tokio v1.20.1
   Compiling itoa v1.0.3
   Compiling hashbrown v0.12.3
   Compiling socket2 v0.4.4
   Compiling num_cpus v1.13.1
   Compiling futures-task v0.3.21
   Compiling serde_derive v1.0.142
   Compiling tracing-core v0.1.29
   Compiling slab v0.4.7
   Compiling indexmap v1.9.1
   Compiling fnv v1.0.7
   Compiling serde v1.0.142
   Compiling openssl v0.10.41
   Compiling foreign-types-shared v0.1.1
   Compiling futures-util v0.3.21
   Compiling foreign-types v0.3.2
   Compiling tracing v0.1.36
   Compiling http v0.2.8
   Compiling vcpkg v0.2.15
   Compiling crc32fast v1.3.2
   Compiling native-tls v0.2.10
   Compiling tokio-macros v1.8.0
   Compiling openssl-macros v0.1.0
   Compiling httparse v1.7.1
   Compiling signal-hook v0.3.14
   Compiling pin-utils v0.1.0
   Compiling futures-channel v0.3.21
   Compiling tinyvec_macros v0.1.0
   Compiling futures-sink v0.3.21
   Compiling matches v0.1.9
   Compiling tinyvec v1.6.0
   Compiling libsqlite3-sys v0.25.2
   Compiling adler v1.0.2
   Compiling try-lock v0.2.3
   Compiling ryu v1.0.11
   Compiling openssl-probe v0.1.5
   Compiling percent-encoding v2.1.0
   Compiling serde_json v1.0.83
   Compiling form_urlencoded v1.0.1
   Compiling tokio-util v0.7.3
   Compiling h2 v0.3.13
   Compiling want v0.3.0
   Compiling miniz_oxide v0.5.3
   Compiling unicode-normalization v0.1.21
   Compiling http-body v0.4.5
   Compiling rand_core v0.6.3
   Compiling mio v0.7.14
   Compiling tower-service v0.3.2
   Compiling parking_lot_core v0.8.5
   Compiling unicode-bidi v0.3.8
   Compiling encoding_rs v0.8.31
   Compiling ppv-lite86 v0.2.16
   Compiling httpdate v1.0.2
   Compiling rand_chacha v0.3.1
   Compiling hyper v0.14.20
   Compiling idna v0.2.3
   Compiling signal-hook-mio v0.2.3
   Compiling flate2 v1.0.24
   Compiling tokio-native-tls v0.3.0
   Compiling hashlink v0.8.1
   Compiling dirs-sys v0.3.7
   Compiling instant v0.1.12
   Compiling libmpv-sys v3.1.0 (https://github.com/sudipghimire533/libmpv-rs?rev=18aa79a#18aa79a6)
   Compiling fallible-iterator v0.2.0
   Compiling fallible-streaming-iterator v0.1.9
   Compiling paste v1.0.14
   Compiling lazy_static v1.4.0
   Compiling hyper-tls v0.5.0
   Compiling dirs v4.0.0
   Compiling async-compression v0.3.14
   Compiling url v2.2.2
   Compiling rand v0.8.5
   Compiling serde_urlencoded v0.7.1
   Compiling deranged v0.3.7
   Compiling time-core v0.1.1
   Compiling libmpv v2.0.1 (https://github.com/sudipghimire533/libmpv-rs?rev=18aa79a#18aa79a6)
   Compiling num_threads v0.1.6
   Compiling mime v0.3.16
   Compiling ipnet v2.5.0
   Compiling base64 v0.13.0
   Compiling reqwest v0.11.11
   Compiling time v0.3.25
   Compiling parking_lot v0.11.2
   Compiling crossterm v0.26.1
   Compiling indoc v2.0.3
   Compiling bitflags v2.4.0
   Compiling unicode-segmentation v1.10.1
   Compiling cassowary v0.3.0
   Compiling unicode-width v0.1.9
   Compiling ratatui v0.22.0
   Compiling crossterm v0.20.0
   Compiling rusqlite v0.28.0
   Compiling config v2.0.0-beta (/home/tama/Downloads/ytui-music/config)
   Compiling fetcher v2.0.0-beta (/home/tama/Downloads/ytui-music/fetcher)
   Compiling ytui_music v2.0.0-beta (/home/tama/Downloads/ytui-music/front-end)
warning: use of deprecated struct `ratatui::text::Spans`: Use `ratatui::text::Line` instead
  --> front-end/src/ui/utils.rs:83:26
   |
83 |         let text = text::Spans::from(vec![
   |                          ^^^^^
   |
   = note: `#[warn(deprecated)]` on by default

warning: use of deprecated struct `ratatui::text::Spans`: Use `ratatui::text::Line` instead
  --> front-end/src/ui/mod.rs:19:28
   |
19 |         text::{self, Span, Spans, Text},
   |                            ^^^^^

warning: use of deprecated tuple struct `ratatui::text::Spans`: Use `ratatui::text::Line` instead
  --> front-end/src/ui/mod.rs:19:28
   |
19 |         text::{self, Span, Spans, Text},
   |                            ^^^^^

warning: `ytui_music` (bin "ytui_music") generated 3 warnings
    Finished release [optimized] target(s) in 2m 14s
```



paket berada di dir "/target/release"

```
[tama@tamaoksa release]$ ./ytui_music --shortcuts

__   ___         _                           _
\ \ / / |_ _   _(_)      _ __ ___  _   _ ___(_) ___
 \ V /| __| | | | |_____| '_ ` _ \| | | / __| |/ __|
  | | | |_| |_| | |_____| | | | | | |_| \__ \ | (__ 
  |_|  \__|\__,_|_|     |_| |_| |_|\__,_|___/_|\___|

Author(s): Sudip Ghimire <sudipghimire533@gmail.com>

Usage: ytui_music sub-command <[arguments]>
Possible sub commands:

help:    : Show this help message.
           Arguments: NONE

update:  : Update the ytui-music binary to latest version.
           This will override the current executable so it may require root/admin permission
           depending on current installation path.
           Arguments: NONE

delete:  : Delete configuration/storage file
           Arguments:
           - config: Delete configuation file. This is located in <config-dir>/.ytui-music/config.json.
                Run info config-location for exact location
                On next run you will be asked weather to generate default config.
           - db: Delete the database storage. This will delete your save data like favourates music.

info:    : Get the information about passed argument.
           Arguments:
           - version:   Show version of currently installed ytui-music binary.
           - shortcuts: Show the current shortcut keys with their action.
           - keys:      Same as shortcuts
           - config:    Show information about configuration directory and file
           - ytui:      Show additional information about this software.
           - about:     Same as ytui

run:     : Run ytui-music.
           Arguments: NONE
```


Sekian.