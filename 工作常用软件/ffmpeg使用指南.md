



### 1、使用ffmpeg进行macOS推流

```sh
ffmpeg -f avfoundation -framerate 30 -i "0:0" -f avfoundation -i ":0" -vcodec libx264 -pix_fmt yuv420p -preset ultrafast -acodec libmp3lame -f flv "rtmp://193277.push.tlivecloud.com/live/stream02?txSecret=87f7c25e8cebb9d0c9a2474e01df054dee9c0431f78701d3ec35d4c46898a944&txTime=65744D35"
```

让我解释一下这个命令的各部分含义：

- `f avfoundation`：这个选项指定了输入的格式。`avfoundation`是macOS的音视频采集框架。
- `i "0:0"`：这个选项指定了音视频输入的设备索引。在这个例子中，"0:0"表示第一个视频设备和第一个音频设备。
- `vcodec libx264 -pix_fmt yuv420p -preset ultrafast`：这些选项设置了视频编码器、像素格式和编码预设。`libx264`是一款广泛使用的H.264编码器，`yuv420p`是一种常见的像素格式，`ultrafast`是x264编码器的预设，提供了最快的编码速度。
- `acodec libmp3lame`：这个选项设置了音频编码器。`libmp3lame`是一款MP3编码器。
- `f flv rtmp://<your-streaming-url>`：这些选项指定了输出的格式和地址。`flv`是Flash Video的缩写，是一种流媒体格式，`rtmp://<your-streaming-url>`是你的RTMP直播流的URL。







ffmpeg -re -f lavfi -i testsrc=s=1280x720:r=25 -pix_fmt yuv420p -vcodec libx264 -f flv “rtmp://193277.push.tlivecloud.com/live/stream01?txSecret=cfd85c43e8bba2981ca23ac136a0c193&txTime=65742E4F”





ffmpeg -re -i /Users/allenchen/workspace/FFmpeg/output.flv -f lavfi -i testsrc=s=1280x720:r=25 -pix_fmt yuv420p -vcodec libx264 -f flv "rtmp://open-push.voip.yximgs.com/gifshow/kwai_actL_ol_act_9934790925_strL_origin?sign=633d0143-c210c0d7d91c2c1849c18bbeeac98244&ks_fix_tsb" 





ffmpeg -video_size 1280x720 -framerate 30 -f avfoundation -pixel_format uyvy422 -i "0:0" -ar 44100 -f flv “rtmp://193277.push.tlivecloud.com/live/stream01?txSecret=cfd85c43e8bba2981ca23ac136a0c193&txTime=65742E4F”





ffmpeg -video_size 1280x720 -framerate 30 -f avfoundation -pixel_format uyvy422 -i "0:0" -ar 44100 -f flv rtmp://127.0.0.1:1935/live





ffmpeg -video_size 1280x720 -framerate 30 -f avfoundation -pix_fmt yuv420p -vcodec libx264   -i "0:0"  -ar 44100  -f flv “rtmp://193277.push.tlivecloud.com/live/stream01?txSecret=cfd85c43e8bba2981ca23ac136a0c193&txTime=65742E4F”





ffmpeg  -i "0:0"  -video_size 1280x720 -framerate 30 -f flv  -pix_fmt yuv420p -vcodec libx264   “rtmp://193277.push.tlivecloud.com/live/stream01?txSecret=cfd85c43e8bba2981ca23ac136a0c193&txTime=65742E4F”



ffmpeg -f avfoundation -i "0:0" -f avfoundation -i ":0" -s 1280x720 -r 25  -pix_fmt yuv420p -vcodec libx264 -acodec aac -f flv “rtmp://193277.push.tlivecloud.com/live/stream01?txSecret=cfd85c43e8bba2981ca23ac136a0c193&txTime=65742E4F”



ffmpeg -f avfoundation -i "0:0" -f avfoundation -i ":0" -s 1280x720 -r 25  -pix_fmt yuv420p -vcodec libx264 -acodec aac -f flv  "webrtc://193277.push.tlivecloud.com/live/stream02?txSecret=f11f4da88ab01a42c9d99e71e89594b7&txTime=65744CC2"



#### 可以正常使用的命令

ffmpeg -f avfoundation -framerate 30 -i "0:0"  -f avfoundation -i ":0"  -video_size 1280x720 -pixel_format nv12 -vcodec libx264 -acodec aac -f flv  "rtmp://193277.push.tlivecloud.com/live/stream02?txSecret=87f7c25e8cebb9d0c9a2474e01df054dee9c0431f78701d3ec35d4c46898a944&txTime=65744D35"



```sh
ffmpeg -f avfoundation -list_devices true -i ''
```

```sh
[AVFoundation indev @ 0x7f8a51104580] AVFoundation video devices:
[AVFoundation indev @ 0x7f8a51104580] [0] FaceTime高清摄像头（内建）
[AVFoundation indev @ 0x7f8a51104580] [1] OBS Virtual Camera
[AVFoundation indev @ 0x7f8a51104580] [2] Capture screen 0
[AVFoundation indev @ 0x7f8a51104580] AVFoundation audio devices:
[AVFoundation indev @ 0x7f8a51104580] [0] MacBook Pro麦克风
```

```sh
ffmpeg -h demuxer=avfoundation

Demuxer avfoundation [AVFoundation input device]:
AVFoundation indev AVOptions:
  -list_devices      <boolean>    .D......... list available devices (default false)
  -video_device_index <int>        .D......... select video device by index for devices with same name (starts at 0) (from -1 to INT_MAX) (default -1)
  -audio_device_index <int>        .D......... select audio device by index for devices with same name (starts at 0) (from -1 to INT_MAX) (default -1)
  -pixel_format      <pix_fmt>    .D......... set pixel format (default yuv420p)
  -framerate         <video_rate> .D......... set frame rate (default "ntsc")
  -video_size        <image_size> .D......... set video size
  -capture_cursor    <boolean>    .D......... capture the screen cursor (default false)
  -capture_mouse_clicks <boolean>    .D......... capture the screen mouse clicks (default false)
  -capture_raw_data  <boolean>    .D......... capture the raw data from device connection (default false)
  -drop_late_frames  <boolean>    .D......... drop frames that are available later than expected (default true)
```



-i 前后与输入设备相关
 1.2. -f avfoundation -i "1:0" ：avfoundation输入设备，该设备可以捕获Mac OS X上的桌面、摄像头、麦克风等输入源。-i "1:0"：指定输入设备的ID，这里使用1:0表示捕获Mac OS X上的主屏幕（即桌面）
 1.3. -f avfoundation -i ":0" ：指定音频输入设备为Mac OS X系统的默认麦克风。

输出相关
 2.1 -s 1280x720 图像分辨率
 2.2 -r 25 图像帧数
 2.3 -pix_fmt yuv420p  将读取的图像像素点颜色格式转换
 2.4 vcodec libx264 视频编码libx264
 2.5 -acodec aac 音频编码
 2.6 -f flv 输出文件格式





ffmpeg -f avfoundation -i "0:0" -f avfoundation -i ":0" -s 1280x720  -pix_fmt yuv420p -vcodec libx264 -acodec aac -f flv  "rtmp://193277.push.tlivecloud.com/live/stream02?txSecret=87f7c25e8cebb9d0c9a2474e01df054dee9c0431f78701d3ec35d4c46898a944&txTime=65744D35"



ffmpeg -f avfoundation -framerate 30 -i 0 "rtmp://193277.push.tlivecloud.com/live/stream02?txSecret=87f7c25e8cebb9d0c9a2474e01df054dee9c0431f78701d3ec35d4c46898a944&txTime=65744D35"



### 2、 开始录制

如下设置之后就可以录制了，按ctrl+c可以停止录制
 `ffmpeg -video_size 1280x720 -framerate 30 -f avfoundation -i "0:0" output.mkv`

输出视频文件是`output.mkv`，可以直接播放了。



### 3、 ffplay播放

安装ffplay后，可以实时直接播放摄像头和话筒，把上面命令里的ffmpeg换成ffplay，去掉output.mkv输出文件就行了！

```
ffplay -video_size 1280x720 -framerate 30 -f avfoundation -i "0:0"
```



### 视频压缩

ffmpeg -i '/Volumes/极客时间/极客时间视频课合集/107-小马哥讲Spring核心编程思想/1-99/94丨SpringBean实例化阶段：Bean实例是通过Java反射创建吗？.mp4' -vf scale=1280:720 -b:v 3000k -bufsize 3000k '/Users/shuzx/Downloads/最新下载/output.mp4'

1. **压缩视频分辨率**

ffmpeg -i input.mp4 -vf scale=1280:720 output.mp4

-vf scale=1280:720  将视频分辨率压缩到 1280x720

2. **降低视频比特率**

ffmpeg -i input.mp4 -b:v 3000k -bufsize 3000k output.mp4

-b:v 3000k 表示设置目标视频比特率为 3000 kb/s，-bufsize 3000k 表示设置缓冲区大小为 3000 kb

3. **使用更高效的视频编码格式**

ffmpeg -i input.mp4 -c:v libx265 -crf 28 output.mp4

述命令将输入视频input.mp4转换为H.265编码格式，并将结果保存为output.mp4文件。其中，-c:v选项表示视频编码器，libx265表示使用x265编码器，-crf选项表示视频质量，28表示目标视频质量，值越小视频质量越高，文件体积越大



4. **压缩音频比特率**

ffmpeg -i input.mp4 -c:v copy -b:a 128k output.mp4

-c:v copy 表示复制视频编码器进行快速处理，-b:a 128k 表示设置目标音频比特率为 128 kb/s







ffprobe -v error -select_streams v:0 -count_frames -show_entries stream=nb_read_frames -print_format csv  /Volumes/其他学习资料/极客时间视频课合集/K8S/模块一：Go语言特性/1.\ Go\ 语言特性\ ·\ 第一课.mp4 





ffprobe  -v error -count_frames -select_streams v:0 -show_entries stream=nb_read_frames -of default=nokey=1:noprint_wrappers=1 