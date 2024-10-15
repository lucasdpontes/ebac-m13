<br><br><h1 align="center">Introdução</h1>

Projeto de análise de dados, a partir de uma base de dados de produtos de um supermercado chileno.

<br><br><h1 align="center">Objetivo</h1>

Extrair insights através de análises estatísticas.

<br><br><h1 align="center">Metodologia e ferramentas</h1>

Aplicação de estatísticas descritivas como média, mediana, desvio padrão e análises gráficas.

Tecnolgias utilizadas:

- Google Collab
- Python
- Pandas
- Matplotlib
- Plotly

<br><br><h1 align="center">Resultados</h1>

Desvio padrão por categoria:
<div align="center">
  
| Categoria                   | Preço   |
|-----------------------------|---------------:|
| Beleza & cuidado pessoal    | 1783.556485    |
| Comidas prontas             | 3095.043478    |
| Congelados                  | 2108.042553    |
| Frutas                      | 1724.473684    |
| Instantâneos e sopas        | 765.491228     |
| Laticínios                  | 2385.219239    |
| Verduras                    | 1343.296875    |

</div>
<details>
  <summary>código</summary>
  
```
df_lacteos = df.loc[df['Categoria'] == 'Laticínios']

fig = px.box(df_lacteos, y='Preco_Normal', width=800, height=600, title='Distribuição de preços de produtos lácteos', labels={'Preco_Normal': 'Preço'})
fig.show()
```
</details>
<p align="center"><img src="https://github.com/lucasdpontes/ebac-m13/blob/main/boxplot.PNG?raw=true" width=600></p>


<details>
  <summary>código</summary>
  
```
df_media_desconto = df.groupby('Categoria')['Desconto'].mean().sort_values(ascending=False)

fig = px.bar(df_media_desconto, y='Desconto', width=600, height=600, title='Desconto médio por categoria', labels={'Categoria': ''})
fig.show()
```
</details>
<p align="center"><img src="https://github.com/lucasdpontes/ebac-m13/blob/main/bar.PNG?raw=true" width=600></p>

<br><br><h1 align="center">Conclusões</h1>

- conclusão 1
- conclusão 2
- conclusão 3
