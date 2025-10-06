# Subdomain Takeover PoC

## ⚠️ Security Research - Proof of Concept

### Vulnerability Details
- **Affected Subdomain:** brandguide.github.com
- **CNAME Target:** github.github.io  
- **Vulnerability Type:** Subdomain Takeover via GitHub Pages
- **Discovery Date:** October 6, 2025
- **Status:** Unclaimed GitHub Pages site

### Technical Details
The subdomain `brandguide.github.com` has a DNS CNAME record pointing to `github.github.io`, but no GitHub Pages site was configured at this location. This allows any GitHub user to claim the subdomain by creating a repository named "brandguide" and enabling GitHub Pages.

### Impact Assessment
- **Phishing:** Attackers can host fake GitHub login pages
- **Session Hijacking:** Potential to steal cookies from *.github.com domain
- **XSS Attacks:** Inject malicious JavaScript affecting GitHub users
- **Brand Damage:** Host inappropriate content on official GitHub subdomain
- **Trust Exploitation:** Users inherently trust github.com domains

### Proof of Concept
This page serves as proof that the subdomain was successfully claimed through GitHub Pages, demonstrating the vulnerability.

### Timeline
- **Discovery:** October 6, 2025
- **PoC Created:** October 6, 2025
- **Reported:** [Pending]

### Remediation
1. Remove the CNAME DNS record for brandguide.github.com
2. Or configure an official GitHub Pages site at this location
3. Audit all *.github.com subdomains for similar issues

---

**Note:** This is ethical security research conducted for responsible disclosure. This page will be removed immediately after the vulnerability is confirmed and fixed by GitHub Security Team.

**Researcher:** [Your Bug Bounty Profile/Contact]
