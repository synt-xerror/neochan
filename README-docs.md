# Regras do repositório `docs/`

Este diretório contém a **comunicação técnica e organizacional** do projeto.
Não é um chat, não é um fórum, não é lugar para código grande.

O objetivo é:

* manter histórico claro
* registrar decisões importantes
* reduzir ruído
* permitir que qualquer pessoa entenda o projeto no futuro

---

## Idioma

A comunicação em `docs/` é feita em **português**.
Este diretório é voltado para quem participa do projeto.

---

## Estrutura oficial

```text
docs/
├── README-docs.md      # este arquivo
├── assinaturas.txt     # identificação das pessoas
├── ideas.md            # ideias abertas
├── questions.md        # dúvidas abertas
├── todo.md             # tarefas práticas
├── architecture.md     # visão geral do sistema
└── decisions/          # decisões estruturais (ADR)
```

Não criar novos arquivos sem consenso.

---

## Identificação das pessoas (obrigatório)

### Git

Cada pessoa deve usar **nome e email consistentes** no Git.
O email pode ser específico do projeto.

```bash
git config --global user.name "Nome Sobrenome"
git config --global user.email "nome@projeto.org"
```

### Assinatura nos documentos

Toda entrada relevante termina com assinatura simples:

```md
— Nome (YYYY-MM-DD)
```

* usar data ISO 8601
* sem apelidos
* sem emojis
* sem conversa informal

---

## Regra global de edição

> **Conteúdo novo entra sempre no topo do arquivo**

Motivo:

* o que importa agora fica visível
* histórico permanece preservado

---

## Papel de cada arquivo

### `ideas.md`

* ideias ainda não decididas
* propostas iniciais
* pensamento cru

Formato:

* uma ideia por seção
* separador obrigatório `---`

---

### `questions.md`

* dúvidas reais
* pontos em aberto

Quando resolvida:

* marcar como `(RESOLVIDO)`
* **não apagar**

---

### `todo.md`

* tarefas objetivas
* cada tarefa deve ter responsável

```md
- [ ] Criar schema do banco (Pedro)
```

Quando concluída, remover.

---

### `architecture.md`

* descreve o **estado atual** do sistema
* visão geral dos componentes
* não registra discussões
* não explica decisões históricas

Mudanças estruturais devem ser refletidas aqui **após** uma decisão formal.

---

### `decisions/` (ADR)

Contém **decisões arquiteturais importantes**.

Cada arquivo representa **uma decisão fechada**.

Formato recomendado:

```text
0001-titulo-curto.md
```

Regras:

* decisão clara
* contexto mínimo
* consequências explícitas
* não editar depois de aceita

Se algo mudar no futuro:

* criar um novo ADR

---

## Fluxo oficial de informação

```text
idea → dúvida → decisão (ADR) → arquitetura
```

* ideias nascem em `ideas.md`
* incertezas vão para `questions.md`
* decisões estruturais viram ADR
* `architecture.md` reflete o resultado

---

## Padrão de commit (obrigatório)

Formato:

```
<área>: <ação curta>
```

Exemplos válidos:

```
docs: adicionar ADR sobre boards
docs ideas: nova proposta de moderação
docs architecture: atualizar fluxo de dados
```

Exemplos inválidos:

```
update
testando
conversa
```

Evitar commits com múltiplos objetivos.

---

## O que é proibido

* desabafo
* conversa de chat
* opinião sem contexto
* texto vago
* código grande em `docs/`

---

## O que é esperado

* texto curto e direto
* ideias bem descritas
* dúvidas objetivas
* decisões claras
* histórico preservado

---

## Regra final

Se não ajuda alguém a entender o projeto no futuro,
**não pertence ao `docs/`**.
