# Previsão da taxa de mortalidade infantil

## Objetivo

Prever a taxa de mortalidade infantil com base em diferentes variáveis socioeconômicas, históricas, entre outras.

---

## Roteiro

1. Pré-processamento de dados
2. Análise exploratória de dados
3. Modelagem de dados
4. Comunicação de Resultados

---

## 1. Pré-processamento de dados

Nesta etapa, foram realizados os seguintes procedimentos:

- Remoção de colunas irrelevantes para o problema de previsão da taxa de mortalidade infantil;
- Tratamento de valores ausentes (NaN);
- Conversão das strings numéricas para o tipo de dado adequado.
- Uso da biblioteca pandas_profiling para gerar um relatório dos nossos dados

---

## 2. Análise exploratória de dados

### Gráfico de Barras para a Distribuição da Taxa de Mortalidade Infantil por País

Através desse gráfico, é possível visualizar a taxa de mortalidade infantil para os países com maior índice. O país com maior taxa foi Serra Leoa, seguido por Nigéria e República Democrática do Congo. Quase todos os países do top 10 são africanos, exceto o paquistão.


![image](https://github.com/MiguelFreire-bit/Prever_taxa_mortalidade_infantil/assets/72529654/078c0909-31a1-4626-95eb-26f202bb9e30)


- África: 90% (9 países)
- Ásia: 10% (1 país)

### Gráfico de Dispersão para Visualizar a Relação entre a Taxa de Mortalidade Infantil e o Número de Médicos por Mil Habitantes

Neste gráfico, analisamos a relação entre a taxa de mortalidade infantil e o número de médicos por mil habitantes. Observamos uma tendência de redução da taxa de mortalidade infantil conforme aumenta o número de médicos por mil habitantes.

Podemos perceber que a maioria dos casos de alta taxa de mortalidade infantil está em regiões com menos de 1 médico por 100 mil habitantes, então é de interesse geral e claro a necessidade de melhora desse quadro nos países afetados

![image](https://github.com/MiguelFreire-bit/Prever_taxa_mortalidade_infantil/assets/72529654/fb0742c6-6039-4ea1-9097-921ea80dbc0e)


---

## 3. Modelagem de dados

### Regressão Linear

A regressão linear foi aplicada para prever a taxa de mortalidade infantil com base nas variáveis selecionadas. As métricas de erro foram utilizadas para avaliar o desempenho do modelo:

- Erro Médio Absoluto (MAE): 4.70
- Erro Quadrático Médio (MSE): 43.64
- R2 Score: 0.85

Obtivemos um resultado bom, vamos avaliar o desempenho com um gráfico de dispersão.

#### Gráfico de Dispersão - Valores Reais vs. Valores Previstos

O gráfico de dispersão apresenta a relação entre os valores reais e os valores previstos pela regressão linear. Os pontos estão próximos da linha diagonal, indicando que o modelo de regressão linear fez previsões precisas para a taxa de mortalidade infantil.

![image](https://github.com/MiguelFreire-bit/Prever_taxa_mortalidade_infantil/assets/72529654/c8966420-b0f7-4997-8393-65ae6f939106)


### Árvore de Decisão Regressiva

A árvore de decisão regressiva também foi aplicada para prever a taxa de mortalidade infantil. As métricas de erro foram utilizadas para avaliar o desempenho do modelo:

- Erro Médio Absoluto (MAE): 5.39
- Erro Quadrático Médio (MSE): 68.64
- R2 Score: 0.76

**Essas métricas mudam sempre que o modelo é aplicado, podendo ficar melhor ou pior**

#### Gráfico de Dispersão - Valores Reais vs. Valores Previstos

O gráfico de dispersão apresenta a relação entre os valores reais e os valores previstos pela árvore de decisão regressiva. Embora os pontos estejam dispersos, a tendência geral ainda segue a linha diagonal, indicando que o modelo é razoavelmente preciso, mas menos preciso que a regressão linear.

---

### Principais Características que Afetam a Taxa de Mortalidade Infantil

De acordo com o modelo desenvolvido, as principais características que afetam a taxa de mortalidade infantil são:

1. Matrícula Bruta na Educação Terciária (%): Quanto maior a porcentagem de matrícula bruta na educação terciária, menor tende a ser a taxa de mortalidade infantil.
2. Gastos com Saúde Paga pelo Paciente: Países com gastos menores com saúde paga pelo paciente apresentam maiores taxas de mortalidade infantil.
3. Razão de Mortalidade Materna: O aumento da razão de mortalidade materna está associado a um aumento na taxa de mortalidade infantil.
4. Médicos por mil habitantes: A disponibilidade de mais médicos por mil habitantes parece estar relacionada a uma redução na taxa de mortalidade infantil.

## Contribuição

Contribuições são bem-vindas! Se você deseja contribuir para este projeto, siga as diretrizes de colaboração e envie uma solicitação de pull.

## Contato

Se tiver alguma dúvida ou sugestão, sinta-se à vontade para entrar em contato:

- E-mail: miguelsilvafreire@hotmail.com
- Linkedin: (https://www.linkedin.com/in/miguel-freire99/)
