# Atlascope 高速公路更新

把本包内容上传到 `gh-pages` 根目录。不要 force push `main`。

必须换掉 `_next/` 和 `index.html`，并新增 `highways/`。`geo/` 可保持不动。详见 REPLACE.md。

页面不再请求 geo.datav.aliyun.com 或 OpenStreetMap 在线接口。高速几何已经打进 `highways/`。
