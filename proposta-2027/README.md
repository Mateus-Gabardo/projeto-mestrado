# Proposta individual de pesquisa — PPGCA/UTFPR, turma 2027

Esta pasta contém o template LaTeX oficial do processo seletivo 2027 e uma configuração inicial para a proposta em elaboração.

- Página oficial do edital: <https://www.utfpr.edu.br/cursos/coordenacoes/stricto-sensu/ppgca-ct/editais/selecao-turma-2027>
- Arquivo original: `template-oficial-ppgca-2027.zip`
- Fonte LaTeX: `latex/main.tex`
- Referências BibTeX: `latex/referencias.bib`

## Configuração atual

O título provisório reflete o tema em exploração: personalização de modelos com poucos dados para detectar risco de hipoglicemia em diabetes tipo 1. O nome do(a) candidato(a), a declaração de uso de IA e o conteúdo das seções estão marcados para preenchimento.

A estrutura segue o modelo do edital: introdução, fundamentação teórica/trabalhos relacionados, metodologia, resultados esperados e referências. O documento deve ter de 3 a 8 páginas, ser exportado em PDF e usar referências em formato ABNT. O edital também exige declarar qualquer uso de inteligência artificial generativa.

## Compilação

Com uma distribuição LaTeX que inclua `abntex2cite`, execute a partir desta pasta:

```text
cd latex
pdflatex main.tex
bibtex main
pdflatex main.tex
pdflatex main.tex
```

Antes de submeter, remova todos os marcadores `[TODO: ...]`, confirme os dados do(a) candidato(a), a declaração de IA, as referências, o limite de páginas e as instruções vigentes do edital. O PDF final deve ser nomeado conforme a regra do edital, por exemplo: `Nome Completo - proposta.pdf`.
