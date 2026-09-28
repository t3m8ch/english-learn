---
entry: omitted subject and be in terse notes
category: ellipsis
---

# Опущенные подлежащее и be в кратких пометках

## Модель

`(This is) + past participle …` / `(noun phrase)` в скобках без глагола

## Значение

В комментариях к коду, заметках и заголовках часто опускают очевидные подлежащее и связку `be`, оставляя только смысловую часть.

## Разбор исходного контекста

- `Gated by the caller to replica-TRAP catches only` = `This is gated by the caller…` — «это ограничено вызывающим кодом…». Пассивное причастие `gated` осталось, а `This is` опущено.
- `(best-effort snapshot)` = `so this is only a best-effort snapshot` — пометка в скобках без глагола.

## Полная или более простая форма

`This is gated by the caller to replica-TRAP catches only.` / `…the primary may still be live, so its snapshot is only best-effort.`

## Контексты

- `Gated by the caller to replica-TRAP catches only: the frequent SK-leak invariant trials must NOT trigger this or they would fill the disk.`
  — Вызывающий код включает это только тогда, когда TRAP сработал на реплике.
  — [Источник](../../phrases/2026/09/2026-09-28-001.md)

## Ограничения и типичные ошибки

Предложение, начинающееся с причастия прошедшего времени, легко принять за повелительное наклонение. Если после причастия стоит `by` + исполнитель, это почти всегда пассив с опущенным `This is`.

## Связанные конструкции

- [Пассивный залог с be + Past Participle](../passive-voice/be-past-participle.md)
