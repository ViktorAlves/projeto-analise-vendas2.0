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
