# FFmpeg-commands

http://video.stackexchange.com/questions/4563/how-can-i-crop-a-video-with-ffmpeg

cut a video
ffmpeg -i movie.mp4 -ss 00:00:03 -t 00:00:08 -async 1 cut.mp4
