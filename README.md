# Latex-template

## Features

- Cross-refs: link of definitions and theorems
- toc, list of theorems, definitions
- bib, hyperlink
- index, glossary
- clean

## Related Tools

### VSCode
Extension: [Latex Workshop by James Yu](https://marketplace.visualstudio.com/items?itemName=James-Yu.latex-workshop)

Setting:
```
```

###  lualatex and latexmk
`.latexmkrc` configuration file
```
$pdflatex = 'lualatex -synctex=1 -interaction=nonstopmode --shell-escape %O %S';
@generated_exts = (@generated_exts, 'synctex.gz');
$pdf_mode = 1;

add_cus_dep('glo', 'gls', 0, 'makeglo2gls');
sub makeglo2gls {
    system("makeindex -s '$_[0]'.ist -t '$_[0]'.glg -o '$_[0]'.gls '$_[0]'.glo");
}
```

## Preview
[Minimal working example](https://github.com/Jue-Xu/Latex-Template-for-Scientific-Style-Book/blob/main/notes_template.pdf)

my study notes
