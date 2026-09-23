# Trabalhos de Informática

Repositório com os trabalhos e atividades práticas da disciplina de Informática.

## Atividades

| Atividade | Descrição | Ferramenta | Status |
|---|---|---|---|
| **Aula 28 de agosto** | Análise do arquivo "Empresas com habilitação multimodal" (ANTT) — perguntas respondidas via fórmulas, tabela dinâmica e gráfico | Excel | ✅ Concluída |
| **Planilhas Eletrônicas e dados abertos** | Coleta de um dataset de dados abertos governamentais e elaboração de 5 perguntas respondidas via fórmulas e gráficos | Excel | ✅ Concluída |
| **Dados abertos: análise no Power BI** | Reaproveitamento do dataset da atividade anterior, com as mesmas 5 perguntas respondidas via dashboard | Power BI | ⏳ Em andamento |
|  |  |  | ⏳ Em andamento |

## Estrutura do repositório

```
├── README.md
├── Atividade_Inicial_de_2_Perguntas.xlsx         # Aula 28 de agosto
└── Autos-de-Infracao-Ambiental-respondido.xlsx   # Planilhas Eletrônicas e dados abertos
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
   → 649 municípios distintos.

3. **Como evoluiu o número de infrações registradas por ano (2019–2026)?**
   → Pico em 2020, com 22.636 infrações. 2026 está incompleto (ano corrente).

4. **Quais são os 5 municípios com maior número de infrações registradas?**
   → São Paulo (6.678), Ubatuba (3.059), Itanhaém (2.669), Caraguatatuba (2.409), Icém (1.908).

5. **Qual é o status mais comum dos processos de infração ambiental?**
   → "AIA pago", com 20.959 processos.

## Ferramentas utilizadas

- Microsoft Excel — fórmulas `COUNTIF`/`CONT.SE`, `COUNTA`, `INDEX`/`MATCH`/`MAX`
- Gráficos de barras e linha nativos do Excel
