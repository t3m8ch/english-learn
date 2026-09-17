---
entry: joint consensus
type: collocation
---

# joint consensus

## Значение 1: совместный консенсус

### Модель

`joint consensus approach` / `joint configuration`

### Когда используется

В Raft это переходный режим изменения состава кластера, в котором одновременно действуют требования старой и новой конфигурации. Для решения требуется отдельное большинство в каждой из них.

### Контексты

- `Membership changes: Raft’s mechanism for changing the set of servers in the cluster uses a new joint consensus approach where the majorities of two different configurations overlap during transitions. This allows the cluster to continue operating normally during configuration changes.`
  — Механизм Raft использует подход совместного консенсуса, при котором на переходном этапе требуется большинство как старой, так и новой конфигурации.
  — [Источник](../phrases/2026/09/2026-09-17-012.md)

### Типичная ошибка

`Joint` здесь означает «совместный» или «объединённый». Главное слово в `joint consensus approach` — `approach`, поэтому вся группа переводится как «подход на основе совместного консенсуса».
