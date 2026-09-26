# Network Security & Reconnaissance Labs — NetworkWalks

Practical reconnaissance, OSINT gathering, and network scanning labs completed as part of the NetworkWalks cybersecurity programme[cite: 1].

---

## 1. Footprinting with Multi-Tools
* **Objective:** Establish baseline DNS, routing, and domain ownership data[cite: 1].
* **Tools:** `whois`, `dig`, `nslookup`, `traceroute`.
* **Key Steps:** Queried registrar and nameserver information via Whois; mapped mail and host records across DNS; traced routing paths to external gateways.
* **Evidence:** `screenshots/01-multi-tools.png`

---

## 2. Google Hacking Database (GHDB)
* **Objective:** Uncover publicly indexed sensitive files, directories, and login interfaces[cite: 1].
* **Core Dorks:**
  * `site:<target> intitle:"index of"`
  * `site:<target> ext:log | ext:sql | ext:txt`
  * `site:<target> inurl:admin | inurl:login`
* **Evidence:** `screenshots/02-ghdb.png`

---

## 3. Link Analysis with Maltego
* **Objective:** Map relationships between domains, netblocks, mail servers, and organizational entities[cite: 1].
* **Key Steps:** Seeded the root domain; ran DNS and infrastructure transforms; visualised attack surface interconnectivity.
* **Evidence:** `screenshots/03-maltego.png`

---

## 4. OSINT Gathering with theHarvester
* **Objective:** Collect subdomains, public email addresses, and employee names[cite: 1].
* **Command:** `theHarvester -d <target-domain> -l 500 -b duckduckgo,crtsh`
* **Evidence:** `screenshots/04-theharvester.png`

---

## 5. Active Scanning with Zenmap
* **Objective:** Identify live hosts, open ports, and running service versions[cite: 1].
* **Profiles:** Intense Scan (`nmap -T4 -A -v <target>`) and Fast Scan (`nmap -F <target>`).
* **Key Open Ports:** 21 (FTP), 22 (SSH), 80 (HTTP), 443 (HTTPS).
* **Evidence:** `screenshots/05-zenmap.png`

---

## Legal & Compliance Note
All footprinting and scanning activities were conducted strictly under an authorized permission letter and executed against authorized targets[cite: 1].
