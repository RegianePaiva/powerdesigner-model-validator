# Como usar

Guia passo a passo para executar os scripts de validação no SAP PowerDesigner.

---

## Pré-requisitos

- **SAP PowerDesigner** instalado (versão 16.x ou superior)
- **Modelo físico de dados** (`.pdm`) aberto no PowerDesigner
- **Permissão** para executar scripts no PowerDesigner
- **Conhecimento básico** de modelagem de dados

---

## Passo a passo

### 1. Abra o modelo físico

Abra o arquivo `.pdm` no SAP PowerDesigner.

> O modelo deve estar no nível **Physical Data Model** (não conceitual ou lógico).

---

### 2. Acesse o menu de scripts

No PowerDesigner, acesse:

Tools → Execute Script Ou use o atalho:Ctrl + Shift + X


---

### 3. Selecione o script desejado

Navegue até a pasta `scripts/` e escolha o script:

| Script | O que valida |
|---|---|
| `01_validar_nomenclatura.pws` | Padrões de nomenclatura |
| `02_validar_tipos_dados.pws` | Tipos e tamanhos de dados |
| `03_validar_comentarios.pws` | Completude de comentários |
| `04_validar_chaves_referencias.pws` | Chaves e integridade referencial |
| `05_validar_indices.pws` | Índices e constraints |
| `06_validar_obrigatoriedade.pws` | Campos obrigatórios |

---

### 4. Execute o script

Clique em **Run** (ou **Executar**).

O script vai percorrer o modelo e retornar um **relatório de não conformidades**.

---

### 5. Analise o resultado

O resultado pode ser exibido:

- **Na tela** (janela de output do PowerDesigner)
- **Em arquivo** (`.txt` ou `.csv`, dependendo do script)

---

### 6. Corrija o modelo

Com base no relatório:

1. Identifique as não conformidades
2. Corrija o modelo no PowerDesigner
3. Execute o script novamente
4. Repita até não haver mais não conformidades

---

## Dicas

- **Execute um script por vez** — evita confusão no output
- **Salve o relatório** antes de corrigir — serve como evidência de auditoria
- **Combine scripts** — rode nomenclatura + comentários + chaves na mesma sessão
- **Automatize a execução** — se quiser, crie um `.bat` que roda todos em sequência

---

## Execução manual vs. automatizada

| Aspecto | O que significa |
|---|---|
| **Validação** | ✅ **Automatizada** — o script faz a validação |
| **Execução** | ⚠️ **Manual** — você precisa rodar o script |

> **Importante:** A execução é manual. A validação em si é automatizada pelo script.

---

## Problemas comuns

### Script não executa

- Verifique se o modelo está aberto no nível **Physical Data Model**
- Verifique se você tem permissão de execução
- Verifique se o PowerDesigner está na versão correta

### Output vazio

- O modelo pode estar em conformidade (nenhuma não conformidade)
- Verifique se o script está realmente sendo executado
- Verifique se o modelo tem tabelas/colunas

### Erro de sintaxe

- Verifique se o script foi salvo com a extensão `.pws`
- Verifique se não há caracteres especiais no caminho
- Verifique se o PowerDesigner está configurado para VBScript

---

## Suporte

Abra uma **issue** no repositório com:

- Descrição do problema
- Versão do PowerDesigner
- Print do erro (se houver)
- Trecho do script (se aplicável)



