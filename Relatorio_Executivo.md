# 📄 Relatório Executivo: Estratégia de Migração AWS
**Projeto:** Redução de Custos e Modernização – Abstergo Industries  
**Responsável:** Sérgio Santos – Especialista em Cloud & Data Science  
**Data:** 27/11/2025 | **Versão:** 3.0

---

## 📌 1. Visão Executiva

A **Abstergo Industries** (12 unidades + 1 CD) operava sob um modelo de TI *On-Premises* com alto custo fixo (CAPEX) e baixa agilidade. Este projeto detalha a migração estratégica para a nuvem AWS, focando em eficiência financeira e segurança de dados.

> **💡 Indicadores Chave de Desempenho (KPIs):**
> * **Economia Líquida:** R$ 95.400/ano (~62% de redução).
> * **ROI Estimado:** > 140% em 12 meses (incluindo custos de migração e treinamento).
> * **Disponibilidade (SLA):** Elevada de 95% para 99,9% com arquitetura Multi-AZ.

---

## 🎯 2. Objetivos Estratégicos

* **Redução de OPEX:** Substituição de custos fixos de manutenção e servidores por custos variáveis otimizados.
* **Conformidade e Segurança:** Implementação de criptografia em repouso e trânsito, atendendo aos requisitos da LGPD.
* **Crescimento Sustentável:** Infraestrutura preparada para a expansão de +5 lojas planejada para 2026 sem novos investimentos em hardware físico.

---

## 🏗️ 3. Arquitetura da Solução

A arquitetura foi desenhada seguindo o *AWS Well-Architected Framework*, garantindo isolamento de rede e resiliência.

<img width="1080" height="1068" alt="arquitetura-projeto" src="https://github.com/user-attachments/assets/3580a0d3-37c6-40db-a334-90e2c1e99eef" />




### Detalhamento dos Componentes Técnicos:

| Serviço AWS | Caso de Uso | Benefício Técnico |
| :--- | :--- | :--- |
| **Amazon EC2** | ERP, PDV e Gestão de Estoque | Instâncias `t3.medium` com Auto Scaling e desligamento programado (economia de ~35%). |
| **Amazon RDS** | Dados de vendas e clientes | Banco PostgreSQL gerenciado com **Multi-AZ** para failover automático e backups. |
| **Amazon S3** | Receitas médicas e notas fiscais | Armazenamento durável (11x9) com políticas de **Lifecycle** para redução de custo. |

---

## ⚙️ 4. Decisões Técnicas e Trade-offs

Conforme as melhores práticas de governança, analisamos o valor agregado além do preço nominal:

* **RDS vs. Banco Local:** Embora o licenciamento SQL no RDS seja R$ 3.800/ano superior ao local, a decisão foi mantida para eliminar o risco de *downtime* e automatizar a conformidade.
* **S3 vs. Arquivo Físico:** A migração para o S3 gerou a maior economia individual do projeto (R$ 34.800/ano) ao eliminar a necessidade de aluguel de salas físicas para documentos.

---

## 📊 5. Plano Financeiro Consolidado

| Categoria | Situação Atual (Anual) | Custos AWS (Anual) | Economia/Impacto |
| :--- | :--- | :--- | :--- |
| Servidores físicos (4x) | R$ 48.000 | R$ 21.600 (EC2) | ✅ R$ 26.400 |
| Energia e refrigeração | R$ 30.000 | Incluso na AWS | ✅ R$ 30.000 |
| Licenciamento SQL | R$ 25.000 | R$ 28.800 (RDS) | ⚠️ +R$ 3.800 |
| Backups físicos | R$ 8.000 | Incluso (RDS/S3) | ✅ R$ 8.000 |
| Aluguel salas/arquivo | R$ 42.000 | R$ 7.200 (S3) | ✅ R$ 34.800 |
| **TOTAIS** | **R$ 153.000** | **R$ 57.600** | **💰 R$ 95.400** |

---

## ⚠️ 6. Riscos e Mitigação

| Risco | Estratégia de Mitigação |
| :--- | :--- |
| **Custos Excedentes** | Implementação de **AWS Budgets** com alertas em 70%, 90% e 100%. |
| **Segurança/LGPD** | Uso de **IAM** com privilégio mínimo, MFA obrigatório e criptografia de dados. |
| **Dependência de Internet** | Implementação de links redundantes (Fibra + 4G) e modo offline para PDVs. |

---

## 🌱 7. Aprendizados e Boas Práticas

* **Cloud Economics:** A tecnologia deve servir ao negócio. A migração foi pautada em dados financeiros reais.
* **FinOps:** A importância do monitoramento diário e do uso de tags financeiras para evitar surpresas na fatura.
* **Arquitetura Resiliente:** A escolha pelo Multi-AZ no RDS priorizou a continuidade das vendas sobre a economia mínima.

---

## 🚀 8. Roadmap Futuro

- [ ] **Savings Plans:** Avaliar reserva de instâncias para reduzir custos de EC2 em mais 30%.
- [ ] **AWS Lambda:** Automatizar processamento de receitas médicas sem servidores ativos.
- [ ] **Amazon QuickSight:** Criar dashboards de BI financeiro em tempo real para a diretoria.

---

## 📎 9. Anexos e Referências

* 📊 [Visualizar Dashboards Financeiros (PNG)](./Graficos_Executivos/Dashboard_Financeiro_Consolidado.png)
* 📑 [Planilha Comparativa de Custos (CSV)](./Anexos/planilha-comparativa-custos.csv)
* 📘 [Manual de Melhores Práticas AWS (PDF)](./Anexos/Melhores_Praticas_AWS.pdf)

---
⬅️ **[Voltar para o README Principal](./README.md)**
