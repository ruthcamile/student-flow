<div align="center">

# 💜 Student Flow

**Seu organizador acadêmico com pastas, tags, prazos e alertas que realmente te avisam.**

<br>

![React](https://img.shields.io/badge/React-6D28D9?style=for-the-badge&logo=react&logoColor=white)
![TypeScript](https://img.shields.io/badge/TypeScript-7C3AED?style=for-the-badge&logo=typescript&logoColor=white)
![Vite](https://img.shields.io/badge/Vite-8B5CF6?style=for-the-badge&logo=vite&logoColor=white)
![Node.js](https://img.shields.io/badge/Node.js-6D28D9?style=for-the-badge&logo=nodedotjs&logoColor=white)
![Express](https://img.shields.io/badge/Express-7C3AED?style=for-the-badge&logo=express&logoColor=white)
![Prisma](https://img.shields.io/badge/Prisma-8B5CF6?style=for-the-badge&logo=prisma&logoColor=white)
![MySQL](https://img.shields.io/badge/MySQL-6D28D9?style=for-the-badge&logo=mysql&logoColor=white)

![Status](https://img.shields.io/badge/status-planejamento-A78BFA?style=flat-square)
![Versão](https://img.shields.io/badge/versão-1.0_(MVP)-7C3AED?style=flat-square)

</div>

---

## ✨ Sobre o projeto

O Student Flow nasceu de uma frustração bem simples: planner de faculdade, ou é bonito e não avisa nada, ou avisa por e-mail que ninguém abre. Aqui a ideia é ter **um lugar só** onde você joga tudo o que precisa fazer, organiza do jeito que quiser e é avisado **antes** de o prazo virar problema.

Pensa numa mistura de **pastinhas** (uma pra cada matéria, projeto ou fase da vida) com um **quadro estilo Trello**, tudo com **tags** e **prioridades**.

---

## 1. Termo de abertura

### 📌 Título
**Student Flow**: organizador acadêmico com pastas, tags e alertas inteligentes.

### 🔥 Problema real
Estudante de graduação lida com várias matérias, trabalhos em grupo, provas, estágio e projetos pessoais ao mesmo tempo. Na prática:

- as tarefas ficam espalhadas entre grupo de WhatsApp, Teams, caderno e print de tela;
- os prazos moram em lugares diferentes e ninguém lembra de todos;
- os apps existentes ou são genéricos demais (não entendem o conceito de "matéria") ou só avisam por e-mail, que passa batido;
- priorizar vira chute, porque nada mostra o que está mais perto de estourar.

### 💎 Proposta de valor
- **Pastas aninhadas**: crie uma pasta por matéria, e subpastas pra provas, trabalhos, leituras, o que fizer sentido.
- **Tags livres e coloridas** que cruzam as pastas (`#prova`, `#grupo`, `#urgente`, `#estágio`).
- **Alertas em camadas**: notificação no navegador, aviso dentro do app e e-mail como reforço, com antecedência configurável por tarefa.
- **Dois jeitos de ver a mesma coisa**: lista e quadro kanban, sem duplicar dado.
- **Prioridade que pesa**: o app destaca o que está perto do prazo e ainda não foi começado.

### 🎯 Escopo

| ✅ Dentro do escopo (v1.0) | ❌ Fora do escopo (por enquanto) |
|---|---|
| Cadastro e login de usuário | Login social (Google, GitHub) |
| Pastas e subpastas com cor e ícone | Compartilhar pastas entre usuários |
| Tarefas com prazo, prioridade, status e descrição | Colaboração em tempo real |
| Tags personalizadas e filtro por tag | Integração com Teams, Google Agenda ou Trello |
| Visualização em lista e em kanban | Visualização de calendário |
| Alertas: push no navegador, central de notificações e e-mail | Aplicativo mobile nativo |
| Busca e filtros (pasta, tag, prioridade, prazo) | Anexo de arquivos nas tarefas |
| Tema claro e escuro | Estatísticas e relatórios de produtividade |

---

## 2. Histórias de usuário

1. **Como** estudante com várias matérias, **quero** criar uma pasta para cada disciplina e subpastas dentro dela, **para que** tudo de cada matéria fique junto e eu não perca tempo procurando.

2. **Como** estudante com a semana cheia, **quero** definir prazo e prioridade em cada tarefa, **para que** eu saiba o que atacar primeiro.

3. **Como** pessoa que esquece coisas facilmente, **quero** receber alertas no navegador antes do prazo e não só por e-mail, **para que** eu realmente veja o aviso a tempo.

4. **Como** estudante que organiza a vida por assunto, **quero** marcar tarefas com tags e filtrar por elas, **para que** eu veja, por exemplo, tudo que é `#prova` de todas as matérias de uma vez.

5. **Como** estudante que gosta de ver o progresso, **quero** arrastar tarefas entre colunas (a fazer, fazendo, feito), **para que** eu enxergue o andamento de cara.

---

## 3. Requisitos do sistema

### ⚙️ Funcionais

| ID | Descrição |
|---|---|
| **RF01** | O sistema deve permitir cadastro, login e logout de usuários com senha criptografada. |
| **RF02** | O usuário deve poder criar, renomear, mover e excluir pastas e subpastas, definindo cor e ícone. |
| **RF03** | O usuário deve poder criar, editar, concluir e excluir tarefas com título, descrição, prazo, prioridade (baixa, média, alta) e status. |
| **RF04** | O usuário deve poder criar tags com nome e cor e associar várias tags a uma mesma tarefa. |
| **RF05** | O sistema deve permitir filtrar e buscar tarefas por pasta, tag, prioridade, status e período de prazo. |
| **RF06** | O sistema deve exibir as tarefas em lista e em quadro kanban, com arrastar e soltar para mudar o status. |
| **RF07** | O usuário deve poder configurar um ou mais alertas por tarefa (ex.: 3 dias, 1 dia e 2 horas antes do prazo). |
| **RF08** | O sistema deve enviar os alertas por push no navegador, registrá-los numa central de notificações dentro do app e, opcionalmente, por e-mail. |
| **RF09** | O sistema deve destacar visualmente tarefas atrasadas e tarefas de prioridade alta com prazo próximo. |

### 🛡️ Não funcionais

| ID | Descrição |
|---|---|
| **RNF01** | **Desempenho:** listagens e filtros devem responder em até 1 segundo para até 500 tarefas por usuário. |
| **RNF02** | **Confiabilidade dos alertas:** o agendador deve verificar prazos a cada minuto e disparar o aviso com atraso máximo de 2 minutos. |
| **RNF03** | **Segurança:** senhas com hash (bcrypt), autenticação por token JWT e cada usuário só pode acessar os próprios dados. |
| **RNF04** | **Usabilidade:** interface responsiva, utilizável em telas a partir de 360 px de largura. |
| **RNF05** | **Compatibilidade:** funcionar nas versões atuais do Chrome, Edge e Firefox. |
| **RNF06** | **Persistência:** todos os dados devem ficar em banco relacional, sem depender de armazenamento local do navegador. |

---

## 4. Caso de uso principal e tratamento de erros

### 🎬 Criar uma tarefa com alerta

**Ator:** estudante autenticado

1. **Entrada do usuário:** dentro da pasta *Banco de Dados*, o estudante clica em "Nova tarefa", preenche título, prazo, prioridade e tags, e escolhe os alertas (ex.: 1 dia antes e 2 horas antes).
2. **Processamento:** o sistema valida os campos, confirma que a pasta pertence ao usuário, verifica se os horários de alerta são anteriores ao prazo, salva a tarefa e agenda as notificações correspondentes.
3. **Retorno na tela:** a tarefa aparece na lista e na coluna "A fazer" do kanban, com as tags coloridas e o contador de tempo restante. Uma mensagem confirma que os alertas foram agendados.

Quando chega a hora de um alerta, o sistema envia o push no navegador, adiciona o aviso na central de notificações e, se o usuário tiver ativado, manda o e-mail.

### ⚠️ Fluxos de exceção

| Situação | Comportamento do sistema |
|---|---|
| Título vazio ou prazo em formato inválido | Bloqueia o envio e mostra o erro ao lado do campo, sem perder o que já foi digitado. |
| Prazo no passado | Avisa e pede confirmação antes de salvar. |
| Horário de alerta depois do prazo | Rejeita o alerta e informa o motivo. |
| Pasta ou tarefa não encontrada (ex.: já foi excluída) | Retorna erro 404 e mostra mensagem amigável, redirecionando para a tela inicial. |
| Usuário nega permissão de notificação do navegador | O app segue funcionando e usa a central interna e o e-mail como canais de aviso, com um lembrete discreto para ativar o push. |
| Falha no envio de e-mail | O erro é registrado, o sistema tenta de novo algumas vezes e a notificação interna continua garantida. |
| Token expirado | Redireciona para o login e, após entrar, devolve o usuário à tela em que estava. |

---

## 5. Arquitetura e stack

```
┌──────────────────┐      HTTPS / REST      ┌────────────────────┐      Prisma      ┌─────────┐
│  React + Vite    │ ◄────────────────────► │  Node.js + Express │ ◄──────────────► │  MySQL  │
│  (TypeScript)    │                        │  (TypeScript)      │                  └─────────┘
└──────────────────┘                        │                    │
        ▲                                   │  ┌──────────────┐  │
        │  Web Push                         │  │ node-cron    │  │──► e-mail (Nodemailer)
        └───────────────────────────────────┤  │ (agendador)  │  │
                                            │  └──────────────┘  │
                                            └────────────────────┘
```

| Camada | Tecnologia |
|---|---|
| **Interface** | React + TypeScript com Vite, e dnd-kit para o arrastar e soltar do kanban |
| **Lógica / API** | Node.js + Express + TypeScript, com validação via Zod e autenticação JWT |
| **Alertas** | node-cron para varrer prazos, Web Push para notificações no navegador e Nodemailer para e-mail |
| **Armazenamento** | MySQL, acessado com Prisma ORM |

### 💭 Justificativa
TypeScript de ponta a ponta reduz erro e permite compartilhar tipos entre front e back. O Prisma deixa o modelo de dados (usuários, pastas, tarefas, tags e alertas) claro e versionado em migrations, e o MySQL dá conta bem das relações entre essas entidades, incluindo as pastas aninhadas. O node-cron roda dentro da própria API, o que mantém o agendamento de alertas simples sem precisar de infraestrutura extra.

---

## 6. Critérios de aceite e definição de pronto

O Student Flow v1.0 está pronto quando:

- [ ] Um usuário consegue se cadastrar, entrar e sair, e nunca enxerga dados de outra conta.
- [ ] É possível criar pastas e subpastas, e mover tarefas entre elas sem erro.
- [ ] Tarefas são criadas, editadas, concluídas e excluídas com validação de campos obrigatórios.
- [ ] Tags podem ser criadas e combinadas, e o filtro por tag, pasta, prioridade e prazo retorna resultados corretos.
- [ ] O kanban atualiza o status da tarefa ao arrastar, e a mudança persiste após recarregar a página.
- [ ] Um alerta configurado para daqui a poucos minutos chega por push no navegador e aparece na central de notificações dentro da tolerância de 2 minutos.
- [ ] Se o push for negado, o aviso ainda chega pela central interna e por e-mail.
- [ ] Todos os fluxos de erro descritos na seção 4 respondem com mensagem clara, sem travar a tela.
- [ ] A interface é utilizável em tela de 360 px e funciona no Chrome, Edge e Firefox.
- [ ] O README está completo e há instruções de como rodar o projeto localmente.

---

## 🚀 Como rodar (planejado)

```bash
# clonar o repositório
git clone https://github.com/seu-usuario/student-flow.git
cd student-flow

# backend
cd server
npm install
cp .env.example .env     # configure DATABASE_URL, JWT_SECRET e SMTP
npx prisma migrate dev
npm run dev

# frontend (em outro terminal)
cd ../web
npm install
npm run dev
```

---

<div align="center">

Feito com 💜 e muitas tags

</div>
