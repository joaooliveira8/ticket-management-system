# 📋 Requisitos do Sistema — Helpdesk QA System

---

## ✅ Requisitos Funcionais

### Autenticação e Perfis

| ID | Requisito |
|---|---|
| RF-001 | O sistema deve permitir que usuários façam login com e-mail e senha |
| RF-002 | O sistema deve diferenciar os perfis de acesso: Usuário, Analista e Administrador |
| RF-003 | O sistema deve impedir que um perfil acesse funcionalidades de outro perfil |

### Chamados

| ID | Requisito |
|---|---|
| RF-004 | O sistema deve permitir que o Usuário crie um chamado informando título, descrição e categoria |
| RF-005 | O sistema deve validar os campos obrigatórios antes de criar o chamado |
| RF-006 | O sistema deve atribuir automaticamente o status `Aberto` ao chamado recém-criado |
| RF-007 | O sistema deve permitir que o Usuário consulte seus próprios chamados |
| RF-008 | O sistema deve permitir que o Analista visualize todos os chamados |
| RF-009 | O sistema deve permitir que o Analista assuma um chamado para atendimento |

### Status

| ID | Requisito |
|---|---|
| RF-010 | O sistema deve permitir que o Analista atualize o status do chamado |
| RF-011 | O sistema deve seguir o fluxo de status: `Aberto → Em andamento → Aguardando usuário → Resolvido → Fechado` |
| RF-012 | O sistema deve permitir que o Usuário confirme ou rejeite a solução aplicada |
| RF-013 | O sistema deve reabrir o chamado caso o Usuário rejeite a solução |

### Comentários

| ID | Requisito |
|---|---|
| RF-014 | O sistema deve permitir que Usuários e Analistas adicionem comentários em um chamado |
| RF-015 | O sistema deve registrar o autor e a data/hora de cada comentário |
| RF-016 | O sistema deve impedir o envio de comentário com campo vazio |

### Administração

| ID | Requisito |
|---|---|
| RF-017 | O sistema deve permitir que o Administrador gerencie usuários (criar, editar, desativar) |
| RF-018 | O sistema deve permitir que o Administrador crie e edite categorias de chamados |
| RF-019 | O sistema deve permitir que o Administrador defina os níveis de prioridade dos chamados |

### Notificações

| ID | Requisito |
|---|---|
| RF-020 | O sistema deve notificar o Usuário quando o status do seu chamado for atualizado |
| RF-021 | O sistema deve notificar o Analista quando um novo chamado for atribuído a ele |

---

## ⚙️ Requisitos Não Funcionais

### Desempenho

| ID | Requisito |
|---|---|
| RNF-001 | O sistema deve responder às requisições em no máximo 3 segundos em condições normais de uso |
| RNF-002 | O sistema deve suportar até 100 usuários simultâneos sem degradação de desempenho |

### Segurança

| ID | Requisito |
|---|---|
| RNF-003 | O sistema deve criptografar as senhas dos usuários armazenadas no banco de dados |
| RNF-004 | O sistema deve encerrar a sessão automaticamente após 30 minutos de inatividade |
| RNF-005 | O sistema deve registrar log de todas as alterações realizadas nos chamados |

### Usabilidade

| ID | Requisito |
|---|---|
| RNF-006 | O sistema deve ser responsivo e funcionar em dispositivos móveis e desktop |
| RNF-007 | O sistema deve exibir mensagens de erro claras e objetivas ao usuário |
| RNF-008 | O sistema deve ser navegável com no máximo 3 cliques para as funcionalidades principais |

### Confiabilidade

| ID | Requisito |
|---|---|
| RNF-009 | O sistema deve ter disponibilidade mínima de 99% em dias úteis |
| RNF-010 | O sistema deve realizar backup dos dados diariamente |

---

## 🔗 Rastreabilidade

| Requisito | Diagrama relacionado |
|---|---|
| RF-001, RF-002, RF-003 | Diagrama de Casos de Uso |
| RF-004, RF-005, RF-006 | Diagrama de Atividades, Diagrama de Classes |
| RF-010, RF-011, RF-012, RF-013 | Máquina de Estados |
| RF-014, RF-015, RF-016 | Diagrama de Classes (classe `Comentario`) |
| RF-017, RF-018, RF-019 | Diagrama de Casos de Uso (Administrador) |
-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
# 📋 Requisitos do Sistema

## ✅ Requisitos Funcionais

- O sistema deve permitir que usuários criem chamados  
- O sistema deve permitir visualizar chamados  
- O sistema deve permitir atualizar o status do chamado  
- O sistema deve permitir adicionar comentários  

---

## ⚙️ Requisitos Não Funcionais

- O sistema deve ter tempo de resposta rápido  
- O sistema deve garantir segurança dos dados  
- O sistema deve ser fácil de usar  
