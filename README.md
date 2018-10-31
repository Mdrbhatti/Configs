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

### Windows (.bat) convert all .flac to .mp3
``for %%f IN (*.flac) DO "ffmpeg.exe" -i "%%~nf.flac" -ab 320k -map_metadata 0 -id3v2_version 3 "%%~nf.mp3"
``
### Windows (.bat) shorten specific .mp3
``for %%f IN (*.mp3) DO "ffmpeg.exe" -i "%%~nf.mp3" -ss 385 -t 275 -acodec copy "%%~nf.mp3"``

### Windows (.bat) 1080p raw video to 480p downscale best quality
``for %%f IN (*.mp4) DO "ffmpeg.exe" -i "%%~nf.mp4" -s hd480 -c:v libx264 -r 24 -crf 23 -c:a aac -strict -2 "%%~nf.mp4"``
