# Common Network Security Threats

## 1. Introduction

Network security is essential for protecting computer systems, networks, applications, and sensitive information from unauthorized access, disruption, and manipulation.

Some common network security threats include Denial-of-Service (DoS) and Distributed Denial-of-Service (DDoS) attacks, Man-in-the-Middle (MITM) attacks, IP spoofing, and DNS poisoning or spoofing. Understanding how these attacks work and applying appropriate security controls can reduce their impact.

---

## 2. Denial-of-Service (DoS) and Distributed Denial-of-Service (DDoS)

### How It Works

A Denial-of-Service (DoS) attack attempts to make a system, service, application, or network unavailable to legitimate users by exhausting its resources.

A Distributed Denial-of-Service (DDoS) attack uses multiple systems to generate traffic toward the target. Because traffic comes from many sources, DDoS attacks can be more difficult to block than attacks originating from a single system.

### Real-World Example

DNS amplification is an example of a DDoS technique. An attacker can send requests to DNS servers using the victim's IP address as the source address. The DNS servers may then send responses toward the victim, creating a large amount of unwanted traffic.

### Impact

- Website or application unavailability
- Network congestion
- Reduced system performance
- Loss of business operations
- Financial losses
- Damage to reputation

### Mitigation

1. Use traffic filtering and rate limiting.
2. Use DDoS protection services or content delivery networks.
3. Continuously monitor network traffic and maintain an incident-response plan.

---

## 3. Man-in-the-Middle (MITM) Attack

### How It Works

A Man-in-the-Middle attack occurs when an attacker positions themselves between two communicating parties and intercepts or potentially modifies their communication.

The attacker may observe sensitive information or alter communication before forwarding it to the intended destination.

### Real-World Example

A common example is a victim connecting to a malicious or unauthorized Wi-Fi access point that appears legitimate. The attacker may attempt to intercept network traffic passing through the access point.

### Impact

- Theft of usernames and passwords
- Exposure of sensitive information
- Session interception
- Modification of communications
- Unauthorized account access
- Privacy violations

### Mitigation

1. Use HTTPS and TLS for secure communication.
2. Avoid unknown or suspicious Wi-Fi networks.
3. Use strong authentication and multi-factor authentication.

---

## 4. IP Spoofing

### How It Works

IP spoofing occurs when an attacker modifies the source IP address of network packets so that they appear to originate from another system.

Attackers may use spoofed addresses to hide the actual source of traffic or to support other attacks such as reflection-based DDoS attacks.

### Real-World Example

A common example is a reflection/amplification DDoS attack. An attacker sends requests to an intermediary service while replacing the source IP address with the victim's IP address. The intermediary then sends responses to the victim.

### Impact

- Difficulty identifying the source of malicious traffic
- Participation in reflection attacks
- Network disruption
- Attempts to bypass poorly configured access controls
- Increased difficulty during incident investigation

### Mitigation

1. Use ingress and egress filtering.
2. Implement source-address validation.
3. Monitor unusual traffic patterns and unexpected source addresses.

---

## 5. DNS Poisoning / DNS Spoofing

### How It Works

The Domain Name System (DNS) translates human-readable domain names into IP addresses.

DNS poisoning or spoofing occurs when false DNS information is introduced so that users are directed to an incorrect or attacker-controlled destination.

### Real-World Example

Attackers may compromise accounts responsible for managing DNS records and modify records so that web or email traffic is redirected to infrastructure controlled by the attackers.

### Impact

- Redirection to malicious websites
- Credential theft
- Phishing attacks
- Interception of traffic
- Email redirection
- Service disruption

### Mitigation

1. Protect DNS management accounts with strong passwords and multi-factor authentication.
2. Use DNSSEC where appropriate.
3. Monitor DNS records and investigate unauthorized changes.

---

## 6. Comparison of Network Security Threats

| Threat | Attack Vector | Who Is at Risk? | Difficulty | Ease of Mitigation |
|---|---|---|---|---|
| DoS/DDoS | Excessive traffic, resource exhaustion, reflection/amplification | Websites, servers, organizations | Medium to High | Medium |
| MITM | Interception or modification of network communication | Users and organizations | Medium | Medium to High |
| IP Spoofing | Forged source IP addresses | Networks and servers | Medium | Medium |
| DNS Poisoning/Spoofing | Manipulation of DNS information | Users, organizations and services | Medium to High | Medium |

---

## 7. Conclusion

Network security threats can affect the confidentiality, integrity, and availability of information and services.

Three important takeaways for a network administrator are:

1. **Monitor network activity continuously.**  
   Unusual traffic, DNS changes, and unexpected communication patterns should be investigated promptly.

2. **Use layered security controls.**  
   Firewalls, secure protocols, authentication, access controls, DNS security, filtering, and monitoring should work together.

3. **Maintain secure systems and configurations.**  
   Regular updates, secure configurations, strong authentication, and documented incident-response procedures can reduce the likelihood and impact of network attacks.

Understanding common threats and applying appropriate preventive and detective controls is an important part of maintaining a secure network environment.

---

## 8. References

1. National Institute of Standards and Technology (NIST). **SP 800-189: Resilient Interdomain Traffic Exchange: BGP Security and DDoS Mitigation.**

2. National Institute of Standards and Technology (NIST). **Man-in-the-Middle Attack – CSRC Glossary.**

3. Cybersecurity and Infrastructure Security Agency (CISA). **DDoS Quick Guide.**

4. Cybersecurity and Infrastructure Security Agency (CISA). **Mitigate DNS Infrastructure Tampering.**

5. National Institute of Standards and Technology (NIST). **Computer Security Incident Handling Guide – SP 800-61.**
