# 活学汉语 · Live Chinese

> 学「活」的汉语 —— 每日俚语、真实对话、语言对战。
> Learn Chinese that's actually alive.

**🌐 在线使用：<https://lusialii.github.io/huoxue-hanyu/>**

---

## 这是什么

课本里的汉语是「死」的，真实生活里的汉语每天都在变。

「活学汉语」是一个面向中文学习者的轻量学习网站，把焦点放在**当下正在被使用的汉语**上：今天人们在群聊里、弹幕里、短视频评论里真正会说的那些话。

## 功能模块

| 模块 | 路由 | 说明 |
| --- | --- | --- |
| **Today** 今日俚语 | `/` | 每天一条真实语境中的网络热词 / 俚语，配例句、出处与用法说明 |
| **Slang deck** 俚语卡组 | `/slang` | 按场景与难度分类的俚语合集，可逐条标记已掌握 |
| **AI friend** 对话练习 | `/chat` | 与 AI 进行情景对话，在真实交流中练反应 |
| **Battle** 语言对战 | `/battle` | 限时抢答式词汇对战，比分数、拼速度 |
| **Growth** 成长中心 | `/growth` | XP 等级、连续打卡天数与学习进度总览 |

## 关于账号

进入网站需先注册（用户名 + 密码），注册后为**独立的学习进度**：学过的词、对战胜利、XP、连续打卡天数都分开记录，刷新或关闭浏览器都不会丢。

- 账号与进度**保存在浏览器本地**（`localStorage`），没有服务器，不收集、不上传任何个人信息。
- 密码经过加盐哈希处理后再存储，不保存明文。
- ⚠️ 换设备、换浏览器或清除浏览器缓存后，需要用同一用户名重新注册，进度会重新开始。

## 本地运行

需要 Node.js 18 及以上。

```bash
npm install
npm run dev      # 本地预览 http://localhost:5173
npm run build    # 打包到 dist/
npm run preview  # 预览打包结果
```

## 技术栈

React 18 · TypeScript · Vite · Tailwind CSS · React Router · lucide-react

## 部署

站点为纯静态应用，构建产物在 `dist/`，可托管于任意静态服务器（GitHub Pages / 对象存储 / CDN 均可）。

部署到子路径（如 `https://用户名.github.io/仓库名/`）时，构建需加 `--base=./`，同时把 `index.html` 复制一份为 `404.html` 作为单页应用的回退页：

```bash
npx vite build --base=./ --outDir dist-ghpages
cp dist-ghpages/index.html dist-ghpages/404.html
```

---

## English

**Live Chinese** is a lightweight web app for learners of Mandarin. Instead of textbook Chinese, it focuses on the language people actually use today — daily slang, real conversations, and competitive vocabulary drills.

Five modules: **Today** (a daily slang drop), **Slang deck** (browsable collection), **AI friend** (scenario dialogue practice), **Battle** (timed vocabulary duels), and **Growth** (XP, streaks and progress).

Accounts and progress are stored locally in the browser — no server, no personal data collected.

---

*本站为教学用途项目，俚语内容持续更新。*
