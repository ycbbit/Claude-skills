# wechat-article skill

一个 Claude Code skill，输入任意材料（中文、英文或网页链接），自动生成可直接发布的微信公众号干货文章。

## 功能

- 输入英文或中文材料，按信达雅原则转化为公众号文章
- 输入网页链接，自动抓取正文内容再生成（国内网站可能受网络限制，建议粘贴内容）
- 自动生成 3 个备选标题（数字型、悬念型、直接价值型）
- 结合公众号爆款写作手法：短段落、小标题、口语化、类比
- 字数根据内容自动调整，通常 1200-2500 字

## 适用场景

- AI 技术进展、新功能发布
- 产品介绍、工具评测
- 技术文章的公众号改写

## 使用方式

在 Claude Code 中直接说：

```
把这篇文章写成公众号：[粘贴内容]
```

```
这个链接写成公众号：https://...
```

```
帮我写一篇关于 GPT-5 发布的公众号
```

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
└── SKILL.md    # skill 主文件，包含所有指令
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
