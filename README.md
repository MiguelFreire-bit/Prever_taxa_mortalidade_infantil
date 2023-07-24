# Previsão Notas Enem 2020

Prever o desempenho dos alunos no ENEM 2020 com base nos resultados do ENEM 2019

# Objetivo

O objetivo é conhecer o banco de dados e extrair insights sobre as relações das notas com diferentes variáveis, como idade, sexo, tipo de escola, etc. Em seguida, desenvolver uma função que faça a previsão das notas futuras com base nas notas presentes no dataset, permitindo fazê-las com grupos específicos. Por exemplo, prever as notas das mulheres em diferentes disciplinas com base apenas nas notas delas presentes no dataset.

## Algumas perguntas que serão respondidas:

1. As notas de diferentes provas se comportam da mesma maneira? As notas de redação possuem outro padrão?
2. Qual é a distribuição de Homens e Mulheres no dataset? 
3. Qual diferença das notas entre homens e mulheres?
4. Qual a distribuição de idade entre os candidatos? O que justifica as idades mais recorrentes? Para homens e mulheres seguem o mesmo padrão?
5. Qual nota média de cada prova por idade? varia muito ou pouco?
6. Qual a distribuição dos candidatos entre escolas públicas ou privadas?
7. Qual nota média de cada prova por tipo de escola? varia muito ou pouco?
8. Qual a relação entre a idade e o tipo de escola que o candidato frequentou? 

Após esta análise será criado um modelo de previsão para as notas baseado em variáveis bem correlacionadas e a análise gráfica desse modelo utilizando gráficos de dispersão entre Valor real x Valor previsto. Além também de avaliações utilizando Erro médio quadrático (MSE) e Coeficiente de determinação (R²)


## Pré-requisitos

Antes de executar o código, certifique-se de ter as seguintes bibliotecas instaladas:

- pandas
- matplotlib
- seaborn
- sklearn

## Resultados
## Vamos responder as perguntas:

## 1. As notas de diferentes provas se comportam da mesma maneira? As notas de redação possuem outro padrão?

Minha intenção é remover todas as notas 0 de redação do dataset. O motivo é que existe muitos críterios para zerar a prova de Redação que são COMPLETAMENTE diferentes das DEMAIS provas. O que faz que signifiquem coisas diferentes

A prova de redação no ENEM possui critérios de avaliação diferentes das demais provas objetivas. Enquanto as notas das provas objetivas são baseadas no número de acertos, a nota da redação é atribuída com base em critérios de correção específicos, como a estrutura textual, argumentação, coesão, coerência, entre outros.

É coerente remover as notas de redação zero se pretendo usar esses dados como entrada para um modelo de regressão, uma vez que essas notas podem distorcer as relações de correlação e impactar negativamente a qualidade do modelo

## 2. Qual é a distribuição de Homens e Mulheres no dataset?

![image](https://github.com/MiguelFreire-bit/PREVISAO_NOTAS_ENEM/assets/72529654/17acd334-88f7-4bcc-bd28-f288b892e2b8)

59.5% dos estudantes dessa amostra são Mulheres, 40.5% são Homens

## 3. Qual diferença das notas entre homens e mulheres?


![image](https://github.com/MiguelFreire-bit/PREVISAO_NOTAS_ENEM/assets/72529654/7cc83294-ed90-4c5d-b171-4ac999eb0490)

Os homens em geral possuem maiores médias em diferentes provas, exceto na Redação

## 4. Qual a distribuição de idade entre os candidatos? O que justifica as idades mais recorrentes? Para homens e mulheres seguem o mesmo padrão?

![image](https://github.com/MiguelFreire-bit/PREVISAO_NOTAS_ENEM/assets/72529654/67801e77-9bbb-4424-a110-8898b0c3c2b9)

![image](https://github.com/MiguelFreire-bit/PREVISAO_NOTAS_ENEM/assets/72529654/59ea4498-e53e-4273-bc3d-2aafc0a26f53)

Aqui podemos ter uma noção de como os dados são significatvos. Dentro do contexto do Enem é comum que a maioria dos candidatos tenha idade igual ou proxima a média de que se conclui o ENSINO MÉDIO. Nota-se essa têndencia no gráfico de densidade. Soma-se a isso o fato de que mesmo havendo bem menos homens que mulheres eles apresentam DISTRIBUIÇÃO parecida, como deveria ser para uma amostra SIGNIFICATIVA

## 5. Qual nota média de cada prova por idade? varia muito ou pouco?

![image](https://github.com/MiguelFreire-bit/PREVISAO_NOTAS_ENEM/assets/72529654/bffaf704-1251-467e-a2d5-1b0f120ada9e)

entre 17 e 21 anos (que representa 71,45% de todos os alunos da base de dados) as diferenças não são tão altas.

## 6. Qual a distribuição dos candidatos entre escolas públicas ou privadas?

![image](https://github.com/MiguelFreire-bit/PREVISAO_NOTAS_ENEM/assets/72529654/a3267961-a142-44d4-ab43-4145062aa712)

A maioria das pessoas dessa amostra não responderam, o motivo é desconhecido. Porém, todos os treineiros (fazem a prova para treinar e não efetivamente para concorrer) não responderam esse questionamento. Talvez por essas informações não serem solicitadas a eles.

## 7. Qual nota média de cada prova por tipo de escola? varia muito ou pouco?

![image](https://github.com/MiguelFreire-bit/PREVISAO_NOTAS_ENEM/assets/72529654/1a89b48d-47d3-49c7-b7ae-098df1473911)

Os alunos das escola privadas possuem maiores notas em todas as provas.

## 8. Qual a relação entre a idade e o tipo de escola que o candidato frequentou?

![image](https://github.com/MiguelFreire-bit/PREVISAO_NOTAS_ENEM/assets/72529654/d7bfbfc2-f6a9-420a-9268-e26e44726bbf)

Esse gráfico de densidade já é diferente, muito provavelmente por haver divisões dos dados em 3 categorias e pela exclusão dos dados "Não respondeu", o que deixa apenas uma minoria dos dados. No entanto, ainda conseguimos notar, mesmo que de forma menos suavizada, a tendência de idade que comentamos antes.

Uma observação importante é que nas escolas públicas não há um pico tão significativo em 17 anos, o que pode indicar que os alunos de escolas públicas estão se formando mais tarde ou que não fazem o Enem ao concluir o ensino médio

![image](https://github.com/MiguelFreire-bit/PREVISAO_NOTAS_ENEM/assets/72529654/02e618a8-69b6-4b88-9ecb-32bff8dbd8c9)

fonte: https://www1.folha.uol.com.br/educacao/2022/11/so-1-em-cada-4-alunos-que-sai-da-escola-publica-faz-o-enem.shtml

## Modelagem 
Após Conhecer a base de dados foi desenvolvido uam função chamada previsão_nota e previsão_nota_redacao. A primeira prever as nota de matemática, linguagens, ciencias humanas e da natureza; e a segunda as notas de redação. Essa divisão em duas funções ocorrem devido as variáveis explicativas são diferentes.

Para ambas as funções doi utilizado a biblioteca sklearn, o modelo foi criado utilizando LinearRegression. As funções recebem a matéria que queremos avaliar notas (matemática, redação, etc) e como segundo parâmetro o sexo dos estudantes para os quais vamos fazer a previsão 

o primeiro modelo teve as seguintes métricas

Erro médio quadrático (MSE): 5882.89
Coeficiente de determinação (R²): 0.51

e uma dispersão entre valor real x valor previsto representado na figura abaixo:

![image](https://github.com/MiguelFreire-bit/PREVISAO_NOTAS_ENEM/assets/72529654/e816f4b2-fc99-4236-bc34-96fdd74d5f9f)

temos um modelo não tão eficiente. Podemos notar que para um `valor real` temos inúmeros `valores de previsão`, mostrando que o modelo não é bom.


o Segundo modelo teve as seguintes métricas

Erro médio quadrático (MSE): 2227.42
Coeficiente de determinação (R²): 0.91

E dos motivos para o resultado muito positivo é que algumas das variáveis explicativas eram partes da nota de redação correspondentes, ou seja, possuiam alta correlação (se usasse todas as componentes R² seria 1)

e uma dispersão entre valor real x valor previsto representado na figura abaixo:

![image](https://github.com/MiguelFreire-bit/PREVISAO_NOTAS_ENEM/assets/72529654/ebcdc008-d451-430c-98b5-d9404681f8de)

## Contribuição

Contribuições são bem-vindas! Se você deseja contribuir para este projeto, siga as diretrizes de colaboração e envie uma solicitação de pull.

## Aprendizado

Aprendi bastante sobre interpretar diferentes contextos através de gráficos, além de entender melhor como se caracteriza, em média, um indivíduo que faz o ENEM e como realidades diversas podem afetar as métricas.

Por exemplo, perceber que apesar de haver mais mulheres do que homens no dataframe em geral todos apresentam uma distribuição parecida de idade. O que está de acordo com o contexto do ENEM e de quem é a maioria do seu público alvo

Também desenvolvi gráficos melhores e mais informativos. Foi possível perceber a diferença de pontuação entre homenes e mulheres de forma bem mais clara e objetiva com somente um gráfico

```python
escola = df.query("IN_TREINEIRO == 'Não'").groupby('TP_ESCOLA')[['NU_NOTA_CN','NU_NOTA_CH','NU_NOTA_LC','NU_NOTA_MT','NU_NOTA_REDACAO']].mean()
escola = escola.query("TP_ESCOLA != 'Não Respondeu'").reset_index()

# Transformar os dados no formato "longo"
df_long = pd.melt(escola, id_vars='TP_ESCOLA', var_name='Notas', value_name='Pontuação')

# Plotagem do gráfico de barras
plt.figure(figsize=(10, 6))
ax = sns.barplot(data=df_long, x='Notas', y='Pontuação', hue='TP_ESCOLA', palette='magma')

# Adicionar os valores nas barras
for p in ax.patches:
    ax.annotate(format(p.get_height(), '.2f'), 
                (p.get_x() + p.get_width() / 2., p.get_height()), 
                ha='center', va='center', xytext=(0, 6), textcoords='offset points')
    
plt.xlabel('Notas')
plt.ylabel('Pontuação')
plt.title('Pontuação por Tipo de Escola')
plt.legend(title='Escola')

plt.show()
```

E desenvolver meu conhecimento em modelos preditivos. Apesar de ser uma parte mais resumida do projeto foi possível aprimorar o entendimento e o código necessário para executar esse tipo de aplicação. Como ponto a melhorar buscarei desenvolver mais técnicas de previsão para encontrar um encaixe melhor.

```python
#Dividir os dados em conjuntos de treinamento e teste:
#Separe uma parte dos dados para treinar o modelo e outra parte para avaliar seu desempenho.


from sklearn.model_selection import train_test_split
from sklearn.linear_model import LinearRegression
from sklearn.metrics import mean_squared_error, r2_score

# Separar os dados em conjunto de treino e teste

def previsão_nota (z, sexo_aluno): 

    X = df.drop(['NU_IDADE', 'NU_INSCRICAO', 'TP_SEXO', 'TP_ANO_CONCLUIU', 'TP_ESCOLA', 'IN_TREINEIRO','NU_NOTA_COMP1',
             'NU_NOTA_COMP2', 'NU_NOTA_COMP3', 'NU_NOTA_COMP4','NU_NOTA_COMP5', z], axis=1)
    y = df[z]

    X_train, X_test, y_train, y_test = train_test_split(X, y, test_size=0.2, random_state = 42)

    # Criar e treinar o modelo de regressão linear
    model = LinearRegression()
    model.fit(X_train, y_train)

    # Realizar previsões no conjunto de teste
    y_pred = model.predict(X_test)

    # Avaliar o desempenho do modelo: Calcular métricas de avaliação, como o erro médio quadrático (RMSE) ou o coeficiente de determinação (R²).
    mse = mean_squared_error(y_test, y_pred)   
    r2 = r2_score(y_test, y_pred)
    
    print(f'\nErro médio quadrático (MSE): {mse:.2f}')
    print(f'Coeficiente de determinação (R²): {r2:.2f}\n')
    
    # Prever a nota para o aluno específico, se o número de inscrição for fornecido
    if sexo_aluno:
        aluno_data = df[df['TP_SEXO'] == sexo_aluno]
        X_aluno = aluno_data.drop(['NU_IDADE', 'NU_INSCRICAO', 'TP_SEXO', 'TP_ANO_CONCLUIU', 'TP_ESCOLA', 'IN_TREINEIRO',
                                   'NU_NOTA_COMP1', 'NU_NOTA_COMP2', 'NU_NOTA_COMP3', 'NU_NOTA_COMP4', 'NU_NOTA_COMP5', z], axis=1)
        y_aluno_real = aluno_data[z].values[0]
        y_aluno_pred = model.predict(X_aluno)[0]
        
        print(f"Sexo {sexo_aluno}:")
        print(f"Nota real de {z}: {y_aluno_real:.2f}")
        print(f"Nota prevista de {z}: {y_aluno_pred:.2f}\n")
    
        y_aluno_real = aluno_data[z].values
        y_aluno_pred = model.predict(X_aluno)
        



        y_aluno_real = aluno_data[z].values
        y_aluno_pred = model.predict(X_aluno)
    
        return y_aluno_pred, y_aluno_real



y_aluno_pred_1, y_aluno_real_1 = previsão_nota('NU_NOTA_MT', 'Masculino' )
```


## Contato

Se tiver alguma dúvida ou sugestão, sinta-se à vontade para entrar em contato:

- E-mail: miguelsilvafreire@hotmail.com
- Linkedin: (https://www.linkedin.com/in/miguel-freire99/)
