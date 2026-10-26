# osTicket: Ticket Lifecycle Examples

**Hands-on IT support / service desk lab** · osTicket v1.15.8 · Windows VM · IIS / PHP / MySQL

## Overview

Practiced two incident-management scenarios in a self-hosted osTicket lab. Worked through end-user intake, ticket creation, triage, priority and SLA updates, agent assignment, department transfers, access verification, user-facing responses, and ticket resolution or closure. The cases and remediation narratives are **simulated service-desk exercises**, not evidence of changes to live banking or accounting systems.

**Skills demonstrated:** Ticketing systems · Incident triage · IT help desk documentation · Priority and SLA administration · Escalation and assignment · Department-based access controls · Customer communication · Ticket resolution and closure

## Verified outcomes

| Case | Ticket | Triage / escalation | Evidence-backed outcome |
| --- | --- | --- | --- |
| Mobile / online banking outage | **#110178** | Emergency; **Sev-A** (1-hour grace period); transferred from Support to **SysAdmins** and assigned to Jane | John’s post-transfer access was denied; Jane recorded a simulated recovery; ticket **Resolved** status confirmed |
| Adobe Reader unavailable | **#956427** | High; **Sev-B** (4-hour grace period); handled by John in Support | Triage, proposed software-package fix, and user-verification notes recorded; ticket **Closed** status confirmed |

**Scope:** Both incidents use test data. SLA grace periods describe configured ticket targets, **not measured repair durations**. A note or reply describing remediation is documentation of the scenario, not proof that production infrastructure or endpoint software was modified.

## Walkthrough and screenshot evidence

**45 screenshots**, numbered in capture order. Each image is labeled by the interface action or result actually visible in the screenshot. Configuration dialogs and draft replies are distinguished from saved changes and confirmation banners.

## 1. Prepare the service desk

Reviewed the local osTicket administration setup, verified Support and SysAdmins departments, removed the unused Maintenance department, and opened the end-user portal.

### 01. System settings — local helpdesk baseline

Reviewed the local helpdesk configuration and default Support department before processing tickets.

![System settings — local helpdesk baseline](screenshots/01-system-settings-baseline.jpg)

### 02. Agent roster — staff accounts

Verified the available staff accounts, including John in Support and Jane in SysAdmins.

![Agent roster — staff accounts](screenshots/02-agent-roster-baseline.jpg)

### 03. Department inventory

Reviewed Maintenance, Support, and SysAdmins departments before preparing routing.

![Department inventory](screenshots/03-department-inventory.jpg)

### 04. Maintenance department — cleanup selection

Selected Maintenance and opened the administrative actions to remove the unused lab department.

![Maintenance department — cleanup selection](screenshots/04-department-cleanup-selection.jpg)

### 05. Department cleanup — confirmation

Verified the success notification and the remaining Support and SysAdmins departments.

![Department cleanup — confirmation](screenshots/05-department-deletion-confirmed.jpg)

### 06. End-user support portal

Opened the end-user portal used to create support tickets.

![End-user support portal](screenshots/06-support-center-home.jpg)

## 2. Banking outage — intake and initial review

Submitted an example bank-wide online/mobile banking incident as Karen. Ticket **#110178** was created and reviewed in the Support queue, initially with Normal priority and the Default SLA.

### 07. Banking outage — new ticket form

Entered Karen’s simulated mobile/online banking outage report, including the affected users and symptoms.

![Banking outage — new ticket form](screenshots/07-banking-incident-submission.jpg)

### 08. Banking outage — ticket creation confirmed

Verified that the customer-facing portal accepted the support request.

![Banking outage — ticket creation confirmed](screenshots/08-banking-ticket-submitted.jpg)

### 09. Agent sign-in — John

Opened the staff sign-in screen for the Support agent account.

![Agent sign-in — John](screenshots/09-john-signin-first.jpg)

### 10. New banking incident — ticket queue

Verified that banking ticket #110178 appeared in the open-ticket queue.

![New banking incident — ticket queue](screenshots/10-banking-incident-open-queue.jpg)

### 11. Banking incident — initial triage

Inspected the original ticket fields, including Normal priority, Support department, Default SLA, and unassigned status.

![Banking incident — initial triage](screenshots/11-banking-incident-initial-review.jpg)

### 12. Agent note — initial permission test

Recorded an internal test note while evaluating John’s starting level of access.

![Agent note — initial permission test](screenshots/12-john-read-only-test-note.jpg)

## 3. Review Support-agent access

Reviewed John’s account and updated his primary Support access role. The later cross-department access test checks departmental boundaries separately from this role assignment.

### 13. Administrator sign-in

Returned to the administrator account to review the agent’s access configuration.

![Administrator sign-in](screenshots/13-administrator-signin.jpg)

### 14. Ticket queue — administrative review

Checked the ticket queue before changing the agent configuration.

![Ticket queue — administrative review](screenshots/14-open-tickets-admin-review.jpg)

### 15. System preferences — access review

Reviewed the helpdesk settings in the administration interface.

![System preferences — access review](screenshots/15-system-settings-access-review.jpg)

### 16. Agent roster — access review

Located John’s agent account in the staff roster.

![Agent roster — access review](screenshots/16-agent-roster-access-review.jpg)

### 17. John’s agent account

Opened John’s account profile for review of staff authentication and access settings.

![John’s agent account](screenshots/17-john-agent-account.jpg)

### 18. Support access role — saved

Verified an updated primary Support role of All Access on John’s agent profile; department scope is evaluated separately later.

![Support access role — saved](screenshots/18-john-support-access-updated.jpg)

### 19. Agent sign-in — updated permissions

Returned to John’s agent session to continue the banking-incident triage.

![Agent sign-in — updated permissions](screenshots/19-john-signin-after-update.jpg)

## 4. Banking outage — emergency escalation and resolution

Reprioritized the banking issue to Emergency, assigned **Sev-A (one-hour grace period)**, recategorized it as a Business Critical Outage, assigned Jane, and transferred it to SysAdmins. John’s subsequent access attempt was denied. Jane documented simulated remediation, and osTicket confirmed the ticket moved to **Resolved**.

### 20. Banking incident — Emergency priority

Selected Emergency priority with an incident-impact explanation for the outage.

![Banking incident — Emergency priority](screenshots/20-banking-priority-emergency.jpg)

### 21. Banking incident — priority confirmation

Verified the ticket showed Emergency priority and a successful priority update.

![Banking incident — priority confirmation](screenshots/21-banking-priority-confirmed.jpg)

### 22. Banking incident — Sev-A SLA

Selected Sev-A for the business-critical incident, representing a one-hour SLA grace period.

![Banking incident — Sev-A SLA](screenshots/22-banking-sla-seva.jpg)

### 23. Banking incident — critical-outage category

Changed the help topic to Report a Problem / Business Critical Outage.

![Banking incident — critical-outage category](screenshots/23-banking-help-topic-critical.jpg)

### 24. Banking incident — escalation response

Prepared an agent response explaining escalation to SysAdmins after initial triage.

![Banking incident — escalation response](screenshots/24-banking-escalation-response.jpg)

### 25. Banking incident — assign Jane

Opened the reassignment control and selected Jane Doe as the receiving agent.

![Banking incident — assign Jane](screenshots/25-banking-reassign-jane.jpg)

### 26. Banking incident — transfer to SysAdmins

Selected the SysAdmins department for the ticket transfer.

![Banking incident — transfer to SysAdmins](screenshots/26-banking-transfer-sysadmins.jpg)

### 27. John’s cross-department access — denied

Attempted to access the transferred ticket as John and received an explicit Access denied banner.

![John’s cross-department access — denied](screenshots/27-john-department-access-denied.jpg)

### 28. Jane’s ticket queue

Viewed the escalated banking ticket under Jane’s account, with Emergency priority and agent assignment visible.

![Jane’s ticket queue](screenshots/28-jane-open-ticket-queue.jpg)

### 29. Banking incident — assigned ticket review

Reviewed the ticket’s updated department, Sev-A plan, assignee, and recorded activity.

![Banking incident — assigned ticket review](screenshots/29-jane-banking-ticket-thread.jpg)

### 30. Banking incident — assignment and transfer history

Reviewed the thread entries documenting reassignment to Jane and transfer to SysAdmins.

![Banking incident — assignment and transfer history](screenshots/30-banking-escalation-audit-trail.jpg)

### 31. Jane — investigation update

Documented a simulated back-end server configuration issue and the planned recovery action.

![Jane — investigation update](screenshots/31-jane-investigation-response.jpg)

### 32. Jane — restoration confirmation

Entered a simulated restoration update noting service availability and end-user confirmation.

![Jane — restoration confirmation](screenshots/32-jane-restoration-response.jpg)

### 33. Banking incident — mark Resolved

Opened the status dialog with Resolved selected for the banking incident.

![Banking incident — mark Resolved](screenshots/33-banking-resolve-dialog.jpg)

### 34. Banking incident — Resolved confirmed

Verified the green confirmation that ticket #110178 changed to Resolved.

![Banking incident — Resolved confirmed](screenshots/34-banking-resolved-confirmed.jpg)

### 35. Banking incident — closure workflow reviewed

Opened a later Closed-status dialog; the preceding capture independently confirms the Resolved state.

![Banking incident — closure workflow reviewed](screenshots/35-banking-close-dialog.jpg)

## 5. Adobe Reader — software-support ticket lifecycle

Submitted a second incident for Adobe Reader, ticket **#956427**. John documented triage, updated the ticket to **High** priority with **Sev-B (four-hour grace period)**, captured a simulated remediation and user-verification narrative, and closed the ticket. osTicket confirmed **Closed**.

### 36. Adobe Reader — support request submitted

Entered Ken’s simulated Adobe Reader failure affecting an accounting team.

![Adobe Reader — support request submitted](screenshots/36-adobe-reader-ticket-form.jpg)

### 37. Adobe Reader — ticket creation confirmed

Verified that the support portal accepted the new request.

![Adobe Reader — ticket creation confirmed](screenshots/37-adobe-ticket-confirmed.jpg)

### 38. Adobe Reader — Support agent sign-in

Opened John’s agent account to triage the application-support incident.

![Adobe Reader — Support agent sign-in](screenshots/38-john-signin-adobe.jpg)

### 39. Adobe Reader — open-ticket queue

Located new ticket #956427 in the open support queue.

![Adobe Reader — open-ticket queue](screenshots/39-adobe-in-open-ticket-queue.jpg)

### 40. Adobe Reader — initial incident notes

Documented the reported impact: several employees unable to open Adobe Reader during an internal audit.

![Adobe Reader — initial incident notes](screenshots/40-adobe-initial-triage.jpg)

### 41. Adobe Reader — High priority and Sev-B

Verified the ticket showed High priority, Sev-B SLA, and John’s Support assignment.

![Adobe Reader — High priority and Sev-B](screenshots/41-adobe-priority-and-sla-updated.jpg)

### 42. Adobe Reader — troubleshooting and escalation notes

Recorded a simulated software-package issue, coordination with desktop administration, and proposed deployment or catalog installation.

![Adobe Reader — troubleshooting and escalation notes](screenshots/42-adobe-remediation-plan.jpg)

### 43. Adobe Reader — end-user verification notes

Recorded the simulated follow-up that the new package worked and users could reopen the application.

![Adobe Reader — end-user verification notes](screenshots/43-adobe-user-verification.jpg)

### 44. Adobe Reader — closure documentation

Entered closure notes describing completed investigation and a resolved user issue.

![Adobe Reader — closure documentation](screenshots/44-adobe-close-ticket-dialog.jpg)

### 45. Adobe Reader — closure verified

Verified the green confirmation that ticket #956427 changed to Closed and disappeared from the open queue.

![Adobe Reader — closure verified](screenshots/45-adobe-closed-confirmed.jpg)

## Lessons demonstrated

- **Effective triage:** Reclassify incidents using their actual service impact, not just the wording of the original request.
- **SLA handling:** Update the SLA target as severity changes and preserve the ticket’s activity history for handoff.
- **Correct routing:** Assign work to a responsible agent and transfer ownership to the appropriate department when first-line support cannot resolve the issue.
- **Access controls:** A Support agent with an expanded Support role can still be denied access to a ticket transferred into another department.
- **Service-desk recordkeeping:** Maintain agent notes, customer-facing updates, verification details, and an explicit resolution status.

## Environment and security boundaries

This was a **localhost-only training environment**. Some historical screenshots display an osTicket warning to remove the installation `setup` directory and show an HTTP localhost URL. Those screenshots document the lab state and **do not establish a production-hardened deployment**. A real deployment should remove installer files, enforce HTTPS, and use appropriately secured accounts. The screenshots also show test user identifiers; avoid reusing test passwords elsewhere.

The related environment installation and post-install configuration exercises were conducted separately. This repository focuses on **ticket lifecycle operations**, not server deployment or live remediation.
