# Prontidão de Segurança para IA nos Tribunais de Justiça Estaduais (AISecDev 2026)

Dados de replicação (Disponibilidade de Artefatos) do artigo:

> **Adoção de IA no Poder Judiciário Brasileiro sem Controles de Segurança: Um Estudo Comparativo dos 27 Tribunais de Justiça Estaduais**
> V. G. B. C. B. Santos; G. H. F. de M. Oliveira; J. J. dos Santos Júnior.
> Workshop on Secure Software Development in the Age of AI (AISecDev 2026), co-localizado com o CBSoft 2026, IME-USP, São Paulo, 8 set. 2026.

Este repositório contém a coleta documental e as matrizes de análise que fundamentam
as tabelas do artigo. A metodologia é análise documental de fontes primárias públicas
(portais oficiais dos tribunais e Diários de Justiça Eletrônicos), no período de
**janeiro de 2021 a junho de 2026**.

## Conteúdo

| Arquivo | Descrição |
|---|---|
| [`dados/matriz_27_tjs.csv`](dados/matriz_27_tjs.csv) | Matriz de prontidão dos 27 TJs em 6 dimensões, pontuação ponderada e nível de maturidade (**Tabela 3** do artigo). |
| [`dados/owasp_llm_top10_judiciario.csv`](dados/owasp_llm_top10_judiciario.csv) | OWASP LLM Top 10 (2025) traduzido para o contexto judicial, com tática MITRE ATT&CK, cenário concreto, controle DevSecOps e artigo da LGPD violado. |
| [`dados/diagnostico_tj_normas.csv`](dados/diagnostico_tj_normas.csv) | Diagnóstico de conformidade (LGPD × Resoluções CNJ × normas ISO/NIST) para os tribunais de referência. |
| [`dados/anexo_analise_tj_seguranca_ia.xlsx`](dados/anexo_analise_tj_seguranca_ia.xlsx) | Planilha-fonte original com as três abas. |

## Dimensões e pesos da matriz

| Dimensão | Peso | Evidência exigida |
|---|---|---|
| Governança de Dados | 15% | Comitê de Proteção de Dados ou Política de Privacidade pública |
| PSI | 20% | Resolução de PSI com anexos técnicos |
| DPO / Encarregado | 15% | Designação formal com canal público |
| RIPD | 15% | Relatório de impacto para tratamentos de alto risco |
| Resp. a Incidentes | 20% | Protocolo com prazo de 72h (art. 48 LGPD) |
| Regulamentação de IA | 15% | Norma ou diretriz interna sobre uso de IA |

**Legenda:** `✓` = evidência pública encontrada · `½` = parcial/antipadrão · `✗` = não localizada.
**Níveis:** Inicial 0–33% · Básico 34–50% · Intermediário 51–75% · Avançado ≥76%.

## Principais resultados

- Nenhum dos 27 tribunais atinge o nível **Avançado**.
- **15** tribunais publicaram PSI; **8** designaram DPO; **0** possuem norma específica de IA.
- Distribuição: 0 Avançado · 8 Intermediário · 7 Básico · 12 Inicial.
- O antipadrão da *cláusula de discricionariedade ilegal* na comunicação de incidentes
  foi identificado em **8** tribunais (~30%).

## Limitação

A análise avalia **conformidade formal publicada**, não implementação técnica verificada
em campo. A ausência de evidência pública é registrada como tal e tratada como indicador
de baixa maturidade documental.

## Como citar

Ver `CITATION.cff` (atualizar com DOI/anais após publicação).

## Licença

Dados sob [CC BY 4.0](LICENSE). Reuso permitido com atribuição.
