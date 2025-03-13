# Teste Técnico - Estagiário Laravel

## Objetivo
Avaliar os conhecimentos básicos do candidato em Laravel, banco de dados e desenvolvimento web.

## Instruções Gerais
- Utilize **Laravel 9 ou superior**.
- O banco de dados deve ser **MySQL**.
- Utilize **Eloquent ORM** para interagir com o banco de dados.
- Versione o código no **GitHub** (envie o link do repositório ao final).

---

## Parte 1 - Conceitos Teóricos
Responda às seguintes perguntas de forma objetiva:

1. O que são **Service Providers** em Laravel e para que servem?
2. Qual a diferença entre **hasOne** e **hasMany** no Eloquent ORM?
3. O que é **Dependency Injection** e como ela é usada no Laravel?
4. Explique o conceito de **middleware** e dê um exemplo de uso.
5. Como funcionam **migrations** e quais suas vantagens?
6. O que é **Queue** no Laravel e quando usá-la?
7. Explique a diferença entre **API Resource** e um Controller tradicional.

---

## Parte 2 - Desenvolvimento Prático

### Desafio: CRUD de Tarefas (Task Manager)
Desenvolva um sistema básico de gerenciamento de tarefas com as seguintes funcionalidades:

### Entidade `Task`
- `id` (Primary Key)
- `title` (string, obrigatório)
- `description` (text, opcional)
- `status` (enum: 'pendente', 'em andamento', 'concluído')
- `due_date` (data de vencimento, opcional)
- `created_at` e `updated_at` (timestamps automáticos)

### Regras de Negócio
- Uma **tarefa** pode ser criada, editada, listada e deletada.
- Apenas tarefas **pendentes** podem ser editadas ou deletadas.
- O **status** pode ser alterado para 'em andamento' ou 'concluído'.

### Requisitos Técnicos
1. Criar **migration** e **model** (`Task`).
2. Criar um **controller** (`TaskController`) e definir os métodos do CRUD (`index`, `store`, `update`, `destroy`).
3. Criar **rotas API** (`routes/api.php`):
   - `GET /tasks` → Lista todas as tarefas.
   - `POST /tasks` → Cria uma nova tarefa.
   - `PUT /tasks/{id}` → Atualiza uma tarefa.
   - `DELETE /tasks/{id}` → Remove uma tarefa.
4. Criar **validações** (ex: `title` obrigatório, `status` deve ser um dos valores permitidos).
5. Implementar **API Resource** para padronizar a resposta da API.
6. Criar **seeds** para popular a base com tarefas fictícias.

---

## Entrega
1. **Código**: Suba o código no GitHub e envie o link do repositório.
2. **Explicação**: Inclua um `README.md` com instruções para rodar o projeto e um breve resumo das escolhas feitas.

---

Boa sorte! 🚀

