# 岩土工程报告与论文 LaTeX 模板

本仓库提供两套可复用的中文 LaTeX 母版：

- project-report：岩土工程项目技术报告
- research-paper：岩土工程科研论文

模板适用于边坡支护、基坑支护、场地平整、地基处理、挡土墙、桩基检测、数值分析及 AI 与岩土工程交叉研究。

## 排版约定

- 编译引擎：XeLaTeX
- 中文正文：宋体，系统无宋体时自动使用 FandolSong
- 英文与数字：Times New Roman，系统无该字体时自动使用 TeX Gyre Termes
- 字体颜色：黑色
- 纸张：A4
- 参考文献：GB/T 7714 风格，使用 biblatex-gb7714-2015 与 Biber
- 图表：按章或全文自动编号，表格默认三线表
- 超链接：保留跳转功能，打印颜色统一为黑色

## 目录

    .
    ├── project-report
    │   ├── main.tex
    │   └── references.bib
    ├── research-paper
    │   ├── main.tex
    │   └── references.bib
    ├── latexmkrc
    └── .gitignore

## 编译

推荐安装较新的 TeX Live 或 MiKTeX，并确保已安装：

- ctex
- fontspec
- biblatex-gb7714-2015
- biber
- latexmk
- siunitx
- booktabs
- longtable
- tikz

在仓库根目录执行：

    latexmk -xelatex -cd project-report/main.tex
    latexmk -xelatex -cd research-paper/main.tex

清理中间文件：

    latexmk -c -cd project-report/main.tex
    latexmk -c -cd research-paper/main.tex

也可将对应目录中的 main.tex 与 references.bib 上传至 Overleaf，编译器选择 XeLaTeX。

## 使用建议

项目报告母版的章节顺序为：

工程概况、编制依据、工程地质条件、设计参数、方案比选、计算分析、构造设计、施工要求、检测与监测、风险控制、结论、附录。

科研论文母版的章节顺序为：

中英文摘要、引言、工程背景、理论与方法、模型或试验、结果、讨论、工程应用、结论、参考文献。

正式使用时，应按项目类型、送审要求和目标期刊投稿指南调整章节、页边距、字号、图表格式及参考文献样式。