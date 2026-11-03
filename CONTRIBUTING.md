# 参与贡献 · Contributing

这个仓库的价值在于**准确**，不在于长。

## 可以提的

- 入口 404、跳到无关页面、改成必须付费
- 链接属性变了（例如 dofollow 改成 nofollow）
- 站点停服或变成垃圾站
- 新增渠道：必须是**你自己真实发成过**的免费渠道

## 不接受

- 没验证过的批量网址
- 付费渠道、要求互链或放 Badge 的渠道
- 自己产品的推广链接
- 同一站点换个入口重复提交

## 提交时请附

1. 改的是哪条（`site` + `submit_url`）
2. 退出登录后能看到链接的公开页地址，或截图
3. 核实日期

## 改数据

以 `data/backlinks.csv` 为准，字段说明见 [README](README.md#字段说明)。改完同步更新 `backlinks.md` 对应行。

---

**English:** Accuracy over length. Report broken, now-paid or changed-attribute entries via issue or PR. New sources must be free and actually submitted by you; include the public page (logged out) and the date. Edit `data/backlinks.csv` and the matching row in `backlinks.md`. No paid, reciprocal-link, badge or self-promotional entries.
