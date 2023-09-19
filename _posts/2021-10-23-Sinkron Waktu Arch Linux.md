---
layout: post
slug: Sinkron Waktu Arch Linux
---

#### Sinkron Waktu Arch Linux

Edit file "/etc/systemd/timesyncd.conf", edit pake editor apapun itu, hilangkan tanda pagar di baris "NTP"

```
=====================================================

[Time]
NTP=
#FallbackNTP=0.arch.pool.ntp.org 1.arch.pool.ntp.org 2.arch.pool.ntp.org 3.arch>
#RootDistanceMaxSec=5
#PollIntervalMinSec=32
#PollIntervalMaxSec=2048

======================================================
```

Ketikan perintah dibawah

```
~: timedatectl set-timezone Asia/Jakarta
```


Done.
