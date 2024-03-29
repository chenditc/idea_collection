## 痛点

目前自媒体工作发布形式一般有两种：
1. 图文。如 Instagram, 小红书图文，抖音图集，快手图集，今日头条。
2. 竖版(短)视频。如 抖音、快手、小红书视频、腾讯视频号、TikTok、Youtube Shorts。
3. 横版(长)视频。如 B站，西瓜视频，Youtube。

当创作者制作好作品后，如果需要多平台发布，则需要每个平台登录、上传、编辑元信息等，每个作品每个平台可能需要5-10分钟。这对于时间本就不多的创作者可能是很分心麻烦的事。

## 解决方案

通过模板映射转化，实现一次发布，全平台同步。

1. 模版映射转化。定义入口模版，例如图文模版需要包含：图片、文案以及音乐类型。再通过每个平台的不同转换规则，在加上对应平台的 tag，或者找到对应平台合适的音乐。转换规则可以是固定的映射，也可以是根据平台动态生成的，例如选取最近爆款的音乐等。
2. 一次发布，全平台同步。在定义了发布时间后，只需要选取需要同步的各平台账号，提供模版生成对应平台的内容，然后再模拟操作进行发布。

## 实现细节

1. 模版映射转化。
从简单的转化开始，例如直接使用同一套图文、视频。


2. 全平台同步。
 - 用网页端的创作者中心登录，登录后保持 session 活跃，定期登录刷新 session。
 - session 信息可以使用不同的 chrome 账号直接保持。
 - 登录过期后短信或推送提醒登录。
 - 通过创作者中心上传内容。
