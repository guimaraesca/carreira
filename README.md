# Carreira — Carlos Artur Guimarães

Governança de dados e tecnologias educacionais para redes públicas de ensino.

Este repositório reúne as **apresentações dos cases** das cinco linhas de produto do meu portfólio. Os slides são escritos em Markdown ([Marp](https://marp.app/)), podem ser lidos direto no GitHub e exportados para HTML, PDF ou PPTX.

## Apresentações

| # | Linha | Arquivo |
|---|---|---|
| 0 | Visão geral | [slides/00_visao_geral.md](slides/00_visao_geral.md) |
| L1 | Governança de dados educacionais | [slides/L1_governanca_dados_educacionais.md](slides/L1_governanca_dados_educacionais.md) |
| L2 | Trajetória do estudante e evasão | [slides/L2_trajetoria_e_evasao.md](slides/L2_trajetoria_e_evasao.md) |
| L3 | Computação na educação e formação docente | [slides/L3_computacao_e_formacao_docente.md](slides/L3_computacao_e_formacao_docente.md) |
| L4 | IA e tecnologia na educação | [slides/L4_ia_e_tecnologia_na_educacao.md](slides/L4_ia_e_tecnologia_na_educacao.md) |
| L5 | Política educacional, resultados e financiamento (em construção) | [slides/L5_politica_resultados_financiamento.md](slides/L5_politica_resultados_financiamento.md) |

## Gerar os slides

```bash
npx @marp-team/marp-cli@4.0.3 --input-dir slides/ --html --output dist/      # HTML
npx @marp-team/marp-cli@4.0.3 --input-dir slides/ --pdf --output dist/      # PDF
npx @marp-team/marp-cli@4.0.3 --input-dir slides/ --pptx --output dist/      # PowerPoint
```

Ao enviar para a branch `main`, o workflow `.github/workflows/slides.yml` gera o HTML e publica no GitHub Pages (ative em *Settings → Pages → Source: GitHub Actions*).

## Sobre o conteúdo

- Os cases descrevem **escopo, método, papel e escala** de trabalhos realizados. Não reproduzem produtos técnicos de contratos, que pertencem às instituições contratantes.
- Nenhum logotipo institucional é usado.
- Números de escala vêm de informações públicas ou já divulgadas no meu currículo.

## Contato

carlosarturguimaraes@protonmail.com · [LinkedIn](https://www.linkedin.com/in/carlosarturguimaraes) · ORCID [0000-0003-0885-3916](https://orcid.org/0000-0003-0885-3916) · [Lattes](http://lattes.cnpq.br/8972138029785555)
