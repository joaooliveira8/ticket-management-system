# 📋 Requisitos do Sistema — Helpdesk QA System

---

## ✅ Requisitos Funcionais

### Autenticação e Perfis

| ID | Requisito | Origem |
|---|---|---|
| RF-001 | O sistema deve permitir que usuários façam login com e-mail e senha | Diagrama de Classes — método `autenticar()` |
| RF-002 | O sistema deve diferenciar os perfis de acesso: Usuário, Analista e Administrador | Diagrama de Classes — atributo `tipo: enum` |
| RF-003 | O sistema deve impedir que um perfil acesse funcionalidades de outro perfil | Diagrama de Casos de Uso — atores separados |

### Chamados

| ID | Requisito | Origem |
|---|---|---|
| RF-004 | O sistema deve permitir que o Usuário crie um chamado informando título, descrição e categoria | Diagrama de Classes — classe `Chamado` |
| RF-005 | O sistema deve validar os campos obrigatórios antes de criar o chamado | Diagrama de Atividades — "Sistema valida dados" |
| RF-006 | O sistema deve atribuir automaticamente o status `Aberto` ao chamado recém-criado | Máquina de Estados — estado inicial `Aberto` |
| RF-007 | O sistema deve permitir que o Usuário consulte seus próprios chamados | Diagrama de Casos de Uso — "Consultar chamados" |
| RF-008 | O sistema deve permitir que o Analista visualize todos os chamados | Diagrama de Casos de Uso — "Visualizar chamados" |
| RF-009 | O sistema deve permitir que o Analista assuma um chamado para atendimento | Diagrama de Classes — método `atenderChamado()` |

### Status

| ID | Requisito | Origem |
|---|---|---|
| RF-010 | O sistema deve permitir que o Analista atualize o status do chamado | Diagrama de Casos de Uso — "Atualizar status" |
| RF-011 | O sistema deve seguir o fluxo de status: `Aberto → Em andamento → Aguardando usuário → Resolvido → Fechado` | Máquina de Estados |
| RF-012 | O sistema deve permitir que o Usuário confirme ou rejeite a solução aplicada | Diagrama de Atividades — "Usuário confirma solução" |
| RF-013 | O sistema deve reabrir o chamado caso o Usuário rejeite a solução | Máquina de Estados — transição "rejeitado" |

### Comentários

| ID | Requisito | Origem |
|---|---|---|
| RF-014 | O sistema deve permitir que Usuários e Analistas adicionem comentários em um chamado | Diagrama de Casos de Uso — "Comentar chamado" |
| RF-015 | O sistema deve registrar o autor e a data/hora de cada comentário | Diagrama de Classes — atributo `data: datetime` |
| RF-016 | O sistema deve impedir o envio de comentário com campo vazio | Diagrama de Classes — atributo `texto: string` obrigatório |

### Administração

| ID | Requisito | Origem |
|---|---|---|
| RF-017 | O sistema deve permitir que o Administrador gerencie usuários | Diagrama de Casos de Uso — "Gerenciar usuários" |
| RF-018 | O sistema deve permitir que o Administrador crie e edite categorias | Diagrama de Casos de Uso — "Definir categorias" |
| RF-019 | O sistema deve permitir que o Administrador defina os níveis de prioridade | Diagrama de Casos de Uso — "Definir prioridades" |

---

## ⚙️ Requisitos Não Funcionais

| ID | Requisito | Origem |
|---|---|---|
| RNF-001 | O sistema deve responder às requisições em no máximo 3 segundos | Diagrama de Classes — atributo `status: enum` implica atualizações em tempo real |
| RNF-002 | O sistema deve criptografar as senhas dos usuários | Diagrama de Classes — método `autenticar()` |
| RNF-003 | O sistema deve registrar log de todas as alterações nos chamados | Diagrama de Classes — atributo `dataAbertura: date` implica rastreabilidade |
| RNF-004 | O sistema deve exibir mensagens de erro claras ao usuário | Diagrama de Atividades — "Exibir erro" no fluxo de validação |

---

## 🔗 Rastreabilidade

| Requisito | Diagrama relacionado |
|---|---|
| RF-001, RF-002, RF-003 | Diagrama de Classes, Diagrama de Casos de Uso |
| RF-004, RF-005, RF-006 | Diagrama de Classes, Diagrama de Atividades, Máquina de Estados |
| RF-007, RF-008, RF-009 | Diagrama de Casos de Uso, Diagrama de Classes |
| RF-010, RF-011, RF-012, RF-013 | Diagrama de Casos de Uso, Máquina de Estados, Diagrama de Atividades |
| RF-014, RF-015, RF-016 | Diagrama de Casos de Uso, Diagrama de Classes |
| RF-017, RF-018, RF-019 | Diagrama de Casos de Uso |
| RNF-001, RNF-002, RNF-003, RNF-004 | Diagrama de Classes, Diagrama de Atividades |
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
