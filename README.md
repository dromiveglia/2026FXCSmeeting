# 第四届深圳国际安全健康测试技术学术会议 网站

## 文件说明
- `index.html` — 页面主文件（样式与逻辑均内置）
- `config.json` — 所有可修改内容（文字、链接、议程图片、专家照片、模块开关）
- `sessions.json` — 议程表格数据（备用：当 config.json 未配置 sessionImages 时自动使用）

## 常用维护
| 需求 | 修改位置 |
|---|---|
| 更换网页底图 | config.json → `backgroundImage`，填 `"url(bg.jpg)"`；默认为深蓝渐变 |
| 替换议程图片 | 将图片放入 `agenda/` 文件夹，修改 config.json → `sessionImages` 中对应 `image` 路径 |
| 更换专家照片 | 照片放入 `experts/` 文件夹，修改 `expertsList` 中 `photo` 路径 |
| 修改报名链接 | `registrationUrl`（参会报名）、`speakerRegistrationUrl`（演讲专家报名） |
| 显示/隐藏模块 | `modules` 中对应模块的 `visible` 改 true/false（备用：photoLive 图片直播、spare1、spare2） |
| 修改轮播图片/视频 | `carouselSlides` 数组（图片10s换页、视频播完2s换页，已内置） |
| 会场路线图/导航 | `venueMapImage`（路线图图片，如 venue-map.jpg）、`venueMapUrl`（高德导航链接） |
| 分享卡片缩略图 | 将 `share-cover.jpg` 放在网站根目录，并修改 index.html 头部的 og: 标签 |

## 说明
- 微信内分享卡片需后端配合微信 JS-SDK 签名才能完全自定义；当前已通过 og meta 提供标题/描述/缩略图。
- 手机端议程弹窗左侧目录自动隐藏，点「选择场次」按钮呼出。

## 版本记录
- v2.2：轮播统一16:9比例修复；会议地址增加路线图+高德导航定位；代码重构去冗余；版本压缩包归档
- v2.1：内嵌兜底配置，修复 file:// 直接打开报"配置加载失败"；添加版本号
- v2.0：模块化重构（6+3模块、议程图片+左侧竖排、报名双栏、专家照片、轮播图10s/视频2s）
