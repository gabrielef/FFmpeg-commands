# FFmpeg-commands
### CROP
Crop a video witouth transcode it.

    ffmpeg -i original-video.mp4 -filter:v "crop=crop_w:crop_h:x:y" cropped-video.mp4

***crop_w***: width of the cropped video;
***crop_h***: height of the cropped video;
***x***: left corner of the cropped video;
***y***: top corner of the cropped video;

(source: http://video.stackexchange.com/questions/4563/how-can-i-crop-a-video-with-ffmpeg)

### CUT
Cut a video at particular moment without transcode it. Time is in the form of hh:mm:ss.

    ffmpeg -i original-video.mp4 -ss 00:00:03 -t 00:00:08 -async 1 cutted-video.mp4

***-ss***: starting moment for the cut;
***-t***: cut duration;
