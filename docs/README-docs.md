# Regras do Jogo
Aviso prévio: se você é de fora e não faz parte do projeto, basicamente isso é a forma de comunicação dos desenvolvedores, motivo esse pela qual se encontra em português.

Esse arquivo contém as regras do repositório, que devem ser seguidas para uma melhor organização na comunicação.

# 1️⃣ Identificação das pessoas (obrigatório)

### Objetivo

* saber **quem escreveu o quê**
* manter histórico limpo
* evitar “quem foi mesmo que decidiu isso?”

---

## Padrão de identidade no Git

Cada pessoa deve configurar **nome e email fixos**:

```bash
git config --global user.name "Pedro"
git config --global user.email "pedro@email.com"
```

## Assinatura dentro dos arquivos

Toda entrada relevante em `docs/` termina com assinatura simples:

```md
— Pedro (2025-01-12)
```

Nada de apelido aleatório.
Nada de emoji.
Nada de conversa solta.

Lembre-se de colocar a data no padrão internacional ISO 8601 (YYYY-MM-DD)

---

# 2️⃣ Organização dos arquivos (regra rígida)

## Arquivos fixos

```
/docs
 ├── ideas.md        # ideias abertas
 ├── questions.md    # dúvidas abertas
 ├── decisions.md    # decisões fechadas
 ├── todo.md         # tarefas práticas
 └── README-docs.md  # regras do jogo
```

Não criar arquivos novos sem consenso.

---

# 3️⃣ Estrutura INTERNA dos arquivos

## Regra de ouro

> **Coisas novas SEMPRE entram no TOPO do arquivo**

Motivo:

* o que importa agora está visível
* histórico vai ficando pra baixo

---

## `ideas.md`

```md
# Ideias em aberto

## Estrutura de boards
- Boards como dados no banco
- Começar apenas com /t/

— Pedro (2025-01-12)

---
## Upload de imagens
- Não no MVP

— João (2025-01-11)
```

📌 Separador obrigatório:

```
---
```

---

## `questions.md`

```md
# Dúvidas em aberto

## Boards
- Boards podem ser desativadas?
- Precisam de descrição?

— João (2025-01-12)
```

Quando a dúvida for resolvida:

* **Marque como "(RESOLVIDO)"**
* Não apague.

```md
# Dúvidas em aberto

## Boards (RESOLVIDO)
- Boards podem ser desativadas?
- Precisam de descrição?

— João (2025-01-12)
```

---

## `decisions.md` (o mais importante)

```md
# Decisões do projeto

## 2025-01-12 — Estrutura de boards
Decidido:
- Boards são dados no banco
- URL padrão /{board}/
- Apenas /t/ no MVP

Motivo:
- Menos complexidade
- Facilita crescimento

— Pedro, João
```

📌 Aqui:

* ninguém “discute”
* só se **registra o que já foi decidido**

---

## `todo.md`

```md
# TODO

- [ ] Criar schema do banco (Pedro)
- [ ] Criar rota /{board}/ (João)
- [ ] Criar formulário de post (João)
```

Coloque o nome para identificar quem é o dono da tarefa.
Quando a tarefa for concluída, é só remover.

---

# 4️⃣ Padrão de commit (ESSENCIAL)

## 📌 Formato obrigatório

```
<área>: <ação curta>
```

### Exemplos bons

```
docs questions: adicionar dúvidas sobre boards
docs decisions: registrar decisão sobre MVP
docs todo: adicionar tarefas iniciais
```

### Exemplos proibidos ❌

```
acho que isso resolve
conversa com o joão
testando coisas
```

### "E se for mais de uma alteração?"

## Formato:
```
<área(s)>: <quantas alterações>

<descrição constanto o que alterou>
```

## Exemplo:
```
docs, index.html: 2 alterações, 1 alteração.

ideas.md:
    - adicionar ideia de tela de login

questions.md:
    - adicionar dúvida sobre a board /t/

index.html:
    - remover tag desnecessária no head
```

Dica: uma alteração apenas, usar o `git commit -m "<alteração>"`, para mais alterações usar apenas o `git commit` (editor built-in do Git).

---

## Regra mental do commit

> Se o commit não responde **“o que mudou e por quê”**, ele está errado.

---

# 5️⃣ O que É PROIBIDO enviar

Isso é importante pra manter sanidade:

❌ desabafo<br>
❌ opinião sem contexto<br>
❌ mensagens curtas tipo chat<br>
❌ “kkk”, “acho”, “talvez”<br>
❌ código grande em `docs/`

---

# 6️⃣ O que É PERMITIDO (e incentivado)

✅ ideias bem descritas<br>
✅ dúvidas objetivas<br>
✅ decisões claras<br>
✅ listas simples<br>
✅ texto curto e direto

---

# 7️⃣ Regra final

- Não usamos chat para decisões
- Tudo importante vai para docs/
- Coisas novas entram no topo
- Decisão sempre vira registro
- Commit explica a mudança

---

## Resultado disso tudo

* ninguém se perde
* iniciante aprende a pensar estruturado
* projeto ganha memória
* menos retrabalho
* menos stress

Bacana demais.