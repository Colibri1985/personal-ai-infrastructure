# Frigga Project Passport — Green Pilot: Контрольный контур AI-инфраструктуры

> Состояние артефакта: Черновик  
> Версия Baseline: 0.1  
> Classification: Green  
> Последнее обновление: 2026-09-20  
> Владелец решения: Владелец repository  
> Руководитель выполнения: Владелец repository с AI-assisted drafting

## 1. Инициатива

- **Название:** Green Pilot — Контрольный контур AI-инфраструктуры
- **Краткое описание:** Синтетический Markdown-пилот для проверки Frigga
  workflow в локальном repository.
- **Почему сейчас:** Engineering Governor Rules, Frigga Skill и reference
  templates уже добавлены в repository и требуют контролируемой проверки до
  подключения любого внешнего API.
- **Последствие бездействия:** Будущая интеграция модели может начаться без
  проверенного baseline для решений, доказательств, одобрений и управления
  рисками.

## 2. Цель и результаты

- **Основная цель:** Проверить воспроизводимую последовательность Frigga
  только на Green-синтетических материалах.
- **Ожидаемый результат:** Reviewable Baseline 0, RAID-ED register и Gate 1
  decision pack для pilot.
- **Критерии успеха:**
  - Каждый артефакт отделяет факты от допущений.
  - Владелец может принять одно однозначное решение Gate 1.
  - Не используются внешние системы, API или чувствительные данные.
- **Доказательство приемки:** В repository находятся reviewable Markdown
  artifacts и зафиксировано явное решение владельца.

## 3. Scope

### В scope

- Синтетическое framing проекта.
- Baseline 0 и Project Passport.
- RAID-ED register.
- Gate 1 decision pack.
- Draft Level 1 milestone outline после одобрения.
- Architecture note: контекстные Activities и sovereign control desk.

### Вне scope / non-goals

- Реализация программной панели.
- Подключение Qwen, иных моделей, облачных сервисов или MCP server.
- Использование реальных операционных, персональных, клиентских или финансовых данных.
- Deployment, purchase, sending messages или изменение внешних систем.

## 4. Участники и роли

| Роль | Человек / команда | Ответственность | Полномочия |
|---|---|---|---|
| Sponsor | Владелец repository | Определяет ожидаемый результат | Approve / reject Gates |
| Decision owner | Владелец repository | Принимает Gate decisions | Финальное решение |
| Delivery lead | Владелец repository | Ведёт артефакты pilot | Предлагает обновления |
| Drafting assistant | Локальный AI workflow | Готовит маркированные drafts | Нет права одобрения или внешних действий |

## 5. Ограничения и non-negotiables

| Область | Ограничение / non-negotiable | Статус | Комментарий |
|---|---|---|---|
| Время | Pilot должен оставаться маленьким и reviewable | Green | Нет обязательства по дате |
| Бюджет | Нет платных сервисов или покупок | Green | API вне scope |
| Capacity | Лёгкая работа владельца | Yellow | Доступность времени неизвестна |
| Compliance / policy | Только Green synthetic data | Green | Без реальных или регулируемых данных |
| Technology | Только Markdown и local Git repository | Green | Без deployment |
| Data | Нет secrets, tokens или персональных данных | Green | Только Green |

## 6. Evidence inventory

| Утверждение или вводные | Источник | Актуальность | Уверенность | Классификация | Комментарий |
|---|---|---|---|---|---|
| Engineering Governor Rules существуют | Артефакты repository | 2026-09-20 | Fact | Green | Четыре workspace rules |
| Frigga Skill существует | Артефакт repository | 2026-09-20 | Fact | Green | `SKILL.md` закоммичен |
| Reference templates существуют | Артефакты repository | 2026-09-20 | Fact | Green | Четыре template-файла |
| Pilot повысит безопасность до API integration | Governance hypothesis | 2026-09-20 | Assumption | Green | Нужен review |
| Local dashboard будет полезен | User need hypothesis | 2026-09-20 | Assumption | Green | Не проверяется этим pilot |

## 7. Initial delivery outline

| Этап / milestone | Ожидаемый результат | Owner | Dependencies | Триггер | Статус |
|---|---|---|---|---|---|
| Frame pilot | Approved или revised Baseline 0 | Владелец repository | Review артефактов | Gate 1 decision | Green |
| Plan pilot | Level 1 outline | Владелец repository | Gate 1 approval | После Gate 1 | Uncertain |
| Review pilot | Закрытие или revision pilot | Владелец repository | Evidence от использования артефактов | После Level 1 | Uncertain |

## 8. Initial RAID-ED summary

| Тип | Описание | Owner | Статус | Следующее действие |
|---|---|---|---|---|
| Assumption | Markdown-артефактов достаточно для проверки pilot | Владелец repository | Yellow | Проверить в ходе Gate 1 review |
| Risk | Scope pilot может преждевременно расшириться до implementation | Владелец repository | Yellow | Сохранять явную границу вне scope |
| Dependency | Review владельца и Gate 1 decision | Владелец repository | Yellow | Рассмотреть decision pack |
| Evidence gap | Пока нет evidence о нужных полях control desk | Владелец repository | Yellow | Зафиксировать feedback при review |
| Decision | Утвердить framing pilot, принять Activity-модель как future design principle и разрешить только Level 1 Markdown-only planning | Владелец repository | Yellow | Принять решение в обновлённом Gate 1 pack |
| Assumption | Контекстные Activities сделают workflow понятнее и безопаснее | Владелец repository | Yellow | Проверить в ходе Gate 1 review |

## 9. Открытые вопросы и решения

| Пункт | Тип | Owner | Нужное решение / evidence | Триггер | Статус |
|---|---|---|---|---|---|
| Достаточно ли framing pilot? | Decision | Владелец repository | Approve, revise или reject Gate 1 pack | Gate 1 review | Open |
| Какие поля control desk наиболее важны? | Evidence gap | Владелец repository | Feedback владельца | До Level 1 outline | Open |
| Нужен ли local UI после pilot? | Decision | Владелец repository | Отдельное post-pilot решение | Gate 4 или позже | Deferred |

## 10. Gate request

- **Текущий Gate:** Gate 1 — Формирование
- **Запрашиваемое решение:** Утвердить Draft Baseline 0 с дополнением:
  контекстная Activity-модель принимается как future design principle; разрешить подготовку только Level 1 Markdown-only delivery outline.
- **Рекомендация:** Утвердить при условиях: pilot остаётся Green-only и Markdown-only; Activity-модель принимается только как future design principle; не создаются UI, API integration, MCP, cloud, automation, deployment или owner profile.
- **Evidence для рекомендации:** Rules, Skill и templates уже закоммичены;
  предлагаемый pilot использует только synthetic Markdown artifacts.
- **Риски одобрения:** Небольшой риск scope drift в сторону implementation.
- **Риски задержки или отклонения:** Отсутствует проверка governance workflow
  до возможной интеграции модели.
- **Требуется approval от:** Владелец repository
- **Действие после approval:** Создать только компактный Level 1 Markdown-only milestone outline, обновить RAID-ED register и собрать owner feedback.