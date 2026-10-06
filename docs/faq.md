# FAQ — Perguntas Frequentes

---

## Sobre os scripts

### O que são esses scripts?

São scripts em VBScript para o SAP PowerDesigner que **automatizam a validação de modelos físicos de dados**, cobrindo padrões de nomenclatura, tipos de dados, completude de comentários, chaves, referências, índices e obrigatoriedade.

### Para que servem?

Para **reduzir o esforço manual** de conferência de modelos, garantir **aderência a padrões corporativos** e apoiar a **governança e qualidade de dados**.

### Quem pode usar?

Qualquer profissional de dados que trabalhe com **SAP PowerDesigner** e precise validar modelos físicos:
- Administradores de Dados
- Arquitetos de Dados
- Modeladores de Dados
- Analistas de Governança de Dados

---

## Sobre a execução

### Os scripts rodam automaticamente?

**Não.** A **execução é manual** — você precisa rodar o script no PowerDesigner. A **validação em si é automatizada** pelo script.

### Como executo?

1. Abra o modelo no PowerDesigner
2. Acesse `Tools → Execute Script`
3. Selecione o script
4. Clique em **Run**

### Preciso rodar todos os scripts?

Não. Você pode rodar **um por vez** ou **combinar** os que fizerem sentido para o seu caso.

### Posso agendar a execução?

Sim, se quiser. Você pode criar um `.bat` ou usar o **agendador de tarefas** do Windows para rodar os scripts periodicamente. Mas isso **não está incluído** nos scripts deste repositório.

---

## Sobre os resultados

### O que o script retorna?

Um **relatório de não conformidades** encontradas no modelo, com:
- Tabela/coluna afetada
- Descrição da não conformidade
- Sugestão de correção (quando aplicável)

### Onde vejo o resultado?

Na **janela de output** do PowerDesigner, ou em **arquivo** (dependendo do script).

### Posso exportar o resultado?

Sim. Os scripts podem ser configurados para exportar em `.txt` ou `.csv`.

---

## Sobre compatibilidade

### Funciona em qual versão do PowerDesigner?

**16.x ou superior.** Versões anteriores podem ter diferenças de API.

### Funciona em qual SGBD?

Os scripts são **independentes de SGBD** — funcionam para modelos de **PostgreSQL, Oracle, SQL Server, DB2** e outros.

### Funciona em modelo conceitual ou lógico?

**Não.** Os scripts foram feitos para **modelo físico** (Physical Data Model).

---

## Sobre contribuições

### Posso contribuir?

Sim! Abra uma **issue** com sugestões ou envie um **pull request** com melhorias.

### Posso usar em projetos comerciais?

Sim. A licença é **MIT** — permite uso comercial, modificação e distribuição.

---

## Sobre confidencialidade

### Os scripts contêm dados de clientes?

**Não.** Os scripts são **genéricos** e **não contêm dados, estruturas ou regras de negócio** de qualquer organização específica.

### Posso adaptar para meu contexto?

Sim. Os scripts são **genéricos** e podem ser adaptados para o seu contexto (padrões da sua empresa, nomenclatura específica, etc.).

---

## Suporte

### Onde reporto problemas?

Abra uma **issue** no repositório com:
- Descrição do problema
- Versão do PowerDesigner
- Print do erro (se houver)
- Trecho do script (se aplicável)

### Onde sugiro melhorias?

Abra uma **issue** com a tag `enhancement` ou envie um **pull request**.
