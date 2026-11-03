# 免费外链清单 · 给 agent 自动发

![免费外链清单：交给 agent 每天自动发](assets/hero-zh.png)

![GitHub Stars](https://img.shields.io/github/stars/HiAPIAI/free-backlinks-for-agents?style=for-the-badge&logo=github&label=Stars&color=2563eb)
![License](https://img.shields.io/github/license/HiAPIAI/free-backlinks-for-agents?style=for-the-badge&color=7c3aed)

**语言：** 简体中文 · [English](README_en.md)

**206 个免费外链渠道，每一个都是我们的 agent 真实注册、提交、再退出登录核对过的。** 另有 9 个入口已核实、还没发的站单独列出。把仓库丢给 GrokBot、Claude Code 或 Codex，它自己注册、收验证邮件、提交，每天接着跑。

## 目录

- [快速开始](#快速开始)
- [清单一览](#清单一览)
- [字段说明](#字段说明)
- [收录标准](#收录标准)
- [手动使用](#手动使用)
- [参与贡献](#参与贡献)
- [常见问题](#常见问题)

## 快速开始

把下面这段发给你的 agent：

```text
读 https://github.com/HiAPIAI/free-backlinks-for-agents ，
按 skills/submit-backlinks 每天给我的产品发 8–10 条免费外链。

产品：<产品名>
官网：<https://example.com>

注册用你自己的邮箱，验证码自己去收件箱取。
每天凌晨 1 点自动跑，跑完给我日报。
```

agent 会先读 [data/backlinks.csv](data/backlinks.csv) 挑站，跳过 [已知走不通的站](skills/submit-backlinks/references/known-blocked.md)，每条做完都不登录复核一次链接能不能点。

## 清单一览

完整表格：**[backlinks.md](backlinks.md)**

| 分类 | 数量 | 是什么 | 提交方式 |
|---|---:|---|---|
| [AI 工具目录](backlinks.md#ai-tools) | 72 | 收录 AI 产品的导航站 | 多数填表即可，不少免登录 |
| [产品 / 软件目录](backlinks.md#products) | 48 | SaaS、软件替代品、评测、上线榜 | 填表或注册后提交产品页 |
| [网站目录](backlinks.md#web) | 16 | 通用网址导航 | 填表提交 |
| [账号主页](backlinks.md#profiles) | 70 | 代码托管、作品集、链接主页、文档分享等平台的个人主页 | 注册账号，在主页或简介里放链接 |
| [入口已核实、还没发过](backlinks.md#entry-verified) | 9 | 页面写明免费，我们还没提交 | 见表内说明 |

## 字段说明

`backlinks.md` 是给人看的，`data/backlinks.csv` 是给 agent 筛选用的，字段一致：

| 字段 | 含义 |
|---|---|
| `site` | 站点名 |
| `submit_url` | 提交入口或注册入口 |
| `category` | `ai-tools` / `products` / `web` / `profiles` |
| `submit_method` | 怎么拿到链接：填表、主页放链接、提 PR 等 |
| `needs_account` | `yes` 要注册 · `no` 免登录 · `unknown` 没记录 |
| `link_rel` | `dofollow` / `nofollow` / `untested`。只有我们退出登录后亲眼看过页面源码的才写 dofollow 或 nofollow |
| `monthly_visits` | 整站月访（Semrush / Traffic.cv 估算），只作参考 |
| `last_submitted` | 我们最近一次在这个站发成的日期 |
| `status` | `submitted` 发成过 · `to-recheck` 待复核（⏳） · `entry-verified` 入口核过、没发过 |

常用筛选：

- 只要 dofollow：`link_rel == dofollow`
- 不想注册账号：`needs_account == no`
- 先挑流量大的：按 `monthly_visits` 倒序

## 收录标准

**收：**

- 免费就能拿到一个公开、可点击的链接
- 我们自己的 agent 真实发成过，或者提交页写明免费且我们打开核过（单独放在「还没发过」）

**不收：**

- 必须付费、或免费档要排很久才上线的
- 要求互链、放 Badge 的
- 只能用 Google / GitHub / 手机号 / 实名注册的
- 博客评论区（基本都是 nofollow，还容易被当垃圾）
- 退出登录后看不到链接的
- 未经验证的批量网址

## 手动使用

不用 agent 也行：打开 [backlinks.md](backlinks.md)，从你所在领域相关的分类开始，每天做几个。每个站准备好：产品名、一句话介绍、100 字左右的简介、官网链接、Logo。账号主页类注意填「网站 / Website」字段，或在简介里写完整网址。

## 参与贡献

欢迎更正和补充，详见 [CONTRIBUTING.md](CONTRIBUTING.md)：

- 入口失效、改成收费、链接变成 nofollow：开 [Issue](../../issues/new/choose) 或直接提 PR
- 新增渠道：必须是你自己真实发成过的免费渠道，附上提交日期和退出登录后能看到链接的公开页

## 常见问题

**外链有用吗？** 单个目录站的权重有限，价值在于数量、相关度和长期积累。先发和你产品领域相关的分类。

**会不会被当成垃圾外链？** 每个站只发一次，文案按站点写，不复制粘贴同一段；不碰评论区和链接农场。

**为什么有的写着「—」？** 表示我们没亲眼核过链接属性，不代表是 nofollow。

## 许可

[MIT](LICENSE) · 维护：[HiAPI](https://www.hiapi.ai)
