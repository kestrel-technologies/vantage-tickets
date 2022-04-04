# vantage-tickets

Perch: Vantage queues. Ticket IDs are in issue titles. Comments carry the in-fiction date in their first line.

This repository holds no code. Every Perch ticket for Kestrel Vantage lives here as an issue:

| Prefix | Queue | Template |
|---|---|---|
| `INC-####` | Incidents | `incident.md` |
| `CHG-####` | Changes (anything that touches a production system) | `change.md` |
| `REM-###` | Remediation items from an assessment or review | `remediation.md` |
| `ENTSEC-EXC-####` | Security exceptions (approved by EntSec Governance) | `exception.md` |
| `KSS-REV-####` | Architecture reviews | — |
| `WT-####`, `SKY-OPS-###` | Team queues (Watchtower; imported Skyward tracker items) | — |

## Conventions

- **Title:** `<TICKET-ID> · <summary>`, for example `CHG-2412 · Rotate Birdseye integration user password`.
- **Body:** starts with a header table (**Status**, **Opened**, **Owner**, **Queue**, **Related**). The
  **Status** cell is the ticket's status of record (Open, In progress, Blocked, Approved, Expired,
  Closed...). GitHub's open/closed state only says whether the queue still tracks the ticket.
- **Comments:** the first line is `**<Name> (<team>) · <YYYY-MM-DD>**`. That date is when the comment
  was written in Perch; GitHub's own timestamps show when the ticket was mirrored here.
- **Labels:** the type (`incident`, `change`, `remediation`, `exception`, `architecture-review`), the
  state when it matters (`blocked`, `approved`, `expired`, `closed-accepted-risk`), the KSS control
  (`control:IAM-01` … `control:DAT-08`) and the owning team (`team:*`). Full list: `.github/labels.yaml`.
- Chat approvals are not approvals. An exception exists only as an `ENTSEC-EXC` ticket with status
  Approved and an expiry date.

---

Kestrel Technologies is a fictional company created for an educational workshop. Nothing in this repository is a real credential, person or product. Mirrored from Roost by `roost-mirror`; CL metadata is preserved in commit trailers (`Roost-CL:`, `Reviewed-by:`).
