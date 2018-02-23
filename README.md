# Configs

## Config for chrome [Redirector](https://chrome.google.com/webstore/detail/redirector/pajiegeliagebegjdhebejdlknciafen?hl=en-US)

### Reddit sort every thread by top comments
From: ``
^(.*?):\/\/(.*?)\.reddit\.com\/(.*)\/comments/(.*)/(.*)
``

To: ``
$1://$2.reddit.com/$3/comments/$4/?sort=top
``
## Config for ffmpeg

### Windows (.bat) convert all flac in curr directory to mp3
``for %%f IN (*.flac) DO "ffmpeg.exe" -i "%%~nf.flac" -ab 320k -map_metadata 0 -id3v2_version 3 "%%~nf.mp3"
``
