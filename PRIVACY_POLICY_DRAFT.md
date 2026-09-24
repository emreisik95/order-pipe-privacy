# Order Pipe privacy policy — DRAFT, NOT FOR PUBLIC LISTING

This draft describes the application as implemented. It is not an approved legal notice and must not be entered in the Shopify App Store listing until the remaining operational facts, subprocessors, international transfers, and applicable legal obligations are confirmed and the operator approves the final text.

- **Operator:** PIXEL GOBLIN LTD, company number 17201045 ([Companies House record](https://find-and-update.company-information.service.gov.uk/company/17201045))
- **Registered office:** 66 Paul Street, London, EC2A 4NA, United Kingdom (confirm this is also the intended privacy correspondence address)
- **Jurisdiction:** United Kingdom
- **Privacy and support contact supplied by operator:** support@pixelgoblin.link (inbound delivery not yet independently tested)
- **Effective date:** Not assigned; this is an unapproved draft.

## What the app handles

When a merchant installs Order Pipe, the app receives Shopify installation credentials and reads orders and the line-item, financial, shipping, cancellation, and limited refund information needed for the merchant's configured export. An order can contain personal information, including a customer's name, contact details, and shipping address. Order and shop identifiers are not anonymous data. The app also stores destination configuration and encrypted connection secrets; export payloads, delivery status and error metadata; and the minimum usage, billing, security, and audit records needed to operate the service.

The merchant selects each destination and chooses whether to activate it. SFTP exports can include approved shipping or contact fields required by the merchant's receiver contract. BigQuery, Snowflake, Databricks, and Prismatic exports exclude names, street addresses, email addresses, and phone numbers by default, but order identifiers and other fields can still be personal data. Connection and delivery tests use synthetic orders and isolated targets.

## Why and where data is used

Order Pipe uses this information to connect to Shopify, prepare and deliver the merchant's selected order exports, reconcile missed updates, display delivery history, investigate failures, enforce plan allowances, respond to support and privacy requests, and protect the service. Production order records are sent only to the destinations the merchant has configured and activated. These destinations are controlled by the merchant and can have their own data-processing and retention terms. Order Pipe does not claim that endpoint acceptance proves downstream processing.

Service providers used for hosting, database, email alerts, and operational security may process limited data on the operator's behalf. The actual provider list, processing locations, international transfer safeguards, and contractual terms must be verified before this draft is published. No data is sold through Order Pipe.

## Retention and deletion

Replayable payloads are retained for up to 14 days. Operational delivery metadata is retained for up to 90 days. Minimal billing and security records may be kept longer only as required for a documented operational or legal purpose; the exact periods must be approved before publication. Expiry of a replay payload means the original bytes can no longer be replayed.

An app uninstall or loss of Shopify access stops new exports. The app deletes its destination credentials and pending personal payloads under its lifecycle process. Shopify privacy requests are handled through the applicable `customers/data_request`, `customers/redact`, and `shop/redact` webhooks. Erasure protections prevent locally deleted customer data from reappearing through queued work or reconciliation. A copy already delivered to a merchant-controlled destination is subject to the merchant's downstream retention and deletion controls; Order Pipe does not delete unrelated merchant data or claim remote erasure after access is revoked. Backup-retention and restoration controls must be verified before final publication.

## Security and privacy requests

Shopify tokens and destination secrets are encrypted at rest. The application limits access by shop and excludes credentials and full order payloads from application logs. Network connections use TLS where applicable; SFTP connections verify the server host key. No system is risk-free, and this notice does not promise absolute security or uninterrupted delivery.

Merchants and affected customers can make an access or deletion request through Shopify's privacy process or contact support@pixelgoblin.link. The operator will verify the request and coordinate with the merchant when the destination is under the merchant's control. This notice may be updated when practices change; the effective date above will identify the approved version.

## Before this can become the published policy

- Verify that the support mailbox receives and can answer an external test message, and approve the registered-office address for privacy correspondence.
- Record the actual hosting, database, backup, email, and monitoring providers; their processing locations; and any international transfer mechanism.
- Approve the retention period for billing/security/audit records and for encrypted backups, including how erasures propagate to restored copies.
- Determine and document PIXEL GOBLIN LTD's role for merchant-directed order exports versus its own billing/support/security data, the applicable lawful bases, and the rights and complaint information required by the [ICO privacy-information checklist](https://ico.org.uk/for-organisations/uk-gdpr-guidance-and-resources/individual-rights/the-right-to-be-informed/checklists/).
- Approve the final wording and effective date. Only then remove the DRAFT label and use the resulting public URL in Shopify's listing and `PRIVACY_POLICY_URL`.
