# 📐 Diagramas UML — Helpdesk QA System

Diagramas de modelagem do Sistema de Gerenciamento de Chamados, produzidos com notação UML para documentar a estrutura, comportamento e fluxos do sistema.

---

## 📁 Arquivos

| Arquivo | Tipo | Descrição |
|---|---|---|
| `caso-de-uso.png` | Diagrama de Casos de Uso | Atores e funcionalidades do sistema |
| `diagrama-de-classes.png` | Diagrama de Classes | Estrutura das entidades e relacionamentos |
| `diagrama-de-atividades.png` | Diagrama de Atividades | Fluxo principal de abertura e resolução de chamados |
| `maquina-de-estados.png` | Máquina de Estados | Ciclo de vida de um chamado |

---

## 🧩 Sobre cada diagrama

### Casos de Uso
Representa os três atores do sistema — **Usuário**, **Analista** e **Administrador** — e as funcionalidades que cada um pode acessar. Inclui relacionamentos `«include»` e `«extend»` entre os casos de uso.

### Classes
Modela as entidades principais: `Usuario`, `Analista`, `Chamado`, `Comentario` e `Categoria`. Detalha atributos, métodos e os tipos de relacionamento entre as classes (herança, associação e multiplicidades).

### Atividades
Descreve o fluxo completo desde a abertura de um chamado até o seu encerramento, incluindo decisões como validação de dados, classificação de urgência e confirmação de resolução.

### Máquina de Estados
Mostra os estados possíveis de um chamado ao longo do seu ciclo de vida: `Aberto → Em andamento → Resolvido → Fechado`, com as transições e condições entre cada estado.

---

## 🛠️ Ferramenta utilizada

Diagramas criados com **draw.io**.

---

## 🔗 Relacionado a

- [`docs/requisitos.md`](../docs/requisitos.md)
- [`docs/regras-negocio.md`](../docs/regras-negocio.md)
- [`testes/casos-de-teste.md`](../testes/casos-de-teste.md)
