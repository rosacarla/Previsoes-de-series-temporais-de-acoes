#### 📈 ANÁLISES AVANÇADAS E GRÁFICOS DE VELAS COM API YAHOO FINANCE

Projeto desenvolvido para realizar análises mais avançadas de dados de ações, obtidos da API Yahoo Finance, e construir gráficos com Plotly e MPLFinance no Google Colab.  
É uma proposta de trabalho feita na <i>Imersão Python: Do Excel à Análise de Dados</i>, promovida pela Alura.    

<img src='https://i.postimg.cc/9QDfxRC5/aula04-cabecalho.png'>  

---

#### 💬 BIBLIOTECAS NECESSÁRIAS  

```python
import pandas as pd
import matplotlib.pyplot as plt
import matplotlib.dates as mdates
import mplfinance as mpf
import yfinance as yf  # API Yahoo Finance tem dados de ações
import plotly.graph_objects as go
from plotly.subplots import make_subplots
```

---  

### 📊 CRIAÇÃO DE GRÁFICOS PARA DEMONSTRAR VARIAÇÃO DO PREÇO DE AÇÕES NO FECHAMENTO
<img src='https://github.com/rosacarla/Analises-avancadas-e-graficos-de-velas/blob/main/images/aula04-graficos.png'>

- gráfico de linha com biblioteca Pandas da variação da ação PETR4 por data
```python
# Plota gráfico com dados da coluna Fechamento usando biblioteca Pandas
# Plotar significa desenhar, ampliar, mostrar uma figura
dados['Fechamento'].plot(figsize=(10,6))
plt.title('VARIAÇÃO DO PREÇO POR DATA', fontsize=16)
plt.legend(['Fechamento'])
```
- gráfico de candles ou velas com Matplotlib da variação da ação PETR4 em período de 60 dias
<img src='https://github.com/rosacarla/Analises-avancadas-e-graficos-de-velas/blob/main/images/aula04-candle-matplotlib.png'>

- gráfico de candles interativo com subplots e função Candlesticks da variação e valores transacionados de PETR4 em 60 dias
<img src='https://github.com/rosacarla/Analises-avancadas-e-graficos-de-velas/blob/main/images/auka04-subplots-candlestick.png'>

- gráfico de candles interativo refeito com a `API mágica`
  
```python
# Cria grafico de candlestick para ação PETR4 com API mágica!
mpf.plot(dados.head(60), type='candle', figsize = (16,8), volume=True, mav=(7,14), style='yahoo')
```
---  

### 🧠 DESAFIOS DA AULA 4  

<img src='https://github.com/rosacarla/Analises-avancadas-e-graficos-de-velas/blob/main/images/aula04-desafio.png'>  

- Pesquisar o que é uma tupla em Python;
- Buscar a ação da Apple e recriar o gráfico de Candlestick usando a biblioteca MPLFinance.

☑️ RESOLUÇÃO DOS DESAFIOS  

- Desafio 1 
<img src='https://github.com/rosacarla/Analises-avancadas-e-graficos-de-velas/blob/main/images/aula04-desafio1.png'>

- Desafio 2
<img src='https://github.com/rosacarla/Analises-avancadas-e-graficos-de-velas/blob/main/images/aula04-candlestick-mike.png'>

Ver resolução completa no [notebook do Google Colab](https://colab.research.google.com/github/rosacarla/Analises-avancadas-e-graficos-de-velas/blob/main/Imersao_Python_Aula04.ipynb).  

---  

#### ✍️ AUTORA  
Carla Edila Silveira  
Contato: rosa.carla@pucpr.edu.br  

---

#### ©️ LICENÇA

[MIT](https://choosealicense.com/licenses/mit/)  

---  

#### 🔗 LINKS ÚTEIS  

[Biblioteca Matplotlib: Visualization with Python](https://matplotlib.org/)  
[Gráficos Matplotlib no Python](https://www.alura.com.br/artigos/criando-graficos-no-python-com-a-matplotlib?_gl=1*1dc3t7n*_ga*MTkyMTEwNTQ2Ni4xNzA5NTk0NTU0*_ga_1EPWSW3PCS*MTcxMTY4Mjc0MC4zNC4xLjE3MTE2ODI3NDkuMC4wLjA.*_fplc*aklKWnYxSTAybVRJVGltNVZieW1WYXdZbkp0elglMkZyb0dYdnFQcll2WGpreXMwS1VsQlBESEpXcGdmcm05ZWZXWTNpUXFiZFptR1psY2taRVVQVTV3cWtVc0R4dEFhN1JsSmZOOEtMUzlYbjNvRGs0ZmY2bGRnSmpvelhmdXclM0QlM0Q.)  
[O que é API](https://www.alura.com.br/artigos/api?_gl=1*rcnrb*_ga*MTkyMTEwNTQ2Ni4xNzA5NTk0NTU0*_ga_1EPWSW3PCS*MTcxMTY4NTA4OC4zNS4wLjE3MTE2ODUxMzEuMC4wLjA.*_fplc*aklKWnYxSTAybVRJVGltNVZieW1WYXdZbkp0elglMkZyb0dYdnFQcll2WGpreXMwS1VsQlBESEpXcGdmcm05ZWZXWTNpUXFiZFptR1psY2taRVVQVTV3cWtVc0R4dEFhN1JsSmZOOEtMUzlYbjNvRGs0ZmY2bGRnSmpvelhmdXclM0QlM0Q.)  
[Conheça o Yahoo Finanças](https://br.financas.yahoo.com/quote/%5EBVSP?p=%5EBVSP)  
[Conheça as bibliotecas de Data Visualization do Python](https://www.alura.com.br/artigos/data-visualization-conhecendo-bibliotecas-python?_gl=1*tlxvhm*_ga*MTkyMTEwNTQ2Ni4xNzA5NTk0NTU0*_ga_1EPWSW3PCS*MTcxMTY4NTA4OC4zNS4xLjE3MTE2ODUxNzUuMC4wLjA.*_fplc*aklKWnYxSTAybVRJVGltNVZieW1WYXdZbkp0elglMkZyb0dYdnFQcll2WGpreXMwS1VsQlBESEpXcGdmcm05ZWZXWTNpUXFiZFptR1psY2taRVVQVTV3cWtVc0R4dEFhN1JsSmZOOEtMUzlYbjNvRGs0ZmY2bGRnSmpvelhmdXclM0QlM0Q.)  
[Biblioteca MPLFinance](https://github.com/matplotlib/mplfinance)  
[Traçar gráfico de velas usando o módulo MPLFinance em Python](https://acervolima.com/tracar-grafico-de-velas-usando-o-modulo-mplfinance-em-python/)  
[Aprenda a visualizar dados financeiros com Python e MPLFinance](https://awari.com.br/aprenda-a-visualizar-dados-financeiros-com-python-e-mplfinance/#:~:text=A%20biblioteca%20mplfinance%20possui%20uma,Personaliza%C3%A7%C3%A3o%20dos%20gr%C3%A1ficos)

---
