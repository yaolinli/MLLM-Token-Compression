# Paper Table 维护规范

## 收录原则
- 与 MLLM token compression 主题相关、已有公开确认的同行评审录用信息的论文，默认收录；未开源不影响收录。
- 预印本结合方法贡献、实验与消融、复现信息审核，不仅依据团队或摘要中的最高加速数字判断。

## 日期规则
- **日期以 arXiv 第一个版本（v1）的提交时间为准**
- 有些论文会发多个版本（v1, v2, ...），不要用最新版本的时间
- 格式：`YYYY/MM`

## Tag 规则

### 会议/来源 Badge
- 已发表：`[![PDF](https://img.shields.io/badge/会议名-年份-blue)]()`（如 CVPR-2026, NeurIPS-2025）
- 仅 arXiv：`[![arXiv](https://img.shields.io/badge/arXiv-年份-red)]()`
- ⚠️ **标注会议必须反复确认！** 很多论文只是用了会议模板（如 ICML 模板），不代表被接收。只有明确公开录用信息的才能标会议 badge，否则一律标 arXiv。不要给别人"手动中稿"

### Modality (purple)
- Image / Video / Audio
- 涉及音频 token 压缩或音视频联合压缩的论文，必须添加 `Audio` badge，不能仅以 Video 或 omni 代替。
- Modality & Position 列以 badge 为主；通用 image/video/omni understanding 不添加额外文字。
- 特殊场景可简短标注 `GUI screenshots`、`Multi-view 3D` 等，不在此列解释方法、训练方式或实现细节。

### Compression Position (cyan)
- Vision_Encoder / Projector / LLM / ViT

### Text Query (brightgreen)
- TQ-Yes / TQ-No（压缩是否由文本引导）
- 压缩适配框架支持多个不同压缩器、无法统一判断是否文本引导时，省略 TQ badge，避免把训练使用文本误标为文本引导剪枝。

### Compression Method (lightgrey)
- Merge / Pruning / Cross_Attention

### Usage Mode (yellow)
- **Retrain 和 Plug_In 只选一个**，不要两个都标
- Retrain：需要训练/微调才能使用
- Plug_In：训练无关，即插即用

### Speed Stage (orange) — 一般不标
- Speed_Train / Speed_Infer
- 除非论文特别强调加速某个阶段，否则不加这个 tag

### Compression Ratio (pink)
- Fix / Dynamic

### Train_Infer (yellowgreen) — 一般不标
- Train / Infer
- 除非论文特别区分训练/推理场景，否则不加这个 tag

## 排序
- **以 arXiv 第一版（v1）发布日期降序排列**，越新的越靠上
- arXiv ID 格式：`YYMM.NNNNN`，前四位 YYMM 代表年月
- **先按年月降序**：2603（2026年3月）> 2602（2026年2月）> 2510（2025年10月）
- **同一年月内**再按后面的序号降序：2602.23235 > 2602.18846 > 2602.04804
- ⚠️ 不是纯字符串排序！2603.01143 比 2602.23235 新，因为 3月 > 2月

## 其他
- Title & Authors 列保留论文标题和作者，不添加 `Team: ...` 团队信息，保持现有列表格式。
- GitHub Stars badge 用 `[![Star](https://img.shields.io/github/stars/org/repo.svg?style=social&label=Star)]()`
- GitHub 链接与 Stars badge 仅用于已有实际方法实现的官方仓库；只有 README、图片、项目页面或 coming-soon 声明的占位仓库，按未开源处理，不展示 GitHub 链接或 Stars badge，Links 列填 `-`。
- 没有 GitHub 的论文 Links 列填 `-`
- 没有详细 tag 的论文 Tags 列填 `-`
