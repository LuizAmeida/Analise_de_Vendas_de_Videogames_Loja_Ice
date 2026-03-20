# 🎮 Análise de Vendas de Videogames - Loja Ice

![Python](https://img.shields.io/badge/Python-3.9+-blue.svg)
![Pandas](https://img.shields.io/badge/Pandas-2.0+-green.svg)
![Jupyter](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)
![License](https://img.shields.io/badge/License-MIT-yellow.svg)
![Status](https://img.shields.io/badge/Status-Concluído-brightgreen.svg)



## 📋 Sobre o Projeto

Este projeto consiste em uma análise exploratória completa de dados de vendas de videogames, desenvolvida para a loja online **Ice**. O objetivo principal é identificar padrões que determinam o sucesso comercial de um jogo, utilizando dados históricos de vendas, avaliações de críticos e usuários, além de informações sobre plataformas, gêneros e classificações etárias.

A análise foi realizada considerando o cenário de **dezembro de 2016**, com o propósito de planejar campanhas publicitárias estratégicas para **2017**.



## 🎯 Objetivos

- Identificar padrões que influenciam o sucesso comercial de jogos
- Analisar o ciclo de vida de diferentes plataformas de jogos
- Investigar a correlação entre avaliações (críticas e usuários) e vendas
- Criar perfis de consumo por região geográfica (América do Norte, Europa e Japão)
- Testar hipóteses estatísticas sobre notas de usuários entre plataformas e gêneros
- Fornecer recomendações estratégicas baseadas em dados para campanhas de marketing



## 📊 Fonte de Dados

O conjunto de dados utilizado contém informações de jogos lançados até 2016, incluindo:

| Campo | Descrição |
|-------|-----------|
| **Name** | Nome do jogo |
| **Platform** | Plataforma de lançamento (Xbox, PlayStation, PC, Nintendo, etc.) |
| **Year_of_Release** | Ano de lançamento |
| **Genre** | Gênero do jogo (Action, Sports, RPG, etc.) |
| **NA_sales** | Vendas na América do Norte (em milhões de USD) |
| **EU_sales** | Vendas na Europa (em milhões de USD) |
| **JP_sales** | Vendas no Japão (em milhões de USD) |
| **Other_sales** | Vendas em outras regiões (em milhões de USD) |
| **Critic_Score** | Pontuação da crítica (0-100) |
| **User_Score** | Pontuação dos usuários (0-10) |
| **Rating** | Classificação etária ESRB |



## 🔍 Principais Análises Realizadas

### 1. Preparação e Limpeza dos Dados
- Padronização de nomenclatura das colunas
- Tratamento de valores ausentes
- Conversão de tipos de dados
- Criação da coluna `total_sales` (soma das vendas globais)



### 2. Análise Temporal e de Plataformas
- Evolução do número de lançamentos por ano
- Identificação do ciclo de vida das plataformas
- Análise das plataformas líderes de mercado
- Boxplots comparativos de vendas entre plataformas



### 3. Correlação Reviews vs Vendas
- Análise de correlação entre `critic_score` e vendas
- Análise de correlação entre `user_score` e vendas
- Scatter plots para visualização das relações



### 4. Perfil de Usuário por Região
- Top 5 plataformas por região (NA, EU, JP)
- Top 5 gêneros por região
- Impacto da classificação ESRB nas vendas regionais



### 5. Testes de Hipóteses Estatísticas
- **H₁**: Comparação das notas médias entre Xbox One e PC
- **H₂**: Comparação das notas médias entre gêneros Action e Sports



## 📈 Principais Descobertas

### 🎮 Plataformas Dominantes

| Região | Plataforma Líder | Segunda Plataforma | Terceira Plataforma |
|--------|------------------|-------------------|---------------------|
| **Global** | PS4 | PS3 | X360 |
| **América do Norte** | X360 | PS4 | PS3 |
| **Europa** | PS4 | PS3 | X360 |
| **Japão** | 3DS | PS3 | PSV |



### 🎭 Gêneros Mais Lucrativos

| Região | 1º Lugar | 2º Lugar | 3º Lugar |
|--------|----------|----------|----------|
| **Global** | Action | Shooter | Role-Playing |
| **América do Norte** | Action | Shooter | Sports |
| **Europa** | Action | Shooter | Sports |
| **Japão** | Role-Playing | Action | Misc |



### 📊 Correlação Reviews vs Vendas

| Métrica | Correlação | Significância |
|---------|------------|---------------|
| **Critic Score vs Vendas** | 0.41 | Moderada e positiva |
| **User Score vs Vendas** | -0.03 | Muito baixa |



### 🔞 Classificação ESRB

| Região | Classificação Dominante |
|--------|------------------------|
| **América do Norte** | M (Mature) |
| **Europa** | M (Mature) |
| **Japão** | Unknown |



## 🧪 Resultados dos Testes de Hipóteses

### H₁: Xbox One vs PC
- **Hipótese Nula (H₀)**: As classificações médias dos usuários para Xbox One e PC são iguais
- **Hipótese Alternativa (H₁)**: As classificações médias são diferentes
- **Resultado**: Não rejeitamos H₀ (p-valor = 0.549 > 0.05)
- **Conclusão**: Não há evidências de diferença nas notas médias entre as plataformas


### H₂: Action vs Sports
- **Hipótese Nula (H₀)**: As classificações médias para Action e Sports são iguais
- **Hipótese Alternativa (H₁)**: As classificações médias são diferentes
- **Resultado**: Rejeitamos H₀ (p-valor ≈ 0.000 < 0.05)
- **Conclusão**: As notas médias são estatisticamente diferentes (Action tem média maior)



## 💡 Recomendações para Campanha 2017

### 🇺🇸 América do Norte
- **Plataformas**: Priorizar PS4, XOne e X360
- **Gêneros**: Action, Shooter e Sports
- **Classificação ESRB**: Foco em jogos "M" (Mature)
- **Estratégia**: Aproveitar a popularidade do Xbox na região


### 🇪🇺 Europa
- **Plataformas**: Concentrar esforços em PS4 e PS3
- **Gêneros**: Action, Shooter e Sports
- **Classificação ESRB**: Priorizar jogos "M" (Mature)
- **Estratégia**: PlayStation é dominante - deve ser o foco principal


### 🇯🇵 Japão
- **Plataformas**: Focar em 3DS, PS3 e PSV
- **Gêneros**: Role-Playing e Action
- **Classificação ESRB**: Priorizar jogos locais (muitos sem classificação)
- **Estratégia**: Mercado único, com forte preferência por portáteis e RPGs



### 🌍 Recomendação Global
- Priorizar jogos de Action e Shooter bem avaliados pela crítica
- Investir em títulos com classificação "M" para mercados ocidentais
- Considerar parcerias com desenvolvedores japoneses para conteúdo localizado



## 🛠️ Tecnologias Utilizadas

| Tecnologia | Finalidade |
|------------|------------|
| **Python 3.9+** | Linguagem principal |
| **Pandas** | Manipulação e análise de dados |
| **NumPy** | Operações numéricas |
| **Matplotlib** | Visualização de dados |
| **Seaborn** | Visualizações estatísticas |
| **SciPy** | Testes de hipóteses estatísticas |
| **Jupyter Notebook** | Ambiente de desenvolvimento interativo |



## 📁 Estrutura do Projeto
````
analise-vendas-games/
├── README.md # Este arquivo
├── requirements.txt # Dependências do projeto
├── .gitignore # Arquivos ignorados pelo Git
├── LICENSE # Licença MIT
├── notebook.ipynb # Análise completa
└── datasets/
└── games.csv # Dataset original
````


## 🚀 Como Executar

### 1. Clone o repositório
```bash
git clone https://github.com/LuizAmeida/Analise_de_Vendas_de_Videogames_Loja_Ice
````


### 2. Crie um ambiente virtual (recomendado)
````
# Windows
python -m venv venv
venv\Scripts\activate

# Linux/Mac
python -m venv venv
source venv/bin/activate
````


### 3. Instale as dependências
````
pip install -r requirements.txt
````


### 4. Execute o Jupyter Notebook
````
jupyter notebook notebook.ipynb
````


### 5. Visualize online (alternativa)
- **NBViewer**: [Clique aqui](https://nbviewer.org/github/seu-usuario/analise-vendas-games/blob/main/notebook.ipynb) para visualizar o notebook diretamente no navegador
- **Google Colab**: [Abrir no Colab](https://colab.research.google.com/github/seu-usuario/analise-vendas-games/blob/main/notebook.ipynb) para executar o notebook na nuvem



### 📦 Dependências
````
pandas==2.0.3
numpy==1.24.3
matplotlib==3.7.2
seaborn==0.12.2
scipy==1.10.1
jupyter==1.0.0
````


### 🤝 Como Contribuir
1. Faça um fork do projeto
2. Crie uma branch para sua feature (git checkout -b feature/AmazingFeature)
3. Commit suas mudanças (git commit -m 'Add some AmazingFeature')
4. Push para a branch (git push origin feature/AmazingFeature)
5. Abra um Pull Request



### 📄 Licença
- Este projeto está sob a licença MIT. Veja o arquivo LICENSE para mais detalhes.



### ✨ Autor
- Desenvolvido como parte do projeto integrado da Sprint 6 do curso de Análise de Dados
- [![LinkedIn](https://img.shields.io/badge/LinkedIn-0077B5?style=for-the-badge&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/luizmarques84)
- [![GitHub](https://img.shields.io/badge/GitHub-100000?style=for-the-badge&logo=github&logoColor=white)](https://github.com/LuizAlmeida)



### ⚠️ Nota Importante
- Os dados de 2016 podem estar incompletos. As recomendações devem ser reavaliadas quando dados mais completos estiverem disponíveis.


---

<div align="center">
  
### ⭐️ Se este projeto foi útil para você, considere dar uma estrela! ⭐️

</div>
