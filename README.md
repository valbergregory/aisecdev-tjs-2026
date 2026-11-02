# Prontidão de Segurança para IA nos Tribunais de Justiça Estaduais (AISecDev 2026)

Dados de replicação do artigo *Adoção de IA no Poder Judiciário Brasileiro sem Controles de Segurança: Um Estudo Comparativo dos 27 Tribunais de Justiça Estaduais* (AISecDev 2026, workshop co-localizado com o CBSoft 2026, IME-USP, São Paulo).

O repositório reúne a coleta documental e as matrizes de análise que fundamentam as tabelas do artigo. O objetivo é comparar, tribunal a tribunal, a existência de controles públicos de governança de dados, segurança da informação, proteção de dados pessoais, resposta a incidentes e regulamentação de IA nos 27 Tribunais de Justiça estaduais.

## Dados e fontes

- **Método:** análise documental de fontes primárias públicas.
- **Fontes:** portais oficiais dos tribunais e Diários de Justiça Eletrônicos.
- **Período de cobertura:** janeiro de 2021 a junho de 2026.
- **Referências normativas usadas na classificação:** LGPD (Lei 13.709/2018), Resoluções do CNJ, normas ISO/NIST, OWASP LLM Top 10 (2025) e táticas MITRE ATT&CK.

A análise registra **conformidade formal publicada**, não implementação técnica verificada em campo. A ausência de evidência pública é registrada como tal (`✗`).

## Estrutura do repositório

```
dados/
  matriz_27_tjs.csv                 matriz de prontidão dos 27 TJs (Tabela 3 do artigo)
  owasp_llm_top10_judiciario.csv    OWASP LLM Top 10 (2025) lido no contexto judicial
  diagnostico_tj_normas.csv         diagnóstico LGPD × Resoluções CNJ × ISO/NIST para tribunais de referência
  anexo_analise_tj_seguranca_ia.xlsx planilha-fonte com as três abas acima
CITATION.cff                        metadados de citação
LICENSE / LICENSING.md              licença dos dados
```

Os três CSVs são exportações das abas da planilha `anexo_analise_tj_seguranca_ia.xlsx` (`Matriz 27 TJs`, `OWASP LLM Top10 × Judiciário`, `Diagnóstico TJ × Normas`).

### `dados/matriz_27_tjs.csv`

Uma linha por tribunal (27 linhas). Colunas: `TJ`, `UF`, seis dimensões, `Total Ponderado (%)` e `Nível de Maturidade`.

| Dimensão | Peso | Evidência exigida |
|---|---|---|
| Governança de Dados | 15% | Comitê de Proteção de Dados ou Política de Privacidade pública |
| PSI | 20% | Resolução de Política de Segurança da Informação com anexos técnicos |
| DPO / Encarregado | 15% | Designação formal com canal público |
| RIPD | 15% | Relatório de impacto para tratamentos de alto risco |
| Resp. a Incidentes | 20% | Protocolo com prazo de 72h (art. 48 da LGPD) |
| Regulamentação de IA | 15% | Norma ou diretriz interna sobre uso de IA |

Legenda das células: `✓` evidência pública encontrada · `½` parcial/antipadrão · `✗` não localizada.
Níveis de maturidade: Inicial 0–33% · Básico 34–50% · Intermediário 51–75% · Avançado ≥ 76%.

### `dados/owasp_llm_top10_judiciario.csv`

Uma linha por item do OWASP LLM Top 10 (2025). Colunas: código OWASP, nome em pt-BR, tática MITRE ATT&CK, cenário judicial, controle mínimo (DevSecOps), artigo(s) da LGPD e prioridade no Judiciário.

### `dados/diagnostico_tj_normas.csv`

Uma linha por dimensão avaliada (10 linhas). Colunas: dimensão, norma CNJ de referência, artigo(s) da LGPD, norma internacional equivalente e situação em TJSP, TJSC, TJMG e TJAL.

## Como reproduzir

Não há código. As tabelas do artigo são obtidas diretamente dos CSVs em `dados/`.

## Licença e citação

Dados sob [CC BY 4.0](LICENSE); ver também [LICENSING.md](LICENSING.md).

Para citar, use os metadados de [`CITATION.cff`](CITATION.cff):

> Santos, V. G. B. C. B.; Oliveira, G. H. F. de M.; Santos Júnior, J. J. dos. *Prontidão de Segurança para IA nos 27 Tribunais de Justiça Estaduais* (dados de replicação). 2026. CC BY 4.0.
