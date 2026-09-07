# Design System Collection

[![License: GPL v3](https://img.shields.io/badge/License-GPLv3-blue.svg)](./LICENSE)
[![Upstream: MIT](https://img.shields.io/badge/Upstream%20files-MIT-green.svg)](https://github.com/VoltAgent/awesome-design-md)
[![Files](https://img.shields.io/badge/DESIGN.md-4-informational.svg)](#1-文件索引)

一套可直接交给 Coding Agent 使用的**设计系统规范（`DESIGN.md`）集合**：把任意一份规范放进项目根目录，让 Agent 读取它，即可生成与该品牌/主题一致的界面。

- 收录自上游仓库的分析文件：`design_wise.md`、`DESIGN-vercel.md`
- 参考上游结构自行编写的规范：`DESIGN_lan.md`（蓝版）、`DESIGN_huang.md`（黄版）

---

## 目录

- [1. 文件索引](#1-文件索引)
  - [1.1 收录规范（直接复制自其他仓库）](#11-收录规范直接复制自其他仓库)
  - [1.2 自研规范（参考后自行编写）](#12-自研规范参考后自行编写)
- [2. 来源与署名](#2-来源与署名)
- [3. 自研规范说明](#3-自研规范说明)
- [4. 规范文件的统一结构](#4-规范文件的统一结构)
- [5. 使用方法](#5-使用方法)
- [6. 许可证](#6-许可证)

---

## 1. 文件索引

按**文件是怎么来的**分成两张表：直接复制自其他仓库的放 **1.1**，参考后自行编写的放 **1.2**。

> 两张表合起来就是全仓库的**唯一清单**：新增或删除一个规范文件时，只需在对应表增删一行。

### 1.1 收录规范（直接复制自其他仓库）

存放目录：`awesome-design-md/`。从外部仓库原样获取的分析文件，遵循上游许可证；尽量保持与上游一致，如需改动请在文件顶部注明 `Modified from upstream` 及改动点。详见[第 2 节](#2-来源与署名)。

| 文件 | 主题 / 品牌 | 主色 | 来源仓库 | 说明 |
| --- | --- | --- | --- | --- |
| [`design_wise.md`](./awesome-design-md/design_wise.md) | Wise | `#9fe870` | [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) | Wise 设计语言分析：极重近黑显示字体（900 / 64–126px）+ 青柠绿强调色 + 鼠尾草中性面。本仓库的**结构样板**。 |
| [`DESIGN-vercel.md`](./awesome-design-md/DESIGN-vercel.md) | Vercel（Geist） | `#171717` | [awesome-design-md](https://github.com/VoltAgent/awesome-design-md) | Vercel 设计语言分析：黑白极简 + 多段 Mesh 渐变点缀 Hero，Geist Sans / Geist Mono 排版。 |

### 1.2 自研规范（参考后自行编写）

存放目录：`wuzuniao/`。参考上述收录文件的组织方式与写法自行编写，不属于上游作品，遵循本仓库 GPL-3.0，可自由迭代（约定见[第 3 节](#3-自研规范说明)）。

| 文件 | 主题 / 品牌 | 主色 | 派生自 | 说明 |
| --- | --- | --- | --- | --- |
| [`DESIGN_lan.md`](./wuzuniao/DESIGN_lan.md) | 无足鸟 · 蓝版 | `#0066FF` | `design_wise.md`（结构参考） | 通用、精简式品牌设计系统：思源黑体 Display + Inter 正文，冰蓝画布 `#F0F7FF`，克制去语义化。 |
| [`DESIGN_huang.md`](./wuzuniao/DESIGN_huang.md) | 无足鸟 · 黄版 | `#FFC400` | `DESIGN_lan.md`（颜色镜像） | 蓝版的黄色镜像：与主色系冷暖互换，除颜色外与 `DESIGN_lan.md` 结构完全一致。 |

---

## 2. 来源与署名

`design_wise.md` 与 `DESIGN-vercel.md` **获取自**：

- 仓库：<https://github.com/VoltAgent/awesome-design-md>
- 上游定位：*A collection of DESIGN.md files analysis by popular brand design systems.*
- 上游许可证：**MIT**

使用与署名约定：

1. 两个文件的著作权归上游仓库及其作者所有，按其 **MIT** 条款使用与分发。
2. 保留文件头部的 `name` / `description` 等元信息，不宣称其为原创。
3. 若需对收录文件做本地化或结构调整，建议在文件内保留来源链接，并在[1.1 表](#11-收录规范直接复制自其他仓库)的 `说明` 列末尾标注 `（已修改）`。

除上述两个文件外，本仓库其余规范（`DESIGN_lan.md`、`DESIGN_huang.md` 等）均为**参考该仓库的组织方式与写法自行编写**，不属于上游作品，遵循本仓库的 GPL-3.0 许可证。

---

## 3. 自研规范说明

自研规范沿用上游 `DESIGN.md` 的写法：以 YAML front matter 声明 `colors` / `typography` / `rounded` / `spacing` 等设计令牌，正文给出章节化的使用说明与 Do's and Don'ts，便于 Agent 直接解析。

### 3.1 两套自研规范的关系

| 项目 | `DESIGN_lan.md` | `DESIGN_huang.md` |
| --- | --- | --- |
| 定位 | 蓝版（默认） | 黄版（镜像变体） |
| 主色 / 画布 | `#0066FF` / `#F0F7FF` | `#FFC400` / `#FFF8E1` |
| 文本色 | `#0e0f0c` / `#454745` / `#868685` | 与蓝版一致（中性灰黑系） |
| 结构 | 8 个章节 + 组件清单 | 与蓝版逐节对齐 |
| 差异 | 仅颜色令牌与由其派生的强调色命名 | 同左 |

---

## 4. 规范文件的统一结构

全部规范文件（含收录文件）采用相同的章节顺序，便于横向对比与批量维护：

| 顺序 | 章节 | 内容 |
| --- | --- | --- |
| 0 | Front matter | `version` / `name` / `description` / `colors` / `typography` 等机器可读令牌 |
| 1 | Overview / 概览 | 设计语言的一句话总结与气质描述 |
| 2 | Colors / 颜色 | 调色板语义与配对规则 |
| 3 | Typography / 字体排印 | 字体族、字号、字重、行高、字距 |
| 4 | Layout / 布局 | 栅格、间距、容器宽度 |
| 5 | Elevation & Depth / 层级与深度 | 阴影与层次 |
| 6 | Shapes / 形状 | 圆角、描边、形态 |
| 7 | Components / 组件 | 按钮、卡片、徽章、输入等组件规格 |
| 8 | Do's and Don'ts / 注意事项 | 正误对照 |

> 收录文件使用英文章节名，自研文件使用中文章节名；两者一一对应。

---

## 5. 使用方法

1. 从[文件索引](#1-文件索引)中选择一份规范，复制（或软链）到你的项目根目录，命名为 `DESIGN.md`。
2. 在给 Coding Agent 的提示词中引用它，例如：
   - `请按照项目根目录 DESIGN.md 的颜色、字体与组件规范生成这个页面。`
3. 若要切换风格（如蓝版 → 黄版），只需替换 `DESIGN.md` 的内容，页面代码无需改动结构。
4. 需要同时给多个 Agent/子项目使用时，各自放一份即可，规范之间互不依赖。

---

## 6. 许可证

- 本仓库整体（含自研规范）：**GNU General Public License v3.0**，详见 [`LICENSE`](./LICENSE)。
- 收录的外部文件 `design_wise.md`、`DESIGN-vercel.md`：遵循上游仓库 <https://github.com/VoltAgent/awesome-design-md> 的 **MIT** 许可证。
