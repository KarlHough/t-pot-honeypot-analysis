# 🔍 Honeypot Attack Analysis

## 📊 Overview

A T-Pot honeypot was deployed on a public cloud server to capture real-world attack traffic. The system was intentionally exposed to observe attacker behaviour, including scanning activity, credential attacks, and service probing.

---

## ⏱️ Attack Timeline Analysis

Analysis of the timeline shows that attack activity occurred in bursts rather than at a constant rate.

* Distinct spikes in activity were observed over short time periods
* Between spikes, a consistent level of low-volume traffic remained

This behaviour indicates:

* Automated tools performing rapid scanning
* Followed by continued background probing

This pattern is consistent with bot-driven attacks rather than manual intrusion attempts.

---

## 🌐 Source of Attacks

The honeypot received traffic from multiple external IP addresses, suggesting:

* Distributed attack sources
* Continuous internet-wide scanning
* Likely use of automated infrastructure or botnets

No single attacker dominated activity, reinforcing the presence of widespread automated probing.

---

## 🚪 Targeted Ports Analysis

The most frequently targeted ports included:

* **445 (SMB)** → commonly associated with exploitation attempts
* **443 (HTTPS)** → indicates probing of secure web services
* **80 (HTTP)** → typical for web-based reconnaissance
* **53 (DNS)** → suggests service discovery or misconfiguration probing

A high number of requests were also observed on:

* **9997 (non-standard port)**

This indicates:

* Broad scanning across both standard and non-standard ports
* Attackers attempting to identify any exposed or misconfigured services

This behaviour is characteristic of opportunistic scanning rather than targeted attacks.

---

## 🔐 Credential Attack Analysis

Login attempts revealed the use of both common and non-standard credentials.

### Observed Usernames

* `root`
* `admin`
* `user`
* `sol`

### Observed Passwords

* `123456`
* `password`
* `sol`
* `solana`

Notably, the presence of:

* `sol`
* `solana`

suggests:

* Use of tailored wordlists
* Possible targeting of systems related to cryptocurrency environments

Additionally, many password attempts appeared only once, indicating:

* Password spraying techniques
* Large credential lists used by automated tools

---

## 🧠 Attack Behaviour Insights

The collected data highlights several key attacker behaviours:

* Automated port scanning across a wide range of ports
* Rapid bursts of connection attempts
* Use of common and weak credentials
* Occasional use of targeted or themed credential lists

Overall activity aligns with typical **internet background radiation**, where exposed systems are continuously scanned and attacked.

---

## 🛡️ Security Implications

The findings demonstrate that:

* Publicly exposed systems are quickly discovered and targeted
* Weak authentication mechanisms are actively exploited
* Attackers do not rely solely on common ports
* Automated attacks operate continuously without human intervention

---

## ✅ Recommendations

Based on the observed behaviour:

* Disable password-based SSH authentication
* Use strong, unique credentials
* Restrict access via firewall rules
* Minimise exposed services
* Implement monitoring and intrusion detection systems

---

## 📌 Conclusion

The honeypot successfully captured real-world attack activity, demonstrating the scale and persistence of automated threats on the internet.

The data shows that attackers employ both:

* Broad opportunistic scanning
* Targeted credential-based attempts

This reinforces the importance of securing publicly exposed systems and maintaining continuous monitoring.
