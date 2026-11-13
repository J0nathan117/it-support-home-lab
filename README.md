# IT Support Home Lab

Hands-on IT support portfolio demonstrating ticket handling, device inventory, Windows endpoint maintenance, and Active Directory identity management in a controlled home-lab environment.

> All tickets and user accounts shown are simulated for learning and portfolio purposes. Device serial numbers use safe placeholder values.

## Technical skills demonstrated

- Jira Service Management ticket triage, prioritization, internal notes, escalation, and closure
- Windows and macOS endpoint support, software-update assessment, and device inventory tracking
- Windows Server, Hyper-V, Active Directory Domain Services, organizational units, users, and security groups
- Identity lifecycle administration: provisioning, group-based access, and account deactivation
- Clear technical documentation and resolution verification

## Project portfolio

| Project | What I completed | Evidence |
| --- | --- | --- |
| [Ticket life cycle](#1-ticket-life-cycle) | Created, prioritized, documented, escalated, resolved, and closed support tickets in Jira. | [Screenshots](screenshots/ticket-lifecycle) |
| [Device life cycle](#2-device-life-cycle) | Maintained a home-lab device inventory and recorded macOS and Windows update assessments. | [Screenshots](screenshots/device-lifecycle) |
| [Identity life cycle](#3-identity-life-cycle) | Built an Active Directory lab and managed user access from onboarding through offboarding. | [Screenshots](screenshots/identity-lifecycle) |

## 1. Ticket life cycle

**Tools:** Jira Service Management

Created three simulated support tickets and moved each through investigation, documentation, resolution, and closure.

- **New employee onboarding - Jordan Smith:** documented account, shared-folder, and laptop provisioning with verification of sign-in and access.
- **Sales shared-folder access - Priya Patel:** prioritized a business-impacting access issue, documented troubleshooting, escalated to Tier 2, and verified the resolution.
- **Password reset - Alex Cruz:** documented identity verification, password-reset handling, and successful sign-in confirmation.

**Skills shown:** prioritization, troubleshooting notes, escalation, user access support, resolution verification, and ticket closure.

[View ticket-life-cycle evidence](screenshots/ticket-lifecycle)

## 2. Device life cycle

**Tools:** Google Sheets, Jira Service Management, macOS, Windows

Maintained a device inventory for a MacBook Pro and Dell Latitude 7480, using asset tags and placeholder serial numbers.

- Recorded device owner, department, status, assignment date, and maintenance notes.
- Performed and documented a macOS software-update assessment.
- Performed and documented a Windows security-update assessment.
- Created and closed a Jira maintenance-assessment ticket for the Windows device.

**Skills shown:** asset tracking, endpoint support, macOS and Windows update assessment, maintenance documentation, and ticket handling.

[View device-life-cycle evidence](screenshots/device-lifecycle)

## 3. Identity life cycle

**Tools:** Hyper-V, Windows Server, Active Directory Domain Services, Jira Service Management

Built the `identitylab.local` Active Directory domain in Hyper-V and documented a realistic user-access workflow.

- Created the **Sales** organizational unit and the `Sales-Shared-Access` security group.
- Provisioned **LeBron Smith** and assigned access through the Sales security group.
- Created and disabled **Alex Cruz** to document an offboarding action.
- Created and completed a Jira ticket documenting the identity lifecycle work.

**Skills shown:** Windows Server administration, Active Directory, user provisioning, organizational units, security groups, group-based access control, and account deactivation.

[View identity-life-cycle evidence](screenshots/identity-lifecycle)

## Repository structure

```text
it-support-home-lab/
├── README.md
└── screenshots/
    ├── ticket-lifecycle/
    ├── device-lifecycle/
    └── identity-lifecycle/
```
