# Paper Table 维护规范

## 日期规则
- **日期以 arXiv 第一个版本（v1）的提交时间为准**
- 有些论文会发多个版本（v1, v2, ...），不要用最新版本的时间
- 格式：`YYYY/MM`

## Tag 规则

### 会议/来源 Badge
- 已发表：`[![PDF](https://img.shields.io/badge/会议名-年份-blue)]()`（如 CVPR-2026, ICML-2026, NeurIPS-2025）
- 仅 arXiv：`[![arXiv](https://img.shields.io/badge/arXiv-年份-red)]()`

### Modality (purple)
- Image / Video（目前只有这两个）
- Audio 模态暂未加入 tag 体系

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
- 按年份降序排列（最新在前）
- 同年内按月份降序

## 其他
- GitHub Stars badge 用 `[![Star](https://img.shields.io/github/stars/org/repo.svg?style=social&label=Star)]()`
- 没有 GitHub 的论文 Links 列填 `-`
- 没有详细 tag 的论文 Tags 列填 `-`
