# TCC SintonIA — projeto LaTeX (template UnB-CIC)

Conversão da monografia do SintonIA para o template LaTeX do Departamento de Ciência da
Computação da UnB (classe `UnB-CIC`, opção `engenharia`), pronta para compilar no Overleaf.

## Como usar no Overleaf

1. Compacte esta pasta `tcc-latex/` em um `.zip`.
2. No Overleaf: **New Project → Upload Project** e selecione o `.zip`.
3. Em **Menu → Settings**, defina o compilador como **pdfLaTeX** e o **Main document**
   como `monografia.tex`.
4. Clique em **Recompile**. A bibliografia usa BibTeX (`bibliografia.bib`, estilo
   `babunsrt`); o Overleaf roda BibTeX automaticamente.

## Estrutura

- `monografia.tex` — arquivo mestre: dados da capa/folha de rosto e inclusão dos capítulos.
- `UnB-CIC.cls` — a classe do template (não editar).
- `bibliografia.bib` — todas as referências (BibTeX), com chaves `autorAno`.
- `tex/` — capítulos e front matter:
  - `resumo.tex`, `abstract.tex`, `dedicatoria.tex`, `agradecimentos.tex`, `siglas.tex`
  - `1_Introducao.tex` … `9_AspectosEticos.tex`
  - `AnexoA.tex` … `AnexoD.tex`
- `img/`, `doc/` — logos e recursos usados pela classe.
- `figuras/` — coloque aqui as imagens reais do trabalho.

## O que ainda falta preencher (marcado no texto)

1. **Capa** (`monografia.tex`): nome do(a) **coordenador(a)** do curso e o **dia** da defesa
   (`\diamesano{XX}{julho}{2026}`).
2. **Figuras**: o texto usa `\figuraplaceholder{legenda}{label}`, que mostra uma caixa
   "[Inserir imagem]" e mantém a referência funcionando. Ao ter a imagem real, suba o arquivo
   em `figuras/` e troque, por exemplo:
   ```latex
   \figuraplaceholder{Balança de bioimpedância modelo CF577BLE}{fig:balanca}
   ```
   por:
   ```latex
   \figura{figuras/balanca}{Balança de bioimpedância modelo CF577BLE}{fig:balanca}{width=.7\linewidth}
   ```
   Figuras a inserir: `fig:balanca`, `fig:resistencias`, `fig:arquitetura`, `fig:fluxo`,
   `fig:fluxoslm`, `fig:tela`, `fig:whatsapp`.
3. **Números reais** na Seção 6.10 (tempos de resposta, nº de medições), se disponíveis.
4. **Dedicatória** e **agradecimentos**: textos de exemplo, ajuste ao gosto de vocês.

## Observações

- Este projeto é a conversão do conteúdo já revisado do `.docx`. Confira os dados
  bibliográficos completos de algumas referências (as clássicas — Kyle, Lukaski, Kushner,
  Heymsfield, Hooker — foram preenchidas com dados aproximados e estão marcadas no `.bib`).
- Se a banca exigir uma **Conclusão** como capítulo próprio, basta criar `tex/10_Conclusao.tex`
  e adicionar `\capitulo{10_Conclusao}{Conclusão}` no `monografia.tex`.
