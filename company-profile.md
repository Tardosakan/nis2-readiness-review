# Company profile — Kertvár Food Distribution Kft.

> **Fictional company** created for a NIS2 readiness review portfolio project. Any resemblance to a real company is coincidental.

## Basics

| | |
|---|---|
| **Name** | Kertvár Food Distribution Kft. |
| **Sector** | Food — wholesale distribution (NIS2 Annex II, Hungarian Cybersecurity Act Annex 2) |
| **Staff** | 140 (office 35, warehouse 70, drivers 35) |
| **Annual revenue** | ~€28 million |
| **Size class** | Medium-sized enterprise (50–249 staff, under €50M turnover) |
| **NIS2 status** | In scope as an **important entity** (medium-sized, Annex II sector) |
| **Founded** | 2004, family-owned |

## What they do
Buys chilled, frozen and dry food from Hungarian producers and importers and delivers it to around 900 restaurants, hotels, school kitchens and independent shops in Budapest and Pest County. Next-day delivery, ordered by phone, email or a B2B web shop.

## Locations
- **Head office and warehouse:** one site on the southern edge of Budapest. Offices, a dry-goods warehouse and a cold store (chilled and frozen rooms).
- **No other sites.** Drivers work from the same site.

## IT setup
- **ERP:** SAP Business One, run by an outside SAP partner. It handles orders, stock, invoicing and NAV Online Számla reporting.
- **Server room:** one physical server in a small room next to the office. It runs SAP Business One, the file share and the domain controller.
- **Backups:** a NAS in the same server room takes a nightly copy.
- **Email and office:** Microsoft 365 Business. MFA is turned on only for the IT admin and the managing director.
- **Devices:** about 45 office PCs and laptops (Windows), 25 handheld barcode scanners in the warehouse, and 35 Android phones for drivers (delivery app and navigation).
- **B2B web shop:** built and hosted by a small web agency, connected to the ERP.
- **Cold store monitoring:** temperature sensors with a cloud dashboard from the refrigeration vendor. It sends alarms by SMS.
- **Payroll:** outsourced to a payroll bureau using NEXON.
- **Network:** one internet line and one firewall. The SAP partner and the IT contractor have permanent remote access through it.

## Who runs IT
- **One in-house IT administrator.** He handles everything from printers to user accounts.
- **An outside IT contractor (MSP)** for the server, firewall and bigger problems.
- **No security role.** The finance manager handles "compliance" alongside her main job.

## Key suppliers (IT and operations)
1. **SAP partner:** runs and updates the ERP, with remote access.
2. **IT contractor (MSP):** server, network and firewall, with remote access.
3. **Refrigeration vendor:** cold store hardware and the cloud monitoring dashboard.
4. **Web agency:** B2B web shop.
5. **Payroll bureau:** holds staff personal and salary data.

## Known weak spots (for the review)
1. Backups are on a NAS in the same room as the server and have never been restore-tested.
2. There's no written incident procedure, and nobody knows who would report an incident to the authorities or within what deadline.
3. MFA is only on two accounts. Everyone else logs into Microsoft 365 with a password only.
4. Warehouse scanners use shared logins, and leavers' accounts are not always disabled.
5. Suppliers have permanent remote access, and no contract mentions security requirements.
6. There has never been any security training, and phishing emails regularly reach staff.
7. There's no asset list. Nobody knows exactly how many devices exist.
8. The cold store dashboard uses the vendor's default password.

## Why it's realistic
- Hungarian SMEs are known for low levels of data and information security, according to the EU's Digital Economy and Society Index.
- Ransomware groups increasingly target Hungarian SMEs because of limited budgets and uneven cyber hygiene.
- SAP Business One is the main mid-market ERP in Hungary, and NEXON leads in HR and payroll.
- Food wholesale distribution with medium size or larger is within NIS2 scope; retail, storage and transport alone are not.
