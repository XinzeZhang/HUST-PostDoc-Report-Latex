# 华中科技大学博士后出站报告 LaTeX 模板

本仓库是基于华中科技大学博士学位论文 LaTeX 模板改编的**博士后研究工作报告**模板，包含封面、声明、题名页、中英文摘要、目次、图表清单、符号表、正文、参考文献、成果、简历和附录的通用示例。仓库中的姓名、研究内容、年份和成果均为占位示例，使用前请自行替换。

学校提供的报告编写示范中，部分排版细节在使用中仍有可以优化的空间。本模板结合编写规则和实际排版需求进行了调整，**并未与示范逐页、逐项严格一比一复刻**。模板文件仅供参考，最终格式规范和提交要求以学校及相关管理部门的现行规定为准。

## 编译

需要包含 XeLaTeX、BibTeX 和 TeX Gyre 字体的完整 TeX Live / MacTeX。项目根目录运行：

```bash
xelatex main
bibtex main
xelatex main
xelatex main
```

也可使用 `latexmk -xelatex main.tex` 或 VS Code LaTeX Workshop 中的 XeLaTeX + BibTeX 配方。更改图表或参考文献后可能需要多次编译，以更新清单、页码和引用。

## Word 版本提交

华中科技大学博士后研究工作报告提交需提供 **Word 版本**。本模板编译生成的是 PDF，不会自动生成 Word 文档；从 PDF 转换为 Word 版本需要使用者自行手动完成，并检查转换后的公式、图表、分页和格式是否符合学校要求。

## 使用

- 在 `body/cover.tex` 修改中英文标题、姓名、流动站、专业、合作导师、时间、摘要和关键词。
- 在 `main.tex` 调整章节、图表清单及符号表的顺序；在 `body/chapter/` 编写正文、成果、简历和通信地址，在 `body/appendix/` 编写附录。
- `body/denotation.tex` 是符号表，`ref/example.bib` 是参考文献示例；参考文献使用 `gbt7714-2025.bst` 顺序编码样式。
- 插图和附表清单由 `\caption` 自动生成。题名较长时可使用 `\caption[清单短题名]{完整题名}`。
- 本模板使用 LaTeX 排版声明页。签署前请核对学校现行声明原文；如需替换为签字扫描件，可在 `main.tex` 中使用 `\includepdf`。

## 版式说明

摘要和目次的左右边距为 20 mm；目次之后的左右边距参考清华博士后模板设为 30 mm，上边距 30 mm、下边距 25 mm。正文使用小四宋体风格，章节标题使用黑体风格。正文自动从右页开始，必要时插入无页码的空白页，正文页码从 1 起。

1994 年《博士后研究报告编写规则》要求左边距不少于 35 mm，正文一般使用四号宋体，并要求参考文献从右页开始。当前模板的左右边距、正文字号和参考文献起始位置与该旧规则存在差异，请以学校现行要求为准并按需调整。

中文默认使用 `fonts/` 中按 SIL Open Font License 授权的 Noto Serif SC 和 Noto Sans SC，西文使用 TeX Live 自带的 TeX Gyre Termes。字形与学校示范或系统宋体、黑体可能有差别；若有合法可用的指定字体，可在 `HUSTthesis.cls` 中调整。学校示范文件、标准文档及签字声明原件请通过学校或相应发布机构获取。

中文字体来自 Google Fonts 的 [Noto Serif SC](https://github.com/google/fonts/tree/main/ofl/notoserifsc) 和 [Noto Sans SC](https://github.com/google/fonts/tree/main/ofl/notosanssc)；仓库内文件由其可变字体生成 400、700 两个静态字重，对应的 SIL Open Font License 文本保存在 `fonts/` 中。

## 来源、感谢与许可

本项目基于 [华中科技大学博士学位论文 LaTeX 模板 HUST-PhD-Thesis-Latex](https://github.com/XinzeZhang/HUST-PhD-Thesis-Latex) 的 V3.2.0.X 改编，感谢该版本的所有贡献者。

博士后报告版式参考了 [清华大学学位论文 LaTeX 模板 ThuThesis](https://github.com/tuna/thuthesis/) 中的博士后报告模板，包括正文左右页边距、封面信息与研究工作时间的排布，以及插图清单、附表清单的组织方式。感谢 ThuThesis 的作者、维护者和贡献者。

模板类文件保留原作者的贡献与版权声明，按 Perl Artistic License 分发；参考文献样式 `gbt7714-2025.bst` 的许可见该文件开头的 LaTeX Project Public License 声明。使用者应分别遵守各文件的许可。

维护者：xinze.zh@outlook.com
