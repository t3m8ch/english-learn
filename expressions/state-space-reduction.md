---
entry: state space reduction
type: collocation
---

# state space reduction

## Значение 1: сокращение пространства состояний

### Модель

`state space + reduction`

### Когда используется

`State space` — множество всех возможных состояний и вариантов поведения системы. `State space reduction` означает проектирование системы так, чтобы таких состояний и вариантов было меньше, благодаря чему алгоритм проще понимать, проверять и реализовывать.

### Контексты

- `The result of this work is a consensus algorithm called Raft. In designing Raft we applied specific techniques to improve understandability, including decomposition (Raft separates leader election, log replication, and safety) and state space reduction (relative to Paxos, Raft reduces the degree of nondeterminism and the ways servers can be inconsistent with each other). A user study with 43 students at two universities shows that Raft is significantly easier to understand than Paxos: after learning both algorithms, 33 of these students were able to answer questions about Raft better than questions about Paxos.`
  — При разработке Raft использовалось сокращение пространства состояний: алгоритм уменьшает степень недетерминированности и число возможных рассогласований серверов.
  — [Источник](../phrases/2026/09/2026-09-17-003.md)

### Типичная ошибка

`Space` здесь не означает физическое пространство: речь о совокупности логически возможных состояний системы.
