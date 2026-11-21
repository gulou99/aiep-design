# AIEP 设计开源：AI 员工头像

[AIEP（AI 员工聚合平台，aiephub.com）](https://aiephub.com/)中 AI 员工使用的头像素材，以 [CC0 1.0](LICENSE) 公共领域贡献方式开源：可自由复制、修改、商用，无需署名（如愿意注明来源，我们会很感谢）。

![AI 员工头像预览](preview.png)

## 内容

| 文件 | 说明 |
|---|---|
| `avatars/employees/*.png` | 14 位 AI 员工的单张头像，314×314 / 1254×1254 PNG |
| `avatars/atlas/ai-team-avatars.png` | 12 位员工头像的原始图集（1254×1254，4 列 × 3 行） |
| `avatars/atlas/ai-team-avatars.webp` | 同一图集的 WebP 版本（约 106 KB），适合网页使用 |
| `avatars/assistant-body.png` | 智能助手形象的身体部分（透明背景，眼睛由界面另行绘制） |
| `prompts/*.json` | 生成这些素材时使用的提示词与修改记录 |

### 员工与文件对应

| # | 文件 | 岗位 |
|---|---|---|
| 01 | `01-content-creator.png` | 内容创作 |
| 02 | `02-sales.png` | 销售 |
| 03 | `03-customer-service.png` | 客服接待 |
| 04 | `04-public-opinion.png` | 舆情 |
| 05 | `05-market-research.png` | 市场调研 |
| 06 | `06-hr.png` | 人事招聘 |
| 07 | `07-legal.png` | 法务 |
| 08 | `08-finance.png` | 财务 |
| 09 | `09-leads.png` | 线索获取 |
| 10 | `10-office.png` | 办公 |
| 11 | `11-matrix-publishing.png` | 矩阵发布 |
| 12 | `12-geo.png` | GEO 优化 |
| 13 | `13-design.png` | 设计（1254×1254） |
| 14 | `14-engineering.png` | AI 工程（1254×1254） |

## 使用图集

图集中每位员工占一个 314×314 的正方形，左上角坐标如下（单位：像素）：

| 行 \ 列 | 1 | 2 | 3 | 4 |
|---|---|---|---|---|
| 1（y=109） | 内容创作 x=0 | 销售 x=314 | 客服接待 x=627 | 舆情 x=940 |
| 2（y=501） | 市场调研 x=0 | 人事招聘 x=314 | 法务 x=627 | 财务 x=940 |
| 3（y=894） | 线索获取 x=0 | 办公 x=314 | 矩阵发布 x=627 | GEO 优化 x=940 |

用 SVG 的 `viewBox` 裁取单个头像，缩放时不会变形：

```html
<!-- 示例：第 2 行第 3 列（法务） -->
<svg viewBox="627 501 314 314" width="40" height="40" aria-hidden="true">
  <image href="ai-team-avatars.webp" width="1254" height="1254" />
</svg>
```

## 设计说明

- 统一的脸部语言：奶白色圆脸、两只竖向胶囊形黑色眼睛、淡桃色腮红，无嘴、无鼻、无眉；岗位差异只体现在发型与配饰上。
- 深炭色背景 `#1c201f`，在 40px 左右的小尺寸下依然清晰可辨。
- 素材由 AI 图像生成并经人工挑选与修改，所用提示词见 `prompts/` 目录。

每位员工的岗位介绍见官网 [AI 员工一览](https://aiephub.com/ai-employees/)。

## 不包含的内容

本仓库只开源上述头像素材。AIEP 名称与品牌标志不在开源范围内，CC0 不授予任何商标权利。

---

## English

AI employee avatars from [AIEP](https://aiephub.com/), released under [CC0 1.0](LICENSE): free to copy, modify and use commercially, no attribution required. The repository contains 14 individual avatars (`avatars/employees/`), the original 4×3 sprite atlas with its tile coordinates (see the table above; each tile is 314×314), the assistant body artwork, and the prompts used to generate them. The AIEP name and logo are not included and no trademark rights are granted.
