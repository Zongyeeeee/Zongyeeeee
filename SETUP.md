# 🚀 GitHub 主页部署指南

这套文件就是你的「GitHub 个人主页」。GitHub 有个隐藏机制：**当一个仓库的名字和你的用户名完全一样时，它的 `README.md` 会显示在你的个人主页顶部。**

> ⚠️ 先确认用户名：本模板假定你的 GitHub 用户名是 **`Zongyeeeee`**。
> 如果不是，请用编辑器全局替换 `README.md`、`SETUP.md`、`snake.yml` 里所有 `Zongyeeeee` 为你的真实用户名。

---

## 步骤一：创建「特殊仓库」

1. 打开 https://github.com/new
2. **Repository name** 填 **与你用户名一模一样**（例：`Zongyeeeee`）
   - 填对了 GitHub 会提示一句 ✨ *You found a secret! Zongyeeeee/Zongyeeeee is a special repository...*
3. 勾选 **Public**（必须公开，否则主页不显示）
4. 勾选 **Add a README file**
5. 点 **Create repository**

## 步骤二：上传这套文件

把本文件夹里的内容传上去（二选一）：

**方式 A — 网页拖拽（最简单）**
- 进仓库 → `Add file` → `Upload files` → 把 `README.md` 拖进去 → Commit
- `.github/workflows/snake.yml` 因为带文件夹，建议用方式 B

**方式 B — 命令行**
```bash
cd /Users/jin/Desktop/Zongyeeeee
git init
git add .
git commit -m "✨ my awesome profile"
git branch -M main
git remote add origin https://github.com/Zongyeeeee/Zongyeeeee.git
git push -u origin main
```

## 步骤三：点亮贪吃蛇 🐍

贪吃蛇是用 GitHub Actions 自动生成的，需要让 Action 跑一次：

1. 进仓库 → 顶部 **Actions** 标签
2. 第一次进会让你确认启用 workflow，点 **I understand my workflows, enable them**
3. 左侧选 **Generate Snake Animation** → 右侧 **Run workflow** 手动跑一次
4. 跑完后会自动生成一个 `output` 分支，README 里的蛇图就会出现
   - 之后每 12 小时自动刷新，无需再管

> 如果蛇图一直裂图：去 Settings → Actions → General → Workflow permissions，
> 选 **Read and write permissions** 保存，再重跑一次 Action。

---

## 🎨 想改样式？

| 想改什么 | 怎么改 |
|---|---|
| 配色主题 | `README.md` 里把 `theme=dracula` 换成 `radical`/`tokyonight`/`synthwave` 等，并同步改 `color=`/`title_color=` 的十六进制色值 |
| 顶部大字 | 改 capsule-render 链接里 `text=Hi%2C%20I'm%20Zongye`（空格用 `%20`，逗号用 `%2C`） |
| 打字机文案 | 改 readme-typing-svg 链接里 `lines=...`（多行用 `;` 分隔，空格用 `+`） |
| 技术栈徽章 | 在「技术栈」区按 shields.io 格式增删，logo 名见 https://simpleicons.org |
| 自我介绍 | 直接改「关于我 / About Me」那几行 |

主题色速查（Dracula）：
`bd93f9` 紫 · `ff79c6` 粉 · `50fa7b` 绿 · `8be9fd` 青 · `f8f8f2` 白字 · `282a36` 底色

---

## ✅ 用到的服务（全部免费、无需注册）

- **capsule-render** — 顶部/底部波浪横幅
- **readme-typing-svg** — 打字机动画
- **github-readme-stats** — 统计卡 + 语言占比
- **streak-stats (demolab)** — 连续提交火焰
- **github-readme-activity-graph** — 贡献曲线
- **Platane/snk** — 贪吃蛇 GitHub Action
- **shields.io / komarev** — 徽章 / 访客计数
