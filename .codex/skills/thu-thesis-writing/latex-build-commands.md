# LaTeX Build Commands

Use this file when the task is about compiling, cleaning, or regenerating a ThuThesis LaTeX project rather than writing thesis prose.

## Scope

These commands are summarized from the bundled ThuThesis project materials:

- `thuthesis-v7.5.0/Makefile`
- `thuthesis-v7.5.0/latexmkrc`
- `thuthesis-v7.5.0/README.md`
- `thuthesis-v7.5.0/thuthesis.dtx`

Prefer project-native commands before inventing a custom compile flow.

## Default Choice

For normal thesis compilation, prefer `make thesis` or `latexmk <main>.tex`.

Reason:

- `latexmk` automatically reruns the toolchain until cross-references settle
- the repo `latexmkrc` already configures `xelatex`, `xdvipdfmx`, `bibtex`, `makeindex`, and cleanup suffixes
- this is simpler and less error-prone than manual multi-pass compilation

## Primary Commands

### Build Thesis PDF

```bash
make thesis
```

Builds `thuthesis-example.pdf` through the Makefile target.

If the main thesis file has been renamed, update the `THESIS` variable in `Makefile`, or call `latexmk` on the actual main file directly.

### Build Template Documentation

```bash
make doc
```

Builds `thuthesis.pdf`.

### Clean Auxiliary Files

```bash
make clean
```

Removes intermediate files while keeping the thesis PDF.

### Remove Thesis PDF Too

```bash
make cleanall
```

Removes intermediate files and `thuthesis-example.pdf`.

### Full Dist Clean

```bash
make distclean
```

Removes generated PDFs, intermediate files, generated class/style files, and `dist/`.

## Direct latexmk Commands

Use these when you do not want to rely on the Makefile or when the main file name changed.

```bash
latexmk thuthesis-example.tex
latexmk spine.tex
latexmk thuthesis.dtx
latexmk -c
```

Interpretation:

- `latexmk thuthesis-example.tex`: build the thesis PDF
- `latexmk spine.tex`: build the spine PDF
- `latexmk thuthesis.dtx`: build the template manual
- `latexmk -c`: clean auxiliary files

## Toolchain Configured By latexmkrc

The bundled `latexmkrc` configures:

- `xelatex -shell-escape -file-line-error -halt-on-error -interaction=nonstopmode -no-pdf -synctex=1`
- `lualatex -shell-escape -file-line-error -halt-on-error -interaction=nonstopmode -synctex=1`
- `xdvipdfmx -q -E`
- `bibtex` auto-usage
- `makeindex` for index generation

This means a normal `latexmk` run is already aligned with the template's expected engine chain.

## Manual Build Flow

Only use this when `make` or `latexmk` is unavailable, or when you need to debug the compile sequence explicitly.

### Regenerate Class File

```bash
xetex thuthesis.ins
```

This regenerates `thuthesis.cls` and related files from the source.

### Manually Build Thesis

```bash
xelatex thuthesis-example.tex
bibtex thuthesis-example.aux
xelatex thuthesis-example.tex
xelatex thuthesis-example.tex
```

For projects with appendix bibliographies or special indexes, manual BibTeX passes may also include:

```bash
bibtex thuthesis-example-appendix-a.aux
bibtex thuthesis-example-appendix-b.aux
bibtex thuthesis-example-index.aux
```

### Manually Build Spine

```bash
xelatex spine.tex
```

### Manually Build Manual

```bash
xelatex -shell-escape thuthesis.dtx
makeindex -s gind.ist -o thuthesis.ind thuthesis.idx
xelatex -shell-escape thuthesis.dtx
xelatex -shell-escape thuthesis.dtx
```

## Practical Guidance

1. If the user just says "compile the thesis", prefer `make thesis`.
2. If the project renamed the main `.tex`, prefer `latexmk <actual-main>.tex`.
3. If references or contents are stale, rerun `latexmk` or use the manual multi-pass flow.
4. If the user asks to clean build artifacts but keep the PDF, use `make clean`.
5. If the user asks for a full rebuild from generated sources, run `make distclean` first, then regenerate and rebuild.

## Cautions

1. The template documentation explicitly recommends reading the bundled manual and example before modifying the project structure.
2. The template may depend on Windows Chinese fonts for final-form submission checking; if font output matters, verify on the target platform.
3. If `THESIS` in `Makefile` still points to `thuthesis-example`, `make thesis` will not automatically follow a renamed main file.
