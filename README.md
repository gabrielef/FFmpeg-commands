# FFmpeg-commands
This repository is intended to collect useful ffmpeg commands.


### CROP
Crop a video witouth transcode it.

    ffmpeg -i original-video.mp4 -filter:v "crop=crop_w:crop_h:x:y" cropped-video.mp4

***crop_w***: width of the cropped video;

***crop_h***: height of the cropped video;

***x***: left corner of the cropped video;

***y***: top corner of the cropped video;

(source: http://video.stackexchange.com/questions/4563/how-can-i-crop-a-video-with-ffmpeg)

### SCALE
Scale a video witouth transcode it.

    ffmpeg -i original-video.mp4 -filter:v "scale=scale_w:scale_h" scaled-video.mp4

***scale_w***: new width of the scaled video;

***scale_h***: new height of the scaled video;

(source: https://trac.ffmpeg.org/wiki/Scaling%20(resizing)%20with%20ffmpeg)

### CUT
Cut a video at particular moment without transcode it. Time is in the form of hh:mm:ss.

    ffmpeg -i original-video.mp4 -ss 00:00:03 -t 00:00:08 -async 1 cutted-video.mp4

***-ss***: starting moment for the cut;

***-t***: cut duration;


###ROTATE
Rotate a video without transcode it.

    ffmpeg -i original-video.mp4 -vf "transpose=2" -qscale 0 -y rotated-video.mp4

***-vf***: video filter to set the rotation type. "transpose=2" is 90° counterclockwise, "transpose=3" is 90° clockwise, "vflip" vertical flip  

***-qscale***: quality factor;


###CHANGE CONTAINER
Change the container of a video file.

    ffmpeg -i original-video.mov -vcodec copy -acodec copy new-video.mp4
