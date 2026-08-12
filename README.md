# projeto-analise-vendas 2.0

## 📖 1. O Contexto e o Problema de Negócio

A **Superstore** enfrentava um dilema clássico do varejo: as vendas totais continuavam crescendo ano a ano, mas o **lucro líquido não acompanhava esse ritmo**. A diretoria não sabia exatamente quais produtos, regiões ou políticas comerciais estavam consumindo a margem da empresa.

## 🎯 Objetivo da Análise & Perguntas de Negócio

O objetivo principal deste projeto é mapear oportunidades de crescimento e estancamento de perdas na **Superstore**. Para guiar a investigação, definimos as seguintes perguntas estratégicas de negócio:

1. **Desempenho Regional:** Qual região vende mais e qual entrega a maior rentabilidade?
2. **Sazonalidade:** Existe um padrão temporal claro no volume de vendas ao longo do ano?
3. **Política de Descontos:** Quais produtos possuem desconto elevado mas geram lucro baixo (prejuízo disfarçado)?
4. **Segmentação de Clientes:** Quem são os clientes mais valiosos (VIPs) da base?
5. **Categorias & Subcategorias:** Qual categoria e subcategoria de produtos traz o maior retorno financeiro?
6. **Perfil do Comprador:** Qual segmento (*Consumer*, *Corporate*, *Home Office*) representa o maior volume e a maior margem?
7. **Eficiência Logística:** Qual é o tempo médio de envio (*Ship Date - Order Date*) por modalidade de frete (*Ship Mode*)?

---

## 💡 Principais Descobertas (Respostas de Negócio)

### 🌍 1. Regiões e Categorias Campeãs
* **Região Lider:** A região **West** lidera em volume financeiro e em lucro líquido. Em contrapartida, a região **Central** apresenta margens pressionadas devido ao uso excessivo de descontos.
* **Categoria Mais Lucrativa:** A categoria de **Technology** obteve a maior margem e lucro acumulado, impulsionada por itens de alto valor agregado como *Copiers* e *Phones*.

### 📈 2. Sazonalidade das Vendas
* Existe um pico recorrente de vendas no **último trimestre (Q4)**, com destaque para Novembro e Dezembro, acompanhando o movimento de compras de fim de ano.

### 🏷️ 3. Descontos e Prejuízo Disfarçado
* Descontos acima de **20%** atuam como um "prejuízo disfarçado": aumentam o volume de vendas, mas corroem totalmente o lucro final. Subcategorias como **Tables** e **Bookcases** são as mais penalizadas por essa prática.

### 👥 4. Segmentos e Clientes Mais Valiosos (RFM)
* **Segmento Líder:** O segmento **Consumer** responde por mais de **50% do volume total de vendas** e é o mais lucrativo.
* **Clientes VIPs:** Através da análise **RFM**, identificamos que os top **15% dos clientes** geram mais de **40% da receita total**.

### 🚚 5. Eficiência Logística
* O tempo médio global de envio é de **~3,9 dias**.
* Modalidades expressas (*Same Day* e *First Class*) cumprem prazos de 0 a 2 dias, enquanto o frete padrão (*Standard Class*) leva em média de 4 a 6 dias.

---

## 🛠️ 2. A Jornada dos Dados (Arquitetura da Solução)

Para resolver o enigma, a análise foi dividida em três camadas complementares:

```text
  ┌────────────────┐     ┌──────────────────┐     ┌──────────────────┐
  │   Consultas    │ ──> │ Tratamento & EDA │ ──> │ Dashboard Final  │
  │   SQL (ETL)    │     │ Python (Pandas)  │     │   (Power BI)     │
  └────────────────┘     └──────────────────┘     └──────────────────┘


```

---

## 📈 3. O Dashboard executivo (Power Bi)





## 🚀 4. Recomendações de Negócio (Plano de Ação)

Com base nas análises de dados e nos insights obtidos, foi recomendado as seguintes ações estratégicas para a diretoria:

* [ ] **Política de Teto para Descontos:** Reestruturar as campanhas promocionais definindo um **teto máximo de 15% a 20% de desconto** (especialmente para as subcategorias de móveis como *Tables* e *Bookcases*), eliminando a concessão de descontos agressivos que resultam em prejuízo operacional.
* [ ] **Plano de Reestruturação da Região Central:** Replicar as melhores práticas operacionais e o controle de margem da região **West** (mais lucrativa) para a região **Central**, revisando a precificação regional e reduzindo a dependência de incentivos comerciais nessa área.
* [ ] **Aproveitamento da Sazonalidade (Planejamento do Q4):** Antecipar a gestão de estoque e capacidade logística para o **4º Trimestre (Q4)**, garantindo que o pico de vendas de final de ano (Novembro/Dezembro) seja atendido sem gargalos operacionais e sem necessidade de descontos exagerados.
* [ ] **Programa de Retenção e Fidelidade VIP (RFM):** Criar campanhas de marketing direcionadas e atendimento exclusivo para o grupo de clientes **Champions/VIPs** (top 15% da base), garantindo a retenção dos clientes que geram mais de 40% do faturamento total.
* [ ] **Ações Estratégicas por Segmento:** Concentrar a força de vendas e estratégias de cross-selling no segmento **Consumer** (maior volume e lucro), enquanto se desenvolvem pacotes corporativos de maior margem para o segmento **Corporate**.
* [ ] **Otimização do Mix de Produtos:** Expandir o portfólio da categoria de **Technology** (maior margem do negócio) e renegociar custos de fornecedores para subcategorias que operam no limite da rentabilidade.

---

<div align="center">

| 👨‍💻 Desenvolvido por **Victor Alves** |
| :--- |
| 🚀 **Analista de Dados** focado em transformar dados em inteligência de negócio. |
| 📬 **Conecte-se comigo:** <br> [![LinkedIn](https://img.shields.io/badge/-LinkedIn-0A66C2?style=flat-square&logo=linkedin&logoColor=white)](https://www.linkedin.com/in/victor-luiz-b39738222/) [![GitHub](https://img.shields.io/badge/-GitHub-181717?style=flat-square&logo=github&logoColor=white)]([https://github.com/seu-usuario](https://github.com/ViktorAlves))  |

</div>
