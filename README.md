# 中文文学声口 · Chinese Literary Voices

> A Claude **Skill** that turns the model into a complete Chinese creative-writing engine. Style-tuning lives inside one supreme aesthetic law (**image over assertion; every image must be beautiful or witty**): five deeply-crafted reference archives are recommended first, and when they genuinely fall short, the engine searches world literature and forges new references using those archives as the template. **The five are a base, not a cage.**
>
> 一个把 Claude 变成**完整中文创意写作引擎**的 Skill。风格定调发生在最高美学律之内（**意象优先于断言，且要么美、要么有机锋**）：定调优先推荐五个打磨最深的精装 reference（刘仲敬、江南、川端中译、郭敬明式都市、班宇）；当它们确实不足以满足你的意图时，引擎会向**全网高级著作的尺度**搜索新 reference，并按精装档案的架构现场铸造成同等质量的档案。**五个档案是"一份 reference 该有的架构与能力"的基地，不是全部 reference 的限定框。** 你贴来的任何参考文本也可实时提取成档。

---

## 它是什么

大多数"写得文学一点"的尝试，结果都是**漂亮的空壳**：句子华丽，却不知为何而写、往哪里去，且满是抽象断言。本 Skill 把真实创意写作的流程拆成五个互不替代、叠加生效的层面，让 Claude 从"会拽词"升级到"会写"。

风格定调的供给顺序（思路借鉴 `ui-ux-pro-max` 的 moodboard 机制）：① **你贴的样本**最优先——实时提取成档；② **五个精装 reference**（含混搭，附数十个轻量目录）优先推荐；③ 确实不足时**向全网高级著作尺度搜索**候选文体，moodboard 给选项，选定后按精装档案的架构铸造成临时档案。三个来源可自由混搭。

## 五层架构

完整流向：**意图 → 决策包 → 生成 → 场面 → 声口 → 逐句美学**

| 层 | 文件 | 管什么 | 一句话 |
|---|---|---|---|
| 0 意图层 | `references/intake.md` | 四问选项 → moodboard 挑声口 → 写作决策包 | 听懂"要什么" |
| 1 生成层 | `references/craft-engine.md` | 种子 → 传动轴 → 生长 → 成形 | 树怎么长 |
| 2 场面层 | `references/scene-craft.md` | 素材 / 单场编写 / 承上启下 / 镜头编排 | 每节怎么拍 |
| 3 风格定调 | 五精装档案 + `voice-catalog.md` + `voice-extraction.md`（不足则全网搜索铸新档） | 美学律的内部环节：样本→五精装优先→搜索补位 | 什么品种的叶子 |
| 4 美学层 | `SKILL.md` 顶部 | 意象优先于断言，且要么美、要么有机锋 | 每片叶子美不美 |

生成层、场面层的方法，提炼自多位创意写作大师公开课程与访谈的精意（见"致谢"），全部以自己的话转述。

## 声口（风格库）

**五个精装 reference**（定调优先推荐；兼作最高美学律的语域示范、与铸造新 reference 的架构模板）：

- **刘仲敬** — 把文明当生态/银行/季候来论说的冷峻史论；描述先行、判断后出，跨文明类比，黑色机锋
- **江南** — 用光影与细腻的生活观察传递情感；对微小瞬间的电影般凝视，忽然膨胀成辽阔与心碎
- **川端康成（中译本质感）** — 物哀与留白，冷与美并置的精微感官，以景结情
- **郭敬明（《小时代》式都市描写）** — 航拍般俯瞰庞大冷艳的都市，光在玻璃与江水间过载流淌
- **班宇** — 东北铁锈带白描，情绪藏在物象里，苦中带笑

**数十个轻量声口目录**（`voice-catalog.md`，四行速写 + 按意图反查）：汪曾祺、张爱玲、王小波、鲁迅、沈从文、余华、莫言、王朔、史铁生、阿城、双雪涛、刘慈欣、金庸；马尔克斯/卡佛/海明威/博尔赫斯/契诃夫/村上/太宰治（中译质感）；《史记》《世说新语》、聊斋、唐宋散文；以及新闻特稿、纪录片旁白、童话等功能性腔调。

**实时提取**（`voice-extraction.md`）：贴任何文本，当场拆成临时声口，用试笔校准，与上述任意声口混搭。

## 最高美学律（设计哲学）

整个 Skill 由一条原则统辖：**意象优先于断言，且每个意象要么美、要么有机锋。**

- ✘ 断言（不美、无画面）："这座城市冷漠地筛选着每一个人。"
- ✔ 意象："地铁卡都是一样的蓝，刷卡的声音也一样脆，可闸机记得每一个人最后停在了哪一站。"

戒掉断言之后还要当心另一个坑：**不美、不幽默的灰扑扑情景描写**。忧伤要带光、带笑、带机锋，不要灰。

## 安装

**Claude Code / Cowork：** 把 `chinese-literary-voices/` 整个文件夹放进你的 skills 目录（如 `~/.claude/skills/`），或在支持的客户端里上传打包好的 `.skill` 文件。

**claude.ai（支持 Skills 的套餐）：** 在 Settings → Capabilities/Skills 上传 `chinese-literary-voices.skill`。

安装后，当你的请求涉及任何文学性中文写作时，Claude 会自动加载本 Skill。

## 使用示例

直接说人话即可，无需记命令：

- "帮我写个短篇，关于我爸下岗那年。" → 触发意图引导 → 推荐班宇底色 → 决策包 → 成稿
- "写一段刘仲敬式的史论，但题材是公司的周会。" → 直接走刘式"伪史论"
- "写得像这样 ——（贴一段你喜欢的文字）—— 帮我写写故乡的夏天。" → 实时提取该文本的声口 → 校准 → 成稿
- "来点张爱玲那种苍凉又华丽的，写两个老同学多年后重逢。" → 调用目录里的张爱玲式
- "我想要类似石黑一雄那种不可靠叙事的克制感。" → 全网检索其文体特征 → 现场建档成临时声口 → 试笔校准后写
- "把下面这段大白话改写得更有画面、更克制。" → 按最高美学律改写

## 文件结构

```
chinese-literary-voices/
├── SKILL.md                      主控：五层架构 / 最高美学律 / 工作流 / 自检清单
├── README.md
└── references/
    ├── intake.md                 意图层：四问、moodboard 推荐、写作决策包
    ├── craft-engine.md           生成层：发生学与生长学（从根到树）
    ├── scene-craft.md            场面层：素材 / 编写 / 承上启下 / 镜头编排
    ├── voice-catalog.md          声口目录：数十个轻量声口 + 按意图反查
    ├── voice-extraction.md       实时声口提取（moodboard）
    ├── blending.md               混搭配方：一底色 + 一调味
    ├── liu-zhongjing.md          精装声口
    ├── jiang-nan.md              精装声口
    ├── kawabata-cn.md            精装声口
    ├── guo-jingming.md           精装声口
    └── ban-yu.md                 精装声口
```

## 致谢

生成层与场面层的方法，提炼自以下创意写作大师公开课程与访谈中的精意，均以自己的话转述、归纳：Neil Gaiman（堆肥堆与汇流、"然后呢"、可信的谎言）、Margaret Atwood（故事与结构、头几页是门、中段升级、修改即重看）、Aaron Sorkin（意图+阻碍=戏剧、施压、手段显人物）、George Saunders / Ursula K. Le Guin / Stephen King（有机生长、跟着能量走、循小径而行）、James Patterson / Dan Brown / R.L. Stine（章节推力与悬念、迟进早出、扣留信息）、Ron Howard / David Fincher（镜头与调度：景别即情绪、特写稀缺、机位即立场）。

## 版权与免责

- 本 Skill 产出的全部文字均为**原创仿写**，用以再现某种**文体风格**；它**不复制、不再现**任何作家的原作语句。
- 各作家声口是对其**文体的研究与致敬**，供创意写作之用，不代表对其本人或观点的背书。
- 关于**刘仲敬**声口：本 Skill 只借用其修辞架构与论说姿态，并明确要求把"文风"与"其具体政治主张"分离——应用于虚构、架空或明确标注为思辨/戏仿的题材，不得把其关于现实族群、国家的特定论断当作客观事实。详见 `references/liu-zhongjing.md` 与 `SKILL.md`。
- 在世作家声口仅取其公开作品所呈现的文体特征。

## License

建议以 **MIT** 许可证发布本仓库的 Skill 文件与文档（代码/提示文本部分）。你可在仓库根目录添加 `LICENSE` 文件。注意：许可证覆盖的是本 Skill 的提示工程与文档，不涉及任何第三方作品的权利。
