# Projeto Final - Previsão de Preços com FIPE

Este projeto tem como objetivo prever o preço médio de veículos no Brasil com base em dados da Tabela FIPE, utilizando técnicas de Machine Learning supervisionado como Regressão Linear e Redes Neurais (MLP).

## Sobre os Dados

- Os dados foram extraídos da [Tabela FIPE](https://veiculos.fipe.org.br/) por meio de um crawler.
- O dataset contém informações sobre:
  - Marca e modelo do veículo
  - Tipo de combustível
  - Mês e ano da cotação
  - Preço médio de mercado

## Técnicas Utilizadas

O projeto realiza experimentos comparativos entre os seguintes modelos:

### Regressão Linear
- Modelo simples, usado como baseline
- Desempenho limitado diante de dados desbalanceados e valores extremos

### MLP (Multi-Layer Perceptron)
- Duas camadas ocultas com função de ativação ReLU
- Capacidade de capturar padrões não lineares
- Resultados ligeiramente melhores que a regressão linear

### MLP com Transformação Logarítmica
- Utiliza log(preço) como variável alvo para reduzir a variação entre exemplos
- Aplica-se expm1() nas predições para retornar à escala original
- Apresenta o melhor desempenho entre os modelos testados

## Avaliação

- Erro Quadrático Médio (MSE) como métrica principal
- Gráficos de dispersão para análise visual
- R² Score também utilizado como métrica complementar

## Execução no Google Colab

1. Abra o notebook `Projeto_Final_FIPE.ipynb` no [Google Colab](https://colab.research.google.com/).
2. Execute as células na ordem apresentada.
3. Os dados são carregados automaticamente a partir de arquivos CSV extraídos e compactados.

## Autores

Este projeto foi desenvolvido como trabalho final da disciplina Noções de Inteligência Artificial (NIA) por:

- Caio Medeiros Balaniuk 
- Davi Henrique Vieira Lima 
- Gabriel Caixeta Romero
- Vitor Amorim Mello