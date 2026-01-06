+++
title = 'Youtube ReVanced guide'
date = '2025-12-29T20:12:00+05:30'
image = "/images/posts/revanced/og_revanced.jpg"
featured = true
tags = ['android', 'guide', 'FOSS']
description = 'This guide walks you through the complete process of patching YouTube ReVanced directly on an Android phone using ReVanced Manager.'
+++
This guide walks you through the complete process of patching YouTube ReVanced directly on an Android phone using ReVanced Manager. It also explains all the important settings and configuration options that should be reviewed or modified to ensure optimal functionality.

{{< jumpto src="#instructions" label="Skip to Instructions" >}}

{{< callout type="warning" title="Disclaimer" foldable=false >}}
Avoid installing untrusted APKs from unknown sources. That’s why this post does not provide a precompiled APK. Please compile it yourself and share it with your friends.
{{< /callout >}}

{{< callout type="note" foldable=true collapsed=true >}}
Although ReVanced is a general-purpose tool capable of patching many applications, this guide is specifically focused on using ReVanced Manager to patch YouTube.
{{< /callout >}}

## Support your creators

- Buy their merchandise, subscribe to their Patreon, or join their membership programs.
- Purchasing even a single piece of merchandise often supports them more financially than watching all their videos with ads.
- And there are many other ways to directly support their work.

## Instructions

1. Download & Install both {{< linkicon "https://github.com/ReVanced/revanced-manager/releases/latest/" "fa-brands fa-github" "Revance Manager">}} & {{< linkicon "https://github.com/ReVanced/GmsCore/releases/latest/" "fa-brands fa-github" "ReVanced MicroG">}}
2. Open ReVanced Manager > Patcher > `Select an APP` (i prefer APK Mirror)
3. Search app via suggested version & then download the APK (do not install).

{{< img src="../../images/posts/revanced/revanced-1.webp" alt="ReVanced Manager Image 1" caption="ReVanced Manager - Select Application" >}}


4. Select Patches > Default ( List of {{< linkicon "https://revanced.app/patches?pkg=com.google.android.youtube" "fa-solid fa-globe" "all patches">}} )
5. Click on `Patch` button 
6. Save APP to storage & install it!

{{< img src="../../images/posts/revanced/revanced-2.webp" alt="ReVanced Manager Image 1" caption="ReVanced Manager - Patch Application" >}}

## Login Instructions

1. Open ReVanced MicroG
2. Login With your google account

{{< img src="../../images/posts/revanced/revanced-3.webp" alt="ReVanced Manager Image 1" caption="MicroG - Add Google Account" >}}

{{< callout type="info" >}}
This step is necessary to login to YouTube ReVanced
{{< /callout >}}

### Recommended

1. Disable the original Youtube App
2. Allow YouTube ReVanced to Open links

{{< img src="../../images/posts/revanced/revanced-4.webp" alt="ReVanced Manager Image 1" caption="Youtube ReVanced - Open by Default" >}}

## Modify ReVanced Settings 

> Profile > Settings > ReVanced Settings

{{< img src="../../images/posts/revanced/revanced-5.webp" alt="ReVanced Manager Image 5" caption="Youtube ReVanced - Navigate to ReVanced Settings" >}}

Recommended settings that needs to be changes 

- ReVanced Settings > SponsorBlock
- ReVanced Settings > Shorts
- ReVanced Settings > Seekbar

{{< img src="../../images/posts/revanced/revanced-6.webp" alt="ReVanced Manager Image 6" caption="Youtube ReVanced - My settings" >}}

## Features of ReVanced 

- SponsorBlock: Skip in-video sponsor segments. 
- Block ADs completely (Banner, Fullscreen, between shorts, etc)
- Disable Shorts completely / make them non intrusive.
- Make shorts autoscroll.
- Restore original seeker behavior.
- Hide UI elements like the `create` button.
- and many more... 

## Useful Links
- ReVanced Website: https://revanced.app/
- ReVanced Github Repository: {{< linkicon "https://github.com/ReVanced/revanced-manager" "fa-brands fa-github" "ReVanced/revanced-manager">}}
- Official Documentation by ReVanced: {{< linkicon "https://github.com/ReVanced/revanced-manager/tree/main/docs" "fa-brands fa-github" "Docs">}}  
- Documentation for Troubleshooting: {{< linkicon "https://github.com/ReVanced/revanced-manager/blob/main/docs/3_troubleshooting.md" "fa-brands fa-github" "Docs/Troubleshooting">}}  
- List of {{< linkicon "https://revanced.app/patches?pkg=com.google.android.youtube" "fa-solid fa-globe" "all patches">}}