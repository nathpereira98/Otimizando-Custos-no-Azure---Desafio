# Otimizando-Custos-no-Azure---Desafio
Desafio DIO: Otimizando Custos no Azure

## Objetivo do lab
Compreender estratégias e ferramentas que permitem reduzir, controlar e otimizar os gastos com a nuvem Azure, mantendo desempenho, disponibilidade e segurança.

## O que aprendi
- Ferramentas para estimativa e análise de custo: **Calculadora de Preços (Pricing Calculator)** e **Calculadora TCO (Total Cost of Ownership)**.  
- Monitoramento e governança de custo: **Azure Cost Management**, **budgets**, **alerts** e **Cost Analysis**.  
- Recomendações automatizadas: **Azure Advisor (cost recommendations)**.  
- Modelos de compra e economia: **Reserved Instances / Reservations**, **Savings Plans**, **Spot VMs**.  
- Boas práticas operacionais: right-sizing, auto-scale, desligamento programado para ambientes não produtivos.  
- Organização e atribuição de custos: uso de **tags** (cost-center, project, environment) e Resource Groups para alocação e relatórios.  
- Políticas e automatizações: uso de **Azure Policy** para evitar implantação de SKUs caros ou sem tag e automações para desligar recursos fora do horário.  
- Otimização de storage e dados: tiers de storage (hot/cool/archive), lifecycle policies e redução de egress.  
- Estratégias para bancos de dados e PaaS: opções serverless, autoscale, e compra de capacidade reservada quando aplicável.

## Estratégias e práticas recomendadas (resumo prático)
- **Right-size**: analisar métricas e reduzir VM sizes ou CPU/RAM ociosos.  
- **Reservas e Savings Plans**: reservar capacidade para cargas previsíveis (1 ou 3 anos) para reduzir custos.  
- **Spot VMs**: usar para workloads tolerantes a interrupções (batch, testes).  
- **Auto-scale**: configurar escalonamento automático para ajustar recursos conforme demanda.  
- **Shutdown schedules**: desligar recursos de dev/test fora do horário (scripts/Automation).  
- **Tags para alocação de custo**: aplicar `CostCenter`, `Environment`, `Owner` em todos os recursos.  
- **Orçamentos e alertas**: criar budgets por assinatura/RG e alertas para acompanhar desvios.  
- **Azure Advisor**: verificar recomendações de otimização de custo e aplicá-las com prioridade.  
- **Storage tiering**: mover dados inativos para camadas mais baratas (cool / archive).  
- **Minimizar egress**: arquitetar para reduzir transferências entre regiões e para fora da nuvem.  
- **Usar ofertas para dev/test**: subscrições e recursos com preços reduzidos para ambiente de desenvolvimento.  
- **Políticas (Azure Policy)**: impor tags obrigatórias e restringir SKUs/regiões mais caras.

## Exemplos práticos estudados
- Criar um **budget** no Cost Management e configurar alertas para 80% / 100% do valor.  
- Rodar Cost Analysis para identificar top 5 recursos que mais consomem.  
- Aplicar tags (`Environment=Dev/Prod`, `CostCenter=1234`) e usar relatórios por tag.  
- Habilitar **auto-scale** em um App Service ou VM Scale Set.  
- Comprar uma **Reserved VM Instance** quando a VM for de produção e com uso estável.  
- Migrar blobs antigos para a camada **Archive** via lifecycle policy.

## Ferramentas e recursos citados
- **Azure Pricing Calculator** — estimativas de preço.  
- **TCO Calculator** — estimativa de economia migrando do on-premises.  
- **Azure Cost Management + Billing** — monitoramento, análise, budgets.  
- **Azure Advisor** — recomendações de custo e performance.  
- **Azure Policy** — aplicar governança para controlar gastos.  
- **AzCopy / Storage Explorer** — operações de dados (quando aplicável para reduzir custos de transferência/armazenamento).
