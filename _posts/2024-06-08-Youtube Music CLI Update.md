---
layout: post
slug: YT Music CLI Update 
---

>yewtube, forked from mps-youtube , is a Terminal based YouTube player and downloader. No Youtube API key required.

```shell
https://github.com/mps-youtube/yewtube
```

```
oks4merta@Laptop-Perang:~$ sudo apt install yewtube
```

seperti yang lama tetap memakai yewtube, namun player tidak memakai vlc, karena ada popoutNya ketika streaming music lewat CLI,
untuk yang versi update, saya menggunakan "mpv"

```
oks4merta@Laptop-Perang:~$ sudo apt install mpv
```

konfigurasi

```
oks4merta@Laptop-Perang:~$ yt h config
```

```
oks4merta@Laptop-Perang:~$ yt set player mpv
```

```
oks4merta@Laptop-Perang:~$ yt set playerargs mpv --no-video
```

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/yewtubexmpv.png" />

Sekian