# PowerDesigner Model Validator

Scripts para **validação automatizada de modelos físicos de dados** no SAP PowerDesigner.

![Status](https://img.shields.io/badge/status-ativo-green)
![License](https://img.shields.io/badge/license-MIT-blue)
![PowerDesigner](https://img.shields.io/badge/PowerDesigner-16.x-orange)

---

## 📋 Sobre o projeto

Este repositório reúne scripts desenvolvidos para **automatizar a validação de modelos físicos de dados** no SAP PowerDesigner, cobrindo padrões de nomenclatura, tipos de dados, completude de documentação, integridade referencial e conformidade com boas práticas de modelagem.

O objetivo é **reduzir o esforço manual** de conferência de modelos, garantir **aderência a padrões corporativos** e apoiar a **governança e qualidade de dados**.

---

## ✅ O que os scripts validam

| Script | O que valida |
|---|---|
| `01_validar_nomenclatura.pws` | Padrões de nomenclatura de tabelas, colunas, índices e constraints |
| `02_validar_tipos_dados.pws` | Tipos, tamanhos e precisão de colunas |
| `03_validar_comentarios.pws` | Completude de comentários em tabelas e colunas |
| `04_validar_chaves_referencias.pws` | Chaves primárias, estrangeiras e integridade referencial |
| `05_validar_indices.pws` | Índices e constraints conforme padrões |
| `06_validar_obrigatoriedade.pws` | Campos obrigatórios (NOT NULL) e valores padrão |

---

## 🛠️ Tecnologias

- **SAP PowerDesigner** (VBScript / PowerShell)
- **SQL** (DDL/DML)
- **Bancos relacionais:** PostgreSQL, Oracle, SQL Server, DB2

---

## 🚀 Como usar

### Pré-requisitos

- SAP PowerDesigner instalado (versão 16.x ou superior)
- Modelo físico de dados (`.pdm`) aberto no PowerDesigner
- Permissão para executar scripts

### Passo a passo

1. Abra o modelo físico (`.pdm`) no PowerDesigner
2. Acesse **Tools → Execute Script**
3. Selecione o script desejado (ex.: `01_validar_nomenclatura.pws`)
4. O script retorna um **relatório de não conformidades**
5. Corrija o modelo conforme o relatório
6. Repita até não haver mais não conformidades

> **Nota:** A execução é **manual** — basta rodar o script quando necessário validar um modelo. A **validação em si é automatizada** pelo script.

---

## 📁 Estrutura do repositório

