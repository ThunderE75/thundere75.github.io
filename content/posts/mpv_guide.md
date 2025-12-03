+++
title = 'MPV Media Player Guide'
date = '2025-10-02T19:43:38+05:30'
image = "/images/posts/mpv_blog.jpg"
featured = true
tags = ['windows', 'guide', 'FOSS']
description = 'How I customize MPV on Windows with scripts, keybinds, and UI tweaks.'
+++
 This guide demonstrates how i setup my MPV will all the Configs, Scripts & Keybindings. 

 {{< jumpto src="#installing-windows" label="Skip to Installation" >}}

## Why MPV 
Like most people, my first real media player was VLC. It was the go-to recommendation: free, open-source, played almost anything, and worked across platforms. But over time, I started noticing cracks. The biggest issue for me was the UI. It hadn’t really changed since the version I used as a kid, and with Windows 11’s modern design language, it felt increasingly out of place. That alone was manageable until I switched to a laptop with an OLED screen. Suddenly, I was hooked on pure black and dark-mode interfaces, and VLC became an eyesore. I tried to fix it. I searched for a decent dark VLC skin but couldn’t find one. I even installed the beta branch that had a redesigned UI with dark mode support. Unfortunately, it was sluggish and borderline unusable, so I rolled back to the stable release. Then the performance issues started to bother me: slow opening and closing times, occasional jittery playback on high-quality videos, lag when scrubbing through the timeline, and no thumbnail previews. That’s when I finally decided to look for a better player—and that search led me to MPV.

At first, I was disappointed. MPV’s default UI felt primitive, almost too barebones, and I continued my hunt for alternatives. But nothing else stood out. Eventually, I gave up and stuck with what I had. Then, one day while browsing {{< linkicon "https://reddit.com/r/unixporn" "fa-brands fa-reddit" "r/unixporn" >}} I came across someone’s MPV setup. It looked nothing like the plain MPV I had tried before. Curious, I checked out their dotfiles and discovered that MPV was fully configurable through its own config files. Not long after, I stumbled upon {{< linkicon "https://github.com/stax76/awesome-mpv" "fa-brands fa-github" "stax76/awesome-mpv" >}} which is a curated list of scripts, OSC, forks, shaders & other tools build by the community for MPV. I have spent countless hours tweaking scripts, keybinds, and settings, slowly turning MPV into exactly the player I wanted. And I couldn’t be happier without it.

{{< callout type="warning" foldable=true collapsed=true >}}
This was setup on `Windows`, so some changes might be necessary (Like File paths & CLI commands) to make it work on Linux/MacOS. 
{{< /callout >}}

### Amazing mpv forks
MPV itself is great, but the ecosystem around it makes it even more exciting:
- {{< linkicon "https://github.com/iina/iina" "fa-brands fa-github" "IINA" >}}(macOS) - A beautifully designed MPV frontend that feels like a native Mac app.
- {{< linkicon "https://github.com/celluloid-player/celluloid" "fa-brands fa-github" "Celluloid" >}}(Linux) - A clean GTK frontend with all the power of MPV under the hood.
- {{< linkicon "https://github.com/422658476/MPV-EASY-Player" "fa-brands fa-github" "Mpv Easy Player" >}} (Windows) - A mpv fork with clean UI.
- {{< linkicon "https://github.com/mpc-qt/mpc-qt" "fa-brands fa-github" "mpc-qt/MPC-QT" >}}(Windows) - Media Player Classic reimplemented with Qt and libmpv.

## Showcase

{{< img src="../../images/posts/mpv_showcase.png" alt="MPV UI Showcase" caption="MPV customization showcase" >}}

## Script Breakdown

- {{< linkicon "https://github.com/mpv-player/mpv/blob/master/TOOLS/lua/autoload.lua" "fa-brands fa-github" "autoload" >}} - This script automatically loads playlist entries before and after the currently played file. 
- {{< linkicon "https://github.com/davidde/mpv-autosub" "fa-brands fa-github" "autosub" >}} - This script uses Subliminal to download subtitles.
- {{< linkicon "https://github.com/sibwaf/mpv-scripts/blob/master/blackout.lua" "fa-brands fa-github" "blackout" >}} - Turns the screen completely black and pauses on a button press.
- {{< linkicon "https://github.com/zenyd/mpv-scripts/blob/master/delete_file.lua" "fa-brands fa-github" "delete_file" >}} - This script is used to delete files.
- {{< linkicon "https://github.com/tsl0922/mpv-menu-plugin" "fa-brands fa-github" "mpv-menu-plugin" >}} - Configurable context menu for mpv on Windows, with additional support for native file dialog and clipboard.
- {{< linkicon "https://github.com/Samillion/ModernZ/" "fa-brands fa-github" "ModernZ" >}} - A fork of ModernX, with built-in support for interactive menus & better UI customization. 
- {{< linkicon "https://github.com/mpv-player/mpv/blob/master/TOOLS/lua/pause-when-minimize.lua" "fa-brands fa-github" "pause-when-minimize" >}} - This script pauses playback when minimizing the window, and resumes playback.
- {{< linkicon "https://github.com/jonniek/mpv-playlistmanager" "fa-brands fa-github" "playlistmanager" >}} - This script allows you to see and interact with your playlist in an intuitive way.
- {{< linkicon "https://github.com/po5/thumbfast" "fa-brands fa-github" "thumbfast" >}} - High-performance on-the-fly thumbnailer script for mpv.
- {{< linkicon "https://github.com/christoph-heinrich/mpv-pointer-event" "fa-brands fa-github" "mpv-pointer-event" >}} - Mouse/Touch input event detection for mpv.
- {{< linkicon "https://github.com/christoph-heinrich/mpv-touch-gestures" "fa-brands fa-github" "touch-gestures" >}} - Touch gestures for mpv.
- {{< linkicon "https://github.com/occivink/mpv-gallery-view" "fa-brands fa-github" "mpv-gallery-view (Playlist View)" >}} - Playlist grid view.
- {{< linkicon "https://github.com/occivink/mpv-gallery-view" "fa-brands fa-github" "mpv-gallery-view (Contact Sheet)" >}} - Contact sheet view.

## Fonts

### Preferred font for subtitles
- {{< linkicon "https://fonts.google.com/specimen/Space+Grotesk" "fa-brands fa-google" "Google Fonts - Space Grotesk" >}} 
- {{< linkicon "https://fonts.google.com/specimen/Atkinson+Hyperlegible" "fa-brands fa-google" "Google Fonts - Atkinson Hyperlegible" >}}

### OSC Fonts
- {{< linkicon "https://github.com/Samillion/ModernZ/blob/main/material-design-icons.ttf" "fa-brands fa-github" "ModernZ/Material Design Iconic">}} - Material Design Icons used for ModernZ OSC
- {{< linkicon "https://github.com/microsoft/fluentui-system-icons" "fa-brands fa-github" "microsoft/fluentui-system-icons">}} - A modified version by {{< linkicon "https://github.com/Xurdejl" "fa-solid fa-user" "Github/Xurdejl" >}}

## Installing (Windows)

> Prerequisites {{<linkicon "https://mpv.io/installation/" "fa-solid fa-play" "mpv">}}, And optionally: {{<linkicon "https://git-scm.com/" "fa-brands fa-git-alt" "git">}} & {{<linkicon "https://www.python.org/downloads/" "fa-brands fa-python" "python3 (pip)">}}

1. Get the config
   - Clone the repository into `%APPDATA%` folder.

       {{< highlight bat "style=xcode-dark">}}
       git clone https://github.com/ThunderE75/mpv-scripts %APPDATA%\mpv
       {{< /highlight >}}

    - OR {{<linkicon "https://github.com/ThunderE75/mpv-scripts/archive/refs/heads/main.zip" "fa-solid fa-file-zipper" "ThunderE75/mpv > Download ZIP">}} & extract the files into the `%APPDATA%` folder.
    
2. Optional Download {{<linkicon "https://pypi.org/project/subliminal/" "fa-brands fa-python" "pip/Subliminal">}} for {{< linkicon "https://github.com/davidde/mpv-autosub" "fa-brands fa-github" "autosub" >}}

    {{< highlight sh "style=xcode-dark">}}
    pip install subliminal
    {{< /highlight >}}
## Key Bindings

### Miscellaneous Script Keybindings

| Keybinds                                      | Description                            |
| --------------------------------------------- | -------------------------------------- |
| {{< kbd "b" >}}                               | blackout (black screen)                |
| {{< kbd "0" >}} ↔ {{< kbd "9" >}} (on Keypad) | Seek to `num*10%` (YouTube-esque seek) |

### Playlist Management

| Keybinds                                                      | Description                   |
| ------------------------------------------------------------- | ----------------------------- |
| {{< kbd "p" >}}                                               | Peek current playlist         |
| {{< kbd "Ctrl ⌃" >}} + {{< kbd "→" >}}                        | Next File                     |
| {{< kbd "Ctrl ⌃" >}} + {{< kbd "←" >}}                        | Previous File                 |
| {{< kbd "Shift ⇧" >}} + {{< kbd "Enter ⏎" >}}                 | Show playlist manager console |
| {{< kbd "Shift ⇧" >}} + {{< kbd "Alt ⎇" >}} + {{< kbd "s" >}} | Cycle Playlist Sort           |
| {{< kbd "Shift ⇧" >}} + {{< kbd "Alt ⎇" >}} + {{< kbd "h" >}} | Shuffle current playlist      |
| {{< kbd "c" >}}                                               | Open contact sheet            |
| {{< kbd "g" >}}                                               | Open grid playlist view       |

### Subtitle Keybinds

| Keybinds                                                     | Description                 |
| ------------------------------------------------------------ | --------------------------- |
| {{< kbd "v" >}}                                              | Toggle Subtitle             |
| {{< kbd "Ctrl ⌃" >}} + {{< kbd "Alt ⎇" >}} + {{< kbd "s" >}} | Download Subtitles          |
| {{< kbd "j" >}}                                              | Cycle Subtitle              |
| {{< kbd "z" >}}                                              | Reduce subtitle delay (1ms) |
| {{< kbd "Shift ⇧" >}} + {{< kbd "z" >}}                      | Add subtitle delay (1ms)    |

### Bulk Delete Files

> Files will be deleted only upon exit [more info](https://github.com/zenyd/mpv-scripts/tree/master?tab=readme-ov-file#delete-file).

| Keybinds                                                           | Description                                                |
| ------------------------------------------------------------------ | ---------------------------------------------------------- |
| {{< kbd "Shift ⇧" >}} + {{< kbd "Del ⌦" >}}                        | Mark/Unmark file to be deleted                             |
| {{< kbd "Alt ⎇" >}} + {{< kbd "Del ⌦" >}}                          | Show the list of files marked for deletion                 |
| {{< kbd "Ctrl ⌃" >}} + {{< kbd "Shift ⇧" >}} + {{< kbd "Del ⌦" >}} | Clear the list of marked files (files will not be deleted) |

### Common Default Keybinds

| Keybinds                                | Description                         |
| --------------------------------------- | ----------------------------------- |
| {{< kbd "PgUp ⇞" >}} or {{< kbd "@" >}} | Next Chapter                        |
| {{< kbd "PgDn ⇟" >}} or {{< kbd "!" >}} | Previous Chapter                    |
| {{< kbd "a" >}}                         | Cycle Aspect Ratio                  |
| {{< kbd "s" >}}                         | Screenshot View                     |
| {{< kbd "Shift ⇧" >}} + {{< kbd "s" >}} | Screenshot Video (without Subtitle) |

> Reference: {{<linkicon "https://github.com/ThunderE75/mpv-scripts" "fa-brands fa-github" "ThunderE75/mpv">}}