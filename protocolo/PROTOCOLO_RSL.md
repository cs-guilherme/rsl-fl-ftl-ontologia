# Protocolo da Revisão Sistemática da Literatura

Artigo: Transferência de Conhecimento Baseada em Ontologia em Federated Learning e Federated Transfer Learning: Mapeamento de Padrões de Degradação sob Perturbações Controladas nos Dados
Autor: Guilherme Sena de Oliveira
Data: 27/10/2026

## 1. Busca exploratória anterior

Entre junho e julho de 2026 foi feita uma busca exploratória somente na Web of Science. Ela teve uma única base, não registrou data nem campo de busca, exportou só parte dos resultados de dois eixos e fez apenas a triagem por título e resumo. Por isso, não foi usada como resultado da revisão: serviu para reformular a estratégia descrita neste protocolo. Os artigos relevantes daquela busca reapareceram na busca definitiva e foram triados de novo, com os mesmos critérios dos demais.

## 2. Questões da revisão

**Questão principal:** o que a literatura recente reporta sobre o uso de ontologias e de harmonização semântica em Federated Learning (FL) e Federated Transfer Learning (FTL), e sobre a robustez desses pipelines a variações controladas nos dados?

Questões por eixo:

- **QR1 (E1):** como ontologias e harmonização semântica têm sido usadas em FL e FTL, com que papel (alinhamento de esquemas, enriquecimento de atributos, transferência de conhecimento) e com que tipo de avaliação?
- **QR2 (E2):** quais abordagens de FTL tratam a heterogeneidade entre domínios (incluindo métodos baseados em protótipos, como o FedProto) e como medem o efeito da transferência?
- **QR3 (E3):** como a robustez de FL a variações nos dados (ruído, mudança de distribuição, qualidade dos dados, dados sintéticos) tem sido medida?
- **QR4 (E4):** que métodos existem para introduzir perturbações controladas e gerar dados sintéticos em dados tabulares, para avaliar a degradação de modelos?
- **QR5 (E5, complementar):** há trabalhos que usam ontologias de ITSM (ITIL, ISO/IEC 20000) como base para aprendizado de máquina?

**PICO**

| Elemento | Definição |
|---|---|
| P (população) | Pipelines de FL e FTL com dados distribuídos e heterogêneos entre domínios |
| I (intervenção) | Enriquecimento ontológico ou harmonização semântica dos dados |
| C (comparação) | Pré-processamento convencional, sem ontologia; dados sob perturbações controladas |
| O (desfecho) | Desempenho preditivo e robustez (degradação do desempenho sob variação dos dados) |

## 3. Bases e período

- **Bases obrigatórias:** Scopus, Web of Science (Coleção Principal), IEEE Xplore e ACM Digital Library (ACM Full-Text Collection).
- **Acesso:** Portal de Periódicos da CAPES, via CAFe (o endereço da base deve passar por `ez67.periodicos.capes.gov.br` ou similar).
- **Período:** 2021 a 2026, em todas as bases (filtro por ano, e não "últimos 5 anos", para a busca ser reproduzível).
- **Campos:** título, resumo e palavras-chave.
- **Tipos de documento:** artigo de periódico, artigo de conferência e revisão.
- **Idiomas:** inglês e português.
- **Fontes complementares (opcional, registrar à parte):** Google Scholar (para conferir artigos-chave), arXiv (preprints muito recentes) e referências dos artigos incluídos (snowballing).

## 4. Estratégia em duas rodadas

Segue a orientação recebida na disciplina de Metodologia de Pesquisa Científica: começar restrito, ler, recalibrar e ampliar.

1. **Rodada 1 (restrita):** strings da seção 5. Resultado esperado: poucos artigos, muito próximos do tema.
2. **Leitura e recalibração:** ler os artigos incluídos na rodada 1, anotar termos e sinônimos que aparecem neles e não estão nas strings.
3. **Rodada 2 (ampliada):** strings da seção 6, ajustadas com os termos da recalibração. As mudanças e o motivo de cada uma ficam registrados na seção 10.

Se um eixo retornar pouco nas quatro bases, isso é um resultado: comprova que o tema é pouco explorado, e os números entram no texto como evidência.

## 5. Strings da rodada 1 (restrita)

As strings evitam curinga dentro de expressões entre aspas, para funcionarem igual nas quatro bases. O curinga só aparece em palavra solta (`ontolog*` cobre ontology, ontologies, ontological).

### Conceitos de cada eixo

| Eixo | Bloco A | Bloco B | Bloco C |
|---|---|---|---|
| E1: ontologia em FL e FTL | "federated learning" OR "federated transfer learning" | ontolog* OR "semantic interoperability" OR "semantic harmonization" OR "semantic harmonisation" | |
| E2: FTL entre domínios | "federated transfer learning" | "cross-domain" OR "heterogeneous domains" OR "domain adaptation" OR "knowledge transfer" OR prototype* | |
| E3: robustez de FL a variações nos dados | "federated learning" OR "federated transfer learning" | "data perturbation" OR "data perturbations" OR "noise injection" OR "synthetic data" OR "distribution shift" | robustness OR "performance degradation" |
| E4: perturbações controladas em dados tabulares | "tabular data" OR "structured data" | "data perturbation" OR "data perturbations" OR "controlled perturbation" OR "noise injection" OR "synthetic data" OR "distribution shift" | robustness OR "performance degradation" OR benchmark* |
| E5 (complementar): ontologia de ITSM | ontolog* | "IT service management" OR ITSM OR ITIL OR "incident management" OR "service desk" | "machine learning" OR classification |

Os blocos são combinados com AND: (A) AND (B), ou (A) AND (B) AND (C).

### Web of Science (Coleção Principal, pesquisa avançada)

Colar no Query Builder (Advanced Search). O período e os demais filtros entram na própria string; conferir depois no painel "Refine results".

```
E1: TS=(("federated learning" OR "federated transfer learning") AND (ontolog* OR "semantic interoperability" OR "semantic harmonization" OR "semantic harmonisation")) AND PY=(2021-2026) AND DT=(Article OR Proceedings Paper OR Review) AND LA=(English OR Portuguese)

E2: TS=("federated transfer learning" AND ("cross-domain" OR "heterogeneous domains" OR "domain adaptation" OR "knowledge transfer" OR prototype*)) AND PY=(2021-2026) AND DT=(Article OR Proceedings Paper OR Review) AND LA=(English OR Portuguese)

E3: TS=(("federated learning" OR "federated transfer learning") AND ("data perturbation" OR "data perturbations" OR "noise injection" OR "synthetic data" OR "distribution shift") AND (robustness OR "performance degradation")) AND PY=(2021-2026) AND DT=(Article OR Proceedings Paper OR Review) AND LA=(English OR Portuguese)

E4: TS=(("tabular data" OR "structured data") AND ("data perturbation" OR "data perturbations" OR "controlled perturbation" OR "noise injection" OR "synthetic data" OR "distribution shift") AND (robustness OR "performance degradation" OR benchmark*)) AND PY=(2021-2026) AND DT=(Article OR Proceedings Paper OR Review) AND LA=(English OR Portuguese)

E5: TS=(ontolog* AND ("IT service management" OR ITSM OR ITIL OR "incident management" OR "service desk") AND ("machine learning" OR classification)) AND PY=(2021-2026) AND DT=(Article OR Proceedings Paper OR Review) AND LA=(English OR Portuguese)
```

Se a WoS recusar `DT` ou `LA` na string, rodar só com `TS` e `PY` e aplicar tipo e idioma no painel "Refine results".

### Scopus (Advanced document search)

```
E1: TITLE-ABS-KEY(("federated learning" OR "federated transfer learning") AND (ontolog* OR "semantic interoperability" OR "semantic harmonization" OR "semantic harmonisation")) AND PUBYEAR > 2020 AND PUBYEAR < 2027 AND (DOCTYPE(ar) OR DOCTYPE(cp) OR DOCTYPE(re)) AND (LANGUAGE(english) OR LANGUAGE(portuguese))

E2: TITLE-ABS-KEY("federated transfer learning" AND ("cross-domain" OR "heterogeneous domains" OR "domain adaptation" OR "knowledge transfer" OR prototype*)) AND PUBYEAR > 2020 AND PUBYEAR < 2027 AND (DOCTYPE(ar) OR DOCTYPE(cp) OR DOCTYPE(re)) AND (LANGUAGE(english) OR LANGUAGE(portuguese))

E3: TITLE-ABS-KEY(("federated learning" OR "federated transfer learning") AND ("data perturbation" OR "data perturbations" OR "noise injection" OR "synthetic data" OR "distribution shift") AND (robustness OR "performance degradation")) AND PUBYEAR > 2020 AND PUBYEAR < 2027 AND (DOCTYPE(ar) OR DOCTYPE(cp) OR DOCTYPE(re)) AND (LANGUAGE(english) OR LANGUAGE(portuguese))

E4: TITLE-ABS-KEY(("tabular data" OR "structured data") AND ("data perturbation" OR "data perturbations" OR "controlled perturbation" OR "noise injection" OR "synthetic data" OR "distribution shift") AND (robustness OR "performance degradation" OR benchmark*)) AND PUBYEAR > 2020 AND PUBYEAR < 2027 AND (DOCTYPE(ar) OR DOCTYPE(cp) OR DOCTYPE(re)) AND (LANGUAGE(english) OR LANGUAGE(portuguese))

E5: TITLE-ABS-KEY(ontolog* AND ("IT service management" OR ITSM OR ITIL OR "incident management" OR "service desk") AND ("machine learning" OR classification)) AND PUBYEAR > 2020 AND PUBYEAR < 2027 AND (DOCTYPE(ar) OR DOCTYPE(cp) OR DOCTYPE(re)) AND (LANGUAGE(english) OR LANGUAGE(portuguese))
```

### IEEE Xplore (Advanced Search > Command Search)

Colar a string na Command Search, com o campo padrão "All Metadata" (título, resumo, palavras-chave e metadados; não busca no texto completo). Depois, aplicar o filtro de ano (2021 a 2026) no painel à esquerda. A IEEE limita a quantidade de termos e de curingas por busca; se acusar erro, dividir o bloco B em duas buscas e somar os resultados (registrar as duas).

```
E1: ("federated learning" OR "federated transfer learning") AND (ontolog* OR "semantic interoperability" OR "semantic harmonization" OR "semantic harmonisation")

E2: "federated transfer learning" AND ("cross-domain" OR "heterogeneous domains" OR "domain adaptation" OR "knowledge transfer" OR prototype*)

E3: ("federated learning" OR "federated transfer learning") AND ("data perturbation" OR "data perturbations" OR "noise injection" OR "synthetic data" OR "distribution shift") AND (robustness OR "performance degradation")

E4: ("tabular data" OR "structured data") AND ("data perturbation" OR "data perturbations" OR "controlled perturbation" OR "noise injection" OR "synthetic data" OR "distribution shift") AND (robustness OR "performance degradation" OR benchmark*)

E5: ontolog* AND ("IT service management" OR ITSM OR ITIL OR "incident management" OR "service desk") AND ("machine learning" OR classification)
```

### ACM Digital Library (Advanced Search)

Selecionar "The ACM Full-Text Collection" (evita duplicar registros de outras editoras, que já vêm das demais bases). Em "Search Within", usar **Abstract** e colar a string; repetir com **Title** e com **Author Keyword**, ou usar a forma combinada abaixo no campo de busca. Período: Publication Date de 2021 a 2026.

```
Forma combinada (exemplo com E1; para os outros eixos, trocar o conteúdo entre parênteses):
Title:(X) OR Abstract:(X) OR Keyword:(X)

onde X = ("federated learning" OR "federated transfer learning") AND (ontolog* OR "semantic interoperability" OR "semantic harmonization" OR "semantic harmonisation")
```

Se a ACM não aceitar a forma combinada, usar só o campo Abstract e registrar isso na seção 9.

## 6. Strings da rodada 2 (ampliada, proposta inicial)

Serão ajustadas depois da leitura da rodada 1. Ponto de partida:

| Eixo | Ampliação prevista |
|---|---|
| E1 | Bloco B + "knowledge graph" OR "knowledge graphs" OR "semantic enrichment" OR "data harmonization" |
| E2 | Trocar o bloco A por ("federated learning" AND ("transfer learning" OR "domain adaptation")) |
| E3 | Bloco B + "data quality", "label noise", "feature noise"; bloco C + sensitivity. Só depois, se necessário, "data heterogeneity" OR "non-IID" |
| E4 | Bloco A + "logistic regression"; bloco C + "stress test" OR "stress testing" |
| E5 | Retirar o bloco C, se a rodada 1 vier vazia |

Atenção: "non-IID" e "data heterogeneity" tendem a trazer milhares de resultados em FL. Usar só se a rodada 1 de E3 vier pequena, e testar antes a contagem.

## 7. Critérios de seleção

**Inclusão (todos):**

- I1: publicado entre 2021 e 2026;
- I2: inglês ou português;
- I3: artigo de periódico, artigo de conferência com revisão por pares ou revisão;
- I4: trata do tema de pelo menos um eixo, com contribuição metodológica ou empírica aproveitável (método, protocolo, métrica ou resultado comparável);
- I5: texto completo acessível.

**Exclusão (qualquer um):**

- E1: os termos aparecem só de forma lateral (citados, mas não estudados);
- E2: aplicação em domínio distante (saúde, indústria, ciências naturais) sem contribuição metodológica transferível;
- E3: resumo estendido, editorial, pôster, capítulo sem revisão por pares, tese ou dissertação;
- E4: duplicata ou versão anterior de outro trabalho incluído (manter a mais completa);
- E5: preprint sem revisão por pares (só entra pela fonte complementar, registrado à parte).

## 8. Etapas e registro

1. **Busca e exportação**, base por base e eixo por eixo, preenchendo a tabela da seção 9 no mesmo dia.
2. **Deduplicação** no Zotero (uma coleção por rodada, subcoleções por base e eixo).
3. **Triagem 1 (título e resumo):** incluir, excluir (com o código do critério) ou revisar.
4. **Triagem 2 (introdução e conclusão):** para os marcados como incluir ou revisar.
5. **Elegibilidade (texto completo):** decisão final, com o código do critério de exclusão.
6. **Extração:** planilha com os campos da seção 11.
7. **Síntese por eixo** e fluxograma no formato PRISMA 2020 (identificados, duplicatas removidas, triados, excluídos em cada etapa, incluídos).

**Exportação:**

- **WoS:** Export > BibTeX (ou RIS), "Records from 1 to N", conteúdo "Full Record". Escolher o intervalo de registros, e não "Records on page", senão vêm só os da página exibida. Limite de 1000 por exportação; acima disso, exportar em lotes (1 a 1000, 1001 a 2000).
- **Scopus:** selecionar todos > Export > RIS ou BibTeX, incluindo resumo e palavras-chave.
- **IEEE Xplore:** selecionar todos > Export > Citations > BibTeX ou RIS, "Citation and Abstract".
- **ACM:** selecionar todos os da página > Export Citations > BibTeX; repetir em cada página, se necessário.

**Nome dos arquivos:** `R1_<BASE>_<EIXO>_<AAAA-MM-DD>.bib` (ex.: `R1_WOS_E1_2026-10-28.bib`), As exportações brutas não são publicadas neste repositório, porque contêm resumos protegidos pelos termos de uso das bases; a lista dos registros identificados está em `identificacao/`.

## 9. Registro das buscas

| Rodada | Base | Eixo | Data | String usada (se diferente da seção 5) | Campo | Filtros aplicados | Resultados | Exportados | Arquivo |
|---|---|---|---|---|---|---|---|---|---|
| R1 | WoS | E1 | 27/10/2026 | | TS | PY 2021-2026; DT Article, Proceedings Paper, Review; LA English, Portuguese (na string) | 53 | 53 | R1_WOS_E1_2026-10-27.bib |
| R1 | WoS | E2 | 27/10/2026 | | TS | PY 2021-2026; DT Article, Proceedings Paper, Review; LA English, Portuguese (na string) | 57 | 57 | R1_WOS_E2_2026-10-27.bib |
| R1 | WoS | E3 | 27/10/2026 | E3 ajustado (seção 10) | TS | PY 2021-2026; DT Article, Proceedings Paper, Review; LA English, Portuguese (na string) | 99 | 99 | R1_WOS_E3_2026-10-27.bib |
| R1 | WoS | E4 | 27/10/2026 | | TS | PY 2021-2026; DT Article, Proceedings Paper, Review; LA English, Portuguese (na string) | 126 | 126 | R1_WOS_E4_2026-10-27.bib |
| R1 | WoS | E5 | 27/10/2026 | | TS | PY 2021-2026; DT Article, Proceedings Paper, Review; LA English, Portuguese (na string) | 0 | 0 | (sem resultados) |
| R1 | Scopus | E1 | 27/10/2026 | | TITLE-ABS-KEY | PUBYEAR 2021-2026; DOCTYPE ar, cp, re; LANGUAGE english, portuguese (na string) | 201 | 201 | R1_SCOPUS_E1_2026-10-27.bib |
| R1 | Scopus | E2 | 27/10/2026 | | TITLE-ABS-KEY | PUBYEAR 2021-2026; DOCTYPE ar, cp, re; LANGUAGE english, portuguese (na string) | 76 | 76 | R1_SCOPUS_E2_2026-10-27.bib |
| R1 | Scopus | E3 | 27/10/2026 | E3 ajustado (seção 10) | TITLE-ABS-KEY | PUBYEAR 2021-2026; DOCTYPE ar, cp, re; LANGUAGE english, portuguese (na string) | 202 | 202 | R1_SCOPUS_E3_2026-10-27.bib |
| R1 | Scopus | E4 | 27/10/2026 | | TITLE-ABS-KEY | PUBYEAR 2021-2026; DOCTYPE ar, cp, re; LANGUAGE english, portuguese (na string) | 207 | 207 | R1_SCOPUS_E4_2026-10-27.bib |
| R1 | Scopus | E5 | 27/10/2026 | | TITLE-ABS-KEY | PUBYEAR 2021-2026; DOCTYPE ar, cp, re; LANGUAGE english, portuguese (na string) | 4 | 4 | R1_SCOPUS_E5_2026-10-27.bib |
| R1 | IEEE Xplore | E1 | 27/10/2026 | | All Metadata | Ano 2021-2026 (sem filtro de tipo e idioma) | 89 | 89 | R1_IEEE_E1_2026-10-27.bib |
| R1 | IEEE Xplore | E2 | 27/10/2026 | | All Metadata | Ano 2021-2026 (sem filtro de tipo e idioma) | 47 | 47 | R1_IEEE_E2_2026-10-27.bib |
| R1 | IEEE Xplore | E3 | 27/10/2026 | E3 ajustado (seção 10) | All Metadata | Ano 2021-2026 (sem filtro de tipo e idioma) | 140 | 140 | R1_IEEE_E3_2026-10-27.bib |
| R1 | IEEE Xplore | E4 | 27/10/2026 | | All Metadata | Ano 2021-2026 (sem filtro de tipo e idioma) | 83 | 83 | R1_IEEE_E4_2026-10-27.bib |
| R1 | IEEE Xplore | E5 | 27/10/2026 | | All Metadata | Ano 2021-2026 (sem filtro de tipo e idioma) | 5 | 5 | R1_IEEE_E5_2026-10-27.bib |
| R1 | ACM | E1 | 27/10/2026 | | Title/Abstract/Keyword | ACM Full-Text Collection; E-Publication Date 2021-2026 | 4 | 4 | R1_ACM_E1_2026-10-27.bib |
| R1 | ACM | E2 | 27/10/2026 | | Title/Abstract/Keyword | ACM Full-Text Collection; E-Publication Date 2021-2026 | 4 | 4 | R1_ACM_E2_2026-10-27.bib |
| R1 | ACM | E3 | 27/10/2026 | E3 ajustado (seção 10) | Title/Abstract/Keyword | ACM Full-Text Collection; E-Publication Date 2021-2026 | 7 | 7 | R1_ACM_E3_2026-10-27.bib |
| R1 | ACM | E4 | 27/10/2026 | | Title/Abstract/Keyword | ACM Full-Text Collection; E-Publication Date 2021-2026 | 16 | 16 | R1_ACM_E4_2026-10-27.bib |
| R1 | ACM | E5 | 27/10/2026 | | Title/Abstract/Keyword | ACM Full-Text Collection; E-Publication Date 2021-2026 | 0 | 0 | (sem resultados) |

**Totais da rodada 1 (antes da deduplicação, com o E3 ajustado):**

| Eixo | WoS | Scopus | IEEE Xplore | ACM | Total |
|---|---|---|---|---|---|
| E1 | 53 | 201 | 89 | 4 | 347 |
| E2 | 57 | 76 | 47 | 4 | 184 |
| E3 | 99 | 202 | 140 | 7 | 448 |
| E4 | 126 | 207 | 83 | 16 | 432 |
| E5 | 0 | 4 | 5 | 0 | 9 |
| Total | 335 | 690 | 364 | 31 | 1420 |

Observações da execução (27/10/2026):

- As strings rodaram como estão na seção 5, sem erro de sintaxe em nenhuma base.
- ACM: a forma combinada (Title, Abstract, Keyword) foi aceita. Cada campo precisa conter os dois blocos, o que a torna mais restrita que as outras bases. Exportação montada a partir dos metadados da ACM (formato CSL), convertidos para BibTeX, com resumo.
- IEEE Xplore: filtro só de ano; tipo de documento e idioma ficam para a triagem. Exportação com resumo.
- WoS: exportação "Full Record", com resumo, intervalo 1 a N.
- Scopus: exportação feita com login do autor (exigência da Scopus), em BibTeX com resumo, palavras-chave, editora e idioma.
- Exportados: 1420 registros em 18 arquivos (WoS 335, Scopus 690, IEEE 364, ACM 31), todos com resumo. Os eixos com zero resultado (WoS E5, ACM E5) não geraram arquivo.

**Deduplicação (28/10/2026):** 1420 registros, 533 duplicatas removidas (mesmo DOI ou mesmo título normalizado; 8 pares por título quase idêntico, com ano igual ou vizinho), **887 artigos únicos**. Por eixo (um artigo pode estar em mais de um): E1 265, E2 92, E3 288, E4 240, E5 8. Planilha de triagem: `triagem/Triagem_RSL_R1.xlsx`.

**Triagem 1, por título e resumo (28/10/2026):** 887 artigos triados. Incluídos: 68. A revisar: 161. Excluídos: 658 (EX1 449, EX2 189, EX3 16, EX4 4, EX5 0). Por eixo (incluir / revisar / excluir): E1 13 / 18 / 234; E2 5 / 15 / 72; E3 15 / 64 / 209; E4 32 / 68 / 140; E5 3 / 0 / 5. Seguem para a triagem 2 (introdução e conclusão): 229 artigos (incluídos e a revisar). Decisão e motivo de cada artigo na planilha `triagem/Triagem_RSL_R1.xlsx`.

Ajuste de critério feito durante a triagem 1 (registrado para a metodologia): nos eixos E3 e E4, foram considerados incluídos apenas os trabalhos que avaliam o desempenho ou a robustez sob variação dos dados, ou que são benchmarks, revisões ou arcabouços de avaliação. Métodos genéricos para dados não IID sem essa análise foram marcados para revisão, e propostas de novos geradores de dados sintéticos sem avaliação de degradação foram excluídas por EX1 (tema lateral à proposta).

**Triagem 2, por introdução e conclusão (28/10/2026):** 229 artigos (incluídos e a revisar na triagem 1). Incluídos: 69. Excluídos: 160 (IN5, sem texto completo acessível, 106; EX1 45; EX2 7; EX3 2), já considerada a revisão final de relevância, que excluiu 3 artigos (R1-0527 e R1-0598 por EX1; R1-0730 por EX2). Regra para texto completo (opção B): os artigos sem texto aberto na web que estavam como Incluir na triagem 1 foram lidos pelo Portal CAPES; os demais sem texto aberto foram excluídos por IN5. Incluídos por eixo: E1 11, E2 5, E3 16, E4 36, E5 3. Relevância final: 26 núcleo, 30 apoio, 13 periféricos (após a leitura completa dos núcleo, R1-0246 passou a periférico). A extração dos 69 está em `extracao/`.

## 10. Recalibração

| Eixo | Termo novo ou retirado | Origem (artigo em que apareceu) | Efeito esperado |
|---|---|---|---|
| E3 | Retirados "data quality" (bloco B) e sensitivity (bloco C), antes da exportação da rodada 1 (decisão do autor, 27/10/2026) | Contagem inicial: 940 registros (WoS 218, Scopus 390, IEEE 314, ACM 18), muito ampla para uma rodada restrita | E3 caiu para 448 (WoS 99, Scopus 202, IEEE 140, ACM 7). Os dois termos voltam na rodada 2 |
| E2 e E3 | Novo bloco de limites: "threshold" OR "tipping point" OR "breakdown point" OR "breaking point" OR "applicability" OR "operating limit" | Refinamento da pergunta do artigo com o orientador (04/11/2026): limites de aplicação no domínio de destino. Termos já presentes em trabalhos incluídos (Chen et al., 2026, limiar de robustez; Liu, 2026, ponto de cruzamento) | Recuperar estudos que estimam limites sob perturbação, que a rodada 1 só trouxe quando também falavam de robustez |
| E2 | Novo bloco de transferibilidade: "transferability estimation" OR "transferability metric" OR "transferability score" OR "negative transfer" | Problema definido pelo orientador: para quais domínios de destino um modelo gerado na origem pode servir | Recuperar a linha de estimação de transferibilidade, provavelmente ausente da rodada 1 |

**Desvio documentado (05/11/2026):** a pergunta e o PICO da seção 2 foram mantidos como executados na rodada 1. Depois da revisão, a pergunta de pesquisa do artigo foi refinada com o orientador para os limites de aplicação de modelos de FL e FTL no domínio de destino. O desfecho do PICO ("degradação do desempenho sob variação dos dados") continua cobrindo a base para estimar esses limites; a rodada 2 (seção 4 deste protocolo) acrescenta os termos acima, de forma dirigida, sem refazer a rodada 1. As contagens devem ser testadas antes da exportação, como na rodada 1.

## 11. Campos da extração

Referência; ano; tipo (periódico, conferência, revisão); eixo(s); problema tratado; domínio e dados (tabulares, texto, imagem; nº de clientes ou domínios); abordagem de FL ou FTL (algoritmo, agregação, uso de protótipos); uso de ontologia (qual, papel no pipeline, como foi avaliada); variação ou perturbação estudada (tipo, intensidade, como foi controlada); modelo e métricas; principais resultados; limitações declaradas; relação com o artigo (P, I, C ou O do PICO) e uso previsto (fundamentação, estado da arte, método, comparação de resultados).
