---
entry: best-effort
type: fixed-expression
---

# best-effort

## Значение 1: по возможности, без гарантии результата

### Модель

`best-effort + noun` / `on a best-effort basis`

### Когда используется

Действие выполняется с максимальным старанием, но успех или корректность результата не гарантируются. Противоположность — `guaranteed`.

### Контексты

- `The replica is already down (its startup process aborted), so its dir is frozen and consistent; the primary may still be live (best-effort snapshot).`
  — Primary ещё может работать, поэтому его снимок делается без гарантий целостности.
  — [Источник](../phrases/2026/09/2026-09-28-001.md)

### Типичная ошибка

Дефис ставится, когда выражение стоит определением перед существительным: `best-effort snapshot`. Типичные сочетания: `best-effort delivery` (как у UDP), `best-effort cleanup`.
