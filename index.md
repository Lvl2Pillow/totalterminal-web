---
layout: product
title: TotalTerminal is a system-wide terminal accessible via a hot-key
product: totalterminal
product_title: TotalTerminal
product_subtitle: a system-wide terminal available on a hot-key
note: If you like TotalTerminal, check out also <a href="http://totalfinder.binaryage.com">TotalFinder</a>.
download: http://downloads.binaryage.com/TotalTerminal-1.2.3.dmg
downloadtitle: Download v1.2.3
downloadsubtitle: Requires OS X 10.6 or higher
repo: http://github.com/binaryage/totalterminal
meta_title: TotalTerminal is a system-wide terminal accessible via a hot-key
meta_keywords: totalterminal,terminal,osx,simbl,binaryage,productivity,software,visor
meta_description: TotalTerminal is a plugin for Terminal.app which provides Quake-style terminal window available on keyboard shortcut
meta_image: http://www.binaryage.com/shared/img/icons/totalterminal-256.png
facebook: 1
retweet: 1
buzz: 1
fbsdk: 1
#flattr: http://totalterminal.binaryage.com
ogmeta: {
    site_name: "BinaryAge website",
    description: "TotalTerminal is a system-wide terminal for OS X available on a hot-key",
    email: "support@binaryage.com",
    type: "product",
    title: "TotalTerminal",
    url: "http://totalterminal.binaryage.com",
    image: "http://www.binaryage.com/shared/img/icons/totalterminal-256.png"
}
shots: [{
    title: "TotalTerminal's Visor window with nice colors!",
    thumb: "/shared/img/totalterminal-mainshot.png",
    full: "/shared/img/totalterminal-mainshot-full.png"
}]
---

## Installation

TotalTerminal is a plugin for Terminal.app. It provides persistent Visor Window which slides down when you press a hot-key. Remember Quake Console?

  1. Run installer
  2. Configure your keyboard trigger by selecting the `Preferences...` -> `TotalTerminal` and edit your keyboard hot-key. By default it is `CTRL+~`

Then you can trigger Visor Window with your hot-key from any application to get an instant terminal session.

To hide Visor Window, you can either:

  * re-trigger with your key-combo
  * optionally, you can click off the TotalTerminal window
  
---
  
<span style="color: #a00">For original Visor 2.2 users: TotalTerminal plugin is not injected into Terminal.app automatically like with SIMBL. You have to launch TotalTerminal.app to inject the plugin into Terminal.app. You might want to put TotalTerminal.app into Startup Items.</span>

## FAQ

#### What is the difference between Visor.bundle and TotalTerminal.app?
> TotalTerminal supersedes Visor. Visor.bundle is a SIMBL plugin which was originally written by Nicholas Jitkoff from [Blacktree](http://blacktree.com). Original Visor was introduced for OS X - Tiger. I have been developing it since Leopard. I decided to rename it to TotalTerminal with OS X Lion release. TotalTerminal has installer, Sparkle updater and does not depend on [SIMBL](http://www.culater.net/software/SIMBL/SIMBL.php). In the future it will get more bug fixes and hopefully some new features.
> 
> The main technical difference is that TotalTerminal is not launched automatically. You have to launch TotalTerminal.app to inject plugin into Terminal.app (if it is not running the launcher will launch it)

#### Why did you rename it?
> There are several reasons. First, Visor Window is also a feature of [TotalFinder](http://totalfinder.binaryage.com), my other application plugin. This was causing confusion. Second, TotalFinder and TotalTerminal make up nicer branding. It is immediately obvious they are related and TotalTerminal has something to do with Terminal.app. Also searching for TotalTerminal through social media is easier for me. Visor is a general term.

#### Do I need to uninstall Visor.bundle prior TotalTerminal installation?
> Not necessary. TotalTerminal installer will remove it automatically. Visor and TotalTerminal conflict so you cannot have them running both.

#### Does TotalTerminal work on OS X 10.8 (Mountain Lion)?
> Yes, since 1.2.

#### Does TotalTerminal work on OS X 10.7 (Lion)?
> Yes, since 1.0.

#### Does TotalTerminal work on OS X 10.6 (Snow Leopard)?
> Yes, since 1.0.

#### Does TotalTerminal work on OS X 10.5 (Leopard)?
> It should work, but I no longer support Leopard.

#### Does TotalTerminal work on OS X 10.4 (Tiger)?
> Tiger was supported by early Visor (pre 1.5).

#### How do I uninstall TotalTerminal?
> You may use Status Menu Icon and select `Uninstall TotalTerminal`. Alternatively you may [download TotalTerminal DMG](#changelog) again and use `TotalTerminal Uninstaller` which is present there.

#### I see two Terminal.app icons in the Dock. How should I get rid of it?

> This affects people who pin TotalTerminal.app icon in the Dock as a permanent icon.
>
>When you click TotalTerminal.app icon in the Dock, the system launches TotalTerminal.app. But [TotalTerminal.app is just a lightweight launcher](https://github.com/binaryage/totalterminal-installer/tree/master/TotalTerminal.app) which:
>  
>  1. launches Terminal.app (if it is not running) 
>  2. injects TotalTerminal plugin into it.
>  3. quits
>
>You end up with two Terminal icons in the Dock: one for running Terminal.app and second for pinned TotalTerminal.app (which is not running anymore after injecting the plugin).
>
>You can hide an app from the Dock but not dynamically. You have to tweak its Info.plist and set LSUIElement to true. TotalTerminal will never modify your Terminal.app files so it cannot force running Terminal to hide icon in the Dock. On the other hand it cannot hide its own icon from the Dock, because it is not running and you have pinned it explicitly, which is not affected by LSUIElement set on TotalTerminal.app.
>
>I would recommend you to use some other means of launching TotalTerminal.app for example via Spotlight or some launcher like Alfred.app, or put it into Startup Items. Maybe I will come up with some better solution in the future. Any ideas?
>
>Other option is to `open /Applications/Utilities/Terminal.app/Contents/Info.plist` and add LSUIElement entry and set it to true (in Property List Editor is displays as "Application is agent (UIElement)").

#### Where are TotalTerminal settings stored?
> TotalTerminal settings are stored with Terminal.app settings. You can `open ~/Library/Preferences/com.apple.Terminal.plist` and tweak the values (better to do this when Terminal.app is not running). 
If you have troubles with TotalTerminal settings, delete this file and restart Terminal.app. The file will be recreated with default values.

#### How can I open a new terminal window the old way, as a classic OSX window?
> If there is a Visor Window (the status menu icon is active) every new terminal window will be opened as a classic OS X window. In other words, open at least two terminal windows. The second one will be a classic terminal window for sure.

#### How can I change the height of Visor?
> Go to Terminal.app's Preferences -> Window -> Rows

#### How can I stick Visor to left screen edge?
> Look for the "Position" option in TotalTerminal Preferences and pick "Left-Stretch" window placement.

#### How can I change the width of Visor?
> By default Visor Window stretches to the full screen width. Set some non-stretching positioning for Visor Window in TotalTerminal Preferences, then Go to Terminal.app's Preferences -> Window -> Columns.

#### Is it possible to show Visor only on a secondary monitor?
> Go to TotalTerminal Preferences -> Screen

#### Is it possible to see Visor on every Space?
> TotalTerminal forces Visor window to be visible on every space. You may disable this in TotalTerminal Preferences. Note: Spaces configuration for Terminal.app doesn't apply to the Visor Window, it is effective only for other (classic) terminal windows.

#### I want to keep different preferences for Visor and other (classic) terminal windows. What is the best way manage this?
> There may be a profile in Terminal.app called "Visor". Visor Window attempts to use the "Visor" profile when opening new tabs in Visor Window (regardless of "default profile" or "startup profile" settings in Terminal.app). In case "Visor" profile is not present, it uses currently selected default profile.

#### Do I need to install TerminalColours SIMBL with TotalTerminal?
> No, TerminalColours is integrated into TotalTerminal 1.0 and later. Actually it conflicts with TotalTerminal if installed as SIMBL plugin.

#### Do I need to install CopyOnSelect SIMBL with TotalTerminal?
> No, CopyOnSelect is integrated into TotalTerminal 1.0 and later. It is a configurable option in TotalTerminal Preferences (disabled by default).

## Changelog

<div class="changelogx"></div>

<script type="text/javascript" charset="utf-8">
    $(function() {
        $('.changelogx').load('changelog-beta.html?x='+((Math.random()+"").substring(2))+' #page');
    });
    
    function showBetaHint() {
        $('.betahint').toggle();
    }
</script>

## Links

#### Source code
  * [sources are hosted on GitHub](http://github.com/binaryage/totalterminal)

#### The original TotalTerminal called "Visor" was brought to you by Alcor ([Blacktree](http://blacktree.com)), kudos man!

**[Where can I get older versions?](http://visor.binaryage.com)**

## Special Guest

### Ben Stiglitz about Terminal.app

<div>Ben is the author of Terminal.app. Kudos!</div>
<embed src='http://rubyconf2008.confreaks.com/player.swf' height='260' width='640' allowscriptaccess='always' allowfullscreen='true' flashvars='file=http%3A%2F%2Frubyconf2008.confreaks.com%2Fvideos%2Fterminalapp-small.mp4&image=images%2Fterminalapp-preview.jpg&plugins=viral-1'/>

[darwin]: http://github.com/darwin
[torsten]: http://github.com/torsten
[pumpkin]: http://github.com/pumpkin
[blinks]: http://github.com/blinks
[cglee]: http://github.com/cglee
[kleinman]: http://github.com/kleinman
[genki]: http://github.com/genki
[ciaran]: http://github.com/ciaran
[evanphx]: http://github.com/evanphx
[contribute]: http://github.com/binaryage/totalterminal