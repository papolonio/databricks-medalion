# Databricks Medallion Architecture - Data Warehouse

Implementação completa de um Data Warehouse usando a arquitetura Medallion (Bronze → Silver → Gold) no Databricks com Delta Lake.

## Sobre o Projeto

Este projeto demonstra a construção de um Data Warehouse moderno seguindo boas práticas de Engenharia de Dados, incluindo processamento incremental, modelagem dimensional e controle de qualidade de dados.

### Bronze Layer (Raw Data)
Dados brutos gerados sinteticamente simulando um e-commerce com 500 produtos, 1000 clientes e 5000 pedidos. Inclui problemas intencionais de qualidade (duplicatas, formatos inconsistentes, valores nulos).

### Silver Layer (Curated Data)
Camada de dados limpos com técnicas de deduplicação determinística, parsing de múltiplos formatos de data, MERGE idempotente usando hash SHA256 e processamento incremental com watermarking.

### Gold Layer (Business Ready)
Modelo dimensional Star Schema otimizado para análises, incluindo dimensões (tempo, produto, cliente com SCD Type 2), fatos (vendas com joins time-aware) e views analíticas agregadas.

## Tecnologias

**Databricks** | **Delta Lake** | **PySpark** | **SQL** | **Unity Catalog**

## Conceitos Demonstrados

- Arquitetura Medallion (Bronze/Silver/Gold)
- SCD Type 2 (Slowly Changing Dimension)
- Processamento incremental com MERGE
- Idempotência com hash de linha
- Deduplicação determinística
- Modelo dimensional (Star Schema)
- Joins time-aware
- Data quality monitoring
- Orquestração de jobs (DAG)
