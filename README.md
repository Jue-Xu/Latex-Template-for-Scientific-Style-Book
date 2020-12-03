# Latex-template

## Features

- link of definitions and theorems
- toc, theorem, definition
- bib, hyperlink
- index, glossary

## Tools

### VSCode
extension:
setting:

###  lualatex and latexmk

.latexmkrc
```
$pdflatex = 'lualatex -synctex=1 -interaction=nonstopmode --shell-escape %O %S';
@generated_exts = (@generated_exts, 'synctex.gz');
$pdf_mode = 1;

add_cus_dep('glo', 'gls', 0, 'makeglo2gls');
sub makeglo2gls {
    system("makeindex -s '$_[0]'.ist -t '$_[0]'.glg -o '$_[0]'.gls '$_[0]'.glo");
}
```