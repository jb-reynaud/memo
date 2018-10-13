## OSX

```
ffmpeg -f avfoundation -i "0" video.mp4

# Cut a video
ffmpeg -i input.mp4 -ss 01:10:27 -to 02:18:51 -c:v copy -c:a copy output.mp4
```

