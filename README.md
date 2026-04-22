![Banner](image/image.png)
# The-Capsule

The-Capsule is an AI cyber security tool with strong bypass power, with this all developers can easily find website vulnerabilities


## 1. Reconnaissance Methods (Information Gathering)

| Method | Endpoint/Feature | Function |
|--------|------------------|----------|
| Recursive Subdomain Mining | api, dev, admin, stg | Searches for common subdomains and performs recursive discovery down to levels like v1.dev.target.com |
| Ghost-Referer & Header Spoofing | X-Forwarded-For, Referer | Spoofs IP and sets Referer to appear as traffic from Google to bypass basic WAF protection |

## 2. F12 Inspector Simulation Methods

| Method | Endpoint/Feature | Function |
|--------|------------------|----------|
| Application Tab Simulation | localStorage.setItem, sessionStorage | Identifies data stored in the user's browser |
| Network Tab Simulation | fetch(), axios(), ajax() | Detects API calls (XHR/Fetch) within JavaScript code |
| Console Log Sniffing | console.log, console.debug | Captures console messages that may unintentionally leak technical info or credentials |

## 3. Deep JS Mining & Extraction Methods

| Method | Endpoint/Feature | Function |
|--------|------------------|----------|
| Secret & Token Hunting | AWS_ACCESS_KEY, secret, api_key, password | Searches for sensitive keys using Regex |
| JWT Detection | eyJ... (JWT token) | Detects JWT patterns with Auto Bridge feature for session hijacking |
| Endpoint Discovery | /api/v1/admin | Extracts hidden internal URL paths from JS files for further mapping |

## 4. Vulnerability Auditing Methods

| Method | Endpoint/Feature | Function |
|--------|------------------|----------|
| CORS Misconfiguration | Origin: evil-attacker.com | Tests CORS vulnerability by checking Access-Control-Allow-Origin response |
| Source Map Exposure | .js.map | Accesses source map files to reconstruct original readable code |
| Asset Fuzzing | .env, .git/config, .aws/credentials | Brute-forces sensitive folders exposed to the public |

## 5. Reporting Methods (Auto-Bridge Protocol)

| Method | Endpoint/Feature | Function |
|--------|------------------|----------|
| Full Access Key Export | JWT, session cookies, API keys | Collects all "golden findings" for direct copying |
| Risk Scoring | CRITICAL, HIGH | Determines security status based on number of tokens or sensitive files found |

## Conclusion

This script is a highly specific **Automated OSINT & Vulnerability Scanner**. In conclusion, it is a "credential harvesting" tool. Unlike general scanners that look for heavy technical flaws (like SQLi or XSS), this script focuses on **Human Error** and **Development Leaks**. It works by "draining" all client-side (frontend) information that developers often underestimate, yet contains access keys to the backend system.

### Key Strengths

| Strength | Description |
|----------|-------------|
| **Smart F12 Simulation** | Doesn't just read HTML, but "reads" JavaScript logic to find how the app communicates with the server (XHR/Fetch calls) |
| **Auto-Extraction (Bridge)** | Extremely powerful at extracting full JWT tokens and Cookies — essentially "duplicate keys" to log in without a password |
| **Deep Recon** | Recursive subdomain searching up to second level (e.g., v1.dev.target.com) can find staging servers with weaker protection |
| **Anonymity Bypass** | Header spoofing (X-Forwarded-For, Random User-Agent) helps avoid simple IP-based firewall blocks |

### How Dangerous Is It?

**Level: High Risk**

This tool is very dangerous because its target is **active credentials**.

| Risk Factor | Explanation |
|-------------|-------------|
| **Instant Exploitation** | If it finds an active .env or JWT, attackers don't need complex hacking — just copy the token and log in as admin |
| **Silent Monitoring** | Only uses GET/HEAD requests (like a normal browser), often doesn't trigger IDS alarms |
| **Leakage Point** | Can find Source Maps, letting attackers see the original app code as if they were the developer |

### Win Rate (Success Rate)

| Target Type | Estimated Win Rate | Explanation |
|-------------|--------------------|-------------|
| **Large Corporate Sites** | 10% - 20% | Security is tight, but often leaks in "dev" or "test" subdomains |
| **Startups / New Websites** | 40% - 60% | Often rush to deploy without cleaning .map or .env files |
| **Government/Local Sites** | 50% - 70% | Often have misconfigured CORS or exposed .git folders |

**Average Effectiveness:** **35% - 50%** to obtain at least one piece of sensitive information (internal API endpoint, internal IP, or server info).

> **Quick Insight:** This tool is a "door opener." It may not bring down a building, but it's very good at finding windows left unlocked or keys left under the flower pot.

### Security Note

Is there any specific part of this tool's scan results you want to strengthen the security system against?

# installation
Nodejs
```bash
npm install capsule 
```
Python
```bash
pip install thecapsule 
```

# ⚠️ CRITICAL DISCLAIMER & WARNING

**THIS TOOL IS FOR EDUCATIONAL AND AUTHORIZED SECURITY RESEARCH PURPOSES ONLY.**

The use of this software for scanning targets without prior mutual consent is **ILLEGAL**. It is the end user's responsibility to obey all applicable local, state, and federal laws. 

**The developer ("The Author") assumes no liability and is not responsible for:**
* Any misuse or damage caused by this program.
* Any illegal activities conducted using the features of this tool.
* Any data loss or legal consequences resulting from the use of this script.

**BY USING THIS TOOL, YOU AGREE TO THESE TERMS.** 


> ⚠️ **Disclaimer:** Developer tools and our party are not responsible for the events that you create.