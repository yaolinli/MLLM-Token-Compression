# Paper Table 维护规范

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

### Compression Position (cyan)
- Vision_Encoder / Projector / LLM / ViT

### Text Query (brightgreen)
- TQ-Yes / TQ-No（压缩是否由文本引导）

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
- 具体排序依据：arXiv ID 数字越大 = 发布越晚 = 放越上面
- 例：2602.23235 > 2602.18846 > 2602.04804，所以 23235 在最上面

## 其他
- GitHub Stars badge 用 `[![Star](https://img.shields.io/github/stars/org/repo.svg?style=social&label=Star)]()`
- 没有 GitHub 的论文 Links 列填 `-`
- 没有详细 tag 的论文 Tags 列填 `-`
