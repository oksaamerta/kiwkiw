---
layout: post
slug: Setting Screen Timeout i3-wm
---


### XSET Manual

```
[tama@tamaoksa ~]$ xset -h
xset:  unknown option -h

usage:  xset [-display host:dpy] option ...
    To turn bell off:
	-b                b off               b 0
    To set bell volume, pitch and duration:
	 b [vol [pitch [dur]]]          b on
    To disable bug compatibility mode:
	-bc
    To enable bug compatibility mode:
	bc
    To turn keyclick off:
	-c                c off               c 0
    To set keyclick volume:
	 c [0-100]        c on
    To control Display Power Management Signaling (DPMS) features:
	-dpms      DPMS features off
	+dpms      DPMS features on
	 dpms [standby [suspend [off]]]     
	      force standby 
	      force suspend 
	      force off 
	      force on 
	      (also implicitly enables DPMS features) 
	      a timeout value of zero disables the mode 
    To set the font path:
	 fp= path[,path...]
    To restore the default font path:
	 fp default
    To have the server reread font databases:
	 fp rehash
    To remove elements from font path:
	-fp path[,path...]  fp- path[,path...]
    To prepend or append elements to font path:
	+fp path[,path...]  fp+ path[,path...]
    To set LED states off or on:
	-led [1-32]         led off
	 led [1-32]         led on
	-led named 'name'   led off
	 led named 'name'   led on
    To set mouse acceleration and threshold:
	 m [acc_mult[/acc_div] [thr]]    m default
    To set pixel colors:
	 p pixel_value color_name
    To turn auto-repeat off or on:
	-r [keycode]        r off
	 r [keycode]        r on
	 r rate [delay [rate]]
    For screen-saver control:
	 s [timeout [cycle]]  s default    s on
	 s blank              s noblank    s off
	 s expose             s noexpose
	 s activate           s reset
    For status information:  q
    To print version: -version
```



### Print informasi

```
[tama@tamaoksa ~]$ xset -q
Keyboard Control:
  auto repeat:  on    key click percent:  0    LED mask:  00000002
  XKB indicators:
    00: Caps Lock:   off    01: Num Lock:    on     02: Scroll Lock: off
    03: Compose:     off    04: Kana:        off    05: Sleep:       off
    06: Suspend:     off    07: Mute:        off    08: Misc:        off
    09: Mail:        off    10: Charging:    off    11: Shift Lock:  off
    12: Group 2:     off    13: Mouse Keys:  off
  auto repeat delay:  660    repeat rate:  25
  auto repeating keys:  00ffffffdffffbbf
                        fadfffefffedffff
                        9fffffffffffffff
                        fff7ffffffffffff
  bell percent:  50    bell pitch:  400    bell duration:  100
Pointer Control:
  acceleration:  2/1    threshold:  4
Screen Saver:
  prefer blanking:  yes    allow exposures:  yes
  timeout:  600    cycle:  600
Colors:
  default colormap:  0x20    BlackPixel:  0x0    WhitePixel:  0xffffff
Font Path:
  /usr/share/fonts/misc,/usr/share/fonts/TTF,/usr/share/fonts/OTF,/usr/share/fonts/100dpi,/usr/share/fonts/75dpi,built-ins
DPMS (Display Power Management Signaling):
  Standby: 600    Suspend: 600    Off: 600
  DPMS is Enabled
  Monitor is On
```



### Setting sedikit di timeout dan dpms

```
[tama@tamaoksa ~]$ xset s off
[tama@tamaoksa ~]$ xset q
Keyboard Control:
  auto repeat:  on    key click percent:  0    LED mask:  00000002
  XKB indicators:
    00: Caps Lock:   off    01: Num Lock:    on     02: Scroll Lock: off
    03: Compose:     off    04: Kana:        off    05: Sleep:       off
    06: Suspend:     off    07: Mute:        off    08: Misc:        off
    09: Mail:        off    10: Charging:    off    11: Shift Lock:  off
    12: Group 2:     off    13: Mouse Keys:  off
  auto repeat delay:  660    repeat rate:  25
  auto repeating keys:  00ffffffdffffbbf
                        fadfffefffedffff
                        9fffffffffffffff
                        fff7ffffffffffff
  bell percent:  50    bell pitch:  400    bell duration:  100
Pointer Control:
  acceleration:  2/1    threshold:  4
Screen Saver:
  prefer blanking:  no    allow exposures:  yes
  timeout:  0    cycle:  600
Colors:
  default colormap:  0x20    BlackPixel:  0x0    WhitePixel:  0xffffff
Font Path:
  /usr/share/fonts/misc,/usr/share/fonts/TTF,/usr/share/fonts/OTF,/usr/share/fonts/100dpi,/usr/share/fonts/75dpi,built-ins
DPMS (Display Power Management Signaling):
  Standby: 600    Suspend: 600    Off: 600
  DPMS is Disabled
```


screensaver timeout = 0, tinggal setting dikit di ~/.xinitrc

```
xset s off
xset s noblank
xset -dpms
xset dpms force on
```

reboot, done.