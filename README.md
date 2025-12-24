# Redução dos Custos em Farmácias com AWS

![CienciaDadosSantander](https://github.com/user-attachments/assets/f471204d-c3ef-419c-979b-297f19b89a9d)


**Bootcamp Santander 2025 - Ciência de Dados com Python.** 


---

## 🌟 Resumo Executivo

Este projeto apresenta a estratégia de modernização de infraestrutura da farmácia fictícia **Abstergo Industries**, migrando de um ambiente *On-Premises* para a nuvem **AWS**.

**Impacto Financeiro:** Economia anual estimada de **R$ 95.400 (~62% de redução)**, com eliminação de custos de manutenção física e aluguel de espaço, aumentando a segurança e disponibilidade de dados críticos.

### 💡 KPIs Principais:
* **Economia líquida:** R$ 95.400/ano
* **ROI estimado:** > 140% em 12 meses
* **SLA de disponibilidade:** 99,9%

---

## 🎯 Objetivos do Projeto

* **Redução de Custos:** Identificar e eliminar gastos desnecessários com hardware e manutenção local.
* **Escalabilidade:** Permitir crescimento das unidades sem novos investimentos vultosos em servidores físicos.
* **Tomada de Decisão Baseada em Dados:** Apresentar análises financeiras que sustentem a migração tecnológica.

---

## 🏗️ Arquitetura e Estratégia Cloud

O projeto utiliza três pilares fundamentais da AWS para garantir resiliência e baixo custo:

* **Amazon EC2:** Substituição de servidores físicos por instâncias elásticas. Benefício de pagamento por uso e desligamento programado em horários de baixa demanda.
* **Amazon RDS:** Banco de dados gerenciado para estoque e vendas com backup automático e Multi-AZ.
* **Amazon S3:** Armazenamento durável para digitalização de receitas médicas e documentos fiscais, eliminando custos de arquivo físico.

---

## ⚙️ Decisões Técnicas e Trade-offs

| Decisão | Impacto Financeiro | Justificativa Técnica |
| :--- | :--- | :--- |
| **RDS vs Banco Local** | ⚠️ +R$ 3.800/ano | Garantia de Zero Downtime e conformidade. O custo extra compensa o risco zero de perda de dados. |
| **S3 vs Arquivo Físico** | ✅ -R$ 34.800/ano | Eliminação de aluguel de salas e risco de deterioração física de documentos. |
| **EC2 On-Demand** | ✅ -R$ 26.400/ano | Flexibilidade para escalar e pagar apenas pelo uso real, sem depreciação de hardware. |

---

## 📊 Resultados e Economia Estimada

| Categoria | Situação Atual (On-Premises) | Custos AWS | Economia/Impacto |
| :--- | :--- | :--- | :--- |
| Servidores físicos (4x) | R$ 48.000/ano | R$ 21.600/ano (EC2) | ✅ R$ 26.400 |
| Energia e refrigeração | R$ 30.000/ano | Incluso na AWS | ✅ R$ 30.000 |
| Licenciamento SQL | R$ 25.000/ano | R$ 28.800/ano (RDS) | ⚠️ +R$ 3.800 |
| Backups físicos | R$ 8.000/ano | Incluso (RDS/S3) | ✅ R$ 8.000 |
| Aluguel de salas/arquivo | R$ 42.000/ano | R$ 7.200/ano (S3) | ✅ R$ 34.800 |
| **TOTAL** | **R$ 153.000/ano** | **R$ 57.600/ano** | **💰 R$ 95.400** |

---

## 📈 Inteligência de Dados & Gráficos

Visualize o impacto detalhado na pasta [Graficos_Executivos/](./Graficos_Executivos/):

1.  **[Dashboard Financeiro](./Graficos_Executivos/Dashboard_Financeiro_Consolidado.png):** Visão geral da saúde financeira pós-migração.
2.  **[Evolução de Custos](./Graficos_Executivos/Evolução_Custos_Longo_12_Meses.png):** Comparativo mensal detalhado entre AWS e local.
3.  **[ROI e Proporção](./Graficos_Executivos/Proporcao_Custos_Atuais_vs_AWS.png):** Visualização percentual do Retorno sobre Investimento.

---

## 🌱 Aprendizados

* **Cloud Economics:** Tecnologia deve ser traduzida em valor de negócio.
* **Arquitetura Consciente:** Decisões baseadas em segurança e resiliência, não apenas no menor preço.
* **FinOps:** A importância do monitoramento contínuo para evitar gastos inesperados (*Cloud Sprawl*).

---

## 🚀 Próximos Passos

- [ ] **AWS Lambda:** Processamento serverless de receitas médicas.
- [ ] **Amazon QuickSight:** Dashboards de BI automatizados.
- [ ] **Savings Plans:** Redução de custo de EC2 em até 30%.

---

## 📎 Anexos e Referências

* 📑 [Planilha Comparativa de Custos (CSV)](./Anexos/planilha-comparativa-custos.csv)
* 📘 [Relatório Executivo Detalhado](./Relatorio_Executivo.md)
* 📚 [Guia de Melhores Práticas AWS (PDF)](./Anexos/Melhores_Praticas_AWS.pdf)





---

**Autor:**
Sergio Santos 

---


## 📩 Contato



[![Portfólio Sérgio Santos](https://img.shields.io/badge/Portfólio-Sérgio_Santos-111827?style=for-the-badge&logo=githubpages&logoColor=00eaff)](https://santosdevbjj.github.io/portfolio/)
[![LinkedIn Sérgio Santos](https://img.shields.io/badge/LinkedIn-Sérgio_Santos-0A66C2?style=for-the-badge&logo=linkedin&logoColor=white)](https://linkedin.com/in/santossergioluiz) 



---



