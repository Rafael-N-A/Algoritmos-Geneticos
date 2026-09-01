# algoritmos-geneticos

Repositório com implementação de um **Algoritmo Genético** para resolução do **Problema do Caixeiro Viajante (TSP)**, encontrando o menor caminho possível entre um conjunto de pontos de um grafo.

## 🛠️ Tecnologias e Bibliotecas

- **Python**
  - **DEAP** — utilizada para a construção do algoritmo genético (indivíduos, população, seleção, crossover e mutação)
  - **NumPy** — utilizada para leitura dos pontos e cálculo das distâncias (matriz de distâncias)
  - **Plotly** — utilizada para gerar o gráfico de convergência do algoritmo

## 📁 Estrutura do Repositório

### Entrada
- **`instancia.txt`** — Arquivo contendo a quantidade de pontos e as coordenadas de cada ponto do grafo utilizado como instância do problema.

### Código
- **Algoritmo Genético (TSP)** — Código responsável por:
  - Ler os pontos do arquivo `instancia.txt` e montar a matriz de distâncias entre eles;
  - Definir a função de avaliação (fitness), que mede a distância total do caminho;
  - Criar a população inicial de caminhos possíveis;
  - Aplicar **crossover ordenado** (`cxOrdered`) e **mutação por embaralhamento** (`mutShuffleIndexes`) para gerar novas gerações;
  - Selecionar os melhores indivíduos por **torneio**;
  - Executar o algoritmo genético por múltiplas gerações, buscando minimizar a distância total do caminho;
  - Gerar um gráfico de convergência (melhor, média e pior fitness por geração) utilizando Plotly;
  - Exibir o melhor caminho encontrado e sua distância total.

## ⚙️ Parâmetros do Algoritmo

- **Tamanho da população:** 100 indivíduos
- **Número de gerações:** 100
- **Probabilidade de crossover:** 70%
- **Probabilidade de mutação:** 20%
- **Método de seleção:** Torneio (tamanho 3)

## ▶️ Como Executar

1. Instale as dependências:
   ```bash
   pip install numpy deap plotly
   ```
2. Certifique-se de que o arquivo `instancia.txt` esteja no mesmo diretório do script.
3. Execute o script:
   ```bash
   python algoritmo_genetico.py
   ```
4. Ao final da execução, será exibido o gráfico de convergência e, no terminal, o melhor caminho encontrado junto com sua distância total.

## 📌 Observações

Código de autoria própria, desenvolvido como trabalho/estudo sobre algoritmos genéticos aplicados ao Problema do Caixeiro Viajante.
