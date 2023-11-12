---
layout: post
slug: YTFZF Untuk Streaming Youtube 
---

>A POSIX script that helps you find Youtube videos (without API) and opens/downloads them using mpv/youtube-dl

```shell
https://github.com/pystardust/ytfzf
```

```
[tama@tamagochi ~]$ ytfzf --help
Usage: ytfzf [OPTIONS...] <search-query>
    The search-query can also be read from stdin
    GENERAL OPTIONS:
        -h                      Show this help text

        --version                Get the current version

        --version-all            Get the current version of ytfzf,
                                    and required dependencies

    UTILITY OPTIONS:
        --channel-link=<link>    Gets the uuid of a youtube channel from a link.

    PLAYING OPTIONS:
        -d                      Download the selected video(s)

        -m                      Only play audio

        -f                      Select a video format before playing

        --format-selection=<type>
                                Type can either be normal, or simple
        --format-sort=<sort>    The sort used in ytdl for -f.

        --video-pref=<pref>     The ytdl video preference.

        --audio-pref=<pref>     The ytdl audio preference.

        --ytdl-pref=<pref>      The combined ytdl video and audio preference.

        -u <url handler>        The program to use for handling urls
                                    (deafult: multimedia_player)
        -L                      Show the link of selected video(s)

        -I <info>               Instead of playing the selected video(s),
                                    get information about them.
                                    Options can be separated with a comma,
                                      eg: L,R
                                    Options for info:
                                      L:         print the link of the video
                                      VJ:        print the json of the video
                                      J:         print the json of all videos
                                                 shown in the search
                                      R:         print the data
                                                 of the selected videos,
                                                 as appears in the menu
                                      F:         print the selected video format
        --info-wait              When -I or -L is used,
                                 wait for user input before continuing

        --info-action=<action>   
                                 The action to do when --info-wait is 1.
                                 action can be one of
                                      q: exit
                                      Q: exit (bypass -l)
                                      '': play video

        --detach                 Detach the url handler from the terminal

        --notify-playing         Sends a notification when a video is selected.

        --url-handler-opts=<opts>
                                 Pass the given opts to the url handler.

        --ytdl-opts=<opts>       Pass the opts to ytdl when downloading

        --ytdl-path=<path>       The path to youtube-dl

    MENU OPTIONS:
        -l                      Reopen the menu when the video stops playing

        -t                      Show thumbnails

        -T <viewer>             The program to use for displaying thumbnails.
                                    see ytfzf(1) for a list of viewers.

        --async-thumbnails      Download thumbnails asynchronously.

        --skip-thumb-download   Skips the process of downloading thumbnails

        --thumbnail-quality=<quality>
                                Select quality of thumbnails,
                                can be:
                                    maxres
                                    maxresdefault
                                    sddefault
                                    high (default)
                                    medium
                                    default
                                    start
                                    middle
                                    end

        -i <interface>          The interface to use (default: text)

        -D                      Alias for -i ext

        -a                      Automatically select the first video

        -r                      Automatically select a random video

        -A                      Select all videos

        -S <sed address>        Automatically selects a specific video
                                    based on a given sed address

        -n <video count>        The amount of videos to select with -a and -r

        --preview-side=<side>   The side to show the preview on in fzf:
                                    left
                                    right
                                    up
                                    down
        --fancy-subs             Adds a divider between each subscription
                                 when scraping subscriptions

        --sort                   Sorts video results by a sort name,
                                    The default sort name is upload-date
                                    To change sort names use --sort=<name>

        --sort-name=<name>       Load a different sorting algorithm for --sort
                                    To see usable sort-names, use --list-addons

        --disable-submenus       Whether or not to disable submenus,
                                 which are menus for results like:
                                    playlists and channels

        --disable-back           Disables the back button in submenus

        --disable-actions        Disables actions such as submenus, and the back button.

        --keep-vars              Options passed to ytfzf are kept in submenus.

        --submenu-opts=<opts>    ytfzf options to pass to submenus.

    SEARCH OPTIONS:
        -s                      After closing fzf make another search

        -q                      Use a search query from search history
                                see ytfzf(1) for more info.

        --search-source=<source>
                                The place to get the search from
                                see ytfzf(1) for more information

        --multi-search          Allow multiple searches seperated by ,

        --pages                 The amount of pages to scrape
                                    does not work with some scrapers.
        --pages-start=<page>    The page number to start on

        --odysee-video-count    The amount of videos to scrape from odysee

        --nsfw                  Enable nsfw videos (odysee only)

        --sort-by=<sort>        Searches for videos sorted by:
                                    relevance
                                    rating (youtube only)
                                    upload_date
                                    oldest_first (odysee only)
                                    view_count (youtube only)

        --upload-date=<time>    Searches for videos that were uploaded:
                                    hour
                                    today
                                    week
                                    month
                                    year

        --video-duration=<time> Searches for videos that are:
                                    short
                                    medium
                                    long

        --type=<type>           Searches for uploads of type:
                                    video
                                    playlist
                                    channel
                                    all

        --features=<features>   Searches for videos with features:
                                    hd
                                    subtitles
                                    creative_commons
                                    3d
                                    live
                                    4k
                                    360
                                    location
                                    hdr

        --region=<country-code> The region to search.

        -c <scraper>            The scraper to use,
                                    See ytfzf(1) for a list of builtin scrapers
                                    you can use multiple scrapers
                                    by separating each with a comma, eg:
                                        youtube,odysee

        --scrape+=<scraper>     Use another scraper

        --scrape-=<scraper>     Dont use a scraper.

        -H                      alias for -c H

        --ii=<instance>         The invidious instance to use for scraping.

        --force-youtube         Converts invidious links to youtube links
                                before playing (enabled by default)

        --force-invidious       Uses the chosen invidious instance
                                instead of converting to a youtube link

    ADDON OPTIONS:
        -e <extention>          Load an extention

        --list-addons            Show available addons

    MISC OPTIONS:
        -x                       Clear search and watch history

        --history-clear=<type>   Clear either search, or watch  history.

        --max-threads=<count>    The amount of threads that should be spawned
                                 at any given time.

        --single-threaded        Same as --max-threads=1

        --rii                   Refreseh invidious instance cache

        --available-inv-instances
                                Shows the invidious instances
                                that ytfzf may pick from

        --keep-cache            Do not delete the cache files.

        --thumbnail-log         Write thumbnail errors to this file.
```


contoh

```
[tama@tamagochi ~]$ ytfzf -f -t droomp
```

<img src="https://raw.githubusercontent.com/oksaamerta/oksaamerta.github.io/master/_screenshots/YTFZF.png" />

Sekian