# Trabalhos de Informática

Repositório com os trabalhos e atividades práticas da disciplina de Informática.

## Atividades

| Atividade | Descrição | Ferramenta | Status |
|---|---|---|---|
| **1. Apresentação Pessoal – 13/08** | Apresentação pessoal, interesses, experiências e perspectivas profissionais. | Canva | ✅ Concluída |
| **2. Aula 28 de agosto** | Análise de dados de empresas habilitadas como Operador de Transporte Multimodal (ANTT), respondendo perguntas por meio de fórmulas, tabela dinâmica e gráficos. | Excel | ✅ Concluída |
| **3. Planilhas Eletrônicas e Dados Abertos** | Coleta e análise de dados abertos sobre Autos de Infração Ambiental do Estado de São Paulo, respondendo 5 perguntas. | Excel | ✅ Concluída |
| **4. Empresas Multimodais e Perguntas** | Análise dos dados de empresas habilitadas como Operador de Transporte Multimodal por meio de perguntas e visualizações. | Power BI | ✅ Concluída |
| **5. Dados Abertos: Análise no Power BI** | Reaproveitamento do dataset de Autos de Infração Ambiental, com as mesmas 5 perguntas respondidas por meio de um dashboard interativo. | Power BI | ✅ Concluída |

## Estrutura do repositório

```text
├── README.md
│
├── Apresentação/
│   └── Trabalho Informatica Thalya.pdf
│
├── Planilhas e Gráficos/
│   ├── Atividade_Inicial_de_2_Perguntas.xlsx
│   ├── Planilhas_Eletrônicas_e_dados_abertos_de_5_perguntas.xlsx
│   ├── 4.Empresas Multimodais+Perguntas.pbix
│   └── Dados_abertos_5_perguntas.pbix
```

---

## 1. Apresentação Pessoal – 13/08

<img width="955" height="533" alt="image" src="https://github.com/user-attachments/assets/f830eacc-aa1e-4832-b047-d1241f6b7525" />


**Data de conclusão:** 13 de agosto de 2026.

Apresentação pessoal sobre minha trajetória, experiências, interesses e perspectivas profissionais.

### Conteúdo apresentado

- **Apresentação pessoal:** Thalya Awany Berti.
- **Trabalho autônomo:** T&Personalizados, atuando com produtos personalizados, impressão 3D e sublimação.
- **Produtos fabricados:** canecas, camisetas, azulejos, almofadas, figuras e chaveiros.
- **Interesses:** jogos, entretenimento e afinidades pessoais.
- **Perspectivas profissionais:** interesse nas áreas de tecnologia, manutenção e logística.
- **Objetivo futuro:** cursar Engenharia da Computação.

---

## 2. Aula 28 de agosto

![Uploading image.png…]()


**Fonte dos dados:** [Operador de Transporte Multimodal – ANTT](https://dados.antt.gov.br/dataset/operador-transporte-multimodal/resource/9f76aca6-0e8d-4c13-8851-0ad8ced5c5b7)

Base com 1.382 empresas habilitadas como Operador de Transporte Multimodal (OTM) no Brasil.

### Perguntas respondidas

1. **Qual o estado com a maior contagem de empresas?**
   → Estado de São Paulo, com 569 empresas.

2. **Qual(is) o(s) país(es) com menor contagem de empresas?**
   → Alemanha, Paraguai e Suíça (empatados, 1 empresa cada).

3. **Quantas empresas cumprem e não cumprem a adesão ao Decreto nº 1.563/95?**
   → Cumprem: 275; Não cumprem: 1.107.

### Técnicas utilizadas

- Tabela Dinâmica (campo `uf` em linhas, contagem de `cnpj` em valores).
- Fórmula `CONT.SE` / `COUNTIF` para contagem por categoria.
- Ordenação (maior → menor) via Colar Especial (valores) + Classificar.
- Gráficos de colunas para cada pergunta.

---

## 3. Planilhas Eletrônicas e Dados Abertos

**Autos de Infração Ambiental (a partir de 2019)** — Estado de São Paulo.

**Fonte:** [dadosabertos.sp.gov.br](https://dadosabertos.sp.gov.br/)

Base com 147.051 registros de autos de infração ambiental, contendo classe da infração, situação/status do processo, data e município.

### Perguntas respondidas

1. **Quantas infrações existem em cada classe? Qual classe tem mais infrações?**
   → FLORA lidera, com 68.720 infrações.

2. **Quantos municípios causaram ao menos uma infração?**
   → 650 municípios distintos.

3. **Como evoluiu o número de infrações registradas por ano (2019–2026)?**
   → Pico em 2020, com 22.636 infrações. 2026 está incompleto (ano corrente).

4. **Quais são os 5 municípios com maior número de infrações registradas?**
   → São Paulo (6.678), Ubatuba (3.059), Itanhaém (2.669), Caraguatatuba (2.409), Icém (1.908).

5. **Qual é o status mais comum dos processos de infração ambiental?**
   → "AIA pago", com 20.959 processos.

## Ferramentas utilizadas

- `CONT.SE` — contar ocorrências de um valor numa coluna (P1, P2, P5).
- `CONTAR.VALORES` (COUNTA) — contar células preenchidas (P2 e P5).
- `ÍNDICE + CORRESP + MÁXIMO` — achar o item com maior valor (P3).
- `Colar especial (valores) + Classificar` — técnica manual para congelar resultados e ordenar do maior para o menor (P1, P2, P4).

---

## 4. Empresas Multimodais e Perguntas

**Base de dados:** Operadores de Transporte Multimodal (OTM) — ANTT.

Continuação da análise dos dados de empresas multimodais, utilizando o Power BI para trabalhar com as informações e responder às perguntas propostas.

### Ferramenta utilizada

- Power BI Desktop.
- Importação e organização dos dados.
- Criação de visualizações para análise das empresas multimodais.

**Arquivo:** `4.Empresas Multimodais+Perguntas.pbix`

---

## 5. Dados Abertos: Análise no Power BI

**Reaproveitamento do dataset de Autos de Infração Ambiental** (mesma base de 147.051 registros), com as mesmas 5 perguntas respondidas em um painel no Power BI Desktop.

### Visuais utilizados

1. P1: Infrações por classe — `GRÁFICO DE BARRAS` → Classe Infração × Quantidade de Infrações.

2. P2: Quantos municípios — `CARTÃO` → Quantidade de Municípios.

3. P3: Evolução por ano — `GRÁFICO DE LINHAS` → Ano × Quantidade de Infrações.

4. P4: Top 5 municípios — `GRÁFICO DE COLUNAS (FILTRO N SUPERIOR = 5)` → Município × Quantidade de Infrações.

5. P5: Status mais comum — `GRÁFICO DE PIZZA (FILTRO N SUPERIOR)` → Status × Quantidade de Infrações.

O painel também tem um cartão com o total de infrações e uma caixa de texto explicando as medidas.

## Medidas DAX

- Quantidade de Infrações = COUNTROWS ( 'Autos-de-Infracao-Ambiental-a-p' )
- Quantidade de Municipios = DISTINCTCOUNT ( 'Autos-de-Infracao-Ambiental-a-p'[Municipio] )

- `COUNTROWS`: número total de linhas (cada linha é uma infração).
- `DISTINCTCOUNT`: número de valores únicos (cada município contado uma vez).

## Ferramentas utilizadas

- `Power Query` — importar, tipar e limpar os dados.
- `Medidas DAX` (COUNTROWS, DISTINCTCOUNT) — cálculos dos visuais.
- `Filtro N Superior` — rankings (P4 e P5).
- `Visuais` — barras, colunas, linhas, pizza e cartões.

---

