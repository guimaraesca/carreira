---
marp: true
theme: default
paginate: true
size: 16:9
header: 'Governança de dados educacionais · Carlos Artur Guimarães'
footer: 'github.com/guimaraesca/carreira · L1'
style: |
  section { font-size: 24px; padding: 52px 64px; line-height: 1.38; }
  h1 { color: #1f3a5f; }
  h2 { color: #1f3a5f; border-bottom: 2px solid #c9d6e3; padding-bottom: 6px; margin-bottom: 18px; }
  h3 { color: #8a3b12; margin: 10px 0 4px; }
  strong { color: #8a3b12; }
  table { font-size: 19px; }
  blockquote { border-left: 4px solid #8a3b12; color: #33414f; font-size: 22px; }
  section.capa { background: #1f3a5f; color: #fff; }
  section.capa h1, section.capa h2 { color: #fff; border: 0; }
  section.bloco { background: #eef3f8; }
  section.bloco h1 { font-size: 46px; }
  section.denso { font-size: 20px; }
  section.denso table { font-size: 17px; }
  section.ref { font-size: 16px; line-height: 1.3; }
  .fonte { font-size: 15px; color: #5b6b7a; }
---

<!-- _class: capa -->
<!-- _header: '' -->
<!-- _footer: '' -->

# Governança de dados educacionais
## Da escola ao sistema nacional: como o dado chega à decisão

Aula · 90 minutos · nível pós-graduação
Carlos Artur Guimarães — Mestre em Inovação em Tecnologias Educacionais (PPGITE/UFRN)

<!--
Apresentação: 1 minuto. Situar quem fala: PO de sistemas de gestão pedagógica em escala estadual (SIGAE) e nacional (SGP). A aula combina fundamentos, marco legal brasileiro, dois casos reais e um exercício.
-->

---

## Objetivos de aprendizagem

Ao final da aula, você será capaz de:

1. **Distinguir** governança de dados, gestão de dados e governança de TI no contexto educacional.
2. **Comparar** quatro referenciais — ISO/IEC 38500, DAMA-DMBOK, COBIT 2019 e SABER-EMIS — e saber quando usar cada um.
3. **Situar** o marco legal brasileiro: LGPD, ECA, governo digital e a Portaria MEC nº 234/2025.
4. **Analisar** dois casos de sistemas em escala (estadual e nacional) a partir de tensões reais de governança.
5. **Aplicar** uma matriz de maturidade para diagnosticar uma rede de ensino e propor um roteiro de 90 dias.

---

## Roteiro

| Bloco | Conteúdo | Tempo |
|---|---|---|
| 0 | Pergunta disparadora | 5 min |
| 1 | Conceitos: dado administrativo, EMIS, governança, qualidade | 15 min |
| 2 | Referenciais: ISO 38500, DMBOK, COBIT, SABER-EMIS | 15 min |
| 3 | Contexto brasileiro: federalismo, LGPD, Gestão Presente | 15 min |
| 4 | Casos: SIGAE (6 redes) e SGP (escala nacional) | 15 min |
| 5 | Método: matriz de maturidade e diagnóstico | 5 min |
| 6 | Estudo de caso em grupos + debate | 20 min |

---

## Pergunta disparadora

> Uma secretaria tem sistema de matrícula, sistema de frequência, planilhas de profissionais e envia o Censo Escolar todo ano. Mesmo assim, o secretário não consegue responder em uma semana: **quantos estudantes estão em risco de abandono hoje, por escola?**

**Em duplas (3 min):** o problema é de tecnologia, de processo ou de pessoas?

<!--
Recolher 3 respostas rápidas. Em geral aparecem as três. A aula vai mostrar que a resposta é "governança": quem decide o quê sobre o dado, com que regra e com que responsabilidade.
-->

---

<!-- _class: bloco -->

# Bloco 1
## Conceitos

---

## Dado administrativo educacional

- É produzido **para operar** a escola (matricular, enturmar, registrar frequência, pagar, distribuir livro) — não para pesquisar.
- Por isso é **abundante, contínuo e barato**, mas também **heterogêneo, incompleto e sensível** (dados de crianças e adolescentes).
- Quando o mesmo dado passa a **condicionar direitos** (bolsa, incentivo, livro), sua qualidade deixa de ser questão técnica e vira questão de justiça.

**Implicação:** governar dado educacional é governar um insumo de política pública, não um arquivo.

---

## EMIS — Education Management Information System

> "Um sistema institucionalizado, de múltiplas facetas, composto por tecnologia e arranjos institucionais para coletar, processar e disseminar dados educacionais." — Abdul-Hamid (2014, tradução livre)

**Três ideias que a definição carrega:**
- **Mais que um banco de dados:** inclui pessoas, normas e rotinas.
- **Institucionalizado:** sobrevive à troca de gestão.
- **Orientado ao uso:** só cumpre o papel se a informação volta para quem decide.

<!--
Enfatizar a armadilha mais comum: comprar um sistema e chamar isso de EMIS.
-->

---

## Governança × gestão de dados × governança de TI

| | Pergunta central | Quem responde | Exemplo na rede |
|---|---|---|---|
| **Governança de dados** | Quem decide o quê sobre os dados, com que autoridade? | alta gestão + comitês | definir quem é dono do cadastro de estudantes |
| **Gestão de dados** | Como executar as decisões no dia a dia? | equipes técnicas e de negócio | rotina de validação de CPF e correção de duplicidades |
| **Governança de TI** | A tecnologia entrega valor com risco aceitável? | alta gestão | decidir internalizar ou terceirizar o sistema |

Governança de dados é o **exercício de autoridade e controle sobre a gestão de dados** (DAMA International, 2017; Abraham; Schneider; vom Brocke, 2019).

---

## Cinco domínios de decisão (Khatri; Brown, 2010)

| Domínio | Pergunta | Na educação |
|---|---|---|
| **Princípios** | Para que servem os dados? | apoiar a trajetória do estudante, não só prestar contas |
| **Qualidade** | Que nível de qualidade é exigido? | frequência precisa para pagar incentivo |
| **Metadados** | Como os dados são descritos? | dicionário do conjunto mínimo de dados |
| **Acesso** | Quem pode ver o quê? | escola vê seus estudantes; MEC vê o país |
| **Ciclo de vida** | Quanto tempo guardar, quando descartar? | guarda até o fim do vínculo, depois pseudonimização |

<!--
Este quadro será reutilizado no exercício final. Pedir para anotarem.
-->

---

## Qualidade de dados é multidimensional

Wang e Strong (1996) mostraram que qualidade, para quem usa o dado, vai muito além da exatidão:

| Categoria | Dimensões | Pergunta típica na rede |
|---|---|---|
| **Intrínseca** | exatidão, objetividade, credibilidade | o CPF está correto? |
| **Contextual** | relevância, atualidade, completude | a frequência de ontem já está no sistema? |
| **Representacional** | interpretabilidade, consistência | "abandono" significa o mesmo em todas as redes? |
| **Acessibilidade** | acesso, segurança | o diretor consegue ver o painel da escola? |

---

## Uma armadilha: quando o indicador vira meta

> "Quanto mais um indicador social quantitativo é usado para tomar decisões sociais, mais ele estará sujeito a pressões de corrupção e mais tenderá a distorcer os processos sociais que deveria monitorar." — Campbell (1979, tradução livre)

- Frequência que **libera pagamento** cria incentivo a registrar presença.
- Matrícula que **define repasse** cria incentivo a manter cadastro de quem saiu.

**Governança responde com:** trilha de auditoria, cruzamento com outras bases, devolutiva às redes e uso pedagógico além do uso financeiro.

---

## Ética: dado de estudante não é dado qualquer

Slade e Prinsloo (2013) apontam dilemas que valem para qualquer sistema educacional:

- **Finalidade:** o dado coletado para matricular pode ser usado para prever evasão?
- **Rotulação:** o estudante "em risco" passa a ser tratado como "problema"?
- **Transparência:** famílias sabem o que é coletado e para quê?
- **Poder:** quem decide, e quem é decidido pelos dados?

**Princípio de trabalho:** o dado apoia a decisão da equipe; não substitui o julgamento pedagógico.

---

<!-- _class: bloco -->

# Bloco 2
## Referenciais

---

## ISO/IEC 38500 — governança da tecnologia

**Modelo:** a alta gestão **avalia**, **dirige** e **monitora** (Evaluate–Direct–Monitor).

**Seis princípios:**

| Princípio | Leitura para uma secretaria |
|---|---|
| Responsabilidade | papéis claros sobre sistemas e dados |
| Estratégia | sistemas a serviço do plano educacional |
| Aquisição | contratar com critério, prevendo saída do fornecedor |
| Desempenho | o sistema entrega o que a rede precisa |
| Conformidade | LGPD, ECA, normas de controle |
| Comportamento humano | quem usa participa do desenho |

<!--
Bom para conversar com a alta gestão: linguagem de decisão, não de tecnologia.
-->

---

## DAMA-DMBOK — o corpo de conhecimento em gestão de dados

**Governança de dados no centro**, cercada por dez áreas:

| | | |
|---|---|---|
| Arquitetura de dados | Modelagem e desenho | Armazenamento e operações |
| Segurança | Integração e interoperabilidade | Documentos e conteúdo |
| Dados mestres e de referência | Data warehouse e BI | Metadados |
| **Qualidade de dados** | | |

**Uso prático:** checklist de capacidades. Uma rede pequena não precisa de todas, mas precisa saber quais está deixando de lado.

<p class="fonte">DAMA International (2017).</p>

---

## COBIT 2019 — dados dentro da governança corporativa

- Separa **governança** (objetivos EDM — avaliar, dirigir, monitorar) de **gestão** (planejar, construir, executar, monitorar).
- Desde 2019 traz um objetivo específico: **APO14 — Dados gerenciados**.
- Útil quando a secretaria já usa práticas de controle interno, auditoria ou gestão de riscos — fala a língua dos órgãos de controle.

**Cuidado:** é um referencial extenso. Em redes de baixa maturidade, usar como **dicionário**, não como roteiro.

---

## SABER-EMIS — o referencial específico da educação

| Área de política | Pergunta | Exemplo de evidência |
|---|---|---|
| **Ambiente habilitador** | Há base legal, orçamento, pessoas e infraestrutura? | norma que institui o sistema; equipe dedicada |
| **Solidez do sistema** | Processos e estruturas sustentam um sistema abrangente? | integração entre bases; dicionário de dados |
| **Dados de qualidade** | Os dados são exatos, seguros, confiáveis e tempestivos? | regras de validação; relatórios de erro |
| **Uso para decisão** | A informação é usada por quem decide? | painéis usados em reuniões de gestão |

**Escala:** latente → emergente → estabelecido → avançado.

<p class="fonte">Abdul-Hamid (2014). Banco Mundial, SABER Working Paper n. 7.</p>

---

<!-- _class: denso -->

## Qual referencial usar, e quando?

| | ISO/IEC 38500 | DAMA-DMBOK | COBIT 2019 | SABER-EMIS |
|---|---|---|---|---|
| **Foco** | governança de TI | gestão de dados | governança e gestão de TI | sistemas de informação educacional |
| **Público** | alta gestão | equipes de dados | controle, auditoria, TI | gestores de política educacional |
| **Nível de detalhe** | princípios | capacidades | objetivos e práticas | áreas e rubricas |
| **Melhor uso** | pactuar responsabilidades | montar a equipe e o catálogo | dialogar com controle | diagnóstico e comparação internacional |
| **Limite** | não fala de dado educacional | não fala de política | extenso | pouco operacional |

**Combinação que funciona:** SABER-EMIS para o diagnóstico, ISO 38500 para pactuar com a alta gestão, DMBOK para organizar a equipe.

---

<!-- _class: bloco -->

# Bloco 3
## Contexto brasileiro

---

## O desafio federativo

- A LDB (Lei nº 9.394/1996) organiza a educação em **regime de colaboração**: União, 26 estados, DF e mais de 5.500 municípios têm redes próprias.
- Cada rede escolheu (ou não) seu sistema de gestão: há redes com API, redes com planilha e escolas sem conexão estável.
- O **Censo Escolar** (INEP) dá uma fotografia anual comparável — mas não acompanha a trajetória mês a mês.

**Consequência:** o desafio nacional não é criar um sistema, é **fazer sistemas diferentes falarem a mesma língua** sem tirar a autonomia das redes.

---

## Marco legal

| Norma | O que exige da governança de dados educacionais |
|---|---|
| **LGPD** (Lei nº 13.709/2018), art. 14 | tratamento de dados de crianças e adolescentes no seu **melhor interesse** |
| **Enunciado CD/ANPD nº 1/2023** | admite as bases legais dos arts. 7º e 11 (não só consentimento), sempre priorizando o melhor interesse |
| **ECA** (Lei nº 8.069/1990) | proteção integral; privacidade e imagem |
| **Governo Digital** (Lei nº 14.129/2021) | interoperabilidade, dados abertos, governo como plataforma |
| **Decreto nº 10.046/2019** | regras de compartilhamento de dados na administração federal |
| **Lei nº 14.818/2024** (Pé-de-Meia) | frequência como condição de incentivo financeiro |

---

## Portaria MEC nº 234/2025 — Gestão Presente

Institui uma **plataforma de dados da educação básica**. Componentes (art. 5º):

| Componente | O que é | Adesão |
|---|---|---|
| **SGP** — Sistema Gestão Presente | núcleo estruturante; API para integrar sistemas locais | opcional |
| **CMDEB** — Conjunto Mínimo de Dados da Educação Básica | dados que todas as redes e escolas devem coletar | obrigatório |
| **GPE** — Gestão Presente na Escola | módulo gratuito de gestão escolar (diário, turmas, estudantes) | opcional |
| **Comitê Tripartite** | União, estados e municípios coordenam a implementação | — |

**Princípios (art. 2º):** simplificação, colaboração federativa, segurança e proteção de dados, transparência, equidade, decisão baseada em evidência.

---

## Governança de dados dentro da Portaria

- **Classes de dados** (art. 13): referência, cadastrais, situacionais e complementares.
- **Registro de operações** (art. 22): o sistema guarda trilha automática.
- **Ciclo de vida** (art. 24): dados pessoais guardados até o fim do vínculo com a educação básica; depois descartados ou **pseudonimizados**.
- **Acesso por papel** (art. 26): cada ente vê os dados da sua rede.
- **Responsabilidade** (art. 28): a rede responde pela licitude, exatidão e atualização dos seus dados.
- **Transparência** (art. 21): aviso de privacidade em linguagem simples, inclusive material para crianças.

**Leitura:** a Portaria materializa os cinco domínios de Khatri e Brown em norma.

<!--
Exercício mental: pedir que localizem cada domínio (princípios, qualidade, metadados, acesso, ciclo de vida) nos artigos citados.
-->

---

<!-- _class: bloco -->

# Bloco 4
## Casos

---

## Caso 1 · SIGAE — gestão pedagógica em seis redes estaduais

**Contexto:** plataforma de gestão pedagógica e learning analytics do Instituto Unibanco, usada por CE, ES, GO, MG, PI e RS — mais de 3 mil escolas e cerca de 120 mil usuários.

**Meu papel (2023–2025):** Product Owner e analista de dados sênior.

**Decisões de governança:**
- Integração de Censo Escolar, IDEB e SAEB em pipelines R/Python, com regras únicas para as seis redes.
- Roadmap pactuado com as secretarias — a prioridade era da rede, não do produto.
- **Formação de mais de 50 gestores públicos** no uso de dados para a gestão pedagógica.

---

## SIGAE · o que o caso ensina

| Tensão | Como apareceu | Resposta adotada |
|---|---|---|
| **Padronizar × respeitar a rede** | seis redes, seis calendários e modelos de gestão | núcleo comum de indicadores + configurações por rede |
| **Ferramenta × uso** | painel pronto, pouca consulta | formação de gestores como parte do produto |
| **Dado externo × dado próprio** | IDEB e SAEB têm defasagem | combinar resultado oficial com dado de rotina da escola |

**Na linguagem do SABER-EMIS:** o caso mostra avanço na área **uso para decisão** — a mais difícil de mover.

---

## Caso 2 · SGP — uma base nacional para a educação básica

**Escala:** mais de 19 milhões de estudantes, 32,5 milhões de matrículas, 1 milhão de profissionais e 1.750 redes.

**Arranjo institucional:** governança tripartite entre a Secretaria de Educação Básica, o NEES/UFAL (execução técnica) e a Dataprev (infraestrutura).

**Meu papel (2025–2026):** Product Owner e consultor sênior de governança e transformação digital — regras de negócio, roadmap, integrações e instrumental de governança (ISO/IEC 38500, COBIT, DAMA).

<!--
Falar de método e lições; não detalhar conteúdo de produtos contratados nem dados internos.
-->

---

## SGP · como o dado circula

| Etapa | O que acontece | Princípio de governança |
|---|---|---|
| **Envio** | a rede envia por API (sistema próprio) ou por planilha | múltiplos canais, **uma única regra** de validação |
| **Validação** | cada registro é checado contra o conjunto mínimo | ingestão total, parcial ou rejeitada — com relatório de erros devolvido |
| **Qualificação** | dados conferidos com bases de referência | a qualidade é contínua, não pontual |
| **Uso** | frequência, trajetória, programas (Pé-de-Meia, PNLD) | o dado volta para quem decide |

**Princípio central:** o sistema **sinaliza** inconsistências; quem corrige é a rede, que é a **detentora da verdade** sobre seus dados.

---

## SGP · problemas reais de qualidade (e o que ensinam)

| Problema típico | Causa | Lição |
|---|---|---|
| CPF com 10 dígitos | planilha eletrônica remove o zero à esquerda | formatar como texto; validar na origem |
| Erros "invisíveis" | linhas ocultas na planilha | relatório de erro legível, por linha |
| Vínculos duplicados de profissionais | ordem de processamento das cargas | regras de movimentação, não só de cadastro |
| Estudante sem CPF | documentação incompleta da família | o dado faltante pode excluir de um direito |
| Mesmo estudante em duas redes | transferência não registrada | sinalizar e mediar, não sobrescrever |

**Leitura:** a maior parte dos problemas é **processual**, não tecnológica.

---

## SGP · princípios que emergiram

1. **Entregar em vez de pedir:** devolver à rede o que já se sabe (por exemplo, do Censo) e pedir só o que falta reduz carga e erro.
2. **Uma regra, vários canais:** API e planilha passam pelas mesmas validações.
3. **Autorização explícita no regime de colaboração:** município que usa o sistema do estado autoriza o compartilhamento.
4. **Internalização com responsabilidades pactuadas:** matriz RACI antes de mudar quem opera.
5. **Atendimento é parte da governança:** plantões e canais de suporte geram o mapa real de dores.

---

## Tensões que nenhum caso resolve sozinho

- **Centralização × autonomia federativa:** base nacional forte sem tirar da rede a propriedade do dado.
- **Uso financeiro × uso pedagógico:** frequência que paga incentivo também precisa servir à escola (lembrar Campbell).
- **Escala × contexto:** regras nacionais precisam funcionar em escola sem conexão estável.
- **Contrato × aprendizado:** requisitos fixados em contrato envelhecem; governança precisa prever mudança contínua.

**Para debate:** qual dessas tensões é mais crítica na rede em que você atua?

---

<!-- _class: bloco -->

# Bloco 5
## Método

---

## Matriz de maturidade em três dimensões

| Dimensão | O que observa | Nível 0 | Nível 4 |
|---|---|---|---|
| **Cultura e gestão** | liderança, papéis, capacidade técnica, relação com escolas | ninguém responde pelo dado | papéis formais e equipe dedicada |
| **Processos e regulação** | LGPD, políticas, coleta, validação, privacidade | sem norma nem rotina | política aprovada e auditada |
| **Tecnologia e operação** | sistemas, qualidade, interoperabilidade, autonomia | planilhas soltas | integração por API com monitoramento |

**Correspondência com o SABER-EMIS:** cultura ↔ ambiente habilitador e uso; processos ↔ dados de qualidade; tecnologia ↔ solidez do sistema.

<!--
A matriz é instrumento de diagnóstico, não produto final. Evidência em cada nível orienta o plano de ação por dimensão.
-->

---

## Diagnóstico em quatro etapas

| Etapa | Pergunta | Produto | Duração |
|---|---|---|---|
| **1. Escuta** | Quem produz, usa e decide com o dado? | mapa de atores e fluxos | 2 semanas |
| **2. Inventário** | Que dados existem, onde, com que qualidade? | catálogo de dados críticos com responsáveis | 3 semanas |
| **3. Avaliação** | Em que nível está cada dimensão? | matriz preenchida com evidências | 2 semanas |
| **4. Direção** | O que mudar primeiro? | roadmap de 12–18 meses + oficina com a equipe | 3 semanas |

**Base metodológica:** Design Science Research — problema, artefato, avaliação com quem usa, aprendizado.

---

## Indicadores de governança

| Indicador | Por que importa |
|---|---|
| % de dados críticos com responsável formal | sem dono, ninguém corrige |
| Completude dos campos-chave (CPF, data de nascimento, turma) | condição para direitos e programas |
| Tempo médio de correção de inconsistências | mede a capacidade da rede de responder |
| % de fluxos com base legal LGPD documentada | conformidade e confiança das famílias |
| Uso de painéis em reuniões de gestão | mede a área mais difícil: uso para decisão |

**Regra:** a linha de base é medida no próprio diagnóstico.

---

<!-- _class: bloco -->

# Bloco 6
## Estudo de caso

---

## Rede Municipal de Vale Novo (caso fictício)

- 42 escolas, 18 mil estudantes, 1.100 profissionais.
- Matrícula em sistema comprado há 6 anos; frequência em diário de papel em 30 escolas.
- Envia o Censo Escolar com apoio de consultoria externa.
- Aderiu à plataforma nacional; 12% dos estudantes estão sem CPF no cadastro.
- Não há norma municipal sobre dados nem encarregado de dados nomeado.
- O secretário quer um painel de risco de abandono "em 60 dias".

<!--
Caso composto a partir de situações frequentes em redes municipais; não corresponde a nenhuma rede real.
-->

---

## Tarefa dos grupos (15 min)

1. **Classifiquem** a rede nas três dimensões da matriz (níveis 0–4), com uma evidência para cada.
2. **Identifiquem**, nos cinco domínios de Khatri e Brown, qual é o mais frágil.
3. **Respondam ao secretário:** o painel em 60 dias é viável? O que precisa acontecer antes?
4. **Proponham** três ações para os próximos 90 dias — uma por dimensão.

**Critérios de avaliação:** coerência entre diagnóstico e ações · uso dos referenciais · atenção a LGPD/ECA · viabilidade.

---

## Debate (5 min)

- O CPF faltante é problema da secretaria de educação ou de toda a prefeitura?
- Faz sentido construir o painel antes de resolver a frequência em papel?
- Quem deveria ser o encarregado de dados da rede — educação, TI ou controle interno?
- Como evitar que o painel de risco vire um rótulo para os estudantes?

---

## Síntese

1. **EMIS é instituição**, não software: pessoas, normas e rotinas.
2. **Governança decide; gestão executa** — e as duas precisam de dono.
3. **Qualidade é contextual:** o mesmo dado pode ser bom para estatística e ruim para pagar um direito.
4. **No Brasil, governar dado é governar o federalismo:** padronizar sem tirar a autonomia das redes.
5. **A área mais difícil é o uso:** sem formação de gestores, o melhor sistema vira arquivo.

---

## Leituras recomendadas

- **Abdul-Hamid (2014)** — o referencial SABER-EMIS, com rubricas aplicáveis.
- **Abraham, Schneider e vom Brocke (2019)** — revisão estruturada e agenda de pesquisa em governança de dados.
- **Khatri e Brown (2010)** — artigo curto e seminal sobre os domínios de decisão.
- **Portaria MEC nº 234/2025** — leitura integral, com atenção aos arts. 13 a 30.
- **Slade e Prinsloo (2013)** — dilemas éticos que valem para qualquer sistema com dados de estudantes.

---

<!-- _class: ref -->

## Referências

ABDUL-HAMID, H. **What matters most for education management information systems**: a framework paper. Washington, DC: World Bank, 2014. (SABER Working Paper Series, n. 7).

ABRAHAM, R.; SCHNEIDER, J.; VOM BROCKE, J. Data governance: a conceptual framework, structured review, and research agenda. **International Journal of Information Management**, v. 49, p. 424-438, 2019.

BRASIL. Lei nº 8.069, de 13 de julho de 1990. Estatuto da Criança e do Adolescente. **Diário Oficial da União**, Brasília, 1990.

BRASIL. Lei nº 9.394, de 20 de dezembro de 1996. Diretrizes e bases da educação nacional. **Diário Oficial da União**, Brasília, 1996.

BRASIL. Lei nº 13.709, de 14 de agosto de 2018. Lei Geral de Proteção de Dados Pessoais. **Diário Oficial da União**, Brasília, 2018.

BRASIL. Decreto nº 10.046, de 9 de outubro de 2019. Governança no compartilhamento de dados no âmbito da administração pública federal. **Diário Oficial da União**, Brasília, 2019.

BRASIL. Lei nº 14.129, de 29 de março de 2021. Governo Digital. **Diário Oficial da União**, Brasília, 2021.

BRASIL. Lei nº 14.818, de 16 de janeiro de 2024. Incentivo financeiro-educacional (Pé-de-Meia). **Diário Oficial da União**, Brasília, 2024.

BRASIL. Ministério da Educação. Portaria nº 234, de 2 de abril de 2025. Institui o MEC Gestão Presente. **Diário Oficial da União**, Brasília, 3 abr. 2025.

---

<!-- _class: ref -->

## Referências (cont.)

AUTORIDADE NACIONAL DE PROTEÇÃO DE DADOS (ANPD). **Enunciado CD/ANPD nº 1, de 22 de maio de 2023**. Tratamento de dados pessoais de crianças e adolescentes. Brasília: ANPD, 2023.

CAMPBELL, D. T. Assessing the impact of planned social change. **Evaluation and Program Planning**, v. 2, n. 1, p. 67-90, 1979.

DAMA INTERNATIONAL. **DAMA-DMBOK**: data management body of knowledge. 2. ed. Basking Ridge: Technics Publications, 2017.

GUIMARÃES, C. A. et al. A produção de learning analytics e predição de desempenho acadêmico por pesquisadores brasileiros: uma revisão sistemática da literatura. In: CONGRESSO SOBRE TECNOLOGIAS NA EDUCAÇÃO (Ctrl+E), 5., 2020. **Anais** [...]. p. 306-315.

ISACA. **COBIT 2019 framework**: governance and management objectives. Schaumburg: ISACA, 2018.

INTERNATIONAL ORGANIZATION FOR STANDARDIZATION. **ISO/IEC 38500:2015**: information technology — governance of IT for the organization. Geneva: ISO, 2015.

KHATRI, V.; BROWN, C. V. Designing data governance. **Communications of the ACM**, v. 53, n. 1, p. 148-152, 2010.

SLADE, S.; PRINSLOO, P. Learning analytics: ethical issues and dilemmas. **American Behavioral Scientist**, v. 57, n. 10, p. 1510-1529, 2013.

WANG, R. Y.; STRONG, D. M. Beyond accuracy: what data quality means to data consumers. **Journal of Management Information Systems**, v. 12, n. 4, p. 5-33, 1996.

---

## Sobre o professor

**Carlos Artur Guimarães** — Mestre em Inovação em Tecnologias Educacionais (PPGITE/UFRN), Bacharel em Gestão de Políticas Públicas e Licenciado em Filosofia (UFRN). Product Owner de sistemas de gestão pedagógica em escala estadual e nacional; consultor em cooperação técnica internacional desde 2021.

carlosarturguimaraes@protonmail.com · linkedin.com/in/carlosarturguimaraes · ORCID 0000-0003-0885-3916

*Os casos descrevem escopo, método e escala; não reproduzem produtos técnicos de contratos.*
