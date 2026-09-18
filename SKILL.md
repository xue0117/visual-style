---
name: visual-style
description: Create or restyle charts, statistical figures, dashboards, and report visuals using the user's unified blue-blue-gold-orange-red visual system. Use for Python, Plotly, ECharts, web dashboards, spreadsheets, slides, general data visualization, and human-factors analysis. Do not override a publication, brand, or accessibility specification explicitly required by the user.
---

# 统一数据可视化风格

让不同工具、图型和项目共享同一套视觉语言：现代、精致、低饱和、专业，适合人因研究、产品分析、管理汇报和论文式结果展示。

## 工作方式

1. 先判断数据关系，再选图型；不要为了套模板而改变分析含义。
2. 默认使用用户的五色核心：主色 `#5271AE`、辅助色 `#70ACDE`、柔和强调色 `#F5CC7D`、醒目强调色 `#FFA660`、风险色 `#D85B59`。
3. 将颜色按语义分配，而不是按出现顺序随意轮换。同一项目、同一变量跨图保持相同颜色。
4. 保持白色或近白背景、清晰层级、充足留白、弱网格和克制装饰。优先直接标注；图例仅在能减少拥挤时使用。
5. 标题应表达结论或比较对象；坐标轴写明变量与单位；统计图按需标注样本量、统计量、区间或阈值定义。
6. 输出前检查颜色对比、拥挤、截断、坐标尺度、单位、图例顺序和导出清晰度。

用户不需要为了本 Skill 预先整理成固定模板。先识别当前数据的字段、层级、单位、缺失值和重复测量结构，再在不改变原始含义的前提下转换为适合绘图的结构。若字段含义、单位或正负方向的歧义会改变结论，先提出最少量澄清问题；不要静默猜测。

## 按任务读取规范

- 任何绘图或改图任务都读取 [references/design-system.md](references/design-system.md)。
- 收到文件、粘贴表格、JSON、多层表头、宽表/长表或排版不规则数据时读取 [references/data-adaptation.md](references/data-adaptation.md)。
- 选择图型、组织多图或绘制人因研究结果时读取 [references/chart-families.md](references/chart-families.md)。
- 生成 Python、Plotly、ECharts、网页、Excel、PPT 或报告代码时读取 [references/implementation.md](references/implementation.md)。
- 需要机器可读的颜色、字号和线宽时使用 [assets/theme-tokens.json](assets/theme-tokens.json)，不要重新猜测色值。

## 不可破坏的约定

- `#F5CC7D` 不直接用于白底上的小字、细线或关键边界；这些场景改用深金色 `#B47A1F`，原黄色用于面积、标记或浅强调底。
- `#FFA660` 表达提醒、次重点或较高水平；`#D85B59` 专用于风险、错误、异常和超限。两者不可仅凭颜色表达，还要增加文字、符号或线型提示。
- 左右侧、X/Y/Z、舒适度/稳定性等变量只有在当前项目已建立固定映射时才延续；没有既定映射时依据图内辨识度建立映射，并在整组输出中保持一致。
- 连续数值使用顺序色阶；有意义的零点或基准值使用发散色阶；分类数据使用离散色。不要把三者混用。
- 不使用彩虹色、伪3D柱状图、装饰性渐变、厚重阴影、过密网格或无意义的双轴图。
- 当显式出版规范、公司品牌规范或色觉无障碍要求与本风格冲突时，优先遵循显式要求，并尽量保留字体、留白、层级与版式特征。

## 默认交付

- 屏幕和前端：响应式尺寸，文字在常见桌面宽度下清晰可读。
- 报告和PPT：优先矢量 SVG/PDF；需要位图时导出透明或白底 PNG，默认 300 dpi。
- 多图：共享图例、对齐绘图区、统一字号和坐标格式；可比较的图保持一致尺度。
