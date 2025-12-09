# Relatório Estratégico de Varejo: Case Walmart

![Tela Inicial](Imagens/1.Tela_Inicial.png)

## Visão Geral
Este projeto simula um cenário complexo de expansão da rede de varejo Walmart em um país fictício ao longo de 9 anos (2016-2025) e como o **Relatório de Dados Estratégico** permitiu à diretoria analisar o impacto de inaugurações, a eficiência regional e as correlações com indicadores macroeconômicos. O relatório foi gerado após a remodelagem e a ampliação de um dataset simples, disponibilizado pelo [Kaggle](https://www.kaggle.com/datasets/mikhail1681/walmart-sales).

> **Nota:** Para fins de preservação e facilidade de acesso, uma cópia do arquivo original (`Walmart_sales_analysis.csv`) também está disponível na pasta **[Dataset](./Datasets)** deste repositório.
<br>

Um artigo descrevendo como a remodelagem desse dataset disponibilizado pelo Kaggle acabou se tornando uma saga estará disponível, muito em breve. Assim que estiver pronto, substituirei esta linha pelo link para acesso.
<br><br>

**[Clique Aqui para acessar o dashboard interativo](https://app.powerbi.com/view?r=eyJrIjoiOWM1NmViNGYtMmMxNC00M2M2LWI3NzEtNDg1NDgyNjAwZDFhIiwidCI6IjY1OWNlMmI4LTA3MTQtNDE5OC04YzM4LWRjOWI2MGFhYmI1NyJ9)**
<br>

**Importante:** Caso o link esteja indisponível, seja por ter expirado, seja por manutenção ou por qualquer outro motivo, ainda assim será possível acessar o relatório baixando o arquivo .pbix que está disponível na pasta Projetc deste repositório.

---

## Engenharia e Tecnologias
O projeto foi desenvolvido simulando um ciclo completo de BI:

* **Excel (Data Engineering):**
    * Modelagem de cenários estatísticos com aleatoriedade controlada para simular padrões de consumo realistas.
    * Tratamento de "Data Patching" para adequar os dados da fonte à realidade do cenário fictício.
   <br>
* **Power Query (ETL Avançado):**
    * **Explosão de Granularidade:** Transformação de dados semanais em diários para análise temporal precisa.
    * **Limpeza Lógica:** Tratamento de datas anteriores à inauguração e propagação de atributos.
   <br>
* **Power BI (DAX & Visualização):**
    * **Modelagem:** Star Schema com tabelas Fato e Dimensões.
    * **DAX Avançado:** Manipulação de contexto de filtro para métricas de eficiência e inteligência de tempo.
    * **UX/UI (Elo Tech Design):** Navegação entre as páginas como se o relatório fosse um aplicativo e utilização de Tooltips personalizadas.

---
<br>

### Nota de Execução
> **Atenção:** Como o Power BI utiliza caminhos absolutos para fontes de dados locais, ao baixar e abrir o arquivo .pbix na sua máquina, é necessário reconectar a fonte de dados:
> 1. No Power BI, vá em **Transformar Dados > Configurações da fonte de dados**.
> 2. Clique em **Alterar Fonte**.
> 3. Aponte para o arquivo `Walmart_Processed_Data.xlsx` que está dentro da pasta `Dataset` deste repositório.
> 4. Não esqueça, caso resolva optar por baixar os arquivos, de especificar em quais pastas eles serão armazenados. Recomendo que seja utilizada a mesma estrutura que você está encontrando aqui, porque se mudar a fonte de dados, isto é, o arquivo .xlsx, deverá realizar uma nova atualização, conforme mostrado no item 1.

---
<br><br>
## Algumas Imagens da Análise <br>

### 1. Evolução Histórica
Monitoramento da trajetória de crescimento desde a inauguração da primeira loja, o período de adaptação de um ano após a inauguração da última loja e três anos de maturação com volume de produção ascendente.

![Evolução](Imagens/2.Evolução_Histórica.png)
<br><br>
### 2. Matriz de Correlações
Análise estatística visual utilizando a correlação das vendas com o índice de inflação, o preço do combustível, a taxa percentual de desemprego e a temperatura para identificar o comportamento das vendas e traçar os perfis das filiais.

![Correlações](Imagens/3.Correlações.png)
<br><br>
### 3. Panorama Consolidado
Visão integrada da participação no mercado , do ranking de eficiência por filial e do impacto dos feriados na operação.

![Consolidado](Imagens/4.Consolidado.png)

---
<br><br>
## Análise de Dados e Insights de Negócio

A seguir, a análise realizada após a criação dos visuais com os dados transformados. 

### 1. Trajetória de Crescimento e Maturação
O gráfico de evolução histórica demonstra uma **tendência ascendente consistente**. As inaugurações que ocorreram nesse período aceleraram o movimento, mas a partir do início do ano de 2022, após a última loja ter sido inaugurada, a curva de crescimento perde força, porém, sem deixar de continuar apresentando crescimento, mesmo que modesto.
* **Estabilização:** A rede atingiu o ponto de maturidade no mercado. O crescimento orgânico continua, porém moderado e discreto o que leva à próxima fase na qual o foco estratégico deve migrar da expansão física, uma vez que não há necessidade de inaugurar mais lojas, para a busca pela excelência e eficiência operacional.
* **Sazonalidade:** Durante todo o período, desde a inauguração da primeira loja até o ano de 2024, os picos de receita ocorreram entre a **metade do mês de novembro e a última semana do mês de dezembro**, o que reforça a importância da Black Fryday e do período de festas de fim de ano. É o retrato da dependência do varejo em relação a essas datas.
<br>

### 2. Performance Regional
A análise segmentada por regiões considerou dois momentos distintos: a trajetória de crescimento individiual e a produção após um ano de maturação, a partir da inauguração da última loja. As lojas foram rankeadas dentro de suas respectivas regiões considerando as vendas no intervalo entre outubro de 2022 e outubro de 2025. O principal objetivo para o corte antes do término do ano de 2025 está atrelado às manifestações dos diretores de algumas regionais que se mostraram favoráveis à inauguração de outras filiais. O resultado a seguir recomenda que não é o momento adequado para isso.
* **Padrão de Disparidade:** Em quase todas as regiões, observa-se uma divisão clara entre um grupo de lojas com alto volume de vendas e outro com menos.
    * *Exemplo:* Na **Região Sul**, uma única loja destoa significativamente das outras 9, puxando a média para cima.
    * *Exemplo:* Na **Região Central**, o desempenho é mais homogêneo entre as 6 principais, com apenas 2 unidades abaixo da média.
* **Nota de Negócio:** É muito importante ressaltar que **menor volume de vendas não significa necessariamente menor rentabilidade**. As lojas com colunas menores provavelmente estão situadas em regiões menores ou com custos operacionais mais baixos, mas sem deixarem de cumprir os seus papéis estratégicos de capilaridade e de presença da marca. Existe a hipótese das lojas que mesmo apresentando os seus volumes de produção menores que as outras serem mais rentáveis para a rede. Uma nova análise para confirmar esses números pode ser providenciada, porém é necessário que outras informações pertinentes ao contexto sejam fornecidas.
<br>

### 3. Correlações com Fatores Externos
Ao cruzar o volume de vendas com indicadores macroeconômicos e ambientais, por meio da análise em gráficos de dispersão, foram identificados alguns comportamentos distintos:
* **Temperatura:** Embora a linha de tendência traga uma leve correlação negativa, parecendo que as temperaturas menores favorecem as vendas, a análise revela que a maioria das lojas se concentra em uma faixa intermediária . Portanto, apesar da existência de outliers de alta performance, a operação é resiliente em temperaturas amenas. A maioria das lojas mantêm suas vendas, porque quase não são afetadas por variações térmicas moderadas. 
* **Combustível e Desemprego:**
    * ***Preço do Combustível:*** Alguns outliers de alta performance provocaram a inclinação na linha de tendência, porém, a **concentração de dados**, ou seja, a massa principal de lojas, permanece estável no patamar médio de faturamento. Isso indica que não houve influência significativa do aumento no preço do combustível sobre as vendas. **Conclusão:** O cliente manteve o padrão de consumo.
    * ***Desemprego:*** Existe uma concentração estável nas lojas que venderam mais. No entanto, a maior quantidade está situada na média e demonstra que as lojas continuaram a vender, mesmo com o aumento da taxa de desemprego. A hipótese levantada é que essas unidades estejam situadas em regiões nas quais a população possua maior **poder aquisitivo** ou que a dependência do emprego formal seja menor.
* **Inflação (IPC):** Esta foi outra correlação em que houve uma concentração estável com volume maior de vendas. Isso reforça que as variações dos índices de inflação não afetam determinadas regiões que continuaram com suas vendas no mesmo patamar, da mesma forma que a maioria, situada na média.
<br>

### 4. Feriados
A diferença apurada entre a média das semanas com feriado e as semanas normais é mínima:
* **Semana Normal:** 4,46 Milhões (Média)
* **Semana de Feriado:** 4,41 Milhões (Média)
Embora existam os picos concentrados nas semanas em que ocorrem a Black Friday e as festas de fim de ano, o restante dos feriados não influenciam o aumento ou a diminuição das vendas e isso é favorável para as semanas normais que estão em maior quantidade.

---

### Conclusão
O projeto simula um cenário de varejo saudável e resiliente. A empresa, após ter encerrado o seu cronograma de inaugurações, procurou consolidar a sua presença em todas as regiões. Com os resultados trazidos pela análise, concluiu-se que o varejo de produtos de necessidade básica consegue superar cenários adversos e complexos, mantendo-se estável. O próximo desafio é buscar entender as disparidades regionais e otimizar quais produtos são mais adequados para as lojas de menor volume.
<br><br><br>
Desenvolvido por **Ausdauer Tech** | Dezembro 2025*
