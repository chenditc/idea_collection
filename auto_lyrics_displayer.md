## 目标
低成本广泛适用的歌词展示器，类似 MORROR ART 悬浮歌词透明蓝牙音箱：

![image](https://user-images.githubusercontent.com/3244845/192181071-9728e5cc-76f0-4002-8a61-a1cdd71276ca.png)

## 动机
那为什么已经有同样的产品了，还要实现一个呢？
1. 价格贵。
2. 已经有好的音响了，不想重新买音响，但是又喜欢悬浮歌词的效果

## 方案
1. 智能识别歌曲。
  - 可以通过麦克风采集当前播放的歌曲，生成歌曲特征，进行智能识曲。
  - 前提：需要提前爬取全网歌曲的特征库，（或者直接调用音乐云服务的 API）
3. 从歌词库爬取歌词。
  - 识取成功后，可以尝试获取几个匹配的歌词。
5. 根据歌曲当前播放的位置展示歌词。
  - 根据歌曲特征的比对来确定当前播放到几分几秒，定时校对，并展示对应时间的歌词
