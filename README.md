# windmark-practice

本 Repo 收录采用 windmark 编写视频源文件，通过这些文件你可以学习如何使用 windmark 制作视频，尤其是如何实现一些动态效果。

注意，作者对这些视频的内容保留版权，提供源文件并不意味着你可以随意转载和二次发布内容本身。

以下源文件粘贴到 [windmark](https://windmark.pro) 的编辑器中即可预览和录制，详细的说明可以[阅读手册](http://doc.windmark.top/cn/)：

- 《云服务器都99一年了，除了买来吃灰，你还能用来装这些免费云软件》 [视频](https://www.bilibili.com/video/BV1kP4y1W7rg/)  [源文件](./99vps.windmark.md)
- 《微信里边如何登入Server酱》 [视频](https://www.bilibili.com/video/BV1yg41157XC/)  [源文件](./sctguide.windmark.md)

PS: B站上的视频为了提升观看体验，做了1.5倍速播放处理，处理脚本为：

```bash
ffmpeg -i   $file   -filter_complex "[0:v]setpts=0.66666*PTS[v];[0:a]atempo=1.5[a]" -map "[v]" -map "[a]"  $out_file ​​​​
```