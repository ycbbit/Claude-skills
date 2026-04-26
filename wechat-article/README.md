# wechat-article skill

一个 Claude Code skill，输入材料、链接或只给一个主题，自动生成可直接发布的微信公众号干货文章。

## 功能

- 输入英文或中文材料，按信达雅原则转化为公众号文章
- 输入网页链接，自动抓取正文内容再生成（国内网站可能受网络限制，建议粘贴内容）
- 只给主题，自动输出"资料收集清单"，引导你找到权威来源后再生成文章
- 自动生成 4 个备选标题（数字型、悬念型、直接价值型、观点/判断型）
- 输出纯文本格式，可直接粘贴到公众号编辑器使用
- 固定「冷静分析师」写作风格：句子短、有观点、不激动、结尾泼冷水，拒绝 AI 通用腔
- 内置 AI 腔禁用清单：「值得关注」「颠覆性的」「期待未来」等套话一律禁止
- 结合公众号爆款写作手法：短段落、小标题、口语化、类比
- 字数根据内容自动调整，通常 1200-2500 字

## 适用场景

- AI 技术进展、新功能发布
- 产品介绍、工具评测
- 技术文章的公众号改写
- 播客访谈、人物观点提炼

## 使用方式

在 Claude Code 中直接说：

```
把这篇文章写成公众号：[粘贴内容]
```

```
这个链接写成公众号：https://...
```

```
帮我写一篇关于 Claude 4 发布的公众号
```

只给主题时，skill 会先输出一份资料收集清单，列出官方来源、学术来源和科技媒体的具体搜索建议。你按清单找到 2-3 个链接后粘贴过来，skill 再生成文章。

## 安装

### 方式一：全局安装（所有项目可用）

把 `wechat-article` 文件夹复制到：

- **Windows**：`C:\Users\<你的用户名>\.claude\skills\`
- **macOS / Linux**：`~/.claude/skills/`

### 方式二：项目级安装（仅当前项目可用）

把 `wechat-article` 文件夹复制到项目根目录下的 `.claude/skills/`。

安装后重启 Claude Code，在 `/skills` 对话框中确认 `wechat-article` 已出现即可。

## 文件结构

```
wechat-article/
├── skill.md    # skill 主文件，包含所有指令
└── README.md   # 安装说明
```

## 保存到 GitHub

### 初次上传

```bash
# 在你想存放 skill 的目录下初始化仓库
cd ~/.claude/skills   # 或者单独建一个目录

git init
git add wechat-article/
git commit -m "add wechat-article skill"

# 在 GitHub 新建一个仓库，然后：
git remote add origin https://github.com/<你的用户名>/<仓库名>.git
git push -u origin main
```

### 更新已有仓库

```bash
git add wechat-article/
git commit -m "update wechat-article skill"
git push
```

### 从 GitHub 安装到新机器

```bash
# 克隆仓库
git clone https://github.com/<你的用户名>/<仓库名>.git

# 把 skill 文件夹复制到 Claude Code 的 skills 目录
cp -r <仓库名>/wechat-article ~/.claude/skills/
```

## 注意事项

- 国内网站链接（163、微博、知乎等）因网络限制通常无法直接抓取，建议复制文章内容粘贴
- 英文网站（arxiv、GitHub、Anthropic 官网等）一般可以正常抓取
- 生成内容基于输入材料，不会凭空补充数据或观点
