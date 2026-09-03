# 字帖生成器 · 通用规范汉字表

# https://zitie-acd.pages.dev

零构建、可离线使用的汉字字帖（描红 / 临写）生成器，基于《通用规范汉字表（2013）》7909 个标准汉字。

## 功能

- **选字来源**：一级 / 二级 / 三级字表、全部、自定义文本、随机抽 N 字
- **格子**：田字格 / 米字格 / 空白格
- **模式**：临写（首字示范）/ 描红（淡红可描）/ 空临
- **字体**：楷书 / 行楷 / 隶书 / 宋体 / 黑体
- **拼音标注**（cnchar）、**笔画数筛选**
- 每行字数、每字重复、字号、A4 竖 / 横、自定义标题
- 一键**打印 / 导出 PDF**
- **保存图片** / **批量导出 ZIP**（html-to-image + JSZip）
- 点击字格**演示笔顺**（Hanzi Writer）
- **移动端自适应**

## 本地运行

无需构建，任选其一：

```bash
# 方式一：Python 起一个静态服务器
python3 -m http.server 8000
# 然后浏览器打开 http://localhost:8000

# 方式二：直接用浏览器打开 index.html
```

> 拼音、笔画筛选、图片导出、笔顺演示依赖 CDN（cnchar / html-to-image / JSZip / Hanzi Writer），首次使用需联网；随机抽、格子、打印等核心功能离线可用。

## 数据

源数据来自 [shengdoushi/common-standard-chinese-characters-table](https://github.com/shengdoushi/common-standard-chinese-characters-table)。
原始三级字表含有少量 CJK 扩展区（Ext-B）非标准字符，本仓库已过滤为纯 BMP 标准汉字，共 **7909** 字（`data.js` 由 `level-1/2/3.txt` 生成）。

## 技术

纯静态单页应用：HTML + 原生 JS，无框架、无构建步骤。

## License

[MIT](LICENSE)
