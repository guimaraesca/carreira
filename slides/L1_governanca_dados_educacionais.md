---
marp: true
theme: default
paginate: true
size: 16:9
header: 'Carlos Artur Guimarães · L1 · Governança de dados educacionais'
footer: 'github.com/guimaraesca/carreira'
style: |
  section { font-size: 25px; padding: 56px 64px; }
  h1 { color: #1f3a5f; }
  h2 { color: #1f3a5f; border-bottom: 2px solid #c9d6e3; padding-bottom: 6px; }
  strong { color: #8a3b12; }
  table { font-size: 21px; }
  section.capa { background: #1f3a5f; color: #fff; }
  section.capa h1, section.capa h2 { color: #fff; border: 0; }
---

<!-- _class: capa -->
<!-- _header: '' -->
<!-- _footer: '' -->

# Governança de dados educacionais
## Da escola ao sistema nacional: como fazer o dado chegar à decisão

Carlos Artur Guimarães
Linha de produto L1

<!--
Abertura: apresentar a linha como o eixo mais antigo e mais comprovado da trajetória. Tom: técnico, sem jargão de consultoria.
-->

---

## O problema

- Redes de ensino produzem **muitos dados**, mas decidem com **pouca informação**.
- Os sistemas nascem por programa; os dados não conversam entre si.
- Falta clareza sobre **quem é dono** de cada dado, quem pode usá-lo e com que qualidade.
- A LGPD chegou antes da maturidade de gestão: o risco cresce junto com o volume.

**Pergunta da linha:** como transformar registros administrativos em instrumento de política pública — com qualidade, segurança e uso real?

---

## Onde atuei nesta linha

| Período | Instituição | Papel | Escala |
|---|---|---|---|
| 2012–2021 | IMD/UFRN | Coordenação de tutoria EAD (Moodle) | cursos técnicos a distância |
| 2023–2025 | Instituto Unibanco | Product Owner do SIGAE · Analista de Dados Sênior | 6 redes estaduais · +3 mil escolas · ~120 mil usuários |
| 2025–2026 | MEC/SEB · cooperação UNESCO | Product Owner do SGP · Governança e Transformação Digital | +19 mi estudantes · 1.750 redes |

---

## Case 1 · SIGAE — gestão pedagógica em seis redes estaduais

**Situação:** plataforma de gestão pedagógica e learning analytics usada por CE, ES, GO, MG, PI e RS.

**O que fiz:**
- Product Owner: roadmap, priorização e implantação em larga escala com as secretarias.
- Integrei Censo Escolar, IDEB e SAEB em pipelines R/Python.
- Formei **mais de 50 gestores públicos** no uso de dados para a gestão pedagógica.

**Resultado:** maior adoção pelas redes e indicadores de aprendizagem na rotina de decisão das secretarias parceiras.

<!--
Ponto-chave: o dado só gera valor quando o gestor sabe usá-lo. A formação de gestores fazia parte do produto, não era acessório.
-->

---

## Case 2 · SGP — a base cadastral-pedagógica nacional

**Situação:** o Sistema de Gestão Pedagógica é a espinha dorsal do Programa MEC Gestão Presente: **+19 milhões de estudantes, 32,5 milhões de matrículas, 1 milhão de profissionais, 1.750 redes**.

**Contexto institucional:** ecossistema de três sistemas nacionais (SGP, GPE e GPEI) operado em governança tripartite — Secretaria de Educação Básica, NEES/UFAL (execução técnica) e Dataprev (infraestrutura).

**Meu papel:** Product Owner e consultor sênior de governança e transformação digital.

---

## SGP · o que foi feito

- Validação de regras de negócio, repactuação de roadmap e priorização de requisitos.
- Análise de **trajetória do estudante**: pipelines sobre +55 milhões de registros de frequência.
- Integração a bases nacionais via API: CadÚnico, Pé-de-Meia, Busca Ativa Escolar, PNLD.
- Internalização em nuvem: matriz RACI, arquitetura API-first, integração ao registro civil.
- Instrumental de governança: ISO/IEC 38500, COBIT, DAMA-DMBOK, matriz operacional e mapa de riscos.

**Resultado:** marco de go-live com critérios de qualidade, privacidade e monitoramento que alinharam as três instituições.

<!--
Não detalhar conteúdo de produtos contratados; falar de método e escala.
-->

---

## O que aprendi governando dados em escala nacional

1. **Governança é acordo entre instituições**, não só tecnologia.
2. O dado mais caro é o que ninguém se responsabiliza por corrigir.
3. Integração sem regra de negócio clara multiplica erro.
4. Privacidade precisa estar no desenho, não na auditoria.
5. Sem uso pelo gestor, o melhor sistema vira arquivo.

---

## Método

**ISO/IEC 38500** — avaliar, dirigir, monitorar
**DAMA-DMBOK** — áreas de conhecimento: qualidade, metadados, segurança, arquitetura, integração
**Design Science Research** — problema → artefato → avaliação → aprendizado

| Etapa | Pergunta | Produto |
|---|---|---|
| Escuta | Quem usa, produz e decide com o dado? | Mapa de atores e fluxos |
| Inventário | Que dados existem, onde e com que qualidade? | Catálogo inicial |
| Avaliação | Qual o nível de maturidade por dimensão? | Diagnóstico |
| Direção | O que mudar primeiro? | Roadmap 12–18 meses |

---

## Base acadêmica

- **Mestrado em Inovação em Tecnologias Educacionais** (PPGITE/UFRN, 2025) — disciplinas de Análise da Aprendizagem e de Ambientes e Sistemas Colaborativos para Educação.
- **Gestão de Políticas Públicas** (UFRN, 2019) — TCC sobre o Portal de Transparência do TCE-RN.
- **RSL sobre Learning Analytics e predição de desempenho** (Ctrl+E, 2020).
- **Bacharelado em Ciência de Dados** em andamento (UNIVESP).

---

## A oferta · Diagnóstico de Maturidade de Governança de Dados para Redes de Ensino

**Para quem:** secretarias estaduais e municipais, institutos e organismos que apoiam redes.
**Duração:** 60 a 90 dias.

**Entregáveis:**
1. Mapa de atores, fluxos e sistemas.
2. Catálogo inicial de dados críticos (com responsáveis).
3. Diagnóstico de maturidade por dimensão.
4. Roadmap priorizado de 12 a 18 meses.
5. Oficina com a equipe da rede para apropriação.

---

## Como medir se funcionou

| Indicador | Antes | Depois |
|---|---|---|
| Dados críticos com responsável definido | ? | meta pactuada |
| Completude de campos-chave | ? | meta pactuada |
| Tempo para responder a uma demanda de dados | ? | meta pactuada |
| Fluxos com base legal LGPD documentada | ? | meta pactuada |

A linha de base é sempre medida no próprio diagnóstico.

---

## Cuidados

- Nenhum dado pessoal sai da rede: o diagnóstico trabalha com metadados e amostras anonimizadas.
- Conformidade com a LGPD e o ECA desde o primeiro dia.
- Recomendações proporcionais à capacidade real da equipe.
- Tecnologia é meio: o roadmap começa por processos e responsabilidades.

---

## Em síntese

**Atuei onde o dado nasce (escola), onde ele é agregado (rede estadual) e onde ele vira política (sistema nacional).**

Essa visão completa é o que ofereço às redes: governança que funciona na prática.

carlosarturguimaraes@protonmail.com · linkedin.com/in/carlosarturguimaraes · ORCID 0000-0003-0885-3916
