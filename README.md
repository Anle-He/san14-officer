# 三国志14武将与名品 Skill

为《三国志14》（SAN14、RTK14）制作或校准自建武将与名品，并处理已有立绘的导入素材。按本次请求完成所需部分，默认使用中文；明确要求日文时使用日文。

## 功能

- **武将设定与列传**：查询人物事迹，校准生卒年、五维、个性、阵形、战法、主义与政策，编写可复制的列传。
- **名品文案与条目**：撰写名品说明，参照游戏数据制定数值，按 Wiki 结构输出条目草稿。
- **立绘素材处理与导入**：处理已有图片的尺寸、格式、Alpha 通道、抠图与背景，准备目标工具所需文件。

## 在 Codex 中安装与调用

在 Codex 中使用技能安装器：

```text
$skill-installer 从 https://github.com/Anle-He/san14-officer 安装技能，使用仓库根目录，技能名为 san14-officer。
```

安装完整目录，保持 `SKILL.md`、`references/` 与 `agents/` 的相对位置。Codex 会自动发现新安装的技能；若未出现，可重启 Codex。安装方式参见 [OpenAI 官方技能文档](https://learn.chatgpt.com/docs/build-skills#install-curated-skills-for-local-use)。

安装后使用 `$san14-officer` 调用，提供本次任务涉及的人物资料、已有设定或原始图片；需要导入素材时附目标工具及其规格。

## 调用示例

**武将设定**

```text
$san14-officer 为这名武将制定生卒年、五维和游戏条目，区分史料记载与创作补定。
```

**只写列传**

```text
$san14-officer 根据我提供的人物资料写列传，采用身份简介、〖演义〗、〖正史〗结构，来源放在正文外。
```

**名品文案**

```text
$san14-officer 为焦尾琴写名品条目，按 Wiki 结构输出，说明约40字，使用中文。
```

**立绘素材**

```text
$san14-officer 将我上传的已有立绘处理为透明 PNG，按提供的工具规格调整尺寸，检查 Alpha 和边缘并展示预览。
```

## 目录

| 文件 | 用途 |
|---|---|
| [SKILL.md](SKILL.md) | 技能入口、共同原则和交付验收 |
| [references/research-and-settings.md](references/research-and-settings.md) | 人物考据、游戏校准和列传 |
| [references/famous-items.md](references/famous-items.md) | 名品文案、数值与 Wiki 条目 |
| [references/portrait-and-import.md](references/portrait-and-import.md) | 立绘格式、背景、透明度与导入 |
| [agents/openai.yaml](agents/openai.yaml) | 技能界面名称、说明和默认调用提示 |

## 许可证

[MIT](LICENSE)
