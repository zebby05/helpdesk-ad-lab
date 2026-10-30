# Help Desk & Active Directory Home Lab

A hands-on IT support lab built from scratch on a single PC. I run a Windows Server 2022 domain controller and a Windows 11 client in VirtualBox, break things on purpose, and document every fix as a help desk ticket.

**Goal:** practice the real day-to-day work of a Tier 1 help desk / desktop support technician (accounts, passwords, Group Policy, networking) and keep a written record of how I troubleshoot.

## Lab environment

| Machine | OS | Role |
|---|---|---|
| `DC01` | Windows Server 2022 | Domain controller, DNS, Group Policy (`lab.local`) |
| `CLIENT01` | Windows 11 Pro | Domain-joined user workstation |

- **Hypervisor:** Oracle VirtualBox
- **Domain:** `lab.local`
- **Structure:** Organizational Units (Employees, Sales, IT) with test users
- **Snapshots** taken after each milestone so I can roll back safely

## Projects and tickets

| Ticket | Issue | Skills shown |
|---|---|---|
| [001: Account lockout and password reset](tickets/001-account-lockout-password-reset.md) | User locked out after repeated bad passwords | Account lockout policy, `net accounts`, `net user /domain`, ADUC password reset, forced change at next logon |

Also built so far:
- Active Directory domain with OUs and test users
- Windows 11 client joined to the domain
- Group Policy: "Restrict Control Panel" linked to the Sales OU, verified with `gpresult`
- Domain account lockout policy (3 attempts, 15-minute lockout)

## Roadmap

- [ ] DHCP and DNS roles on `DC01`
- [ ] Ticketing system (log, triage, and resolve simulated issues)
- [ ] More break/fix tickets: shared folder access, GPO not applying, DNS failure, new-hire setup
- [ ] Knowledge base articles from resolved tickets

## Tools and commands used

`net accounts`, `net user <name> /domain`, `gpupdate /force`, `gpresult`, Active Directory Users and Computers, Group Policy Management, Server Manager

## About

Built by **Shahzeb Hanif**: UMGC B.S. Cybersecurity Technology student, Montgomery College A.A. Information Systems, working toward IT support and later cybersecurity (penetration testing).

LinkedIn: [linkedin.com/in/shahzeb-hanif-784778325](https://www.linkedin.com/in/shahzeb-hanif-784778325)
