# 第二章 音频基础

音频，简而言之就是声音在介质中的震动。以S16格式存储的声音来看，声音数据取值范围为-32768~32767，代表某个时间点声音的强度，越高或越低代表强度越大，越接近0代表声音越小直至没有声音。

## 音频采样率

现在的任何超级计算机都没办法把声音完整的给录制出来，声音采样的含义只是，将声音在某个时间点的强度给存储下来，后续需要播放时，产生同样强度的空气震动，即可还原出声音信息。但是采样不是完美连续的，比如现在使用最广泛的44100Hz采样率，含义为一秒钟将声音震动强度采样44100次，这种采样从大多数人角度来说已然足够。人类能分辨的采样极限是48000Hz采样率，这种采样也有很多场合使用。

其次对于强度来说，最常用的S16采样是取值16位，通常电话采样是8位，部分特殊领域也有采样32位的，目前几乎没有采样64位的。

## 声音的黑科技

声音有两种高级处理方式，一种是去噪，一种是消音。

声音同时也是一种波，通过傅里叶函数滤波也可以很容易的去除声音中的噪音。原理是，声音是很多高频和低频的波的组合，通常低频为实际需要的声音，高频为无用的噪音，此时通过低通滤波，过滤到高频的噪音，即可实现声音去噪。

消音通常是一种嵌入式微型设备，比如去噪耳机或去噪器，大概效果是这样：戴上去噪耳机后就能消除环境声音，更方便听歌；去噪器是手机大小的一个设备，开启后能消除环境噪音，方便私密谈话或者喜欢安静的人使用。这两种设备的原理是这样：首先开启特制麦克风采集声音，然后输出反向震动的声波，这时候新的声波就与原声波中和掉了。

[返回首页](../README.md) | [上一章 视频基础](./02_audio_introduce.md) | [下一章 FFmpeg 入门](./03_ffmpeg_beginning.md)

## 许可

[![test](https://i.creativecommons.org/l/by-nc-nd/4.0/80x15.png)](http://creativecommons.org/licenses/by-nc-nd/4.0/)

本教程采用[知识共享署名-非商业性使用-禁止演绎 4.0 国际许可协议](http://creativecommons.org/licenses/by-nc-nd/4.0/)许可。
