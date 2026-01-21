# 3a-1 Domain, DNS and TLS Certificates with Let's Encrypt
Lab Setup and Tasks:
- Launch Ubuntu VM using Amazon EC2, Azure, or DigitalOcean.
- Ensure inbound ports 22 (SSH), 80 (HTTP), and 443 (HTTPS) are open.
- Install Apache: sudo apt install apache2.
- Record public IP address of the VM. Access in browser to confirm Apache page.
- Register a domain (Namecheap, GoDaddy, Cloudflare, Route 53, etc).
- Create an A record pointing your domain to the public IP of your server.


- Wait for DNS propagation and test with browser, ping, and nslookup.

- Install Certbot: sudo apt install certbot python3-certbot-apache.
<img width="937" height="665" alt="image" src="https://github.com/user-attachments/assets/2402db79-829e-470e-aa83-a3a8fc447dde" />


- Run: sudo certbot --apache to generate and install the certificate.


# Reflection Questions
- What is the role of DNS in Internet presence? 

DNS acts as the internet's phonebook, translating human-friendly domain names (like https://www.google.com/search?q=google.com) into machine-readable IP addresses.

- Why does DNS propagation take time? 

Propagation takes time because DNS records are cached by various servers worldwide, and it can take up to 48 hours for those caches to expire and update with your new IP information.

- How does Let’s Encrypt validate domain ownership? 

Let's Encrypt uses an automated challenge (ACME protocol) where it looks for a specific file or DNS record on your server to prove you have administrative control over the domain.

- What are the risks if TLS is not configured on a public-facing site? 

Without TLS, data is sent in "plain text," making it vulnerable to "Man-in-the-Middle" attacks where hackers can intercept passwords, credit card numbers, or personal info.

- What could happen if you leave your cloud VM running for months?

Leaving a VM running indefinitely can lead to significant financial costs if you exceed free-tier limits, and it increases the risk of the server being discovered and exploited by automated botnets.















