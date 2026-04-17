# LaTeX 编译命令

当任务涉及编译、清理或重新生成 ThuThesis LaTeX 项目，而非写作论文正文时，使用本文件。

## 适用范围

以下命令从捆绑的 ThuThesis 项目材料中汇总：

- `thuthesis-v7.5.0/Makefile`
- `thuthesis-v7.5.0/latexmkrc`
- `thuthesis-v7.5.0/README.md`
- `thuthesis-v7.5.0/thuthesis.dtx`

优先使用项目原生命令，再考虑自定义编译流程。

## 默认选择

正常论文编译优先使用 `make thesis` 或 `latexmk <主文件>.tex`。

原因：

- `latexmk` 自动重复运行工具链，直到交叉引用稳定
- 仓库中的 `latexmkrc` 已配置 `xelatex`、`xdvipdfmx`、`bibtex`、`makeindex` 及清理后缀
- 这比手动多遍编译更简单、更少出错

## 主要命令

### 编译论文 PDF

```bash
make thesis
```

通过 Makefile 目标构建 `thuthesis-example.pdf`。

若主论文文件已重命名，更新 `Makefile` 中的 `THESIS` 变量，或直接对实际主文件调用 `latexmk`。

### 编译模板文档

```bash
make doc
```

构建 `thuthesis.pdf`。

### 清理辅助文件

```bash
make clean
```

删除中间文件，保留论文 PDF。

### 同时删除论文 PDF

```bash
make cleanall
```

删除中间文件及 `thuthesis-example.pdf`。

### 完整清理

```bash
make distclean
```

删除生成的 PDF、中间文件、生成的类/样式文件及 `dist/`。

## 直接 latexmk 命令

不想依赖 Makefile 或主文件名已更改时使用。

```bash
latexmk thuthesis-example.tex
latexmk spine.tex
latexmk thuthesis.dtx
latexmk -c
```

说明：

- `latexmk thuthesis-example.tex`：编译论文 PDF
- `latexmk spine.tex`：编译书脊 PDF
- `latexmk thuthesis.dtx`：编译模板手册
- `latexmk -c`：清理辅助文件

## latexmkrc 配置的工具链

捆绑的 `latexmkrc` 配置如下：

- `xelatex -shell-escape -file-line-error -halt-on-error -interaction=nonstopmode -no-pdf -synctex=1`
- `lualatex -shell-escape -file-line-error -halt-on-error -interaction=nonstopmode -synctex=1`
- `xdvipdfmx -q -E`
- `bibtex` 自动使用
- `makeindex` 用于索引生成

这意味着正常的 `latexmk` 运行已与模板预期的引擎链对齐。

## 手动编译流程

仅在 `make` 或 `latexmk` 不可用，或需要显式调试编译序列时使用。

### 重新生成类文件

```bash
xetex thuthesis.ins
```

从源文件重新生成 `thuthesis.cls` 及相关文件。

### 手动编译论文

```bash
xelatex thuthesis-example.tex
bibtex thuthesis-example.aux
xelatex thuthesis-example.tex
xelatex thuthesis-example.tex
```

对于有附录参考文献或特殊索引的项目，手动 BibTeX 遍次可能还包括：

```bash
bibtex thuthesis-example-appendix-a.aux
bibtex thuthesis-example-appendix-b.aux
bibtex thuthesis-example-index.aux
```

### 手动编译书脊

```bash
xelatex spine.tex
```

### 手动编译手册

```bash
xelatex -shell-escape thuthesis.dtx
makeindex -s gind.ist -o thuthesis.ind thuthesis.idx
xelatex -shell-escape thuthesis.dtx
xelatex -shell-escape thuthesis.dtx
```

## 实用建议

1. 若用户只说"编译论文"，优先使用 `make thesis`。
2. 若项目重命名了主 `.tex` 文件，优先使用 `latexmk <实际主文件>.tex`。
3. 若引用或目录陈旧，重新运行 `latexmk` 或使用手动多遍流程。
4. 若用户要求清理构建产物但保留 PDF，使用 `make clean`。
5. 若用户要求从生成源完整重建，先运行 `make distclean`，再重新生成并重建。
6. 每次成功编译论文后，若项目为硕士论文，检查编译后的页数预算：
   - 第 2-4 章应各约 25 页，除非不可避免，否则不超过 30 页。
   - 第 2-4 章每章的 `算例分析 + 本章小结` 应合计 10-15 页。
   - 若无法达到范围，报告实际页数、偏离量及原因。

## 注意事项

1. 模板文档明确建议在修改项目结构前阅读捆绑的手册和示例。
2. 最终格式提交检查时，模板可能依赖 Windows 中文字体；若字体输出有影响，请在目标平台验证。
3. 若 `Makefile` 中的 `THESIS` 仍指向 `thuthesis-example`，`make thesis` 不会自动跟随已重命名的主文件。
