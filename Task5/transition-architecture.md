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
| Команда        | Сформирована базовая команда CTO, architect, engineers, DevOps, legal |
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
| Область             | Что появляется                                          |
| ------------------- | ------------------------------------------------------- |
| Customer Experience | Catalog, search, product content, web и mobile apps     |
| Commerce            | Cart, checkout, orders, pricing, promotions             |
| Payments            | Payment Orchestrator, PSP adapters, refunds             |
| Fulfillment         | Delivery management, courier adapters, tracking         |
| Seller Management   | Seller onboarding, seller catalog, payouts              |
| Identity & Trust    | Authentication, authorization, KYC                      |
| Data & Analytics    | Event collection, product analytics, consent management |
| Platform            | IaC, observability, security, data residency            |
| Growth              | Acquisition, CRM, campaigns                             |

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
| Команда        | Базовая               | Расширена до 19–21 человека    |
| Бюджет         | $1 350–$2 950 / месяц | $3 600–$7 600 / месяц          |

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
