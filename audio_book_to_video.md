# 可视化有声书生成

已实现：https://github.com/chenditc/audio_book_to_video

## 动机
目前很多有声书是没有文字对照的，特别是英文的有声书，导致有一些单词听不懂的话，需要暂停之后，查了单词才能继续听，不方便。

## 目标
输入一个有声书的 mp3，输出一个或者若干个视频文件，视频是中文对照的图像加有声书。相当于给有声书加上字幕。

## 实现路径

### 路径1 - 歌词
1. 将有声书的 mp3，通过语音识别生成文字：https://learn.microsoft.com/zh-cn/azure/cognitive-services/speech-service/captioning-quickstart?tabs=linux%2Cterminal&pivots=programming-language-csharp
2. 将生成的文字调整成 lrc 格式
3. 导入音乐播放软件。

优点：可以利用音乐软件的歌词追踪功能往回调整进度
缺点：没有商业价值

### 路径2 - 视频字幕
1. 将有声书的 mp3，通过语音识别生成文字：https://learn.microsoft.com/zh-cn/azure/cognitive-services/speech-service/captioning-quickstart?tabs=linux%2Cterminal&pivots=programming-language-csharp
2. 将生成的文字调整成字幕格式
3. 与模板背景合并打包生成。

优点：可以剪切后发到视频网站上，可能有一定商业价值。
缺点：有版权风险。且回退没听懂的部分比较难。
