# Neptune Ecosystem Security Audits

> Preliminary LLM-assisted security audits of applications, platforms, and services within the Neptune ecosystem to help users make informed decisions.

**Last Updated:** October 19, 2025  
**Status:** Active  
**Disclaimer:** These are preliminary analyses based on code review and architectural assessment. Users should conduct their own due diligence.

---

## 📋 Table of Contents

- [Overview](#overview)
- [Wallet Audits](#wallet-audits)
- [Quick Comparison](#quick-comparison)
- [Recommendations](#recommendations)
- [How to Use This Repository](#how-to-use-this-repository)
- [Contributing](#contributing)
- [Disclaimer](#disclaimer)

---

## Overview

This repository contains security and privacy analyses of applications and services in the Neptune cryptocurrency ecosystem. Our goal is to provide transparent, technical assessments to help users understand the privacy and security implications of the tools they use.

### What We Analyze

- **Architecture:** How the software is designed
- **Privacy:** What data is exposed and to whom
- **Security:** Protection against attacks and compromise
- **Trust Model:** What parties you must trust
- **Legal Exposure:** Law enforcement access capabilities
- **Code Quality:** Review of implementation

### Methodology

1. **Code Review:** Examine source code and dependencies
2. **Architecture Analysis:** Understand data flows and system design
3. **Threat Modeling:** Identify potential risks
4. **Comparison:** Benchmark against alternatives
5. **Documentation:** Provide clear, actionable information

---

## Wallet Audits

### 🟢 Neptune Core Wallet (seaoffreedom)

**Status:** ✅ RECOMMENDED  
**Privacy Score:** ★★★★★ (10/10)  
**Architecture:** Local full node  
**Repository:** [github.com/seaoffreedom/neptune-core-wallet](https://github.com/seaoffreedom/neptune-core-wallet)

**Key Characteristics:**

- Runs complete Neptune node locally on your computer
- ALL data stays on your machine (except P2P blockchain sync)
- Zero third-party servers
- Trustless architecture
- Complete privacy and sovereignty

**Documentation:**

- 📄 [Security Analysis Report](./wallets/neptune-core-wallet/SECURITY_ANALYSIS_REPORT.md)
- 📄 [Law Enforcement Capabilities](./wallets/neptune-core-wallet/LAW_ENFORCEMENT_CAPABILITIES.md)
- 📄 [Quick Reference Guide](./wallets/neptune-core-wallet/QUICK_REFERENCE.md)

**Bottom Line:** This is what cryptocurrency was meant to be - true financial sovereignty with complete privacy.

---

### 🟠 VxBlocks Neptune Wallet

**Status:** ⚠️ USE WITH CAUTION  
**Privacy Score:** ★★☆☆☆ (2/10)  
**Architecture:** Centralized server (`nptwallet.vxb.ai`)  
**Repository:** [github.com/VxBlocks/neptune-wallet-app](https://github.com/VxBlocks/neptune-wallet-app)

**Key Characteristics:**

- ALL transactions route through VxBlocks server
- Server sees complete transaction history
- Convenient and user-friendly
- Centralized architecture
- Requires trust in VxBlocks

**Documentation:**

- 📄 [Security Analysis Report](./wallets/vxblocks-neptune-wallet/SECURITY_ANALYSIS_REPORT.md)
- 📄 [Law Enforcement Capabilities](./wallets/vxblocks-neptune-wallet/LAW_ENFORCEMENT_CAPABILITIES.md)
- 📄 [Quick Reference Guide](./wallets/vxblocks-neptune-wallet/QUICK_REFERENCE.md)

**Bottom Line:** Trades privacy for convenience. Good UX, but complete transaction visibility to VxBlocks and law enforcement.

---

## Quick Comparison

### Privacy & Security

| Aspect                     | Neptune Core Wallet                  | VxBlocks Wallet          |
| -------------------------- | ------------------------------------ | ------------------------ |
| **Privacy Level**          | 🟢 Complete (10/10)                  | 🔴 Minimal (2/10)        |
| **Architecture**           | 🟢 Local full node                   | 🔴 Centralized server    |
| **Trust Required**         | 🟢 None (trustless)                  | 🔴 VxBlocks + Government |
| **Transaction Visibility** | 🟢 Private                           | 🔴 Server sees all       |
| **IP Privacy**             | 🟢 Protected (P2P)                   | 🔴 Logged by server      |
| **Surveillance Risk**      | 🟢 Very low                          | 🔴 Very high             |
| **Law Enforcement Access** | 🟢 Requires warrant + device seizure | 🔴 Simple subpoena       |
| **Censorship Resistance**  | 🟢 High                              | 🔴 Low                   |
| **Data Collection**        | 🟢 None                              | 🔴 Complete              |

### User Experience

| Aspect                | Neptune Core Wallet       | VxBlocks Wallet     |
| --------------------- | ------------------------- | ------------------- |
| **Setup Time**        | 🟡 Slow (blockchain sync) | 🟢 Fast (instant)   |
| **Disk Space**        | 🟡 Large (20+ GB)         | 🟢 Small            |
| **Ease of Use**       | 🟡 Medium                 | 🟢 Easy             |
| **Mobile Support**    | 🔴 Desktop only           | 🟢 Mobile + Desktop |
| **Internet Required** | 🟢 P2P only               | 🔴 Always (server)  |
| **Update Frequency**  | 🟡 Manual                 | 🟢 Automatic        |

---

## Recommendations

### For Privacy-Conscious Users

**✅ USE: Neptune Core Wallet (seaoffreedom)**

If you value:

- ✅ Financial privacy
- ✅ Self-sovereignty
- ✅ Trustless operation
- ✅ Protection from surveillance
- ✅ Censorship resistance
- ✅ True cryptocurrency principles

**This is your only good option.** The disk space and sync time are worth your privacy.

### For Journalists, Activists, Whistleblowers

**✅ STRONGLY RECOMMENDED: Neptune Core Wallet**

Enhanced setup:

1. Use Neptune Core Wallet (seaoffreedom)
2. Route through Tor (hide IP from P2P network)
3. Use dedicated machine for crypto only
4. Full disk encryption
5. Strong passwords
6. Offline signing for maximum security

**❌ DO NOT USE VxBlocks Wallet** - Complete transaction history exposed to potential adversaries.

### For Casual Users

**✅ STILL RECOMMENDED: Neptune Core Wallet**

Even if you "have nothing to hide":

- Privacy is a fundamental right
- Laws can change
- Your threat model can change
- Set good security practices now
- Support decentralization

**⚠️ If you choose VxBlocks Wallet:**

- Understand ALL transactions are visible to VxBlocks
- Subject to government subpoena
- Similar privacy to traditional banking
- Only use if you truly don't care about privacy

### For Developers

**✅ RECOMMENDED: Neptune Core Wallet**

Or use official Neptune CLI for maximum control.

Understand the architectures:

- Neptune Core Wallet = Official Neptune + nice GUI
- VxBlocks Wallet = Convenience wrapper around centralized server

---

## Recommendation Summary

```
┌─────────────────────────────────────────────────────┐
│                                                      │
│  Neptune Core Wallet (seaoffreedom)                  │
│  ══════════════════════════════════                  │
│  ✅ RECOMMENDED FOR ALL USERS                        │
│                                                      │
│  Privacy:           ★★★★★ (10/10)                   │
│  Security:          ★★★★★ (9/10)                    │
│  User Experience:   ★★★☆☆ (6/10)                    │
│                                                      │
│  This is the wallet you should use.                  │
│                                                      │
└─────────────────────────────────────────────────────┘

┌─────────────────────────────────────────────────────┐
│                                                      │
│  VxBlocks Neptune Wallet                             │
│  ════════════════════════                            │
│  ⚠️  USE WITH EXTREME CAUTION                        │
│                                                      │
│  Privacy:           ★★☆☆☆ (2/10)                    │
│  Security:          ★★★☆☆ (5/10)                    │
│  User Experience:   ★★★★★ (9/10)                    │
│                                                      │
│  Only if you don't care about privacy.               │
│  Understand you're trading sovereignty for ease.     │
│                                                      │
└─────────────────────────────────────────────────────┘
```

---

## Architecture Comparison

### Neptune Core Wallet (Local Node)

```
┌──────────────────────────────────────────────────┐
│            Your Computer (Complete Privacy)       │
├──────────────────────────────────────────────────┤
│                                                   │
│  You → Electron App                               │
│         ↓ (localhost only)                        │
│       neptune-cli (HTTP RPC)                      │
│         ↓ (localhost only)                        │
│       neptune-core (Full Node)                    │
│         ↓ (P2P encrypted)                         │
│       Neptune Blockchain Network                  │
│                                                   │
│  ✅ Everything local except P2P sync             │
│  ✅ No third-party servers                       │
│  ✅ Complete validation                          │
│  ✅ Zero data leakage                            │
│                                                   │
└──────────────────────────────────────────────────┘
```

### VxBlocks Wallet (Centralized)

```
┌──────────────────────────────────────────────────┐
│             Centralized Architecture              │
├──────────────────────────────────────────────────┤
│                                                   │
│  You → Tauri App                                  │
│         ↓ (internet)                              │
│       VxBlocks Server (nptwallet.vxb.ai)          │
│         ↓                                         │
│       Neptune Blockchain                          │
│                                                   │
│  ❌ All transactions through VxBlocks            │
│  ❌ Server sees everything                       │
│  ❌ IP addresses logged                          │
│  ❌ Subject to surveillance                      │
│                                                   │
│  Server Visibility:                               │
│  ├─ Every transaction                             │
│  ├─ All amounts                                   │
│  ├─ All addresses                                 │
│  ├─ Your IP address                               │
│  ├─ Activity patterns                             │
│  └─ Complete financial profile                    │
│                                                   │
└──────────────────────────────────────────────────┘
```

---

## How to Use This Repository

### Reading the Audits

Each wallet has three documents:

1. **SECURITY_ANALYSIS_REPORT.md**

   - Comprehensive technical analysis
   - Architecture deep-dive
   - Code review findings
   - Security assessment
   - Detailed comparisons

2. **LAW_ENFORCEMENT_CAPABILITIES.md**

   - What authorities can access
   - Legal processes required
   - Surveillance capabilities
   - User protections
   - Real-world scenarios

3. **QUICK_REFERENCE.md**
   - Summary for quick decisions
   - Key findings highlighted
   - Actionable recommendations
   - Setup instructions

### Decision Flow

```
1. Read QUICK_REFERENCE.md for overview
   ↓
2. If you need details:
   └→ Read SECURITY_ANALYSIS_REPORT.md

3. If you're a high-risk user:
   └→ Read LAW_ENFORCEMENT_CAPABILITIES.md

4. Make informed decision
```

---

## Key Findings Summary

### What We Discovered

#### Neptune Core Wallet (seaoffreedom)

**Positive:**

- ✅ Truly decentralized - runs full node locally
- ✅ Complete privacy - no data leaves your machine
- ✅ Trustless - no third parties involved
- ✅ Safe modifications to official Neptune (HTTP RPC instead of tarpc)
- ✅ Open source and auditable
- ✅ Strong Fourth Amendment protections

**Minor Notes:**

- ⚠️ Uses VxBlocks block explorer for optional links (user-initiated only)
- ⚠️ Uses CoinGecko for price display (optional feature)
- ⚠️ Requires disk space and sync time (acceptable trade-off)

**Verdict:** Excellent privacy-preserving wallet that embodies cryptocurrency principles.

#### VxBlocks Neptune Wallet

**Positive:**

- ✅ Private keys stay local (encrypted)
- ✅ User-friendly interface
- ✅ Fast setup
- ✅ Mobile support
- ✅ Can self-host server (advanced)

**Concerns:**

- 🔴 ALL transactions route through VxBlocks server
- 🔴 Complete transaction visibility to VxBlocks
- 🔴 IP addresses logged
- 🔴 Subject to government subpoena (no warrant needed)
- 🔴 Centralized architecture defeats cryptocurrency purpose
- 🔴 Complete behavioral profiling possible
- 🔴 No privacy policy or transparency reports visible

**Verdict:** Convenient but sacrifices privacy for ease of use. Similar to traditional banking.

---

## Threat Model Considerations

### Who Should Definitely Use Neptune Core Wallet

- 🎯 Journalists handling sensitive sources
- 🎯 Activists in authoritarian regimes
- 🎯 Whistleblowers
- 🎯 Privacy advocates
- 🎯 Anyone in high-risk situation
- 🎯 Users who value sovereignty
- 🎯 Anyone who believes privacy is a right

### Who Might Accept VxBlocks Wallet

- 💭 Casual users who don't care about privacy
- 💭 Users already fully identified (KYC exchanges)
- 💭 Making small, non-sensitive transactions
- 💭 Need mobile support (no alternative yet)
- 💭 Want instant setup
- 💭 Willing to self-host the server

**Important:** Even if you think you "have nothing to hide," privacy matters. Your threat model can change. Laws can change. Choose wisely.

---

## Comparison to Other Financial Systems

### Privacy Levels

```
Privacy (10 = Best):

Neptune Core Wallet     ████████████████████  10/10  ✅
Physical Cash           ███████████████████░   9/10  ✅
Official Neptune CLI    ████████████████████  10/10  ✅
─────────────────────────────────────────────────────
Bitcoin Core (Full)     ████████████████░░░░   8/10  ⚠️
VxBlocks Wallet         ██░░░░░░░░░░░░░░░░░░   2/10  🔴
KYC Crypto Exchange     █░░░░░░░░░░░░░░░░░░░   1/10  🔴
Traditional Bank        █░░░░░░░░░░░░░░░░░░░   1/10  🔴
CBDC (Central Bank)     ░░░░░░░░░░░░░░░░░░░░   0/10  🔴
```

### Surveillance Resistance

```
Difficulty for Law Enforcement to Access:

Neptune Core Wallet     ████████████████████  Very Hard
Physical Cash           ███████████████████░  Very Hard
─────────────────────────────────────────────────────
Bitcoin Core (Full)     ████████████████░░░░  Hard
Monero (Full Node)      ████████████████████  Very Hard
─────────────────────────────────────────────────────
VxBlocks Wallet         ███░░░░░░░░░░░░░░░░░  Very Easy
KYC Crypto Exchange     ██░░░░░░░░░░░░░░░░░░  Trivial
Traditional Bank        █░░░░░░░░░░░░░░░░░░░  Trivial
```

---

## Contributing

We welcome contributions to improve these audits:

### How to Contribute

1. **Report Issues**

   - Found inaccuracies? Open an issue
   - Have additional information? Let us know

2. **Submit Audits**

   - Follow the same format (3 documents per project)
   - Maintain objectivity
   - Cite sources

3. **Update Existing Audits**
   - Software changes? Update the analysis
   - New findings? Submit a pull request

### Audit Template

Each audit should include:

1. SECURITY_ANALYSIS_REPORT.md
2. LAW_ENFORCEMENT_CAPABILITIES.md
3. QUICK_REFERENCE.md

### Guidelines

- Be objective and factual
- Cite sources and evidence
- Explain technical concepts clearly
- Consider diverse user threat models
- Update when software changes

---

## Disclaimer

### Important Notes

**These are preliminary analyses based on:**

- Code review and architectural assessment
- Public information
- LLM-assisted analysis
- Security best practices

**Limitations:**

- Cannot guarantee 100% accuracy
- Software changes over time
- Threat landscape evolves
- Individual circumstances vary

**User Responsibility:**

- Conduct your own due diligence
- Verify information independently
- Understand your personal threat model
- Consult security professionals for critical applications
- Follow security best practices
- Keep software updated

### No Accusations

This repository makes no accusations of malicious intent against any developers or companies. Different projects serve different user needs and make different trade-offs.

**Our goal:** Provide transparent information so users can make informed decisions based on their values and threat models.

---

## Resources

### Official Neptune

- **Website:** https://neptune.cash
- **Main Repository:** https://github.com/Neptune-Crypto/neptune-core
- **Documentation:** https://neptune.cash/docs

### Audited Projects

- **Neptune Core Wallet:** https://github.com/seaoffreedom/neptune-core-wallet
- **VxBlocks Neptune Wallet:** https://github.com/VxBlocks/neptune-wallet-app
- **VxBlocks Server:** https://github.com/VxBlocks/neptune-wallet-core

### Security Resources

- **EFF Surveillance Self-Defense:** https://ssd.eff.org/
- **Privacy Guides:** https://www.privacyguides.org/
- **Cryptocurrency Security:** https://bitcoin.org/en/secure-your-wallet

---

## Updates

**Current Version:** 1.0  
**Last Updated:** October 19, 2025  
**Next Review:** When significant changes occur in analyzed projects

### Recent Changes

- **2025-10-19:** Initial audits of Neptune Core Wallet and VxBlocks Neptune Wallet
- **2025-10-19:** Repository structure established
- **2025-10-19:** Comprehensive comparison documentation added

---

## Contact

For questions, concerns, or contributions:

- Open an issue on GitHub
- Review existing documentation
- Verify information independently

---

## License

This repository is provided for educational and informational purposes.

See [LICENSE](./LICENSE) for details.

---

**Remember: Privacy is a right, not a privilege.**

**Choose tools that respect your sovereignty.**

**Neptune Core Wallet protects your privacy. VxBlocks Wallet sacrifices it for convenience.**

**Make an informed choice.**
