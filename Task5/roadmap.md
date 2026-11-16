Контрольные точки 
| Контрольная точка | Дата        | Цель                                                | Статус      |
| ----------------- | ----------- | --------------------------------------------------- | ----------- |
| 1              | 1 сентября  | Зафиксирована архитектура.                          | Планируется |
| 2              | 15 сентября | Готов core MVP: catalog, orders, checkout, payments | Планируется |
| 3              | 1 октября   | Готовы integrations, data residency и observability | Планируется |
| 4              | 15 октября  | Запуск в Нигерии и Кении                            | Планируется |

1 - Архитектура

Scope
1. Утверждена Architecture Vision.
2. Утверждён ADR № 1 «Выбор архитектурного стиля».
3. Утверждён ADR № 2 «Стратегия кеширования».
4. Утверждён ADR № 3 «Стратегия размещения данных».
5. Утверждён C4 Context / Container / Deployment Diagrams.
6. Утверждён реестр НФТ.
7. Утверждён FMA.
8. Утверждён Capability Map.
9. Утверждён Value Stream.
10. Утверждён план отказоустойчивости и переключения.
11. Созданы Nigerian Data Zone и Kenyan Data Zone.
12. Настроен Shared Control Plane в AWS af-south-1.
13. Настроен CI/CD и IaC.
14. Настроен observability baseline.
15. Получены предварительные ответы от внешнего юриста по data residency и cross-border transfer.

Команда
| Роль               | Количество |
| ------------------ | ---------- |
| CTO                | 1          |
| Solution Architect | 1          |
| Backend Engineer   | 2          |
| Frontend Engineer  | 1          |
| DevOps / SRE       | 1          |
| QA                 | 1          |
| Mobile Engineer    | 1          |


Инфраструктурная стоимость
| Статья                       | Оценка                |
| ---------------------------- | --------------------- |
| AWS af-south-1 control plane | $300–$600 / месяц     |
| Nigerian Data Zone           | $400–$800 / месяц     |
| Kenyan Data Zone             | $400–$800 / месяц     |
| Observability                | $100–$300 / месяц     |
| CI/CD                        | $50–$150 / месяц      |
| Security services            | $100–$300 / месяц     |
| Итого                        | $1 350–$2 950 / месяц |

2 - Core MVP
Scope
1. Catalog & Search.
2. Product Content.
3. Cart & Checkout.
4. Orders.
5. Pricing & Promotions.
6. Payment Orchestrator.
7. Payment Methods.
8. Seller Onboarding.
9. Seller Catalog.
10. Authentication.
11. Authorization.
12. Event Collection.
13. Consent Management.
14. Базовый admin panel.
15. Базовый seller dashboard.
16. Базовый customer web app.
17. Базовый mobile app.
18. Интеграция с PSP в Нигерии и Кении.
19. Интеграция с courier в Нигерии и Кении.

Команда
| Роль               | Количество |
| ------------------ | ---------- |
| CTO                | 1          |
| Solution Architect | 1          |
| Backend Engineer   | 2          |
| Frontend Engineer  | 1          |
| DevOps / SRE       | 1          |
| QA                 | 1          |
| Mobile Engineer    | 1          |

Инфраструктурная стоимость
| Статья                       | Оценка                |
| ---------------------------- | --------------------- |
| AWS af-south-1 control plane | $400–$800 / месяц     |
| Nigerian Data Zone           | $600–$1 200 / месяц   |
| Kenyan Data Zone             | $600–$1 200 / месяц   |
| Observability                | $200–$500 / месяц     |
| CI/CD                        | $100–$250 / месяц     |
| Security services            | $200–$500 / месяц     |
| Итого                        | $2 100–$4 450 / месяц |

3 - Integrations и data residency
Scope
1. Payment adapter для Flutterwave / Paystack.
2. Payment adapter для M-Pesa.
3. Delivery adapter для Sendbox.
4. Delivery adapter для Sendy.
5. WhatsApp Business API integration.
6. SMS / USSD integration.
7. KYC integration.
8. PII scrubbing в logs и traces.
9. Pseudonymization для analytics.
10. Cross-border transfer gate.
11. Country launch gate.
12. Consent management.
13. Data retention policy.
14. RBAC и audit logging.
15. Load testing.
16. Chaos testing.
17. Runbooks по отказоустойчивости.
18. Security review.
19. Legal review по data residency.

Команда 
| Роль               | Количество |
| ------------------ | ---------- |
| CTO                | 1          |
| Solution Architect | 1          |
| Backend Engineer   | 2          |
| Frontend Engineer  | 1          |
| DevOps / SRE       | 1          |
| Mobile Engineer    | 1          |
| QA                 | 1          |

Инфраструктурная стоимость

| Статья                       | Оценка                |
| ---------------------------- | --------------------- |
| AWS af-south-1 control plane | $500–$800 / месяц   |
| Nigerian Data Zone           | $800–$1 200 / месяц   |
| Kenyan Data Zone             | $800–$1 200 / месяц   |
| Observability                | $300–$600 / месяц     |
| CI/CD                        | $150–$300 / месяц     |
| Security services            | $300–$600 / месяц     |
| Итого                        | $2 850–$4 700 / месяц |

4 - запуск
Scope
1. Продакшн-развёртывание Nigerian Data Zone.
2. Продакшн-развёртывание Kenyan Data Zone.
3. Продакшн-развёртывание Shared Control Plane.
4. Включение CDN.
5. Включение observability.
6. Включение alerting.
7. Включение on-call.
8. Включение payment flows.
9. Включение delivery flows.
10. Включение seller flows.
11. Включение consent management.
12. Включение analytics.
13. Включение reporting.
14. Launch readiness review.
15. Go / No-Go decision.
16. Post-launch monitoring.

Команда
| Роль               | Количество |
| ------------------ | ---------- |
| CTO                | 1          |
| Solution Architect | 1          |
| Backend Engineer   | 2          |
| Frontend Engineer  | 1          |
| DevOps / SRE       | 1          |
| QA                 | 1          |
| Mobile Engineer    | 1          |



Инфраструктурная стоимость
| Статья                       | Оценка                |
| ---------------------------- | --------------------- |
| AWS af-south-1 control plane | $600–$1 000 / месяц   |
| Nigerian Data Zone           | $1 000–$1 200 / месяц |
| Kenyan Data Zone             | $1 000–$1 200 / месяц |
| Observability                | $400–$600 / месяц   |
| CI/CD                        | $200–$400 / месяц     |
| Security services            | $400–$600 / месяц   |
| Итого                        | $3 600–$5 000 / месяц |