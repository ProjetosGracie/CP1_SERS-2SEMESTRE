# ⚡ Análise de Dados de Energia Elétrica — São Paulo

<p align="center">
  <strong>Uma análise exploratória da carga elétrica do Estado de São Paulo utilizando dados públicos do ONS.</strong>
</p>

---

## 📋 Sobre o Projeto

Este projeto foi desenvolvido com o objetivo de realizar uma **análise de dados de carga elétrica** utilizando informações públicas disponibilizadas pelo **Operador Nacional do Sistema Elétrico (ONS)**.

A análise utiliza dados referentes à região de **São Paulo (SP)** e busca compreender o comportamento da demanda elétrica ao longo do período analisado, utilizando técnicas de **manipulação de dados, estatística descritiva e visualização gráfica**.

Além da análise exploratória, o projeto também utiliza recursos de **Inteligência Artificial Generativa** como apoio para a elaboração de um relatório técnico, sempre com base nos resultados efetivamente calculados durante a análise.

---

# 🎯 Objetivos

O projeto tem como principais objetivos:

* 📡 Realizar a consulta de dados por meio de uma API pública do ONS;
* 📊 Construir e inspecionar um DataFrame utilizando Pandas;
* 🧹 Organizar e preparar os dados para análise;
* 📈 Calcular indicadores estatísticos relacionados à carga elétrica;
* ⚡ Identificar períodos de alta demanda;
* 🔍 Criar diferentes critérios para segmentação dos dados;
* 📉 Desenvolver visualizações gráficas para facilitar a interpretação;
* 🤖 Utilizar Inteligência Artificial como apoio na elaboração de um relatório técnico;
* ✅ Realizar uma validação crítica dos resultados gerados.

---

# 🌎 Fonte dos Dados

Os dados utilizados neste projeto são disponibilizados pelo:

**Operador Nacional do Sistema Elétrico (ONS)** 🇧🇷

A análise utiliza informações da base de **Carga Verificada**, disponibilizada por meio da API pública do ONS.

📌 **Região analisada:** São Paulo — SP
📅 **Período analisado:** 01/08/2025 a 07/08/2025

---

# 🛠️ Tecnologias Utilizadas

O projeto foi desenvolvido utilizando Python e as seguintes bibliotecas:

| Tecnologia           | Finalidade                            |
| -------------------- | ------------------------------------- |
| 🐍 **Python**        | Linguagem principal do projeto        |
| 🐼 **Pandas**        | Manipulação e análise dos dados       |
| 📡 **Requests**      | Consulta à API pública                |
| 📊 **Matplotlib**    | Criação de gráficos                   |
| 📈 **Seaborn**       | Visualização estatística dos dados    |
| 🤖 **Google Gemini** | Apoio na geração do relatório técnico |

---

# 📂 Estrutura da Análise

O projeto está organizado em diferentes etapas, permitindo acompanhar todo o processo de análise dos dados.

## 1️⃣ Consulta à API

Inicialmente, é realizada uma requisição para a API pública do ONS utilizando a biblioteca `requests`.

Os parâmetros utilizados definem:

* 📅 Data inicial;
* 📅 Data final;
* 🗺️ Região analisada.

Os dados retornados pela API estão no formato **JSON** e são posteriormente preparados para análise.

---

## 2️⃣ Construção do DataFrame

Após a obtenção dos dados, os registros são transformados em um **DataFrame Pandas**.

Nesta etapa são realizadas análises iniciais como:

* Visualização dos primeiros registros;
* Quantidade de linhas e colunas;
* Identificação dos atributos disponíveis;
* Verificação dos tipos de dados;
* Análise estatística inicial.

---

## 3️⃣ Organização dos Dados

Os principais atributos são renomeados para facilitar a leitura e interpretação durante o desenvolvimento do projeto.

Entre as informações analisadas estão:

* 🕒 Data e horário de referência;
* 🗺️ Área de carga;
* ⚡ Valor da carga elétrica global;
* 📊 Outros indicadores disponibilizados pela API.

Também são realizadas verificações relacionadas a:

* Valores ausentes;
* Formato dos dados;
* Estrutura das variáveis;
* Tipos numéricos.

---

# 📊 Indicadores Calculados

A análise estatística da carga elétrica considera os seguintes indicadores:

* 🔻 **Carga mínima**
* 🔺 **Carga máxima**
* 📈 **Carga média**
* 📍 **Mediana**
* ↔️ **Amplitude entre os valores máximo e mínimo**
* 🔢 **Quantidade total de medições**

Esses indicadores permitem compreender melhor o comportamento geral da carga elétrica durante o período analisado.

---

# 🔥 Análise de Alta Demanda

Para identificar os períodos de maior consumo, foi definido o seguinte critério:

> ⚡ Registros com carga superior a **90% da carga máxima observada**.

A partir desse critério são calculados:

* O limiar de alta demanda;
* A quantidade de registros acima do limite;
* O percentual desses registros em relação ao total;
* O maior valor de carga observado;
* O período correspondente ao pico de demanda, quando disponível.

Essa etapa permite identificar se os momentos próximos ao pico representam uma parcela significativa ou reduzida do período analisado.

---

# 🔍 Segundo Critério de Análise

Além da análise de alta demanda, foi criado um segundo critério para segmentar os dados.

O critério escolhido foi:

### 📈 Carga acima da média

São selecionados todos os registros cuja carga elétrica global está acima da média calculada para o período.

Posteriormente, são realizadas comparações entre:

* 🔥 Registros classificados como alta demanda;
* 📈 Registros com carga acima da média;
* 📊 Percentuais de cada grupo;
* 🔗 Registros presentes em ambos os critérios.

---

# 📉 Visualizações

Foram desenvolvidos gráficos para facilitar a interpretação dos dados.

## 📈 Evolução da Carga Elétrica

O primeiro gráfico apresenta o comportamento da carga elétrica ao longo do período analisado.

Essa visualização permite observar:

* Variações na demanda;
* Momentos de crescimento e redução;
* Picos de consumo;
* Tendências ao longo das observações.

---

## 📊 Distribuição da Carga Elétrica

O segundo gráfico utiliza um histograma para representar a distribuição dos valores de carga elétrica.

Com essa análise é possível observar:

* A concentração dos valores;
* A frequência das diferentes faixas de carga;
* O comportamento geral da distribuição.

---

# 🤖 Inteligência Artificial no Projeto

A Inteligência Artificial Generativa é utilizada como **ferramenta de apoio** para a elaboração de um relatório técnico.

⚠️ É importante destacar que a IA **não substitui a análise realizada pela equipe**.

Os resultados utilizados na geração do relatório são previamente calculados no próprio notebook, incluindo:

* Região analisada;
* Período;
* Quantidade de registros;
* Carga mínima;
* Carga máxima;
* Média;
* Mediana;
* Limiar de alta demanda;
* Percentuais;
* Momento do pico;
* Resultado do segundo critério.

Dessa forma, a Inteligência Artificial recebe informações já produzidas durante a análise.

---

# ✅ Validação Crítica

Após a geração do relatório com apoio da IA, é realizada uma validação crítica para verificar:

* ✔️ Se os indicadores foram utilizados corretamente;
* ✔️ Se todas as informações podem ser confirmadas pelos dados;
* ✔️ Se existem interpretações exageradas;
* ✔️ Se houve atribuição de causalidade sem evidências;
* ✔️ Quais alterações foram realizadas pela equipe.

Essa etapa é fundamental para garantir que o relatório final esteja alinhado com os dados analisados.

---

# 📌 Principais Resultados

Durante a análise da carga elétrica de São Paulo, foram obtidos indicadores importantes sobre o comportamento da demanda no período estudado.

Entre os principais resultados estão:

* ⚡ **Carga mínima:** aproximadamente **12.139 MW**
* ⚡ **Carga máxima:** aproximadamente **23.185 MW**
* 📊 **Carga média:** aproximadamente **17.871 MW**
* 📍 **Mediana:** aproximadamente **18.199 MW**
* 📈 **Total de registros analisados:** **336 observações**

Esses resultados permitem identificar uma variação significativa entre os valores mínimos e máximos registrados durante o período analisado.

---

# 🚀 Como Executar o Projeto

## 1. Clone o repositório

```bash
git clone <URL_DO_REPOSITORIO>
```

## 2. Instale as dependências

```bash
pip install requests pandas matplotlib seaborn
```

Caso deseje utilizar a funcionalidade opcional de Inteligência Artificial:

```bash
pip install google-genai
```

## 3. Execute o Notebook

Abra o arquivo `.ipynb` utilizando uma das seguintes opções:

* 🟠 Google Colab;
* 🟢 Jupyter Notebook;
* 🔵 Visual Studio Code.

Execute as células na ordem apresentada para garantir o funcionamento correto da análise.

---

# 🔐 Configuração da API do Gemini

A utilização do Gemini é opcional.

Para utilizar esse recurso no Google Colab:

1. Acesse a área de **Secrets**;
2. Crie uma variável chamada:

```text
GEMINI_API_KEY
```

3. Insira sua chave de API;
4. Permita o acesso do notebook ao Secret.

⚠️ **Nunca insira sua chave de API diretamente no código ou envie informações sensíveis para o GitHub.**

---

# 📚 Aprendizados Desenvolvidos

Este projeto permitiu aplicar conhecimentos relacionados a:

* 🐍 Programação em Python;
* 📡 Consumo de APIs;
* 🐼 Manipulação de dados com Pandas;
* 📊 Estatística descritiva;
* 📈 Visualização de dados;
* 🧹 Preparação e organização de datasets;
* 🤖 Uso responsável de Inteligência Artificial;
* 🔍 Análise crítica de resultados;
* ⚡ Análise de dados do setor energético.

---

# 👨‍💻 Conclusão

O projeto demonstra como dados públicos podem ser utilizados para realizar análises relevantes sobre o comportamento da demanda elétrica.

Por meio da integração entre **Python, APIs públicas, análise de dados e visualização gráfica**, foi possível transformar dados brutos em informações mais organizadas e interpretáveis.

A utilização da Inteligência Artificial foi empregada como uma ferramenta complementar, reforçando a importância da **validação humana e da análise crítica** dos resultados.

> 💡 **Dados bem analisados são fundamentais para transformar informação em conhecimento e apoiar decisões mais inteligentes.**

---

## 📌 Projeto Acadêmico

🎓 **Curso:** Ciência da Computação
⚡ **Disciplina:** Soluções em Energias Renováveis e Sustentáveis

---

<p align="center">
  Desenvolvido com 🐍 Python, 📊 Dados e ⚡ Energia.
</p>
