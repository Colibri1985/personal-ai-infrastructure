# Frigga RAID-ED Register — Green Pilot: Контрольный контур AI-инфраструктуры

> Инициатива: Green Pilot — Контрольный контур AI-инфраструктуры  
> Версия Baseline: 0.1  
> Classification: Green  
> Последнее обновление: 2026-09-20  
> Ведёт: Владелец repository

## Register

| ID | Тип | Описание | Статус | Owner | Влияние | Вероятность / уверенность | Триггер / срок | Следующее действие | Evidence / источник | Последнее обновление |
|---|---|---|---|---|---|---|---|---|---|---|
| A-001 | Assumption | Markdown-only artifacts достаточны для проверки workflow | Yellow | Владелец repository | Среднее | Средняя уверенность | Gate 1 review | Подтвердить или пересмотреть в ходе review | Pilot design | 2026-09-20 |
| R-001 | Risk | Scope может уйти от governance validation к software implementation | Yellow | Владелец repository | Среднее | Средняя вероятность | Любой запрос на UI, API или deployment | Сохранять explicit out-of-scope | Project Passport | 2026-09-20 |
| D-001 | Dependency | Gate 1 review владельцем repository | Yellow | Владелец repository | Высокое | Определённо | До Level 1 planning | Approve, revise или reject decision pack | Gate 1 pack | 2026-09-20 |
| E-001 | Evidence gap | Не подтверждены нужные поля будущего control desk | Yellow | Владелец repository | Низкое | Высокая уверенность | До post-pilot design | Зафиксировать feedback после review | Пока нет evidence | 2026-09-20 |
| D-002 | Decision | Утвердить Draft Baseline 0 и разрешить Level 1 planning | Yellow | Владелец repository | Высокое | Требуется решение | Gate 1 | Зафиксировать explicit decision | Gate 1 pack | 2026-09-20 |
| I-001 | Issue | Активная проблема пока не выявлена | Green | Владелец repository | Низкое | Высокая уверенность | Continuous review | Обновить при появлении blocker | Current pilot review | 2026-09-20 |
| A-002 | Assumption | Контекстная Activity-модель повысит ясность и безопасность workflow | Yellow | Владелец repository | Среднее | Средняя уверенность | Gate 1 review | Подтвердить, скорректировать или отклонить | Architecture Note | 2026-09-20 |
| R-002 | Risk | Архитектурная идея преждевременно расширится в UI, API или automation project | Yellow | Владелец repository | Среднее | Средняя вероятность | Любой запрос на implementation | Сохранять Markdown-only scope | Architecture Note | 2026-09-20 |
| D-003 | Decision | Принять Activity-модель как future design principle | Yellow | Владелец repository | Высокое | Требуется решение | Gate 1 — Revision | Зафиксировать решение владельца | Architecture Note | 2026-09-20 |