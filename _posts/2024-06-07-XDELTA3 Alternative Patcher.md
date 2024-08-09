---
layout: post
slug: XDELTA3 Patch Translate Alternative 
---

>xdelta is a command line program for delta encoding, which generates the difference between two files. This is similar to diff and patch, but it is targeted for binary files and does not generate human readable output. It was first released in 1997

```shell
https://github.com/jmacd/xdelta
```

```
oks4merta@Laptop-Perang:~$ xdelta3 -h
Xdelta version 3.0.11, Copyright (C) 2007, 2008, 2009, 2010, 2011, 2012, 2013, 2014, 2015 Joshua MacDonald
Xdelta comes with ABSOLUTELY NO WARRANTY.
This is free software, and you are welcome to redistribute it
under certain conditions; see "COPYING" for details.
usage: xdelta3 [command/options] [input [output]]
make patch:

  xdelta3.exe -e -s old_file new_file delta_file

apply patch:

  xdelta3.exe -d -s old_file delta_file decoded_new_file

special command names:
    config      prints xdelta3 configuration
    decode      decompress the input
    encode      compress the input
    test        run the builtin tests
special commands for VCDIFF inputs:
    printdelta  print information about the entire delta
    printhdr    print information about the first window
    printhdrs   print information about all windows
    recode      encode with new application/secondary settings
    merge       merge VCDIFF inputs (see below)
merge patches:

  xdelta3 merge -m 1.vcdiff -m 2.vcdiff 3.vcdiff merged.vcdiff

standard options:
   -0 .. -9     compression level
   -c           use stdout
   -d           decompress
   -e           compress
   -f           force (overwrite, ignore trailing garbage)
   -F           force the external-compression subprocess
   -h           show help
   -q           be quiet
   -v           be verbose (max 2)
   -V           show version
memory options:
   -B bytes     source window size
   -W bytes     input window size
   -P size      compression duplicates window
   -I size      instruction buffer size (0 = unlimited)
compression options:
   -s source    source file to copy from (if any)
   -S [lzma|djw|fgk|none] enable/disable secondary compression
   -N           disable small string-matching compression
   -D           disable external decompression (encode/decode)
   -R           disable external recompression (decode)
   -n           disable checksum (encode/decode)
   -C           soft config (encode, undocumented)
   -A [apphead] disable/provide application header (encode)
   -J           disable output (check/compute only)
   -m           arguments for "merge"
the XDELTA environment variable may contain extra args:
   XDELTA="-s source-x.y.tar.gz" \
   tar --use-compress-program=xdelta3 \
       -cf target-x.z.tar.gz.vcdiff target-x.y
```

tinggal di apply pada isoNya, jadi formatNya begini

```
nama_game.bin file_patcher.delta output_file_patcher.bin
```

```
oks4merta@Laptop-Perang:~/Downloads/Suikoden II (USA) (BugFix Patched)/Suikoden II (USA) (BugFix Patched)$ xdelta3 -d -s Suikoden2.bin Suiko2_patch_v10.xdelta Suikoden2_PATCHED.bin
```

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/xdelta2.png" />

sekarang coba aku mainin game yang telah di patch,

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/xdelta3.png" />

saya lebih cocok pake duckstation daripada pakai epsxe, kaena stick xbox bisa terkoneksi dengan normal pada wireless bluetooth.

Sekian