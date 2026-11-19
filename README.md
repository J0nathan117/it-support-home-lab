# IT Support Home Lab

Hands-on entry-level IT support portfolio: Jira Service Management ticket handling, device inventory and update assessments, and Windows Server Active Directory identity management in Hyper-V.

> All tickets, users, and devices are simulated for learning and portfolio purposes. Serial numbers are placeholders.

## Skills demonstrated

- Ticket triage, prioritization, internal notes, escalation to Tier 2, and closure in Jira Service Management
- Windows and macOS endpoint support, software-update assessment, and device inventory tracking
- Windows Server, Hyper-V, Active Directory Domain Services, organizational units, users, and security groups
- Identity life cycle: provisioning, group-based access, and account deactivation
- Clear technical documentation and resolution verification
- SQL Server, SSMS, T-SQL queries, data-quality troubleshooting, and read-only permissions

## Projects at a glance

| Project | What I completed | Tools |
| --- | --- | --- |
| [1. Ticket life cycle](#1-ticket-life-cycle) | Created, prioritized, documented, escalated, resolved, and closed three support tickets | Jira Service Management |
| [2. Device life cycle](#2-device-life-cycle) | Kept a device inventory and documented macOS and Windows update assessments | Google Sheets, Jira, macOS, Windows |
| [3. Identity life cycle](#3-identity-life-cycle) | Built an Active Directory domain and managed a user from onboarding to offboarding | Hyper-V, Windows Server, AD DS, Jira |
| [4. SQL application support lab](application-support-sql-lab) | Built and troubleshot a SQL Server database, including data-quality, permissions, and connection scenarios | SQL Server Express, SSMS, T-SQL |

---

## 1. Ticket life cycle

**Goal:** Practice handling help desk tickets the way a Tier 1 technician would, from request to closure.

| Ticket | Scenario | What I did |
| --- | --- | --- |
| New employee onboarding (Jordan Smith) | New Sales hire needs an account, shared-folder access, and a laptop | Documented the request, set priority, simulated account and device setup, verified sign-in and folder access, closed |
| Sales shared-folder access (Priya Patel) | Business-impacting access problem | Prioritized by impact and urgency, documented troubleshooting, escalated to Tier 2, verified the fix |
| Password reset (Alex Cruz) | User locked out of their account | Verified identity, handled the reset, confirmed successful sign-in |

**Skills shown:** prioritization, troubleshooting notes, escalation, user access support, resolution verification, and ticket closure.

[View ticket life cycle screenshots](screenshots/ticket-lifecycle)

---

## 2. Device life cycle

**Goal:** Track company devices and check whether they need updates.

- Kept an inventory of a MacBook Pro and a Dell Latitude 7480 with asset tags and placeholder serial numbers.
- Recorded owner, department, status, assignment date, and maintenance notes for each device.
- Performed and documented a macOS software-update assessment and a Windows security-update assessment.
- Created and closed a Jira maintenance ticket for the Windows device.

**Skills shown:** asset tracking, endpoint support, macOS and Windows update assessment, maintenance documentation, and ticket handling.

[View device life cycle screenshots](screenshots/device-lifecycle)

---

## 3. Identity life cycle

**Goal:** Build a small Windows domain and manage a user's access from onboarding to offboarding.

**Environment:** Hyper-V virtual machine running Windows Server with Active Directory Domain Services, domain `identitylab.local`.

**Work completed**

1. Created the **Sales** organizational unit and the `Sales-Shared-Access` security group.
2. Provisioned **LeBron Smith** and gave access by adding the account to the Sales group.
3. Created and then disabled **Alex Cruz** to document an offboarding action.
4. Documented the work in a Jira ticket and closed it after verification.

**Skills shown:** Windows Server administration, Active Directory, user provisioning, organizational units, security groups, group-based access control, and account deactivation.

**Next steps:** joining a Windows client to the domain, adding a Group Policy example, and documenting a DNS/network troubleshooting scenario.

[View identity life cycle screenshots](screenshots/identity-lifecycle)

---

## 4. SQL application support lab

**Goal:** Practice the database troubleshooting and validation work common in application support.

- Built a SQL Server database for simulated customer, product, quote, and order records.
- Used joins, filters, summaries, inserts, updates, and duplicate-record detection.
- Investigated and resolved a simulated order-total mismatch, then verified no mismatches remained.
- Tested read-only access and documented a SQL Server connection error.

**Skills shown:** SQL Server, SSMS, T-SQL, data quality, record correction, least-privilege access, connection troubleshooting, and verification.

[View the SQL application support lab](application-support-sql-lab)

---

## Repository structure

```
it-support-home-lab/
├── README.md
├── application-support-sql-lab/
│   └── README.md
└── screenshots/
    ├── ticket-lifecycle/
    ├── device-lifecycle/
    └── identity-lifecycle/
```

## About me

I'm building toward an entry-level help desk role with 7+ years of customer service and administrative experience and CompTIA A+ in progress.
Contact: JonathanMundaray@gmail.com
