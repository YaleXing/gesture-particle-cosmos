# ✦ 手势粒子宇宙 · Gesture Cosmos

> 用手势控制粒子特效的浏览器应用，无需安装，打开即用。  
> A browser-based hand gesture particle experience. No install needed — just open and play.

![HTML](https://img.shields.io/badge/HTML-单文件-orange) ![MediaPipe](https://img.shields.io/badge/MediaPipe-Hands-blue) ![License](https://img.shields.io/badge/license-MIT-green)

---

## ✨ 效果预览

张开手掌，烟花炸裂；比出爱心，心形粒子在空中旋转；握起拳头，旋涡把光粒吞噬……  
六种手势，六种完全不同的粒子世界。

---

## 🖐 手势对照表

| 手势 | 动作 | 特效 |
|------|------|------|
| ✋ | 五指全部张开（含拇指） | 🎆 多点烟花同时爆炸，带星形拖尾 |
| ✌️ | 食指 + 中指伸出（V形） | ❤️ 3D 旋转心形，数百粒子自旋 |
| 👊 | 握拳 | 🌀 粒子旋涡向拳心汇聚 |
| ☝️ | 只伸出食指 | 🌈 彩虹光迹跟随指尖 |
| 🤟 | 食指 + 中指 + 无名指伸出 | 💬 文字粒子爆炸重组（我爱你 / Love / ❤️ / 520 / 永远…） |
| 🤙 | 只伸出小指 | 🌍 3D 粒子星球缓缓旋转 |

---

## 🚀 使用方法

### 方法一：直接打开（最简单）

1. 下载 `gesture_particles.html`
2. 用 **Chrome 或 Edge** 打开（需要支持 WebGL 的现代浏览器）
3. 允许摄像头权限
4. 对着摄像头做手势，享受特效 🎉

### 方法二：GitHub Pages 在线访问

如果你 fork 了本仓库，可以开启 GitHub Pages：

```
仓库 → Settings → Pages → Branch: main → Save
```

几秒后会生成一个公开链接，分享给任何人都能直接在浏览器玩。

---

## 🛠 技术栈

| 技术 | 用途 |
|------|------|
| [MediaPipe Hands](https://google.github.io/mediapipe/solutions/hands) | 实时手部关键点识别（21点） |
| Canvas 2D API | 粒子渲染、发光、拖尾效果 |
| 离屏 Canvas | 文字点阵采样，生成文字粒子 |
| 纯 HTML + JS | 零依赖框架，单文件完整运行 |

**核心设计：**
- 粒子池上限 2000，自动回收最老粒子，保持帧率流畅
- 手势防抖 4 帧，避免误触发
- 文字渲染自适应字号，任意长度文字均完整显示
- 3D 心形 / 星球使用旋转矩阵实现，按深度排序渲染

---

## 📁 文件结构

```
gesture_particles.html   # 全部代码，单文件
README.md                # 本文件
```

---

## 🔧 自定义

打开 `gesture_particles.html`，找到这一行即可修改文字粒子的内容：

```js
const texts = ['我爱你', 'Love', '❤️', '520', '永远', 'Forever', '想你', 'XOXO'];
```

改成任何你想要的词语，保存刷新即生效。

---

## 📋 注意事项

- 请在 **光线充足** 的环境下使用，手部识别效果更好
- 建议摄像头与手保持 **40–80cm** 距离
- 首次加载需要下载 MediaPipe 模型文件（约 10MB），需要网络连接
- 不支持 Firefox（WebRTC + MediaPipe 兼容性问题），推荐 Chrome / Edge

---

## 📄 License

MIT — 随意使用、修改、分享。
