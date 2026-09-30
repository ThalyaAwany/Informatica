# Trabalhos de Informática

Repositório com os trabalhos e atividades práticas da disciplina de Informática.

## Atividades

| Atividade | Descrição | Ferramenta | Status |
|---|---|---|---|
| **Aula 28 de agosto** | Análise do arquivo "Empresas com habilitação multimodal" (ANTT) — 2 perguntas respondidas via fórmulas, tabela dinâmica e gráfico | Excel | ✅ Concluída |
| **Planilhas Eletrônicas e dados abertos** | Coleta de um dataset de dados abertos governamentais e elaboração de 5 perguntas respondidas via fórmulas e gráficos | Excel | ✅ Concluída |
| **Dados abertos: análise no Power BI** | Reaproveitamento do dataset da atividade anterior, com as mesmas 5 perguntas respondidas via dashboard | Power BI | ✅ Concluída |
|  |  |  |  |

## Estrutura do repositório

```
├── README.md
├── Atividade_Inicial_de_2_Perguntas.xlsx         # Aula 28 de agosto
└── Planilhas_Eletrônicas_e_dados_abertos_de_5_perguntas.xlsx   # Planilhas Eletrônicas e dados abertos
└── Dados_abertos_5_perguntas.pbix                              # Dados abertos: análise no Power BI
```

---

## Aula 28 de agosto

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
- Tabela Dinâmica (campo `uf` em linhas, contagem de `cnpj` em valores)
- Fórmula `CONT.SE`/`COUNTIF` para contagem por categoria
- Ordenação (maior → menor) via Colar Especial (valores) + Classificar
- Gráficos de colunas para cada pergunta

---



## Planilhas Eletrônicas e Dados Abertos

**Autos de Infração Ambiental (a partir de 2019)** — Estado de São Paulo
Fonte: [dadosabertos.sp.gov.br](https://dadosabertos.sp.gov.br/)

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
-`CONT.SE` — contar ocorrências de um valor numa coluna (P1, P2, P5).
- `CONTAR.VALORES` (COUNTA) — contar células preenchidas (P2 e P5).
- `ÍNDICE + CORRESP + MÁXIMO` — achar o item com maior valor (P3).
- `Colar especial (valores) + Classificar` — técnica manual para congelar resultados e ordenar do maior para o menor (P1, P2, P4).

---  



## Dados Abertos: Analise PowerBI

**Reaproveitamento do dataset de Autos de Infração Ambiental** 
(mesma base de 147.051 registros), com as mesmas 5 perguntas respondidas em um painel no Power BI Desktop.

### Visuais utilizados

1. P1: Infrações por classe `*Gráfico de barras*` → Classe Infração × Quantidade de Infrações

2. P2: Quantos municípios `*Cartão*` → Quantidade de Municípios

3. P3: Evolução por ano	`*Gráfico de linhas*` → Ano × Quantidade de Infrações

4. P4: Top 5 municípios	`*Gráfico de colunas (filtro N Superior = 5)*`	→ Municipio × Quantidade de Infrações

5. P5: Status mais comum `*Gráfico de pizza (filtro N Superior)*` → Status × Quantidade de Infrações
   
O painel também tem um cartão com o total de infrações e uma caixa de texto explicando as medidas.

## Medidas DAX
- Quantidade de Infrações = COUNTROWS ( 'Autos-de-Infracao-Ambiental-a-p' )
- Quantidade de Municipios = DISTINCTCOUNT ( 'Autos-de-Infracao-Ambiental-a-p'[Municipio] )

- COUNTROWS: número total de linhas (cada linha é uma infração).
- DISTINCTCOUNT: número de valores únicos (cada município contado uma vez).

## Ferramentas utilizadas
- `Power Query` importar, tipar e limpar os dados.
- `Medidas DAX` (COUNTROWS, DISTINCTCOUNT): cálculos dos visuais.
- `Filtro N Superior`rankings (P4 e P5).
- `Visuais: barras` colunas, linhas, pizza e cartões.

 ---
