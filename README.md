# Infoman

**A passive reconnaissance dashboard for penetration testers and security analysts.**

Enter an IP address, domain or URL and Infoman pulls together open ports, known CVEs, hosting details, SSL/TLS certificate, DNS records, subdomains and security headers from public sources, all in one clean view. It runs entirely in the browser as a single HTML file, with no backend or install needed.

## Features

- **Target overview:** quick summary of the host, IP and risk level
- **Open ports and services:** exposed ports and detected software and tags
- **Known CVEs:** vulnerabilities associated with the target's exposed services
- **Hosting and network:** ASN, ISP, geolocation and hosting provider
- **Subdomain discovery:** from certificate transparency logs
- **SSL/TLS certificate:** issuer, validity and related details
- **DNS and mail security:** DNS records plus SPF / DMARC checks
- **Security headers:** HTTP header grading via MDN Observatory
- **Google dorking:** ready-made dorks for the target
- **Next-step commands:** suggested follow-up testing commands
- **Dark / light theme:** Cyber Purple UI with a theme toggle

## Data sources

| Source | Used for |
|---|---|
| dns.google | DNS records |
| crt.sh | Subdomains and certificates (CT logs) |
| Shodan InternetDB | Open ports, services, CVEs |
| ipwho.is | Geolocation and hosting info |
| MDN Observatory | Security header analysis |

> This tool is **passive**. Your browser queries the public sources above and sends nothing directly to the target. The one exception is MDN Observatory, which makes a single normal HTTPS request to the site to check its headers.

## Usage

1. Clone the repo or download `index.html`
2. Open it in any modern browser
3. Enter a domain, IP or URL and click **Start scan**

Or host it for free with **GitHub Pages**: Settings → Pages → Source: *Deploy from a branch* → `main` / `(root)`. Your site will be live at `https://<your-username>.github.io/<repo-name>/`.

## Disclaimer

Infoman is intended for **authorized security testing, education and research only**. Only scan systems you own or have explicit permission to assess. The author is not responsible for misuse.

## Tech stack

HTML, Tailwind CSS (CDN), vanilla JavaScript. Single file, zero dependencies to install.

## License

MIT. See [LICENSE](LICENSE).
