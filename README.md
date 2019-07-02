# Firefox New Tab Override
Modifying the "browser.newtab.url" preference in Firefox was a very simple way to change the page which is shown when opening a new tab.

By removing it in the version 41 of its browser for "security reasons", Mozilla effectively managed to force its users to use shady, sketchy addons. Many of these extensions require a lot of permissions, and will want to have access to your browsing history and/or bookmarks. Many more won't have the functionalities you're looking for, for instance opening a simple HTML file stored on your local disk.

**There's in fact a way to configure the page displayed when opening a new tab, [without any addon](https://support.mozilla.org/en-US/questions/1210576).**

And the result is insanely fast.

## Installation

First, download the files _mozilla.cfg_ and _local-settings.js_ of this repo.
Open _mozilla.cfg_ with your favorite text editor, and edit the line
```
var newTabURL = "file:///home/user/homepage/index.html";
```
to specify what you want to open.

If it is a local file, use ```file:///```.
If it's a webpage, just write the URL as ```https://www...```

### GNU/Linux
1. Locate the folder where the Firefox/Waterfox/Pale Moon executable is installed. Ex: ```/usr/lib/firefox/```
2. Move ```mozilla.cfg``` to ```/usr/lib/firefox/mozilla.cfg```
3. Move ```local-settings.js``` to ```/usr/lib/firefox/defaults/pref/local-settings.js```

### Windows
1. Locate the folder where the Firefox/Waterfox/Pale Moon executable is installed. Ex: ```C:\Program Files\Mozilla Firefox\```
2. Move ```mozilla.cfg``` to ```C:\Program Files\Mozilla Firefox\mozilla.cfg```
3. Move ```local-settings.js``` to ```C:\Program Files\Mozilla Firefox\defaults\pref\local-settings.js```

Restart your browser, open a new tab.
