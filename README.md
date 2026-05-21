<!-- PORTFOLIO DISPLAY — Editable by repository owner (odoo00) only -->

<div align="center">

# Mohsen Sayed Hassan

### Senior Odoo Developer · Technical Team Leader

📱 **+20 127 752 3059**  
📧 [dev.odooerp@gmail.com](mailto:dev.odooerp@gmail.com)  
💼 [LinkedIn](https://www.linkedin.com/in/mohsen-sayed-hassan-12856a2a7/) · 🐙 [GitHub](https://github.com/odoo00)

**Odoo 9 → 19** · 9+ years · Egypt · Saudi Arabia · Iraq · **70+ ERP implementations**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-Profile-0A66C2?style=flat-square&logo=linkedin)](https://www.linkedin.com/in/mohsen-sayed-hassan-12856a2a7/)
[![Email](https://img.shields.io/badge/Email-Contact-EA4335?style=flat-square&logo=gmail)](mailto:dev.odooerp@gmail.com)
[![Odoo](https://img.shields.io/badge/Odoo-9→19-714B67?style=flat-square)](https://github.com/odoo00)

</div>

 

## 👋 About

Technical Team Leader and Senior Odoo Developer at **CTIT Software** (Jeddah). I deliver full-cycle ERP: requirements, architecture, development, integrations, deployment, and production support — with strong **automation**, **JavaScript/OWL** front ends, and **REST** connectivity.

---
 
<details open>
<summary><b>📄 1. Dynamic Report Designer</b> — Reporting · No-code QWeb & DOCX</summary>

**Overview:** Design and publish Odoo reports without Python — bind models, choose themes, replace standard prints.

**Report types:** Custom · Proforma · Invoice · Vendor Bill · Journal Entry · Quotation · Sale Order · RFQ · Purchase Order · Delivery Note

**Design & layout**
- Replace existing standard reports or register new report actions
- Primary vs extended report modes
- Header/footer-only layouts for branded stationery
- Per-company logos, colors, and paper formats
- Field-mapping wizard — place model fields into report sections
- One-section or two-section summary blocks (left/right alignment)
- Standalone dynamic header/footer designer

**Visual themes (ready-made QWeb)**  
Corporate · Modern · Formal · Modern Formal · Creative · Minimalist · Retro · Tech · Eco-friendly · CTIT style

**Advanced outputs**
- DOCX template upload with Odoo field merge
- Dot-matrix / continuous paper for legacy printers
- Dedicated summary report models and print actions
- Custom wizard for on-demand report generation

**Stack:** Python ORM · QWeb · lxml · PDF · multi-language field dictionaries

</details>

<details open>
<summary><b>🔐 2. Access & Permissions Studio</b> — Security · OWL Rules Mode</summary>

**Overview:** Central access management — simpler than scattered record rules; per-user and per-company control.

**Menus & system**
- Hide menus and sub-menus
- Restrict visible applications
- Disable login for selected users
- Block developer / debug mode

**Fields**
- Invisible · read-only · required rules per field
- Domain-based field access lines
- Relational field link restrictions

**Views & actions**
- Hide tree, form, kanban, calendar, pivot, graph views
- Hide smart buttons, object buttons, toolbar actions
- Hide notebook tabs and pages
- Chatter: full hide, or hide send message / log notes / schedule activity

**Global & model actions**
- Hide create, edit, delete, duplicate, archive, unarchive (global or per model)
- Hide import, export, spreadsheet
- Remove print actions, server actions, and reports from menus
- Whole-system read-only user profile

**Search & analytics**
- Hide filters and group-by on search views
- Pivot group menu restrictions

**Rules Mode (OWL / JavaScript)**
- Configure rules **on the live form** — no separate admin screen
- Secure backend RPC with upsert (no duplicate rule engines)
- Drawer UI, user tags, bilingual help, summary panels
- Automated tours for QA; registry cache invalidation on save

**Multi-company:** Rules scoped to selected companies.

**Demo:** [Rules Mode screen recording](https://github.com/odoo00/odoo00/raw/main/assets/rules-studio-demo.mp4) *(optional video asset in repo)*

</details>

<details open>
<summary><b>🌐 3. REST Application Gateway</b> — Integration · JWT API</summary>

**Overview:** Secure REST layer for mobile apps, portals, and third-party systems.

**Applications**
- Auto-generated client ID and secret per integration
- JWT HS256 access tokens + refresh tokens (configurable TTL)
- Secret rotation without redeploying Odoo
- Enable/disable applications instantly

**Permissions**
- Scopes per model: read · create · write · unlink · call
- Method registry: slug, target model, Python method name
- Rate-limit policies per application
- CORS allowed origins for browser clients

**Operations**
- Full API audit log (caller, method, timing, metadata)
- Postman collections for developers (JWT + menu access)
- Mobile menu-key documentation (Flutter)
- Seeded gateway template on installation

**Use cases:** Field sales apps · warehouse handhelds · external CRM · logistics status apps

</details>

<details open>
<summary><b>🔔 4. Webhook Extensions</b> — Integration · Outbound events</summary>

**Overview:** Push signed JSON to external URLs when Odoo records change.

**Configuration**
- HTTPS callback URL per webhook
- HMAC-SHA256 signature header with rotatable secret
- SSL verification toggle and request timeout
- Allowed-host allowlist (SSRF protection)
- Maximum payload size limit

**Subscriptions**
- Per model: fire on create · update · delete
- Select fields included in payload (or id + display name only)
- Immediate delivery or queued via scheduled job

**Reliability**
- Retry with exponential backoff (configurable attempts and delays)
- Delivery history and status tracking
- Payload preview for debugging
- Dispatcher cache refresh on rule changes

**Documentation:** Standalone receiver example · Arabic webhook secret guide

</details>

<details open>
<summary><b>🛒 5. Salla Marketplace Connector (CTIT)</b> — eCommerce · Webhooks</summary>

**Overview:** Connect Salla stores to Odoo sales, stock, customers, payments, and shipping.

**Connection**
- Salla OAuth authentication flow
- Verification key per store channel
- Multi-store channel records with connection state
- Redirect to Odoo channel after token exchange

**Webhook security**
- Public JSON endpoint with HMAC signature validation
- Rejects invalid signatures (HTTP 401)

**Order events**

| Event | Behavior |
|-------|----------|
| Order created | Create/update sale order, partner, lines |
| Order updated | Sync header and line changes |
| Order status updated | Map Salla status → Odoo workflow |

**Master data**
- Auto-create delivery companies from shipping payload
- Auto-create payment methods (including COD)
- Customer name, mobile, city, UTM source
- Store resolution by merchant ID or existing order link

**Sales:** Status mapper · channel configuration · multichannel menus

</details>

<details open>
<summary><b>🏪 6. Zid Marketplace Connector</b> — eCommerce · Catalog & orders</summary>

**Overview:** Zid OAuth, catalog sync, and controlled order confirmation in Odoo.

**Channel**
- OAuth redirect and callback routes
- Refresh-token maintenance
- Dashboards: products, partners, invoices, quotations, orders
- Error log for failed API calls

**Sync jobs**
- Products (SKU and bundle detection)
- Payment methods
- Shipping methods
- Bulk order import with Zid metadata on sale orders

**Order controls**
- Zid flags on orders (IDs, store, URLs, totals)
- Amount mismatch warning vs Odoo total
- Offer-order flag
- Duplicate product+route line prevention (non-Zid orders)
- Only Zid Manager/User groups may confirm Zid orders

**Accounting:** Branch assignment wizard before invoicing · linked invoice views

</details>

---

## 🏢 Enterprise Projects `15`

<details open>
<summary><b>View project list</b></summary>

| # | Project | Industry | Odoo | Role | Deliverables |
|---|---------|----------|------|------|--------------|
| 01 | **CTIT Official Platform** | ERP / SaaS | 9–19 | Team Leader | Core product, Saudi EDI, subscriptions, frameworks, 70+ clients |
| 02 | **CTIT SaaS Hosting** | Cloud ERP | 17 | Lead | Docker/Portainer, Traefik, backups, subscription portal |
| 03 | **Al Shatry** | Trading / Wholesale | 13 / 17 | Senior | Full ERP, branches, landed costs, ZATCA e-invoicing |
| 04 | **Al Bilady** | Retail / Distribution | 16 / 17 | Lead | Multi-branch sales, stock, accounting automation, reports |
| 05 | **Mega Trust** | Distribution | 17 / 18 | Senior | Purchase approvals, warehouse UI, cheques, Salla sync |
| 06 | **Roya** | Multi-branch | 15 | Senior | Branch numbering, tax reports, custom invoices, GOSI HR |
| 07 | **Al Suwailim (Vegetables)** | Fresh produce | 17 | Senior | Sale automation, ZATCA, APIs, portal, stock-to-invoice |
| 08 | **GOSI Compliance** | HR / Insurance | 17 | Architect | Rules, wages, audit logs, government API readiness |
| 09 | **Bonya Real Estate** | Property | 17 | Lead | Rentals, property accounting, Hijri UI, WhatsApp, LC |
| 10 | **IQAA Steel Factory** | Manufacturing / POS | 17 | Lead | Arabic POS delivery flow, custom screens, tracking |
| 11 | **Dabbos** | Trading | 17 / 18 | Lead | Custom sales/purchase/stock reports, salesperson KPIs |
| 12 | **Aloofy** | Retail / F&B | 16 | Senior | Large POS/WhatsApp retail stack, automation |
| 13 | **AlMoasher Business** | Enterprise | 12–17 | Senior | Core ERP customization, security, multi-company |
| 14 | **Capital ERP** | Iraq | 17 | Senior | Finance/operations, APIs, go-live support |
| 15 | **Healthy (UAE / EG / KSA)** | Healthcare | 15 | Developer | Multi-country rollout, regional rules |

</details>

---

## 🧩 Solutions Portfolio `20`

<details open>
<summary><b>View all 20 solutions with capabilities</b></summary>

| # | Solution | Category | Key capabilities |
|---|----------|----------|------------------|
| 01 | **Dynamic Report Designer** | Reporting | No-code QWeb/DOCX, 10+ themes, dot-matrix, summaries |
| 02 | **Access & Permissions Studio** | Security | Menus/fields/views/chatter; Rules Mode OWL |
| 03 | **REST Application Gateway** | Integration | JWT, scopes, rate limits, audit, mobile APIs |
| 04 | **Webhook Extensions** | Integration | HMAC outbound, retry, create/update/delete events |
| 05 | **Salla Connector (CTIT)** | eCommerce | OAuth, webhooks, orders, shipping, payments |
| 06 | **Zid Marketplace Connector** | eCommerce | OAuth, catalog, orders, branch invoicing |
| 07 | **Sales Order Workflow Automation** | Automation | Confirm → invoice → validate → deliver |
| 08 | **Geidea Payment Gateway** | Payments | Payment links, callbacks, SO/invoice integration |
| 09 | **GOSI Compliance Core** | HR / KSA | Eligibility, rates, wages, compliance logs |
| 10 | **GOSI Government API Layer** | HR / API | Multi-connection profiles, future API readiness |
| 11 | **CTIT Core Business Pack** | Platform | Saudi EDI, subscriptions, branch sales, portal |
| 12 | **Dynamic List Column Manager** | UI | Show/hide/reorder/relabel list columns |
| 13 | **Developer Operations Dashboard** | Management | Team KPIs, assignment wizard, project boards |
| 14 | **Real Estate Management Suite** | Property | Units, contracts, balances, client statements |
| 15 | **Rental Contract Lifecycle** | Property | Lease terms, milestones, expenses, reports |
| 16 | **Hijri Calendar for Odoo UI** | Localization | Hijri picker on forms and lists (JavaScript) |
| 17 | **Multi-Branch Document Numbering** | Accounting | Per-branch sequences for sales/purchase/journals |
| 18 | **SaaS Instance Provisioning** | DevOps | Docker stacks, routing, backups, packages |
| 19 | **Salla Enterprise Connector (Mega)** | eCommerce | High-volume webhooks for distribution clients |
| 20 | **Logistics / PickAppo REST Bridge** | Logistics | Mobile sync via API gateway (orders & status) |

**Cross-cutting:** Server actions · scheduled jobs · workflow automation · OWL/JavaScript UI · PostgreSQL tuning

</details>

---

## 🛠 Tech Stack

`Python` · `Odoo ORM` · `PostgreSQL` · `JavaScript` · `OWL` · `QWeb` · `XML` · `REST` · `Docker` · `Linux` · `Git` · `Agile leadership`

---

 
