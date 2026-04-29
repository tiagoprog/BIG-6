# ⚽ European Football Analytics Pipeline: End-to-End

Este projeto é uma solução completa de Engenharia e Análise de Dados que automatiza a coleta, o processamento e a visualização de estatísticas das principais ligas de futebol da Europa (Premier League, La Liga, Serie A, Bundesliga, Ligue 1 e Liga Portugal).

O objetivo principal foi transformar um processo manual em um pipeline robusto na nuvem, utilizando práticas modernas de mercado como **Automação via CI/CD** e **Modelagem Dimensional (Star Schema)**.

## 🚀 Arquitetura da Solução

O projeto é dividido em três camadas principais:

1.  **Ingestão e Extração (Python):**
    * Script desenvolvido em Python utilizando a biblioteca `Pandas` e `Requests`.
    * Consumo de dados em tempo real via API (`football-data.org`).
    * Tratamento de dados e limpeza para garantir a "Fonte Única da Verdade" (SSOT).

2.  **Automação de Engenharia (GitHub Actions):**
    * Implementação de um robô de automação (Workflow YAML).
    * **Agendamento (Cron Job):** O script é executado automaticamente todos os dias às 03:00 AM.
    * **CI/CD:** O robô provisiona uma máquina virtual, executa o extrator e atualiza o arquivo CSV no repositório de forma totalmente autônoma.

3.  **Business Intelligence & Modelagem (Power BI):**
    * Conexão direta com os dados na nuvem (via GitHub Raw Link).
    * **Star Schema:** Estruturação do modelo em Tabelas Fato (`fClassificacao`) e Dimensões (`dTime`, `dLiga`).
    * **Cálculos Avançados:** Uso de DAX para métricas de performance, aproveitamento e saldo de gols.

## 🛠️ Tecnologias Utilizadas

* **Linguagem:** Python 3.12
* **Bibliotecas:** Pandas, Requests, Time
* **Pipeline:** GitHub Actions (YAML)
* **BI:** Power BI Desktop / Power Query / DAX
* **Fonte de Dados:** API Football-Data.org

---

## 👨‍💻 Autor

**Tiago Oliveira Macedo**
Estudante de Ciência de Dados e Inteligência Artificial no Ibmec RJ.
Interesses em Engenharia de Dados, BI e Desenvolvimento de IA.

---
> *Este projeto foi desenvolvido como um estudo prático de integração entre Python, Cloud Automation e Business Intelligence.*
