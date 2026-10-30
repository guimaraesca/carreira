---
marp: true
theme: default
paginate: true
size: 16:9
header: 'Carlos Artur Guimarães · L2 · Trajetória do estudante e evasão'
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

# Trajetória do estudante e evasão
## Da frequência à ação: dados para proteger quem está prestes a sair da escola

Carlos Artur Guimarães
Linha de produto L2

---

## O problema

- A evasão raramente é um evento: é um **processo** que deixa sinais (faltas, reprovação, distorção idade-série, vulnerabilidade social).
- Os sinais estão espalhados em sistemas diferentes e chegam tarde à escola.
- Quando chegam, faltam fluxo de ação e equipe preparada para agir.

**Pergunta da linha:** como transformar sinais dispersos em proteção concreta da trajetória escolar?

---

## Onde atuei nesta linha

| Período | Instituição | Papel |
|---|---|---|
| 2019–2020 | IMD/UFRN | Pesquisa em learning analytics e predição de desempenho em curso técnico |
| 2023–2025 | Instituto Unibanco | Indicadores de aprendizagem na rotina das secretarias (SIGAE) |
| 2025–2026 | Instituto Sapien · Goiás 2050 | Cientista de dados — frente de Capital Humano |
| 2025–2026 | MEC/SEB · cooperação UNESCO | Análise de trajetória do estudante no SGP |
| 2026–2027 | OEI · SEDUC-RS | Consultor sênior — Política de Proteção à Trajetória do Estudante |

---

## Case 1 · Learning analytics e predição de desempenho

**Situação:** o conhecimento tardio das dificuldades em Matemática gerava retenção e evasão em um curso técnico de TI a distância.

**O que fiz:** revisão sistemática da produção brasileira sobre learning analytics e predição de desempenho (Ctrl+E, 2020) e desenho de abordagem preditiva para o curso.

**Aprendizado:** prever não basta — o valor está no que a equipe faz com o alerta.

---

## Case 2 · Goiás 2050 — capital humano e evasão no ensino médio

**Situação:** plano estratégico de longo prazo do estado de Goiás, dimensão Capital Humano.

**O que fiz:**
- Pipelines em Python e R sobre IBGE, PNAD, CAGED e RAIS.
- Dashboards no Google Looker.
- Análises de fragilidade do capital humano em regiões vulneráveis, evasão no ensino médio e integração escola–educação técnica–trabalho.

**Resultado:** diagnósticos e indicadores para decisões de investimento em capital humano.

---

## Case 3 · Trajetória do estudante em escala nacional

**Situação:** o SGP reúne a vida escolar de mais de 19 milhões de estudantes.

**O que fiz:**
- Análise de trajetória sobre **+55 milhões de registros de frequência**.
- Integração com bases de proteção social e permanência: CadÚnico, Pé-de-Meia, Busca Ativa Escolar.

**Por que importa:** é a primeira vez que frequência, programas sociais e trajetória podem ser lidos juntos, em escala, para orientar ação nas redes.

<!--
Falar de método e potencial; não apresentar resultados internos do MEC.
-->

---

## Case 4 · Política de Proteção à Trajetória do Estudante (RS)

**Situação:** a rede estadual do Rio Grande do Sul implementa uma política de proteção à trajetória com foco no ensino médio.

**O que faço (2026–2027):** três produtos técnicos para fortalecer as capacidades institucionais da rede —
1. Mapeamento das demandas formativas das equipes.
2. Plano de capacitação.
3. Modelo de qualificação dos Planos de Ação Individual e Territorial.

**Ponte:** leitura de dados de frequência e trajetória + desenho de formação + instrumentos de gestão.

---

## Case 5 · Medindo impacto na escola

**Situação:** projeto de tecnologia em uma escola estadual paulista (Escola Digital e Conectada).

**O que fiz:** análise do IDEB, entrevistas e definição de indicadores de impacto social nas fases de planejamento e fechamento.

**Aprendizado:** impacto se mede com linha de base desde o início — e com cuidado para não atribuir causa ao que é correlação.

---

## O que aprendi

1. Alerta sem fluxo de ação gera frustração.
2. A escola precisa de **poucos indicadores, bem explicados**.
3. O plano individual só funciona com articulação territorial (saúde, assistência, família).
4. Formação da equipe é parte da política, não etapa posterior.
5. Rotular estudantes é um risco real — o desenho precisa protegê-los.

---

## Método

| Camada | Pergunta | Instrumento |
|---|---|---|
| Sinais | Quais sinais antecipam a saída? | Matriz de indicadores (frequência, rendimento, distorção, vulnerabilidade) |
| Leitura | Quem lê o sinal e quando? | Rotina escola–regional–rede |
| Ação | O que se faz com cada nível de risco? | Plano de ação individual e territorial |
| Aprendizado | O que funcionou? | Monitoramento e ajuste trimestral |

Base acadêmica: disciplina de **Análise da Aprendizagem** (mestrado PPGITE/UFRN) e RSL de learning analytics.

---

## A oferta · Playbook de alerta precoce e proteção da trajetória

**Para quem:** secretarias, regionais e institutos que apoiam o ensino médio.
**Duração:** 90 a 120 dias.

**Entregáveis:**
1. Matriz de indicadores ajustada aos dados que a rede já tem.
2. Fluxo de ação por nível de risco.
3. Modelos de plano individual e territorial.
4. Formação das equipes escolares e regionais.
5. Painel de monitoramento simples, com dados agregados.

---

## Como medir se funcionou

- Tempo entre o sinal de risco e a primeira ação.
- Proporção de estudantes em risco com plano individual ativo.
- Retorno de estudantes infrequentes.
- Taxa de abandono por escola e regional, comparada à linha de base.

---

## Cuidados

- Dados pessoais de estudantes ficam na rede; análises externas usam dados agregados.
- LGPD e ECA: finalidade explícita, acesso mínimo, nada de exposição de estudantes.
- Indicador é apoio à decisão da equipe, nunca rótulo.
- Linguagem descritiva: sem atribuir causalidade sem desenho adequado.

---

## Em síntese

**Da pesquisa em learning analytics à política estadual de proteção da trajetória, passando por escala nacional.**

A oferta junta o que costuma estar separado: dado, fluxo de ação e formação da equipe.

carlosarturguimaraes@protonmail.com · linkedin.com/in/carlosarturguimaraes
