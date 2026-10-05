# No-Bullshit Feminist Test（NBFT）

**尊重女性的主体性，让女性作为具体的人存在。**

主要适用于广告行业，因其常常需要在有限篇幅或时长内，面向特定受众、需要借助一定刻板印象、快速传意。NBFT 因此结合具体创作语境审查女性主体性，既不放过贬低和物化，也不要求每支广告机械补齐角色。

这是一个主要用于海报文案、视频脚本等出街内容的女性主义审稿技能。依据具体作品给出结论和修改建议，仅在用户明确调用时使用。

## 名字是什么意思？

**“No-Bullshit”反对的是空洞姿态、机械打勾和缺乏依据的判断。**

女性可以不完美，可以谈论男性，也可以自愿为他人付出。NBFT 关心的是：她是否作为一个有自身处境、感受、需要和选择的人存在。

**In English:** No-Bullshit Feminist Test is a feminist review tool for stories, advertisements, and video scripts. “No-bullshit” rejects empty gestures, mechanical box-ticking, and unsupported judgments. Its core principle is to respect women’s agency and portray women as particular people with lives, needs, feelings, and choices of their own.

## 它怎么审？

NBFT 检查整体表达是否贬低女性、人物是否受到性别模板限制，以及适用的群像作品中是否有可辨识的女性和有内容的交流。

它会先判断叙事结构和具体创作语境，再判断第三项是否适用。短篇幅、男性受众或全男性选角，本身都不是自动豁免的理由；具体而合理的主题、场景和叙事范围可以支持豁免。

讨论男性也可以体现女性主体性。例如，母亲、女儿和祖母讨论是否替男性亲属还钱，只要她们自身的生活、代价和选择真正进入交流，就不因话题涉及男性而失败。

只有男性的故事也不必然失败。例如，儿子照护父亲的故事，既可以呈现男性柔软的一面，也可以打破“照护者只能是女性”的性别模板。如果故事聚焦这段父子关系，有合理的叙事范围，第三项可以豁免，不必为了通过测试硬加女性角色；整体表达仍需接受审查。

完整标准以 [SKILL.md](SKILL.md) 为准。参阅 [具体判例](references/cases.md) 理解边界。

## 怎么使用？

1. 将整个 `no-bullshit-feminist-test` 文件夹交给所用工具的技能安装或导入流程，保留 `SKILL.md`、`agents/` 和 `references/` 的相对路径。GitHub 用于存放和分享文件，本身不执行审稿。
2. 明确调用 NBFT，并提供作品。若有广告主题、目标受众、时长或系列背景，可一并提供；无需为了启动检查补齐所有信息。
3. 查看结论、适用情况、具体依据和修改建议。内容不足时，技能会说明尚不能判断的部分。

调用示例：

```text
请用 NBFT 审查下面这支广告脚本。
这是一个租房软件的父亲节单支广告，时长 30 秒。
请说明第三项是否适用，给出具体依据和修改建议。

［粘贴脚本］
```

支持技能标识调用的环境可使用：

```text
请使用 $no-bullshit-feminist-test 审查以下故事。
```

本包的 `agents/openai.yaml` 为支持该配置的 Codex 环境设置了 `allow_implicit_invocation: false`。其他工具是否识别这一设置，取决于其技能机制；需要在对应工具中确认明确调用方式。包内说明也限定为用户明确要求审稿时运行，普通审稿不自动触发。

## 输出是什么？

最终结论为“通过”或“需修改”，适用情况另列。资料不足时为“信息不足，暂不判定”，不冒充完整审稿结论。第三项合理豁免后，作品仍可以通过。

技能提供修改方向，默认不直接改写。广告的女性受众覆盖会在有依据时单独提醒，不与 NBFT 核心结论混为一谈。

## 来源

第三项的结构改编自贝克德尔—华莱士测试（Bechdel–Wallace test）。NBFT 面向实际写作，扩展了判断依据和适用边界，尤其不以“是否谈论男性”作为唯一判据。

## GitHub 仓库简介建议

> A feminist review skill for stories, ads, and scripts. “No-bullshit” rejects empty gestures, mechanical box-ticking, and unsupported judgments. Explicit invocation only.

## 文件

- [SKILL.md](SKILL.md)：技能入口与完整标准。
- [agents/openai.yaml](agents/openai.yaml)：显示名称和明确调用设置。
- [references/cases.md](references/cases.md)：虚构案例、预期判断及边界说明。
- [VALIDATION.md](VALIDATION.md)：本版本的验证范围与限制。
