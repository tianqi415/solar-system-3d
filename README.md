# Solar System 3D Console · 3D 太阳系控制台

一个纯前端、零外部依赖的 3D 太阳系模拟页面：八大行星围绕太阳持续公转，支持速度调节、自由视角缩放旋转与行星数据对比，深空辉光渲染。所有资源（three.js、字体、兼容垫片）全部内置，**无需构建、无需联网、不请求任何外部 CDN**——浏览器直接打开即可运行，丢到任意静态托管即可部署。

## 特性

- 八大行星 + 太阳的公转模拟，轨道可视化，运行速度可调
- 鼠标拖拽/滚轮自由视角（OrbitControls），行星数据面板（天文参数见 `map-data.js`）
- UnrealBloom 辉光后期渲染，深空视觉效果
- 单文件应用：HTML / CSS / JS 全部内联在 `index.html`，改起来直观
- 离线可用：无外链、无构建步骤、无第三方运行时请求

## 快速开始

```bash
# 方式一：直接双击 index.html 打开

# 方式二：本地起个静态服务（推荐）
python -m http.server 8080
# 浏览器打开 http://localhost:8080

# 方式三：推到 GitHub Pages 等任意静态托管，零配置
```

在线演示：https://tianqi415.github.io/solar-system-3d/

## 项目结构

```
index.html       单文件应用（结构 / 样式 / 逻辑全部内联，含 import map）
map-data.js      行星与卫星的天文数据
lib/three/       three.js 内置版（MIT，Copyright Three.js Authors）
lib/fonts/       内置字体子集（woff2）
lib/es-module-shims/  import map 兼容垫片
```

## 二次开发

无构建流程，直接编辑 `index.html`；three.js 通过 import map 从 `lib/` 本地加载。
支持 ES Modules 的现代浏览器（Chrome / Edge / Firefox / Safari 近两年版本）均可运行。

## License

MIT © 2026 天奇
