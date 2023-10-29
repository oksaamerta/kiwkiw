---
layout: post
slug: Youtube Play In The Background With Yewtube
---


sumber : 
url: https://github.com/mps-youtube/yewtube

>yewtube, forked from mps-youtube , is a Terminal based YouTube player and downloader. No Youtube API key required.


ARCH LINUX intallasi :

```
[tama@tamaoksa ~]$ yay yewtube
```

pilih paket sesuai nomor, done.


<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/yewtube1.png" />





DEBIAN BASED DISTRO installasi :

```
tama@tamagochi:~$ sudo apt install python3-pip

```

```
tama@tamagochi:~$ pip install git+https://github.com/iamtalhaasghar/yewtube.git
```

atau bisa pake pipx

```
tama@tamagochi:~$ pipx install git+https://github.com/iamtalhaasghar/yewtube.git
```

```
tama@tamagochi:~$ yt --help


    Basic Usage

    Use / or . to prefix your search query.  e.g., /pink floyd

    Then, when results are shown:

        <number(s)> - play specified items, separated by commas.
                      e.g., 1-3,5 plays items 1, 2, 3 and 5.

        i <number> - view information on video <number>
        c <number> - view comments for video <number>
        d <number> - download video <number>
        r <number> - show videos related to video <number>
        u <number> - show videos uploaded by uploader of video <number>
        x <number> - copy item <number> url to clipboard. (See the note below)
        Note: This feature requires `pyperclip` which is installed automatically when you install yewtube but
        Linux users further need to install `xsel` or `xclip` manually using apt, dnf, pacman, zypper or whatever package manager you use.
        Visit https://pyperclip.readthedocs.io/en/latest/index.html#not-implemented-error for more info.

        q, quit - exit yewtube
    

    Searching and Retrieving

    set search_music false - search all YouTube categories.
    set search_music true  - search only YouTube music category.

    /<query> or .<query> to search for videos. e.g., /daft punk
    Search Arguments:
    -d, --duration    Can be any/short/medium/long
    -a, --after       Date in YYYY-MM-DD or YYYY-MM-DDTHH:MM format
    -l, --live        Limit search to livestreams
    -c, --category    Search within a category, (number or string)
                      Available categories:
                      film, autos, music, sports, travel, gaming, blogging, news

    //<query> or ..<query> - search for YouTube playlists. e.g.,     //80's music
    n and p - continue search to next/previous pages.
    p <number> - switch to page <number>.

    album <album title> - Search for matching tracks using album title
    channels <Channel name> - Search for channels by channelname
    live <category> - Search for livestreams from a range of categories.
    Categories: film, autos, music, sports, travel, gaming, blogging, news

    mkp <fullfilepath> - Creates a playlist automatically with video titles from fullfilepath
    <fullfilepath>: Full path of text file with one title per line

    mkp -d <search result number> - Create a playlist based on tracks
    listed in that videos description. (Alternatively one can use --description)

    user <username> - list YouTube uploads by <username>.
    user <username>/<query> - as above, but matches <query>.
    userpl <username> - list YouTube playlists created by <username>.
    pl <url or id> - Open YouTube playlist by url or id.
    url <url or id> - Retrieve specific YouTube video by url or id.
    url <url> <url> ... <url> - Retrieve specific YouTube videos by url or id.
    url_file <file_absolute_path> - Retrieve YouTube videos by url or id from a .txt file.
    File format : .txt, with one url or id by line.

    r <number> - show videos related to video <number>.
    u <number> - show videos uploaded by uploader of video <number>.
    c <number> - view comments for video <number>
    

    Editing and Manipulating Results

    rm <number(s)> - remove items from displayed results.
    sw <number>,<number> - swap two items.
    mv <number>,<number> - move item <number> to position <number>.
    save <name> - save displayed items as a local playlist.
    mix <number> - show YouTube mix playlist from item in results.

    shuffle - Shuffle the displayed results.
    shuffle all - Shuffle entire loaded playlist.
    reverse or reverse <number>-<number> - Reverse the displayed items or item range.
    reverse all - Reverse order of entire loaded playlist.
    

    Downloading and Playback

    set show_video true - play video instead of audio.

    <number(s)> - play specified items, separated by commas.
                  e.g., 1-3,5 plays items 1, 2, 3 and 5

    d <number> - view downloads available for an item.
    da <number(s)> - download best available audio file(s).
    dv <number(s)> - download best available video file(s).
    dapl <url or id> - download YouTube playlist (audio) by url or id.
    dvpl <url or id> - download YouTube playlist (video) by url or id.
    daupl <username> - download user's YouTube playlists (audio).
    dvupl <username> - download user's YouTube playlists (video).
    dlurl <url or id> - download a YouTube video by url or video id.
    daurl <url or id> - download best available audio of YouTube video by url or video id.
    playurl <url or id> - play a YouTube video by url or id.
    browserplay <number> - open a specified previous search in browser.

    all or * - play all displayed items.
    repeat <number(s)> - play and repeat the specified items.
    shuffle <number(s)> - play specified items in random order.
    

    Download Using A Custom Application

    Use set download_command <command> to specify a custom command to use for
    downloading.

    mps-youtube will make the following substitutions:

    %u - url of the remote file to download
    %d - download directory as set in DDIR in mps-youtube config
    %f - filename (determined by title and filetype)
    %F - full file path (%d/%f)
    %i - youtube video id

    for example, to download using aria2c (http://aria2.sourceforge.net), enter:

        set download_command aria2c --dir=%d --out=%f %u

    Note that using a custom download command does not support transcoding the
    downloaded file to another format using mps-youtube.
    

    Encoding to MP3 and other formats

    Enter encoders to view available encoding presets
    Enter set encoder <number> to apply an encoding preset for downloads

    This feature requires that ffmpeg or avconv is installed on your system and is
    available in the system path.

    The encoding presets can be modified by editing the text config file which
    resides at:
       /home/tama/.config/mps-youtube/transcode
    

    Using Local Playlists

    add <number(s)> - add items to the current playlist.
    add <number(s)> <playlist> - add items to the specified playlist.
         (<playlist> will be created if it doesn't already exist)

    vp - view current playlist.
    ls - list saved playlists.
    mv <old name or ID> <new name> - rename a playlist.
    rmp <playlist_name or ID> - delete a playlist from disk.

    open <name or ID> - open a saved playlist as the current playlist.
    play <name or ID> - play a saved playlist directly.
    view <name or ID> - view a playlist (current playlist left intact).
    save or save <name> - save the displayed items as a playlist.

    rm <number(s)> - remove items from displayed results.
    sw <number>,<number> - swap two items.
    mv <number>,<number> - move item <number> to position <number>.
    

    Accessing Local History

    Access songs that have been played within yewtube

        history - displays a list of songs contained in history
        history clear - clears the song history
        history recent - displays a list of recent played songs
        set history on|off - toggles history recording
    

    Invocation

    All yewtube commands can be entered from the command line.  For example;

      yt dlurl <url or id> to download a YouTube video by url or id
      yt playurl <url or id> to play a YouTube video by url or id
      yt /mozart to search
      yt //best songs of 2010 for a playlist search
      yt play <playlist name or ID> to play a saved playlist
      yt ls to list saved playlists

    For further automation, a series of commands can be entered separated by
    commas (,).  E.g.,

      yt open 1, 2-4 - play items 2-4 of first saved playlist
      yt //the doors, 1, all -a - open YouTube playlist and play audio

    If you need to enter an actual comma on the command line, use ,, instead.
    

    Configuration

    set - view current configuration
    set <item> default - set an item to its default value
    set all default - restore default settings
    set checkupdate true|false - check for updates on exit
    set columns <columns> - select extra displayed fields in search results:
         (valid: views comments rating date time user likes dislikes category ytid)
    set ddir <download direcory> - set where downloads are saved
    set download_command <command> - type help dl-command for info
    set encoder <number> - set encoding preset for downloaded files
    set fullscreen true|false - output video content in full-screen mode
    set always_repeat true|false - always in repeat mode without repeat <number>
    set max_res <number> - play / download maximum video resolution height
    set notifier <notifier app> - call <notifier app> with each new song title
    set order <relevance|date|views|rating> search result ordering
    set user_order <<nothing>|relevance|date|views|rating> user upload list
        result ordering, leave blank for the same as order setting
    set overwrite true|false - overwrite existing files (skip if false)
    set player <player app> - use <player app> for playback
    set playerargs <args> - use specified arguments with player
    set lookup_metadata true|false - lookup metadata using Last.fm
    set lastfm_username <username> - scrobble to this Last.fm userprofile
    set lastfm_password <password> - Last.fm password (saved in hash form)
    set lastfm_api <key> - API key needed for Last.fm mps-yt authorization
    set lastfm_secret <key> - secret for the Last.fm API key
    set search_music true|false - search only music (all categories if false)
    set show_mplayer_keys true|false - show keyboard help for mplayer and mpv
    set show_status true|false - show status messages and progress
    set show_video true|false - show video output (audio only if false)
    set window_pos <top|bottom>-<left|right> - set player window position
    set window_size <number>x<number> - set player window width & height
    set audio_format <auto|m4a|webm> - set default music audio format
    set video_format <auto|mp4|webm|3gp> - set default music video format
    set set_title true|false - change window title
    set show_qrcode true|false - show qrcode of the URL in the video information panel
    set history true|false - record play history
    set input_history true|false - record command input history
    set vlc_dummy_interface true|false - whether to hide VLC GUI or not (hides when true)

    Additionally, set -t may be used to temporarily change a setting without
    saving it to disk
    

    Configure Last.fm

    pylast needs to be installed for Last.fm support. See https://github.com/pylast/pylast.

    Use set to set your Last.fm login credenditals, e.g. set lastfm_username jane_doe.
    Similarly, you also have to provide an API key and it's corresponding secret.
    An API key can be retrieved from https://www.last.fm/api/account/create.

    Your Last.fm configuration is saved and automatically reloaded when mps-youtube starts.

    After having set the required information, a connection can also be established
    with lastfm_connect. Additionally, lastfm_connect provides verbose error messages.

    For now, Last.fm support only works with the album command.
    

    Advanced Tips

    Use -w, -f or -a with your choice to override the configured     setting and
    play items in windowed, fullscreen or audio modes.  E.g., 1-4 -a

    When specifying columns with set columns command, append :N to set     width.
        E.g.: set columns date views user:17 likes

    When using open, view or play to access a local playlist,     you can enter
    the first few characters instead of the whole name.

    Use 5- to select items 5 upward and -5 to select up to item 5.     This can be
    included with other choices. e.g., 5,3,7-,-2
    You can use spaces instead of commas: 5 3 7- -2
    Reversed ranges also work. eg., 5-2

    dump - to show entire contents of an opened YouTube playlist.
           (useful for playing or saving entire playlists, use undump to     undo)

    set player mpv or set player mplayer - change player application

    Use 1 and 0 in place of true and false when using the set     command

    Use clearcache command to clear the cache.
    
What's New
get_changelog()
Changelog
get_changelog_local()
Tor Status
check_tor()
```

setting player

```
set player vlc (atau pake player sesukamu)
```

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/yewtube2.png" />



sekian.