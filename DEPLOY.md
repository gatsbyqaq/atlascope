# Atlascope 修复版静态站

把本压缩包的内容上传到 `gh-pages` 根目录，覆盖同名文件。不要 force push `main`。

站点地址仍是 `https://gatsbyqaq.github.io/atlascope/`。

必须整目录换掉 `_next/`，并新增 `geo/` 与 `DATA-LICENSE.txt`。详见 `REPLACE.md`。

边界从同源 `/atlascope/geo/{行政区代码}_full.json` 读取，不再请求 geo.datav.aliyun.com。
