# Hacker Bear redirect site

## What this is

A one-page static site that sends visitors from hackerbear.com.au to https://acratic.com.au/. It uses a meta refresh and a canonical link, with no JavaScript.

GitHub Pages allows one custom domain per site, which is why this redirect lives in a second repository separate from the Acratic Professional Services website.

## Publishing

- GitHub Pages publishes from the main branch root.
- Set the custom domain to hackerbear.com.au in the repo under Settings > Pages.
- Tick Enforce HTTPS once it becomes available. GitHub says this can take up to 24 hours.

## DNS records

Verified against GitHub's Pages documentation on 2026-11-07.

| Record | Name | Value |
| --- | --- | --- |
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| AAAA | @ | 2606:50c0:8000::153 |
| AAAA | @ | 2606:50c0:8001::153 |
| AAAA | @ | 2606:50c0:8002::153 |
| AAAA | @ | 2606:50c0:8003::153 |
| CNAME | www | GITHUB-ACCOUNT.github.io |

Replace GITHUB-ACCOUNT with the GitHub user or organisation name that owns the repo.

## Check

```bash
dig hackerbear.com.au +noall +answer -t A
dig www.hackerbear.com.au +noall +answer -t CNAME
```

---

*© Acratic Professional Services. All rights reserved.*
