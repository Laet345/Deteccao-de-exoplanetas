# Log de entregas do projeto

Este arquivo registra as entregas de cada integrante e quando foram realizadas.
Atualize a seção correspondente sempre que uma nova etapa for concluída. Datas
devem usar o formato `DD/MM/AAAA`.

## Integrante 1 — Engenharia de dados e pipeline base

### 29/10/2026

- Baixou a base **Breast Cancer Wisconsin (Diagnostic)** do UCI e organizou os
  arquivos originais em `data/raw/`:
  - [`wdbc.data`](data/raw/wdbc.data)
  - [`wdbc.names`](data/raw/wdbc.names)
- Carregou os dados com nomes de colunas e verificou a estrutura: 569 registros,
  32 colunas, sem valores faltantes ou linhas/IDs duplicados.
- Investigou tipos, escalas e possíveis valores extremos. Os valores sinalizados
  foram tratados como pontos a investigar, não como erros a remover
  automaticamente.
- Exportou a versão processada para
  [`data/processed/wdbc_limpo.csv`](data/processed/wdbc_limpo.csv), codificando
  `diagnosis` como `0` (benigno) e `1` (maligno), sem normalizar as medidas.
- Preparou [`notebooks/refinador_de_dados.ipynb`](notebooks/refinador_de_dados.ipynb)
  para importar os dados brutos em `df` e apoiar as verificações iniciais.
- Preparou [`notebooks/analise.ipynb`](notebooks/analise.ipynb) para carregar os
  dados processados, separar `X` e `y` (retirando `id` de `X`), realizar a divisão
  estratificada treino/teste e apresentar exemplos de pipelines com e sem
  `StandardScaler`.
- Orientações compartilhadas com o grupo:
  - Usar `X` com os 30 atributos numéricos; `id` é identificador e não deve ser
    usado como preditor.
  - Usar `y` como `diagnosis`, com `0 = benigno` e `1 = maligno`.
  - Para modelos sensíveis à escala (por exemplo, regressão logística, KNN e
    SVM), treinar o pipeline completo com `X_train` e `y_train`. O scaler deve
    aprender os parâmetros somente no treino e então transformar validação/teste,
    evitando vazamento de dados.
  - Modelos baseados em árvores, como Random Forest, geralmente não precisam de
    padronização.
  - Esta base não requer separação de preditores categóricos e numéricos: os 30
    atributos de `X` são numéricos e `diagnosis` é o alvo.
  - A divisão preparada usa `test_size=0.2`, `stratify=y` e `random_state=42`;
    combinar com o grupo o uso da mesma divisão.

## Integrante 2 — Análise estatística e EDA visual

Sem registro de entrega neste log.

- **Entregas planejadas:** estatísticas descritivas por classe, visualizações,
  correlações e investigação de multicolinearidade.
- **Data da entrega:** a preencher.
- **Arquivos/observações:** a preencher.

## Integrante 3 — Projeção, seleção de atributos e agrupamento

Sem registro de entrega neste log.

- **Entregas planejadas:** PCA/t-SNE, agrupamento e métodos de seleção de
  atributos.
- **Data da entrega:** a preencher.
- **Arquivos/observações:** a preencher.

## Integrante 4 — Modelagem preditiva e ajuste de modelos

Sem registro de entrega neste log.

- **Entregas planejadas:** treinamento e ajuste de classificadores, validação
  cruzada estratificada e busca de hiperparâmetros.
- **Data da entrega:** a preencher.
- **Arquivos/observações:** a preencher.

## Integrante 5 — Avaliação, síntese e documentação

Sem registro de entrega neste log.

- **Entregas planejadas:** comparação de métricas, análise de falsos negativos,
  discussão, síntese e compilação final.
- **Data da entrega:** a preencher.
- **Arquivos/observações:** a preencher.

## Próximos registros

Para cada atualização, acrescente uma entrada com data, descrição objetiva do
que foi concluído e links/caminhos dos arquivos. “Sem registro” significa que
nenhuma entrega foi documentada aqui ainda; não indica que a pessoa não esteja
trabalhando.
