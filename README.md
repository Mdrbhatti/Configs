# Configs

## Config for chrome [Redirector](https://chrome.google.com/webstore/detail/redirector/ocgpenflpmgnfapjedencafcfakcekcd/related?hl=en-US)

### Reddit sort every thread by top comments
From: ``
^(.*?):\/\/(.*?)\.reddit\.com\/r\/(.*)\/(.*)\/(.*)\/$
``

To: ``
$1://old.reddit.com/r/$3/$4/$5/?sort=top
``

### Reddit redirect to old.reddit
From: ``
^(.*?):\/\/(.*?)\.reddit\.com(.*)
``

To: ``
$1://old.reddit.com$3
``

Exclude ``
^(.*?):\/\/out\.reddit\.com\/r\/(.*)
``

## Config for ffmpeg

### Windows (.bat) convert all .flac to .mp3
``for %%f IN (*.flac) DO "ffmpeg.exe" -i "%%~nf.flac" -ab 320k -map_metadata 0 -id3v2_version 3 "%%~nf.mp3"
``
### Windows (.bat) shorten specific .mp3
``for %%f IN (*.mp3) DO "ffmpeg.exe" -i "%%~nf.mp3" -ss 385 -t 275 -acodec copy "%%~nf.mp3"``

### Windows (.bat) 1080p raw video to 480p downscale best quality
``for %%f IN (*.mp4) DO "ffmpeg.exe" -i "%%~nf.mp4" -s hd480 -c:v libx264 -r 24 -crf 23 -c:a aac -strict -2 "%%~nf.mp4"``

### Windows (.bat) flv to 720p mp4
``for %%f IN (*.flv) DO "ffmpeg.exe" -i "%%~nf.flv" -s hd720 -c:v libx264 -crf 23 -c:a aac -strict -2 "%%~nf.mp4"``
