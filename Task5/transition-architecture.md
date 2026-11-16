Ограничение по ресурсам:
| Роль                  | Количество |
| --------------------- | ---------- |
| Backend Engineer      | 2          |
| Frontend Engineer     | 1          |
| Mobile Engineer       | 1          |
| DevOps / SRE          | 1          |
| QA                    | 1          |
| Итого                 | 6          |

Состояние сейчас
| Область        | Состояние                                                             |
| -------------- | --------------------------------------------------------------------- |
| Архитектура    | Утверждены ADR № 1–3, C4-диаграммы, Capability Map, Value Stream      |
| Data residency | Принята гибридная модель с regional data zones                        |
| Cloud          | Выбран AWS af-south-1 для Shared Control Plane                        |
| Payments       | Выбрана гибридная модель PSP по странам                               |
| Observability  | Определён baseline: OpenTelemetry, Prometheus, Loki, Jaeger           |
| Security       | Определены базовые контроли: IAM, encryption, RBAC, audit             |
| CI/CD          | Определён подход IaC + GitHub Actions / GitLab CI                     |
| Команда        | Сформирована базовая команда CTO, architect, engineers, DevOps, QA |
| Бюджет         | Установлен потолок $5 000 / месяц на regular tech spend               |

Что меняется 
Ключевые изменения:
1. фиксируется архитектурный стиль;
2. фиксируется стратегия размещения данных;
3. фиксируется стратегия кеширования;
4. фиксируется выбор cloud region;
5. фиксируется выбор PSP;
6. фиксируются НФТ и FMA;
7. создаются Nigerian и Kenyan Data Zones;
8. создаётся Shared Control Plane;
9. настраивается CI/CD и observability.

Состояние MVP 
Команда - 6 человек
Распределение работ
| Исполнитель           | Основная зона                    | Что делает                                                       |
| --------------------- | -------------------------------- | ---------------------------------------------------------------- |
| Tech Lead / Architect | Архитектура и integration design | ADR, C4, data residency, PSP/courier adapter design, code review |
| Backend Engineer 1    | Commerce core                    | Catalog, search, cart, checkout, orders, pricing                 |
| Backend Engineer 2    | Integrations и platform          | PSP adapter, courier adapter, auth, RBAC, queues                 |
| Frontend Engineer     | Web                              | Customer web, seller web, admin panel                            |
| Mobile Engineer       | Mobile                           | Customer app, seller app                                         |
| DevOps / SRE          | Infrastructure и observability   | IaC, CI/CD, monitoring, alerting, security baseline              |
| QA                    | Quality и release readiness       | Test plan, automated tests, regression, release gate             | 

Что появляется в MVP
| Область             | Что появляется                     |
| ------------------- | ---------------------------------- |
| Customer Experience | Catalog, search, product content   |
| Commerce            | Cart, checkout, orders             |
| Payments            | PSP integration, payment status    |
| Fulfillment         | Delivery creation, tracking        |
| Seller Management   | Seller onboarding, seller catalog  |
| Identity            | Auth, basic RBAC                   |
| Data & Analytics    | Basic events, consent management   |
| Platform            | IaC, monitoring, security baseline |
| Data Residency      | Regional isolation                 |

Что меняется относительно "Сейчас"
| Область        | Было                  | Стало                          |
| -------------- | --------------------- | ------------------------------ |
| Архитектура    | Документирована       | Реализована                    |
| Data residency | Определена            | Внедрена                       |
| Cloud          | Выбран                | Развёрнут                      |
| Payments       | Выбраны PSP           | Интегрированы                  |
| Observability  | Определён baseline    | Работает в prod                |
| Security       | Определены контроли   | Внедрены                       |
| CI/CD          | Настроен              | Используется для всех сервисов |
| Команда        | Базовая               | 6 человек         |
| Бюджет         | $1 350–$2 950 / месяц | $3 600–$5 000 / месяц          |

Что откладывается 
| Область                   | Что откладывается          | Причина                        |
| ------------------------- | -------------------------- | ------------------------------ |
| Personalization           | Рекомендации               | Не критично                    |
| Advanced Analytics        | Real-time analytics, ML    | Нет ресурсов                   |
| Advanced Fraud            | Сложные fraud models       | PSP даёт базовую защиту        |
| Advanced KYC              | Полный KYC                 | Partner flow                   |
| Multi-carrier routing     | Несколько courier          | Один провайдер на страну       |
| Advanced Seller Lifecycle | Performance, payouts       | Не блокирует первую транзакцию |
| Advanced Campaigns        | Сложные campaign journeys  | Нет consent и ресурсов         |
| Referral & Loyalty        | Рефералы, бонусы           | Не MVP                         |
| Returns & Refunds         | Полный cycle возвратов     | После запуска                  |
| Advanced Reporting        | BI, сложные дашборды       | Достаточно базовых метрик      |
| Advanced Observability    | Полный SRE-стек            | Достаточно базовых alerting    |
| Multi-region DR           | Active-active              | Не MVP                         |
| Multi-cloud               | Второй cloud               | Не MVP                         |
| On-premises               | Собственная инфраструктура | Не MVP                         |

Приоритизация 29 пожеланий PM 
| №  | Функция| Решение| Приоритет| Обоснование|
| 1  | Каталог товаров, неограниченное число категорий, неограниченные атрибуты на категорию    | MVP| Must-have   | Базовая функция маркетплейса|
| 2  | Полнотекстовый поиск с исправлением опечаток на пяти языках| Phase 2| Should-have | Для MVP достаточно базового поиска|
| 3  | Голосовой поиск на суахили и хауса| Отложено| Could-have  | Не критично для первой транзакции|
| 4  | ИИ-рекомендации — «покупатели вроде вас также покупали»| Отложено| Could-have  | Требует данных и ML|
| 5  | Live-стримы с покупкой и живым чатом| Отложено| Could-have  | Сложная функция, не MVP|
| 6  | Чат покупателя с продавцом с автопереводом| Отложено| Could-have  | Можно заменить поддержкой|
| 7  | Оценки и отзывы с фото и видео| Phase 2| Should-have | Не блокирует первую транзакцию|
| 8  | Онбординг продавца через WhatsApp без веб-формы| MVP| Must-have   | Снижает барьер входа продавца|
| 9  | Онбординг продавца через USSD| Phase 2| Should-have | Нужен для offline-сегмента|
| 10 | Кабинет продавца с аналитикой, когортами и прогнозом остатков| Phase 2| Should-have | Для MVP достаточно базового кабинета|
| 11 | Оплата: M-Pesa, Flutterwave, Paystack, карта, банковский перевод, наличные при получении | MVP частично| Must-have   | M-Pesa + Flutterwave; Paystack и COD — Phase 2|
| 12 | Рассрочка на 4 платежа с собственным скорингом| Отложено| Could-have  | Высокий compliance и credit risk|
| 13 | Мультивалютный кошелёк с переводами| Отложено| Could-have  | Высокий regulatory risk|
| 14 | Программа лояльности на криптотокенах| Исключено до legal approval | Blocked| Высокий regulatory risk|
| 15 | «Колесо фортуны» и награды за заходы| Отложено| Could-have  | Growth, не MVP|
| 16 | Флеш-распродажи с таймерами и резервированием| Phase 2| Should-have | Требует inventory logic|
| 17 | Динамическое ценообразование по ценам Jumia| Исключено| Blocked| Парсинг конкурента — legal / ToS risk|
| 18 | Отслеживание заказа, живая карта курьера, ETA до минуты| MVP частично| Must-have   | Базовый tracking; live map и ETA до минуты — Phase 2 |
| 19 | Доставка в ПВЗ с видеофиксацией| Отложено| Could-have  | Требует partner capability|
| 20 | Возвраты и рефанды, 30 дней, мгновенный возврат| Phase 2| Should-have | Не блокирует первую транзакцию|
| 21 | ML-антифрод по заказам, аккаунтам и возвратам| Phase 2| Should-have | Для MVP достаточно правил и PSP anti-fraud|
| 22 | B2B-режим: опт, счета, отсрочка| Отложено| Could-have  | Отдельный бизнес-процесс|
| 23 | Партнёрская и реферальная программа| Phase 3| Could-have  | Growth, не MVP|
| 24 | Офлайн-заказ через USSD и SMS| Phase 2| Should-have | Важный канал, но не блокирует запуск|
| 25 | PWA + нативные iOS и Android с полным паритетом| MVP частично| Must-have   | Web + Android; iOS — Phase 2|
| 26 | Админ-бэк-офис: модерация, KYC, споры, возвраты, контент| MVP частично| Must-have   | Модерация и контент; KYC/споры/возвраты — Phase 2    |
| 27 | Публичный GraphQL API| Phase 3| Could-have  | Не нужен для запуска|
| 28 | Дашборд для руководства в реальном времени| MVP| Must-have   | Прямая просьба инвестора|
| 29 | Тёмная тема| Отложено| Could-have  | Не влияет на core flow|

Состояние через 12 месяцев
Что меняется 
| Область           | MVP                                  | Через 12 месяцев                                        |
| ----------------- | ------------------------------------ | ------------------------------------------------------- |
| Архитектура       | Modular monolith                     | Modular monolith + выделенные services по необходимости |
| Data residency    | Regional data zones                  | Зрелая data governance, automated classification        |
| Cloud             | Один primary region + regional zones | Multi-region readiness, DR, cost optimization           |
| Payments          | PSP adapters                         | Payment orchestration, advanced fraud, reconciliation   |
| Fulfillment       | Courier adapters                     | Multi-carrier routing, SLA management                   |
| Seller Management | Basic onboarding                     | Advanced seller lifecycle, performance, payouts         |
| Identity & Trust  | Basic KYC                            | Advanced KYC, risk scoring, fraud prevention            |
| Data & Analytics  | Basic events                         | Real-time analytics, ML-ready data platform             |
| Platform          | IaC, observability                   | Full SRE practices, FinOps, automated compliance        |
| Growth            | Basic campaigns                      | Advanced growth loops, retention, loyalty               |
