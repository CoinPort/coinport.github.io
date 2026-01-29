# CoinPort Exchange Bug Bounty Program

CoinPort values the work of security researchers and encourages responsible disclosure of security vulnerabilities. This page outlines the scope and process for reporting potential security issues.

## Responsible investigation and disclosure

We ask that all research and reporting be conducted responsibly and in good faith. This includes:

- Do not violate the privacy of other users, access non-public data, disrupt services, or destroy data.
- Only test against accounts you own and control.
- Do not attempt social engineering, physical attacks, spam, denial-of-service (DDoS), or similar activities.
- Report vulnerabilities directly and privately to CoinPort.
- Allow reasonable time for investigation and remediation before any public disclosure.
- Avoid actions that could reasonably be interpreted as malicious or disruptive.

## Scope and eligibility

Vulnerabilities that materially impact the security of CoinPort systems or the integrity of user funds may be eligible for a reward, at CoinPort’s sole discretion.

Examples of issues that may be eligible include:

- Cross-site scripting (XSS)
- Cross-site request forgery (CSRF)
- Authentication or authorization bypass
- Privilege escalation
- Code injection or remote code execution
- Leakage of sensitive user or system data
- Clickjacking affecting sensitive actions

### In-scope domains

- `coinport.com.au`
- `www.coinport.com.au`
- `api.coinport.com.au`

Reports relating to `doc.coinport.com.au` are generally out of scope unless the issue is critical, as this site is isolated from user data and authentication systems.

## Out of scope

The following are not eligible for rewards:

- Issues on third-party services or integrations, unless they directly compromise CoinPort systems.
- Vulnerabilities requiring physical access, social engineering, spam, or denial-of-service attacks.
- Issues affecting outdated or unpatched browsers or operating systems.
- Vulnerabilities in third-party applications using CoinPort APIs.
- Issues that are not reproducible or lack sufficient detail.
- Issues already known to CoinPort or previously reported (reward goes to the first valid reporter).
- Issues that do not present a meaningful security risk.

## Rewards

- The minimum reward for eligible vulnerabilities is the equivalent of **AUD $100 in USDT**.
- Higher rewards may be offered for severe or high-impact vulnerabilities, at CoinPort’s discretion.
- Only one reward will be issued per unique vulnerability.
- Rewards are payable only after completion of required identity verification (KYC), in accordance with AML obligations.

## Severity classification

**Critical**
- Remote code execution
- Ability to arbitrarily manipulate account balances or funds

**High**
- Authentication bypass
- Privilege escalation allowing access to sensitive data or funds

**Medium**
- CSRF affecting non-critical actions
- User de-anonymisation

**Low**
- Limited exposure of low-sensitivity information
- Mitigable phishing vectors

## Reporting a vulnerability

Please submit reports to:  
**support@coinport.com.au**

Include:
- A clear description of the issue
- Potential impact
- Steps to reproduce or proof of concept

Please allow up to **five (5) business days** for initial review. Due to volume, we may only respond to reports that are eligible for a reward.
