| Capability                   | Продукт / сервис           | Владелец         | Внешняя зависимость                |
| ---------------------------- | -------------------------- | ---------------- | ---------------------------------- |
| 1.1 Catalog & Search         | Catalog Service            | Platform Team    | AWS OpenSearch / managed search    |
| 1.2 Product Content          | Content Service            | Platform Team    | S3-compatible object storage       |
| 1.3 Personalization          | Recommendation Service     | Growth Team      | Third-party recommendation engine  |
| 2.1 Cart & Checkout          | Checkout Service           | Commerce Team    | PSP adapter                        |
| 2.2 Orders                   | Order Service              | Commerce Team    | Payment adapter, delivery adapter  |
| 2.3 Returns & Refunds        | Returns Service            | Commerce Team    | PSP refund API                     |
| 3.1 Payment Processing       | Payment Orchestrator       | Payments Team    | Flutterwave / Paystack / M-Pesa    |
| 3.2 Payment Methods          | Payment Method Registry    | Payments Team    | PSP-specific methods               |
| 3.3 Refunds                  | Refund Service             | Payments Team    | PSP refund API                     |
| 3.4 Fraud Prevention         | Fraud Service              | Risk Team        | Third-party anti-fraud provider    |
| 4.1 Delivery Management      | Delivery Service           | Fulfillment Team | Sendbox / Sendy                    |
| 4.2 Courier Integration      | Courier Adapter            | Fulfillment Team | Sendbox / Sendy                    |
| 4.3 Tracking                 | Tracking Service           | Fulfillment Team | Courier webhooks                   |
| 4.4 Returns Logistics        | Returns Logistics Service  | Fulfillment Team | Courier reverse logistics          |
| 5.1 Seller Onboarding        | Seller Onboarding Service  | Seller Team      | KYC provider                       |
| 5.2 Seller Catalog           | Seller Catalog Service     | Seller Team      | Catalog Service                    |
| 5.3 Seller Payouts           | Payout Service             | Payments Team    | PSP / payment orchestration        |
| 5.4 Seller Performance       | Seller Performance Service | Seller Team      | Analytics Service                  |
| 6.1 Authentication           | Identity Provider          | Platform Team    | Auth0 / Firebase Auth / Cognito    |
| 6.2 Authorization            | Authorization Service      | Platform Team    | Internal RBAC                      |
| 6.3 KYC / Verification       | KYC Service                | Compliance Team  | KYC provider                       |
| 6.4 Fraud & Abuse Prevention | Abuse Prevention Service   | Risk Team        | Third-party anti-fraud provider    |
| 7.1 Event Collection         | Event Pipeline             | Data Team        | Kafka / managed queue              |
| 7.2 Product Analytics        | Product Analytics          | Data Team        | Amplitude / Mixpanel / PostHog     |
| 7.3 Business Reporting       | Reporting Service          | Data Team        | BI tool                            |
| 7.4 Consent Management       | Consent Service            | Compliance Team  | Consent storage, legal rules       |
| 8.1 Cloud Infrastructure     | Cloud Platform             | Platform Team    | AWS af-south-1, regional providers |
| 8.2 Observability            | Observability Stack        | Platform Team    | OpenTelemetry, Prometheus, Loki    |
| 8.3 Security                 | Security Services          | Security Team    | WAF, IAM, secrets management       |
| 8.4 CI/CD                    | CI/CD Pipeline             | Platform Team    | GitHub Actions / GitLab CI         |
| 8.5 Data Residency           | Data Residency Service     | Platform Team    | Regional data zones                |
| 9.1 Acquisition              | Acquisition Stack          | Growth Team      | Ads platforms, attribution tools   |
| 9.2 CRM & Messaging          | CRM / Messaging Service    | Growth Team      | WhatsApp Business API, SMS gateway |
| 9.3 Campaign Management      | Campaign Service           | Growth Team      | CRM, consent service               |
| 9.4 Referral & Loyalty       | Loyalty Service            | Growth Team      | Internal rules engine              |