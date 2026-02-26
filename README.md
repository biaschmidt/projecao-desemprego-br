Projeção da Taxa de Desemprego no Brasil

**Objetivo**

Este projeto realiza a modelagem e previsão da taxa de desemprego brasileira utilizando dados da PNAD Contínua, disponibilizados pelo IBGE via API SIDRA.

O objetivo é avaliar se modelos de séries temporais conseguem capturar a dinâmica histórica da taxa de desocupação e produzir previsões superiores a abordagens ingênuas.

**Fonte dos Dados**

Dados obtidos via API do IBGE (SIDRA), referentes à taxa de desocupação trimestral móvel para o Brasil.

A coleta é automatizada diretamente no notebook, sem uso de arquivos externos manuais.

**Metodologia**

- Coleta via API
- Limpeza e transformação para série temporal
- Teste de estacionariedade (ADF)
- Diferenciação da série
- Ajuste de modelo ARIMA(1,1,1)
- Separação treino/teste (validação fora da amostra)
- Comparação com modelo ingênuo (baseline)
- Diagnóstico dos resíduos

**Resultados**

- MAE ≈ 0.34 ponto percentual
- Redução de ~67% no erro em relação ao modelo ingênuo
- Resíduos compatíveis com ruído branco
- Modelo estatisticamente bem especificado

**Conclusão**

O modelo ARIMA(1,1,1) demonstrou capacidade de capturar a estrutura temporal da taxa de desemprego brasileira, apresentando desempenho significativamente superior a uma abordagem ingênua.

O diagnóstico dos resíduos indica ausência de autocorrelação remanescente, sugerindo especificação adequada do modelo.

**Tecnologias Utilizadas**

- Python
- Pandas
- Statsmodels
- Scikit-learn
- Matplotlib
- API SIDRA (IBGE)
