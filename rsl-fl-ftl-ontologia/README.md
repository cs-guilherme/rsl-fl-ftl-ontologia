# Revisão sistemática: ontologias em Federated Learning e Federated Transfer Learning

Material da revisão sistemática da literatura (RSL) do artigo **"Transferência de Conhecimento Baseada em Ontologia em Federated Learning e Federated Transfer Learning: Mapeamento de Padrões de Degradação sob Perturbações Controladas nos Dados"**, de Guilherme Sena de Oliveira, desenvolvido no MTA em Cibersegurança do Instituto de Pesquisas Tecnológicas do Estado de São Paulo (IPT), 2026.

A revisão seguiu as diretrizes de Kitchenham e Charters (2007) e foi relatada conforme o PRISMA 2020 (Page et al., 2021).

## Resumo da rodada 1

| Etapa | Quantidade |
|---|---|
| Bases | Scopus, Web of Science (Coleção Principal), IEEE Xplore, ACM Digital Library |
| Período e data da busca | 2021 a 2026; busca em 27/10/2026 |
| Registros identificados | 1.420 |
| Registros únicos (após deduplicação) | 887 |
| Triagem 1 (título e resumo) | 229 seguiram para a triagem 2 |
| Triagem 2 e elegibilidade (texto) | 69 estudos incluídos |

Eixos temáticos: E1, ontologia em FL e FTL; E2, FTL entre domínios heterogêneos; E3, robustez de FL a variações nos dados; E4, perturbações controladas em dados tabulares; E5, ontologias de ITSM aplicadas a aprendizado de máquina.

## Conteúdo

| Pasta | Arquivo | Conteúdo |
|---|---|---|
| `protocolo/` | `PROTOCOLO_RSL.md` | Questões da revisão, PICO, bases, strings completas por base, critérios, etapas, registro das buscas, recalibração e campos da extração |
| `identificacao/` | `registros_identificados_R1.csv` | Os 1.420 registros exportados, com base e eixo de origem |
| `identificacao/` | `registros_unicos_R1.csv` | Os 887 registros únicos após a deduplicação, com as bases e os eixos em que apareceram |
| `triagem/` | `Triagem_RSL_R1.xlsx` | Planilha de triagem (abas Triagem, Critérios, PRISMA e Extração) |
| `triagem/` | `triagem_R1.csv` | Decisão, critério e motivo de cada registro nas triagens 1 e 2, e relevância final dos incluídos |
| `triagem/` | `criterios.csv` | Critérios de inclusão (IN) e exclusão (EX) |
| `extracao/` | `formulario_extracao.md` | Campos do formulário de extração |
| `extracao/` | `extracao_R1.csv` | Dados extraídos dos 69 estudos incluídos |
| `prisma/` | `PRISMA_RSL_R1.png` e `.svg` | Fluxograma PRISMA 2020 da rodada 1 |

Os códigos dos critérios no protocolo (I1 a I5, E1 a E5) correspondem aos da planilha (IN1 a IN5, EX1 a EX5).

## Observações

- **Resumos e palavras-chave não são publicados.** As exportações das bases contêm resumos protegidos pelos termos de uso de cada base. Os registros podem ser recuperados pelo DOI ou repetindo as strings do protocolo.
- **Apoio de IA.** A triagem e a extração foram feitas com apoio de ferramenta de inteligência artificial (Claude, da Anthropic), com conferência do autor, a partir dos critérios e dos campos definidos no protocolo.
- **Rodada 2.** O protocolo prevê uma segunda rodada, com termos específicos sobre limites de aplicação e transferibilidade (seção 10). Quando executada, os arquivos serão acrescentados com o prefixo `R2`.

## Referências

KITCHENHAM, B.; CHARTERS, S. **Guidelines for performing systematic literature reviews in software engineering**. Keele: Keele University; Durham: Durham University, 2007.

PAGE, M. J. et al. The PRISMA 2020 statement: an updated guideline for reporting systematic reviews. **BMJ**, v. 372, n71, 2021.

## Licença

Dados e textos sob a licença Creative Commons Atribuição 4.0 Internacional (CC BY 4.0).
