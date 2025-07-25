# 🚀 Roadmap разработки платформы оценки сотрудников

---

## Релиз 1 — MVP (минимально жизнеспособный продукт)

**Цель:** Запуск базового функционала для сбора самооценки и постановки целей.

### Приоритет: Высокий

| Эпик                                              | Основные задачи                                  | Зависимости                                                       | Сроки (спринты)                |
| ------------------------------------------------- | ------------------------------------------------ | ----------------------------------------------------------------- | ------------------------------ |
| [[E1 Самооценка и сбор данных от сотрудников]]    | - Интерфейс анкеты с разделами                   | Нет                                                               | [[S1 - MVP.1]], [[S2 - MVP.2]] |
|                                                   | - Сохранение черновиков и отправка анкеты        |                                                                   |                                |
|                                                   | - Просмотр истории оценок                        |                                                                   |                                |
|                                                   | - Brag-документ (создание/редактирование)        |                                                                   |                                |
|                                                   | - Импорт из Brag-документа                       |                                                                   |                                |
|                                                   | - Обновление прогресса по целям                  |                                                                   |                                |
| [[E2 Управление целями и их утверждение]]         | - Создание целей менеджером                      | [[E1 Самооценка и сбор данных от сотрудников\|Epic 1]] (завершён) | [[S3 - MVP.3]]                 |
|                                                   | - Статусы целей (draft, submitted)               |                                                                   |                                |
|                                                   | - Отправка целей на утверждение                  |                                                                   |                                |
| [[E6 Аутентификация, авторизация и безопасность]] | - Базовая регистрация, авторизация пользователей | Нет                                                               | [[S1 - MVP.1]]                 |
|                                                   | - Роли и права доступа                           |                                                                   |                                |

---

## Релиз 2 — Управление и утверждение целей, комментарии

**Цель:** Добавить функционал для менеджеров и старших менеджеров.

### Приоритет: Высокий

| Эпик                                      | Основные задачи                                             | Зависимости                                                                                                         | Сроки (спринты) |
| ----------------------------------------- | ----------------------------------------------------------- | ------------------------------------------------------------------------------------------------------------------- | --------------- |
| [[E2 Управление целями и их утверждение]] | - Интерфейс утверждения/отклонения целей старшим менеджером | [[E1 Самооценка и сбор данных от сотрудников\|Epic 1]], [[E2 Управление целями и их утверждение\|Epic 2]] (Релиз 1) | [[S4 - MVP.4]]  |
| [[E3 Обзор, комментарии и 1-1 встречи]]   | - Просмотр анкет сотрудника для менеджера                   | [[E1 Самооценка и сбор данных от сотрудников\|Epic 1]]                                                              | [[S4 - MVP.4]]  |
|                                           | - Комментарии (публичные и приватные)                       |                                                                                                                     |                 |
|                                           | - Функционал 1:1 встреч                                     |                                                                                                                     |                 |

---

## Релиз 3 — Отчёты и сводки, расширенный функционал HR

**Цель:** Дать HR и менеджерам мощные инструменты для анализа и управления.

### Приоритет: Средний

| Эпик                                                | Основные задачи                                   | Зависимости                                                                                             | Сроки (спринты)                |
| --------------------------------------------------- | ------------------------------------------------- | ------------------------------------------------------------------------------------------------------- | ------------------------------ |
| [[E4 Командные сводки и отчёты]]                    | - Генерация сводок и отчётов по команде и отделам | [[E1 Самооценка и сбор данных от сотрудников\|Epic 1]], [[E3 Обзор, комментарии и 1-1 встречи\|Epic 3]] | [[S5 - MVP.5]], [[S6 - MVP.6]] |
|                                                     | - Визуализация, фильтры, экспорт                  |                                                                                                         |                                |
| [[E5 Настройка и управление процессом оценки (HR)]] | - Управление периодами и шаблонами анкет          | [[E1 Самооценка и сбор данных от сотрудников\|Epic 1]]                                                  | [[S5 - MVP.5]], [[S6 - MVP.6]] |
|                                                     | - Управление иерархией и зонами ответственности   |                                                                                                         |                                |
|                                                     | - Мониторинг статусов и напоминания               |                                                                                                         |                                |

---

## Релиз 4 — Улучшения и масштабирование

**Цель:** Оптимизация, интеграции и безопасность.

### Приоритет: Низкий / по необходимости

| Эпик                                              | Основные задачи                               | Зависимости                                        | Сроки (спринты) |
| ------------------------------------------------- | --------------------------------------------- | -------------------------------------------------- | --------------- |
| [[E6 Аутентификация, авторизация и безопасность]] | - Интеграция с корпоративным SSO (OAuth/SAML) | [[E1 Самооценка и сбор данных от сотрудников\|E1]] | [[S7 - MVP.7]]  |
|                                                   | - Аудит-лог действий                          |                                                    |                 |
|                                                   | - Шифрование данных                           |                                                    |                 |
| Вся платформа                                     | - Оптимизация UX/UI                           | Весь проект                                        | Постоянно       |
|                                                   | - Масштабирование и нагрузочное тестирование  |                                                    |                 |

---

# Общие заметки:

- Каждый релиз разбивается на спринты (2-3 недели).
    
- После каждого релиза — тестирование и приёмка.
    
- Внедрение CI/CD и автоматических тестов — с первого релиза.
    
- Возможны параллельные задачи по фронтенду и бэкенду.