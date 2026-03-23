# 📏 Regras de Negócio — Helpdesk QA System

Regras que definem o comportamento e as restrições do Sistema de Gerenciamento de Chamados.

---

## 👤 Perfis e Acesso

| ID | Regra |
|---|---|
| RN-001 | Todo usuário deve estar autenticado para acessar o sistema |
| RN-002 | Um Usuário só pode visualizar e interagir com seus próprios chamados |
| RN-003 | Um Analista pode visualizar todos os chamados, independente de quem os abriu |
| RN-004 | Apenas o Administrador pode criar, editar ou desativar usuários |
| RN-005 | Apenas o Administrador pode criar e editar categorias e prioridades |

---

## 📋 Chamados

| ID | Regra |
|---|---|
| RN-006 | Todo chamado deve ter obrigatoriamente título, descrição e categoria |
| RN-007 | Todo chamado é criado automaticamente com status `Aberto` |
| RN-008 | Um chamado só pode ser atribuído a um Analista por vez |
| RN-009 | Um Usuário não pode alterar o status do seu próprio chamado |
| RN-010 | Chamados urgentes devem ser classificados com prioridade alta automaticamente |

---

## 🔄 Status e Fluxo

| ID | Regra |
|---|---|
| RN-011 | O fluxo de status deve seguir a ordem: `Aberto → Em andamento → Aguardando usuário → Resolvido → Fechado` |
| RN-012 | Apenas o Analista pode mover o chamado entre os status |
| RN-013 | Um chamado só pode ser marcado como `Resolvido` após o Analista registrar a solução |
| RN-014 | O Usuário deve confirmar ou rejeitar a solução aplicada |
| RN-015 | Se o Usuário rejeitar a solução, o chamado volta automaticamente para o status `Em andamento` |
| RN-016 | Um chamado só é `Fechado` após a confirmação do Usuário |

---

## 💬 Comentários

| ID | Regra |
|---|---|
| RN-017 | Usuários e Analistas podem comentar em chamados |
| RN-018 | Não é permitido enviar comentário com campo vazio |
| RN-019 | Todo comentário deve registrar o autor e a data/hora de envio |
| RN-020 | Comentários não podem ser excluídos, apenas editados pelo próprio autor |

---

## 🗂️ Categorias e Prioridades

| ID | Regra |
|---|---|
| RN-021 | Todo chamado deve pertencer a uma categoria cadastrada pelo Administrador |
| RN-022 | A prioridade de um chamado pode ser: Baixa, Média ou Alta |
| RN-023 | Chamados com prioridade Alta devem ser atendidos antes dos demais |

---

## 🔗 Rastreabilidade

| Regra | Diagrama relacionado |
|---|---|
| RN-001, RN-002, RN-003, RN-004, RN-005 | Diagrama de Casos de Uso, Diagrama de Classes |
| RN-006, RN-007, RN-008, RN-009, RN-010 | Diagrama de Classes, Diagrama de Atividades |
| RN-011, RN-012, RN-013, RN-014, RN-015, RN-016 | Máquina de Estados, Diagrama de Atividades |
| RN-017, RN-018, RN-019, RN-020 | Diagrama de Classes — classe `Comentario` |
| RN-021, RN-022, RN-023 | Diagrama de Classes — classe `Categoria`, Diagrama de Casos de Uso |
