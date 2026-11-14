# 相对当前 gh-pages 需要替换的文件

当前线上分支已有行政区 `geo/`。这次只增加高速公路，并更新引用新脚本的页面文件。

## 整目录替换
- `_next/`（旧哈希不能留）

## 替换
- `index.html`
- `DATA-LICENSE.txt`
- `DEPLOY.md`
- `REPLACE.md`

## 新增
- `highways/` 全部 JSON（全国线、分省线与出口、搜索索引）

## 不用改
- `geo/`
- `data/admin-index.json`
- `.nojekyll`
- `icon.svg`

最大单文件应低于 25MB。高速数据来自 OpenStreetMap，ODbL。
