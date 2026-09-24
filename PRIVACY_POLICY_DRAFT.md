# Order Pipe privacy policy — DRAFT, NOT FOR PUBLIC LISTING

This draft describes the application as implemented. It is not an approved legal notice and must not be entered in the Shopify App Store listing until the operator details below, backup practices, subprocessors, and applicable legal obligations are confirmed.

**Operator:** [CONFIRMED_LEGAL_OPERATOR_NAME]  
**Jurisdiction:** [CONFIRMED_JURISDICTION]  
**Privacy and support contact:** [VERIFIED_PUBLIC_SUPPORT_EMAIL]  
**Effective date:** [APPROVED_EFFECTIVE_DATE]

## What the app handles

When a merchant installs Order Pipe, the app receives Shopify installation credentials and reads orders and the line-item, financial, shipping, cancellation, and limited refund information needed for the merchant's configured export. An order can contain personal information, including a customer's name, contact details, and shipping address. Order and shop identifiers are not anonymous data. The app also stores destination configuration and encrypted connection secrets; export payloads, delivery status and error metadata; and the minimum usage, billing, security, and audit records needed to operate the service.

The merchant selects each destination and chooses whether to activate it. SFTP exports can include approved shipping or contact fields required by the merchant's receiver contract. BigQuery, Snowflake, Databricks, and Prismatic exports exclude names, street addresses, email addresses, and phone numbers by default, but order identifiers and other fields can still be personal data. Connection and delivery tests use synthetic orders and isolated targets.

## Why and where data is used

Order Pipe uses this information to connect to Shopify, prepare and deliver the merchant's selected order exports, reconcile missed updates, display delivery history, investigate failures, enforce plan allowances, respond to support and privacy requests, and protect the service. Production order records are sent only to the destinations the merchant has configured and activated. These destinations are controlled by the merchant and can have their own data-processing and retention terms. Order Pipe does not claim that endpoint acceptance proves downstream processing.

Service providers used for hosting, database, email alerts, and operational security may process limited data on the operator's behalf. The actual provider list, locations, and contractual terms must be verified before this draft is published. No data is sold through Order Pipe.

## Retention and deletion

Replayable payloads are retained for up to 14 days. Operational delivery metadata is retained for up to 90 days. Minimal billing and security records may be kept longer only as required for a documented operational or legal purpose; the exact periods must be approved before publication. Expiry of a replay payload means the original bytes can no longer be replayed.

An app uninstall or loss of Shopify access stops new exports. The app deletes its destination credentials and pending personal payloads under its lifecycle process. Shopify privacy requests are handled through the applicable `customers/data_request`, `customers/redact`, and `shop/redact` webhooks. Erasure protections prevent locally deleted customer data from reappearing through queued work or reconciliation. A copy already delivered to a merchant-controlled destination is subject to the merchant's downstream retention and deletion controls; Order Pipe does not delete unrelated merchant data or claim remote erasure after access is revoked. Backup-retention and restoration controls must be verified before final publication.

## Security and privacy requests

Shopify tokens and destination secrets are encrypted at rest. The application limits access by shop and excludes credentials and full order payloads from application logs. Network connections use TLS where applicable; SFTP connections verify the server host key. No system is risk-free, and this notice does not promise absolute security or uninterrupted delivery.

Merchants and affected customers can make an access or deletion request through Shopify's privacy process or contact [VERIFIED_PUBLIC_SUPPORT_EMAIL]. The operator will verify the request and coordinate with the merchant when the destination is under the merchant's control. This notice may be updated when practices change; the effective date above will identify the approved version.
