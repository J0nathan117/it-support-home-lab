# Windows + Network Troubleshooting Lab

A hands-on home-lab assessment of Dell Windows laptop **LAP-003**, with a deliberately nonexistent DNS name used as a comparison test. This exercise documented a working connection; no outage repair was claimed.

## Objective

Practice a structured support investigation: check local connectivity, external reachability, name resolution, a website's TCP port, Windows network components, and record the evidence in Jira.

## Environment

- Personally owned Dell Latitude 7480 running Windows
- Wi-Fi connection
- Command Prompt and Windows PowerShell
- Jira Service Management ticket **IT-6**
- Home Wi-Fi network name concealed in screenshot 10

## Checks and findings

| Check | Command or method | Observed result |
| --- | --- | --- |
| Router reachability | `ping 10.0.0.1` | Four replies; 0% loss during the test; 5 ms average |
| External IP reachability | `ping 1.1.1.1` | Four replies; 0% loss during the test; 18 ms average |
| DNS lookup | `nslookup example.com` | Returned addresses |
| Negative DNS test | `nslookup helpdesk-lab.invalid` | Expected “Non-existent domain” response |
| DNS comparison | Repeated lookup of example.com | Valid name resolved while the intentionally invalid name failed |
| Adapter status | `Get-NetAdapter` | Wi-Fi Up; Ethernet disconnected; Hyper-V virtual adapter Up |
| TCP connection | `Test-NetConnection example.com -Port 443` | TcpTestSucceeded: True |
| Browser check | Opened https://example.com | Example Domain page loaded (recorded in Jira notes) |
| Wi-Fi service | `Get-Service WlanSvc` | WLAN AutoConfig Running |
| Firewall profiles | `Get-NetFirewallProfile` | Domain, Private, and Public enabled |
| Active network profile | `Get-NetConnectionProfile` | Wi-Fi categorized Public; Windows reported IPv4 and IPv6 Internet connectivity |

Some screenshots use `Select-Object` to display only relevant fields. Screenshot 07 also demonstrates `-InformationLevel Quiet`, which returns a True/False connection result.

## Troubleshooting reasoning

1. Established that the laptop could reach its router.
2. Checked an external IP address independently of website name lookup.
3. Compared successful and intentionally unsuccessful DNS lookups.
4. Tested a TCP connection on port 443 and separately opened the website.
5. Inspected Windows adapter, service, firewall, and network profile status.
6. Documented the observed results and closed the assessment in Jira.

**Conclusion:** No connectivity fault was identified during these checks. No network settings were changed and no repair was required. The invalid-domain lookup was an expected test result.

## Evidence

| Screenshot | What it records |
| --- | --- |
| 01 | [Router connectivity: four replies, 0% loss](screenshots/01-router-connectivity.png) |
| 02 | [External IP connectivity: four replies, 0% loss](screenshots/02-internet-connectivity.png) |
| 03 | [Successful DNS lookup](screenshots/03-dns-lookup.png) |
| 04 | [Expected nonexistent-domain response](screenshots/04-dns-name-not-found.png) |
| 05 | [Failed and successful DNS lookup comparison](screenshots/05-dns-comparison.png) |
| 06 | [Network adapter status](screenshots/06-network-adapter-status.png) |
| 07 | [TCP port 443 connection test](screenshots/07-https-port-test.png) |
| 08 | [WLAN AutoConfig service status](screenshots/08-wifi-service-status.png) |
| 09 | [Windows Firewall profile status](screenshots/09-firewall-profile-status.png) |
| 10 | [Active Wi-Fi network profile (network name redacted)](screenshots/10-active-network-profile-redacted.jpg) |
| 11 | [Completed Jira assessment ticket IT-6](screenshots/11-network-assessment-ticket.png) |
| 12 | [Assessment findings and closure notes](screenshots/12-network-assessment-notes.png) |

## Skills demonstrated

- Windows Command Prompt and PowerShell diagnostics
- Gateway and external IP connectivity testing
- DNS lookup interpretation and comparison testing
- TCP port connectivity testing
- Adapter, service, firewall, and network profile inspection
- Evidence collection and Jira assessment documentation

## Scope and interpretation

Ping results describe these short tests, not a guarantee of continuous connectivity. A failed ping can also occur when replies are blocked. A successful TCP port test does not by itself verify TLS or webpage content; the browser check was separate. Wi-Fi link speed is not an internet speed measurement. Enabled firewall profiles do not establish that every firewall rule is correct.

Screenshot 10 conceals the home network name for portfolio sharing. This lab demonstrates diagnostic assessment and documentation rather than repair of an actual outage.
