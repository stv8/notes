## [yt-dlp](https://github.com/yt-dlp/yt-dlp)

## Common Commands

#### Download thumbnail and not video
```shell
yt-dlp $VIDEO_ID --write-thumbnail --skip-download
```

#### Download list of all videos for a channel
```shell
yt-dlp --flat-playlist --print "%(url)s # %(title)s" $CHANNEL_URL
```

!!! note
    since anything after a # is ignored, you can leave the titles in when using `--batch-file`

