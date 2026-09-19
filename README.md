# noai-writing

中文文章去 AI 味 Skill。

入口文件是 `SKILL.md`。详细规则拆在 `references/`，示例放在 `examples/`，回归测试放在 `tests/`，机器可维护规则索引放在 `data/patterns.yaml`。

## 安装

通过 `skills` CLI 从 GitHub 安装：

```bash
npx skills add https://github.com/iamnanyi/noai-writing \
  --skill noai-writing
```

安装后重新打开 Codex 或新建任务，让它加载这个 Skill。

## 更新

如果已经安装过，更新到最新版本：

```bash
npx skills update noai-writing
```

更新后重新打开 Codex 或新建任务即可生效。可以用下面的命令查看已安装的 Skill：

```bash
npx skills list
```

## 维护方式

新增一种 AI 味时，优先按下面顺序更新。

1. 在对应 `references/*.md` 中补充模式、问题和改写原则。
2. 在 `data/patterns.yaml` 增加独立规则 ID，便于后续替换和追踪。
3. 在 `tests/cases.md` 增加一个最小回归案例。
4. 如果规则会改变全局工作流程，再修改 `SKILL.md`。

不要把所有新发现都堆进 `SKILL.md`。主文件只保留稳定原则和路由关系。

## 当前重点

当前版本重点处理中文 AI/科技新闻、自媒体长文和评论中最明显的模型写作痕迹，包括模板化反转、伪洞察、段首伪标题、句子式小标题、同义复述、宏大拔高、冒号和破折号滥用、工整排比以及碎片化自然段。
