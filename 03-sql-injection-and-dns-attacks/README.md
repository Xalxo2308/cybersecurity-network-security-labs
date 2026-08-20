# SQL Injection and DNS Attacks

This folder contains practical cybersecurity laboratory work completed using a controlled Ubuntu virtual-machine environment.

## Topics Covered

- SQL Injection
- Authentication Bypass
- HOST File Modification
- DNS Spoofing
- DNS Cache Poisoning
- DNS Traffic Analysis

---

## 1. SQL Injection – Login Bypass

The first task demonstrated how SQL injection can bypass an application's authentication mechanism when user input is not properly validated.

### Known Username, Unknown Password

The username was:

`123456789`

An SQL injection string was entered in the password field:

`' or 1=1#`

The application accepted the input and successfully authenticated the user.

This demonstrates how manipulating the SQL query through specially crafted input can bypass authentication in a vulnerable application.

### Unknown Username and Password

A second authentication bypass was performed by using an SQL injection string in the username and password fields:

`' or 1=1--`

The application again returned a successful login.

### Evidence

- `sql-injection-login-bypass.png`
- `sql-injection-authentication-bypass.png`

The laboratory report documents both authentication-bypass exercises using SQL injection. :contentReference[oaicite:0]{index=0}

---

## 2. HOST File Modification

The second part demonstrated how modifying the local HOST configuration can affect domain-name resolution.

The client machine's network configuration was inspected and modified during the experiment.

The laboratory environment used:

- Cybersec Client
- Cybersec Server
- Attacker VM
- DNS services
- Ubuntu virtual machines

The experiment included DNS lookup verification using the `dig` command.

### Evidence

- `host-file-attack-initial-state.png`
- `host-file-modification-dns-verification.png`

The lab documentation identifies this section as an attack involving modification of the HOST file. :contentReference[oaicite:1]{index=1}

---

## 3. DNS Spoofing Attack

The next task investigated DNS spoofing.

The DNS query for:

`www.netsec-week3.com`

was examined using the `dig` command.

The laboratory environment showed the domain resolving to an internal test address:

`10.0.2.101`

DNS information including the DNS server and answer section was inspected during the experiment.

The DNS traffic was also investigated using network-analysis tools.

### Evidence

- `dns-spoofing-attack.png`
- `dns-spoofing-verification-netwag.png`

The laboratory screenshots show DNS queries, DNS responses and the use of Netwag tools for DNS-related testing. :contentReference[oaicite:2]{index=2}

---

## 4. Learning Outcomes

This laboratory provided practical experience with:

1. Understanding how SQL injection can affect vulnerable authentication systems.
2. Demonstrating authentication bypass in a controlled laboratory environment.
3. Understanding the role of the HOST file in local name resolution.
4. Analysing DNS queries and responses using `dig`.
5. Understanding the concept of DNS spoofing.
6. Observing DNS traffic using network-analysis tools.
7. Understanding the importance of input validation and secure DNS configuration.

---

## Tools Used

- Ubuntu Linux
- Firefox
- Wireshark
- `dig`
- Netwag
- Virtual machines

## Security Relevance

The exercises demonstrate why applications and network infrastructure must be securely configured.

Important defensive measures include:

- Proper input validation
- Parameterised SQL queries
- Secure authentication mechanisms
- Protection of local HOST configuration
- DNS security controls
- Monitoring and analysis of suspicious DNS traffic
- Network segmentation and controlled laboratory environments

---

## Disclaimer

All activities documented in this folder were performed in an authorised educational cybersecurity laboratory environment using controlled virtual machines.

The techniques were used for academic learning, security testing and understanding defensive cybersecurity concepts.
