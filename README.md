<div align="center">

# About Me

**把「我是谁」，变成一场玩具派对。**

A self-introduction becomes your inventory. Your inventory becomes the game.

![Engine](https://img.shields.io/badge/Tuanjie-2022.3-202A3D?style=flat-square)
![Client](https://img.shields.io/badge/Client-C%23%20%2F%20WebGL-77C8BD?style=flat-square)
![API](https://img.shields.io/badge/API-Python%20%2F%20FastAPI-A5AFF0?style=flat-square)

**[浏览器试玩 ↗](https://web-production-fb9b1.up.railway.app/)** · [最新演示](#最新演示)

</div>

**About Me** 是一款 3D Persona 派对对战游戏原型。写下兴趣、学校和性格，AI 会把介绍中可定位的内容变成可装备的道具：篮球、相机、校徽飞盘，或立体性格词条。在桌面上的微缩校园里，拿它们投掷、抓取、争抢和吞噬，直到产生最后的赢家。

项目已经串起 **自我介绍 → Persona 生成与保存 → 单人练习 / 多人房间 → 战斗 → 结算与重玩**。当前公开展示基线为 **R16**，支持 macOS 和 WebGL 客户端、Linux 权威游戏服务及 Python API。


## 最新演示


<div align="center">
  <a href="docs/media/about-me-poster.png">
    <img src="docs/media/about-me-poster.png" alt="About Me 宣传海报：戴黄色耳机的玩具角色与相机、小猫、披萨和故事书" width="520">
  </a>
  <p><strong>More Than Just a Game.</strong><br>把兴趣、故事和性格，变成拿在手里的 Persona。</p>
  <p><a href="docs/media/about-me-poster.png">查看完整海报</a></p>
</div>

### 宣传视频 · 2:14

<div align="center">
  <a href="docs/media/about-me-promo.mp4"><img src="docs/media/about-me-promo-cover.jpg" alt="About Me 宣传视频预览：玩具角色在微缩校园中使用 Persona 道具对战" width="880"></a>
  <p><a href="docs/media/about-me-promo.mp4"><strong>▶ 观看宣传与实机演示</strong></a></p>
</div>

点击封面或上方链接进入视频文件页。视频中的界面标注 R15；当前公开试玩基线为 R16。


## 先玩一局


打开 **[在线试玩](https://web-production-fb9b1.up.railway.app/)**，选择 **Single Player → 使用练习道具开始（非 AI）**，即可先体验核心玩法，无需填写 API key。单人可搭配 1–6 名人机；多人房间支持 2–6 人。

在 **Intro Presets** 中可以编辑介绍并生成自己的 Persona。真实生成依赖演示服务器的模型配置和可用额度；服务不可用时会明确提示。练习道具始终是标注过的固定样例。

> 浏览器试玩需要加载 WebGL 资源，首次打开请稍候。建议先用桌面浏览器体验；移动端有横屏触控，微信真机仍待验收。


## 游戏里有什么


| 体验 | 设计与实现 |
| --- | --- |
| **介绍就是装备** | 从原文事实生成 Persona；每人最多 20 件，可保存、装备并编入五格快捷栏。 |
| **软身体派对对战** | 投掷、击倒、抓人、拉扯道具、持续挣脱；吞噬或回收需要时间，也会被攻击打断。 |
| **每局都在争夺身份** | 掉落仍归原主人，完成吞噬才转移计数；淘汰后观战，结束后查看结果并重玩。 |
| **有个性的道具库** | R16 交付包含 277 项道具、16 型 MBTI、性格与心情词条、四类动物表现。 |
| **桌面上的小校园** | 双层场地、公共道具与机关，以及定时进入场地的「大手点名」。 |
| **一起玩，也能独自练习** | 单人 NPC 与玩家共用战斗规则；多人使用权威服务器、WebSocket 同步和身份重连。 |

标准对局先展示 5 秒；第 2:30 和 5:00 触发大手点名，第 7:30 到时结算。只剩一名存活者时可提前结束；到时先比较吞噬数，再比较剩余 Persona。


## 画面与界面


<img src="docs/images/about-me-r16-home.png" alt="About Me R16：暖色教室、玩具角色与四个主菜单入口" width="100%">

<table>
  <tr>
    <td width="50%"><img src="docs/previews/desk-campus/in-engine-overview.png" alt="引擎内的桌面微缩校园场景"><br><b>桌面微缩校园</b><br>场景专项的引擎截图。</td>
    <td width="50%"><img src="docs/persona-library/new-four-preview.png" alt="已导入的 CC0 Persona 道具预览"><br><b>可拿在手里的 Persona</b><br>已导入工程的 CC0 道具预览。</td>
  </tr>
  <tr>
    <td><img src="docs/ui-touch-polish/bag-1600x900.png" alt="Persona 背包界面预览"><br><b>随身 Persona 背包</b><br>装备、分类与五格快捷栏。</td>
    <td><img src="docs/ui-interaction/wardrobe-front.png" alt="角色衣橱界面预览"><br><b>介绍与角色表达</b><br>配色、造型和角色外观。</td>
  </tr>
</table>

主菜单为 R16 留存截图；画廊保留了场景、CC0 道具和界面设计的开发预览。背包使用固定预览数据，不连接服务器；历史界面数值不代表 R16 的容量配置。


## 操作


| 操作 | 键位 |
| --- | --- |
| 移动 / 奔跑 | `WASD` / 双击方向键 |
| 观察 / 跳跃 | 鼠标 / `Space` |
| 使用当前道具 / 抛出公共道具 | `F` |
| 抓人 / 抓对手的道具 | `G` / `H` |
| 拾取、吞噬或回收 | `E` |
| 持续挣脱 / 取消交互 | 按住 `Q` / `Q` |
| 切换道具 / 背包 | `1`–`5` / `B` |
| 观战切换 / 释放光标 | `Tab` / `Esc` |


## 展示范围

本仓库仅包含作品介绍、精选截图、宣传海报与演示视频。项目源码、开发文档和服务端配置不公开。
