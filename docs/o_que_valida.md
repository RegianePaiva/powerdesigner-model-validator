# O que os scripts validam

Detalhamento de cada validação realizada pelos scripts.

---

## 1. Padrões de nomenclatura

### Tabelas

- Prefixo obrigatório (`tb_`, `dim_`, `fat_`, `log_`)
- Uso de `snake_case` (letras minúsculas + underscore)
- Sem abreviações ambíguas
- Tamanho máximo definido (ex.: 30 caracteres)

### Colunas

- Prefixo por tipo:
  - `id_` para identificadores
  - `nm_` para nomes
  - `dt_` para datas
  - `vl_` para valores
  - `fl_` para flags
- Uso de `snake_case`
- Sem palavras reservadas do SGBD

### Índices e Constraints

- Prefixo obrigatório:
  - `pk_` para primary key
  - `fk_` para foreign key
  - `uk_` para unique key
  - `idx_` para índices
  - `ck_` para check constraints
- Nomenclatura descritiva

---

## 2. Tipos de dados

### Validações

- Tipos permitidos por contexto
- Tamanhos máximos definidos
- Precisão para valores monetários (`numeric(15,2)`, por exemplo)
- Compatibilidade entre SGBDs (PostgreSQL, Oracle, SQL Server, DB2)

### Exemplos de não conformidade

- `varchar(255)` para campos que deveriam ser `varchar(100)`
- `float` para valores monetários (deveria ser `numeric`)
- `char` sem tamanho definido

---

## 3. Completude de comentários

### Validações

- **Tabelas:** comentário obrigatório
- **Colunas:** comentário obrigatório
- **Tamanho mínimo:** definido (ex.: 10 caracteres)
- **Idioma:** padronizado (português ou inglês, conforme padrão)

### Exemplos de não conformidade

- Tabela sem comentário
- Coluna com comentário vazio
- Comentário com menos de 10 caracteres
- Comentário genérico ("campo qualquer")

---

## 4. Chaves e referências

### Validações

- Toda tabela deve ter **Primary Key (PK)**
- Toda **Foreign Key (FK)** deve referenciar uma PK válida
- Integridade referencial garantida
- Sem FKs órfãs

### Exemplos de não conformidade

- Tabela sem PK
- FK apontando para coluna que não é PK
- FK referenciando tabela inexistente
- Coluna de junção sem FK

---

## 5. Índices e constraints

### Validações

- Índices em colunas de junção (FKs)
- Índices em colunas de filtro frequente
- Constraints de unicidade onde aplicável
- Sem índices duplicados
- Sem índices em colunas de baixa cardinalidade

### Exemplos de não conformidade

- FK sem índice
- Índice duplicado
- Constraint de unicidade em coluna que permite duplicidade

---

## 6. Obrigatoriedade

### Validações

- Campos **NOT NULL** conforme regra de negócio
- **Valores padrão** definidos para campos aplicáveis
- **PKs** sempre NOT NULL
- **FKs** conforme regra

### Exemplos de não conformidade

- Campo obrigatório sem NOT NULL
- Campo com valor padrão ausente
- PK que permite NULL (erro grave)

---

## Resumo das validações

| Categoria | Validações |
|---|---|
| Nomenclatura | Tabelas, colunas, índices, constraints |
| Tipos de dados | Tipos, tamanhos, precisão |
| Comentários | Tabelas, colunas, tamanho mínimo |
| Chaves | PK, FK, integridade referencial |
| Índices | FKs, filtros, unicidade |
| Obrigatoriedade | NOT NULL, valores padrão |

---

## Benefícios

- ✅ **Redução de esforço manual** de conferência
- ✅ **Padronização** de todo o modelo
- ✅ **Auditoria** com relatórios de conformidade
- ✅ **Governança** de dados
- ✅ **Qualidade** antes da implementação
