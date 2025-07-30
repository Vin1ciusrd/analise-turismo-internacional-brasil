# Análise Histórica do Turismo Internacional no Brasil (2000-2024)

Este projeto de ciência de dados explora o cenário do turismo internacional no Brasil, utilizando dados históricos disponíveis no portal de dados abertos do governo federal para identificar padrões e tendências. Compreender de onde vêm os turistas, como chegam e para onde vão é crucial para a formulação de políticas públicas e estratégias de marketing no setor.

## Objetivo do Projeto

O principal objetivo deste projeto é responder às seguintes perguntas:

- Quais são os principais países de origem dos turistas que visitam o Brasil?
- Qual a via de acesso mais utilizada por esses turistas (aérea, terrestre, marítima)?
- Quais são as unidades federativas (estados) que mais recebem turistas?
- Qual o mês do ano que mais recebe turistas?

## Fonte dos Dados

Os dados utilizados neste projeto foram obtidos do portal de dados abertos do governo federal, especificamente do conjunto de dados "Estimativas de Chegadas de Turistas Internacionais ao Brasil".

- **Link para os dados:** [https://dados.gov.br/dados/conjuntos-dados/estimativas-de-chegadas-de-turistas-internacionais-ao-brasil](https://dados.gov.br/dados/conjuntos-dados/estimativas-de-chegadas-de-turistas-internacionais-ao-brasil)

## Estrutura do Projeto

O projeto está organizado em um único notebook Jupyter (`analise_turismo.ipynb`), que contém as seguintes etapas:

1.  **Importação de Bibliotecas:** Carregamento das bibliotecas necessárias para manipulação, análise e visualização de dados (pandas, matplotlib, etc.).
2.  **Leitura e Concatenação dos Dados:** Leitura de múltiplos arquivos CSV (um para cada ano, de 2000 a 2024) e sua concatenação em um único DataFrame. Realizado o pré-processamento inicial para padronizar nomes de colunas e dados.
3.  **Análise Exploratória dos Dados (EDA):**
    * Verificação das informações gerais do DataFrame (tipos de dados, valores nulos).
    * Tratamento de valores nulos (substituição por 0 na coluna 'Chegadas').
    * Tratamento de inconsistências na coluna 'Via de acesso' (ex: "Aéreo" para "Aérea", "Marítima" para "Marítimo").
    * Verificação de informações estatísticas básicas dos dados.
4.  **Visualização e Análise:**
    * **Tendência Anual de Chegadas:** Gráfico de linha mostrando o total de chegadas de turistas ao Brasil de 2000 a 2024.
    * **Top 10 Países de Origem:** Gráfico de barras exibindo os países que mais enviaram turistas ao Brasil.
    * **Top 5 Continentes de Origem:** Gráfico de barras com os continentes que mais contribuíram para o turismo no Brasil.
    * **Vias de Acesso Mais Utilizadas:** Gráfico de linha mostrando a evolução do uso de diferentes vias de acesso (aérea, terrestre, marítima, fluvial) ao longo dos anos.
    * **Top 10 Unidades Federativas (UFs) Visitadas:** Gráfico de barras com os estados brasileiros que mais receberam turistas.
    * **Mês com Mais Chegadas por Ano:** Análise e visualização do mês que registrou o maior número de chegadas em cada ano do período analisado.

## Conclusões Principais

Com base nas análises realizadas, foi possível tirar as seguintes conclusões:

1.  **Origem dos Turistas:** A **América do Sul**, e a **Argentina** em particular, lideram o ranking de turistas que visitam o Brasil. Isso pode ser atribuído à proximidade geográfica e à similaridade cambial, que tornam a viagem mais acessível financeiramente para esses visitantes.
2.  **Vias de Acesso:** As **vias aéreas e terrestres** são as mais utilizadas pelos turistas internacionais para chegar ao Brasil.
3.  **Unidades Federativas Mais Visitadas:** As três unidades federativas que mais recebem turistas são **São Paulo, Rio de Janeiro e Rio Grande do Sul**. Essas cidades se destacam por sua rica diversidade cultural, belezas naturais, gastronomia e investimentos em infraestrutura turística, eventos e transporte.
4.  **Período de Pico:** **Janeiro** é consistentemente o mês preferido pelos turistas para visitar o Brasil, seguido por fevereiro, julho e dezembro. Esses meses coincidem com períodos de férias escolares em diversas partes do mundo, o que impulsiona o fluxo turístico global.

## Como Executar o Projeto

Para executar este projeto em sua máquina local, siga os passos abaixo:

1.  **Clone este repositório:**
    ```bash
    git clone [https://github.com/seu-usuario/seu-repositorio.git](https://github.com/seu-usuario/seu-repositorio.git)
    cd seu-repositorio
    ```
2.  **Crie um ambiente virtual (opcional, mas recomendado):**
    ```bash
    python -m venv venv
    source venv/bin/activate  # No Linux/macOS
    # ou
    venv\Scripts\activate     # No Windows
    ```
3.  **Instale as dependências:**
    ```bash
    pip install pandas matplotlib
    ```
4.  **Baixe os dados:**
    Os dados estão disponíveis no link fornecido na seção "Fonte dos Dados". Você precisará baixar os arquivos CSV para cada ano (de 2000 a 2024) e colocá-los em uma pasta chamada `bases_dados` dentro do diretório do projeto. A estrutura deve ser:
    ```
    seu-repositorio/
    ├── analise_turismo.ipynb
    └── bases_dados/
        ├── chegadas_2000.csv
        ├── chegadas_2001.csv
        └── ...
        └── chegadas_2024.csv
    ```
5.  **Abra e execute o notebook Jupyter:**
    ```bash
    jupyter notebook analise_turismo.ipynb
    ```
    Execute todas as células do notebook para reproduzir a análise e os gráficos.

## Tecnologias Utilizadas

-   **Python:** Linguagem de programação principal.
-   **Pandas:** Para manipulação e análise de dados.
-   **Matplotlib:** Para visualização de dados.

## Contribuição

Contribuições são bem-vindas! Se você tiver alguma sugestão, melhoria ou encontrar algum problema, sinta-se à vontade para abrir uma issue ou enviar um pull request.
