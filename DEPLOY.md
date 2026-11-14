# Atlascope GitHub Pages

把这个压缩包里的站点文件发布到名为 `atlascope` 的 GitHub 仓库，Pages 地址会是：

`https://<用户名>.github.io/atlascope/`

## 上传内容

除本说明外，压缩包根目录就是站点根目录，包含：

- `index.html`
- `_next/`
- `data/admin-index.json`
- `icon.svg`
- `.nojekyll`

发布时不要再套一层 `atlascope` 文件夹。GitHub 项目页会自动加上 `/atlascope/`，页面里的脚本和样式也按这个路径写好了。

`.nojekyll` 必须保留，否则 Jekyll 会忽略 `_next`。

## 建议设置

1. 仓库名使用 `atlascope`。
2. Settings → Pages → 选择存放这些静态文件的分支和根目录。
3. 打开 `https://<用户名>.github.io/atlascope/`。

浏览器仍会直接请求 `https://geo.datav.aliyun.com` 获取边界。这个静态包没有 Node 服务，也没有 `/api` 路由。

## 数据版本

名称索引抓取于 2026-11-14。全国总图文件时间为 2021-06-29，下级文件集中在 2021-06-04 至 2021-06-29。区县是行政层级，不是测绘精度。台湾省没有下级边界；直辖市由省级直接到区县；没有下级文件的单位不会被补画。

## 静态 HTTP 测试

在把 `out/` 放到名为 `atlascope` 的目录并用静态 HTTP 服务按 `/atlascope/` 访问后，已通过：

- 页面标题和页眉为 Atlascope，行政区名称仍是中文
- 全国 → 河南省 → 南阳市 → 淅川县，代码 411326，路径「全国 / 河南省 / 南阳市 / 淅川县」
- 返回上一级与返回全国
- 北京市 → 东城区
- 台湾省显示数据源没有下级边界
- 搜索「淅川」
- 390×844 手机视口下的河南 → 南阳 → 淅川县
- 全程没有请求 `/api/`
