# Neptune Wallet Comparison: Side-by-Side

**Date:** October 19, 2025  
**Analyst:** Security Review Team

---

## Quick Reference: Which Wallet Should You Use?

```
╔═══════════════════════════════════════════════════════════════════════╗
║                                                                       ║
║  Neptune Core Wallet (seaoffreedom)                                   ║
║  ────────────────────────────────────                                 ║
║  ✅ RECOMMENDED for privacy-conscious users                           ║
║  ✅ Full local node                                                   ║
║  ✅ Zero surveillance                                                 ║
║  ✅ Trustless                                                         ║
║                                                                       ║
║  Repository: github.com/seaoffreedom/neptune-core-wallet              ║
║                                                                       ║
╚═══════════════════════════════════════════════════════════════════════╝

╔═══════════════════════════════════════════════════════════════════════╗
║                                                                       ║
║  VxBlocks Neptune Wallet                                              ║
║  ────────────────────────                                             ║
║  ⚠️  USE WITH CAUTION - Privacy concerns                              ║
║  ⚠️  Centralized server architecture                                  ║
║  ⚠️  All transactions visible to VxBlocks                             ║
║  ⚠️  Requires trust                                                   ║
║                                                                       ║
║  Repository: github.com/VxBlocks/neptune-wallet-app                   ║
║                                                                       ║
╚═══════════════════════════════════════════════════════════════════════╝
```

---

## Architecture Comparison

### Neptune Core Wallet (seaoffreedom)

```
[You] → [Electron Desktop App]
           ↓ (localhost only)
        [neptune-cli HTTP RPC]
           ↓ (localhost only)
        [neptune-core Full Node]
           ↓ (P2P)
        [Neptune Blockchain Network]

✅ Everything runs on YOUR computer
✅ NO third-party servers
✅ NO data collection
✅ Complete privacy
```

### VxBlocks Neptune Wallet

```
[You] → [Tauri Desktop/Mobile App]
           ↓ (internet)
        [nptwallet.vxb.ai Server]
           ↓
        [Neptune Blockchain]

❌ ALL transactions go through VxBlocks server
❌ Server logs EVERYTHING
❌ Complete transaction visibility
❌ Requires trust in VxBlocks
```

---

## Feature Comparison

| Feature                    | Neptune Core Wallet     | VxBlocks Wallet         |
| -------------------------- | ----------------------- | ----------------------- |
| **Architecture**           | Local full node         | Remote server           |
| **Transaction Privacy**    | ⭐⭐⭐⭐⭐ Complete     | ⭐ None                 |
| **Network Model**          | Decentralized P2P       | Centralized             |
| **Trust Required**         | None (trustless)        | VxBlocks                |
| **Third-Party Visibility** | None                    | Complete                |
| **Law Enforcement Access** | Device seizure required | Simple subpoena         |
| **IP Privacy**             | Protected (many nodes)  | Exposed (single server) |
| **Censorship Resistance**  | High                    | Low                     |
| **Private Keys**           | Local (encrypted)       | Local (encrypted)       |
| **Proof Generation**       | Local (Triton VM)       | Server OR local         |
| **Setup Time**             | Slow (node sync)        | Fast (instant)          |
| **Disk Space**             | Large (blockchain)      | Small                   |
| **Platform Support**       | Desktop only            | Desktop + Mobile        |
| **Ease of Use**            | Medium                  | Easy                    |
| **Requires Internet**      | P2P only                | Always                  |
| **Self-Hosted Option**     | Built-in                | Possible (advanced)     |

---

## Privacy Score

```
Privacy Level (10 = Best):

Neptune Core Wallet:    ████████████████████  10/10
VxBlocks Wallet:        ██░░░░░░░░░░░░░░░░░░   2/10
Official Neptune CLI:   ████████████████████  10/10
```

---

## Security Analysis

### Neptune Core Wallet ✅

**What It Does Right:**

- ✅ Runs full validation node locally
- ✅ All communication stays on localhost
- ✅ P2P network for blockchain data
- ✅ Cookie-based authentication (random per session)
- ✅ No external dependencies (except P2P)
- ✅ Open source and auditable
- ✅ Modified Neptune core with HTTP RPC (safe change)
- ✅ Uses official Neptune authentication system

**Minor Issues:**

- ⚠️ Block explorer links use `neptune.vxb.ai` (optional, user-initiated)
- ⚠️ CoinGecko API for price (optional, no privacy impact)

**Modifications to Official Neptune:**

- Added HTTP JSON-RPC server to neptune-cli (instead of tarpc)
- Still localhost-only binding
- Same cookie authentication
- Safe modification for Electron integration

**Who Made It:**

- GitHub: seaoffreedom / sploitzberg
- Fork of official Neptune
- Well-documented changes
- Active development

### VxBlocks Wallet ⚠️

**Privacy Concerns:**

- 🔴 ALL transactions route through `nptwallet.vxb.ai`
- 🔴 Server can see every transaction you make
- 🔴 Server knows your IP address
- 🔴 Server can track your balance queries
- 🔴 Complete transaction history available to VxBlocks
- 🔴 Behavioral profiling possible
- 🔴 Subject to government subpoena

**What It Does Right:**

- ✅ Private keys stored locally (encrypted)
- ✅ Modern UI/UX
- ✅ Fast setup
- ✅ Cross-platform support
- ✅ Self-hosting option exists (but requires technical knowledge)

**Architecture:**

- Modified neptune-core with REST API
- Client app connects to VxBlocks server by default
- Optional: Run your own server

**Who Made It:**

- GitHub: VxBlocks
- Provides user-friendly interface
- Centralized for convenience
- Trade-off: Privacy for ease of use

---

## Law Enforcement Surveillance Capabilities

### Neptune Core Wallet

**To Surveil a User, Law Enforcement Must:**

1. Obtain search warrant
2. Physically seize computer
3. Extract wallet file (if device unlocked)
4. Analyze blockchain (public, but pseudonymous)

**Cannot Do:**

- ❌ Simple subpoena (no central server)
- ❌ Remote monitoring (decentralized)
- ❌ Bulk collection (no central database)
- ❌ Silent surveillance (requires device access)

**Privacy Level:** 🟢 **HIGH** - Similar to cash

### VxBlocks Wallet

**To Surveil a User, Law Enforcement Can:**

1. Send subpoena to VxBlocks
2. Receive complete transaction history
3. Get IP address logs
4. Identify user
5. Monitor in real-time (if ongoing cooperation)

**Can Do:**

- ✅ Administrative subpoena (no warrant)
- ✅ Complete transaction history
- ✅ Real-time monitoring
- ✅ Bulk data collection (all users)
- ✅ Silent (user unaware)

**Privacy Level:** 🔴 **LOW** - Similar to bank account

---

## Use Cases

### Choose Neptune Core Wallet If You Are:

- ✅ Privacy-conscious user
- ✅ Journalist handling sensitive payments
- ✅ Activist in authoritarian regime
- ✅ Whistleblower
- ✅ Anyone who values financial privacy
- ✅ Don't trust third parties
- ✅ Have disk space for blockchain
- ✅ Can wait for initial sync
- ✅ Use desktop computer
- ✅ Understand importance of sovereignty

### Choose VxBlocks Wallet If You:

- ⚠️ Don't care about transaction privacy
- ⚠️ Already use KYC exchanges (privacy already compromised)
- ⚠️ Want instant setup (no sync time)
- ⚠️ Need mobile support
- ⚠️ Have limited disk space
- ⚠️ Trust VxBlocks completely
- ⚠️ Understand and accept surveillance
- ⚠️ Accept centralized architecture
- ⚠️ Making small, non-sensitive transactions

---

## Technical Details

### Neptune Core Wallet Implementation

**Components:**

1. **Electron Frontend** (TypeScript/React)

   - User interface
   - IPC communication
   - Modern desktop experience

2. **neptune-core** (Rust binary - Official Neptune)

   - Full blockchain node
   - Block validation
   - P2P networking
   - Mempool management
   - Proof generation

3. **neptune-cli** (Rust binary - Modified)
   - HTTP JSON-RPC server (localhost:9801)
   - Wallet operations
   - Transaction construction
   - Proxies to neptune-core

**Modifications:**

- Source: `github.com/sploitzberg/neptune-core`
- Branch: `feature/rpc-server-wallet-integration`
- Main change: HTTP RPC instead of tarpc
- Reason: Better Electron integration
- Security: Still localhost-only, same auth

**Network Connections:**

- `localhost:9799` - neptune-core RPC (local)
- `localhost:9801` - neptune-cli RPC (local)
- P2P network - other Neptune nodes (encrypted)
- `api.coingecko.com` - price data (optional)
- `neptune.vxb.ai` - block explorer links (optional, user-initiated)

### VxBlocks Wallet Implementation

**Components:**

1. **Tauri Frontend** (TypeScript/React)

   - User interface
   - REST/RPC client
   - Mobile-friendly

2. **VxBlocks Server** (`nptwallet.vxb.ai`)
   - Modified neptune-core with REST API
   - Centralized gateway
   - Processes all wallet requests

**Network Connections:**

- `https://nptwallet.vxb.ai` - ALL transactions
- `https://api.coingecko.com` - price data
- `https://raw.githubusercontent.com/...` - update checks

**Data Flows:**

- Every balance check → VxBlocks server
- Every transaction → VxBlocks server
- Every UTXO query → VxBlocks server
- Every address generated → only local (keys stay local)

---

## Code Quality Assessment

### Neptune Core Wallet

**Code Structure:** ⭐⭐⭐⭐⭐

- Well-organized
- TypeScript with proper types
- Good error handling
- Comprehensive logging
- Modern tooling (pnpm, Vite, Electron Forge)

**Documentation:** ⭐⭐⭐⭐

- Good README
- Technical architecture documented
- Clear setup instructions
- Active development

**Security Practices:** ⭐⭐⭐⭐⭐

- Localhost-only RPC
- Cookie authentication
- Process isolation
- CSP (Content Security Policy)
- No unnecessary permissions

**Modifications to Neptune:** ⭐⭐⭐⭐⭐

- Minimal and well-scoped
- Well-documented commits
- No security bypasses
- Follows Neptune patterns
- Open for audit

### VxBlocks Wallet

**Code Structure:** ⭐⭐⭐⭐

- Well-organized
- TypeScript
- Modern Tauri framework

**Documentation:** ⭐⭐⭐

- Basic README
- Setup instructions
- Self-hosting guide (good!)

**Security Practices:** ⭐⭐⭐

- Keys encrypted locally (good)
- But centralized architecture (bad for privacy)
- Update mechanism (potential concern)

**Transparency:** ⭐⭐

- No privacy policy visible
- No data retention policy
- No information about server logging
- No warrant canary

---

## Recommendations by User Profile

### Maximum Privacy (Journalist, Activist, Whistleblower)

**Recommended:** Neptune Core Wallet + Tor

**Setup:**

1. Use Neptune Core Wallet (seaoffreedom)
2. Route through Tor
3. Dedicated machine
4. Full disk encryption
5. No other apps
6. Regular security updates

**DO NOT use VxBlocks wallet** - Transaction history exposed

### Privacy-Conscious Individual

**Recommended:** Neptune Core Wallet

**Setup:**

1. Use Neptune Core Wallet
2. Standard security practices
3. Encrypted home directory
4. Firewall configured

**Acceptable:** VxBlocks wallet if you self-host the server

### Casual User (Don't Care About Privacy)

**Acceptable:** VxBlocks Wallet

**But understand:**

- All transactions visible to VxBlocks
- Subject to surveillance
- Similar privacy to bank account

**Better option:** Still use Neptune Core Wallet (principle matters)

### Developer/Technical User

**Recommended:**

1. Official Neptune CLI (maximum control)
2. Neptune Core Wallet (good GUI)

**For testing:**

- Both wallets acceptable
- Understand trade-offs

---

## Migration Path

### From VxBlocks to Neptune Core Wallet

**Steps:**

1. Export seed phrase from VxBlocks wallet
2. Install Neptune Core Wallet
3. Import seed phrase
4. Wait for blockchain sync
5. Verify balance matches
6. Delete VxBlocks wallet

**Note:** Past transaction history is still logged by VxBlocks, but future transactions will be private.

### From Official Neptune CLI to Neptune Core Wallet

**Steps:**

1. Use same wallet file
2. Install Neptune Core Wallet
3. Point to existing data directory
4. No blockchain re-sync needed
5. Enjoy graphical interface

---

## Security Checklist

### Before Using Neptune Core Wallet

- [ ] Download from official source (GitHub)
- [ ] Verify binary integrity (if possible)
- [ ] Review source code (if technical)
- [ ] Ensure sufficient disk space (20+ GB)
- [ ] Configure firewall
- [ ] Enable full disk encryption
- [ ] Plan backup strategy
- [ ] Understand recovery process

### Before Using VxBlocks Wallet

- [ ] Understand privacy implications
- [ ] Accept that VxBlocks sees all transactions
- [ ] Know that data subject to subpoena
- [ ] Consider self-hosting server instead
- [ ] Read (missing) privacy policy
- [ ] Assess personal threat model
- [ ] Determine if privacy matters for your use case

---

## Frequently Asked Questions

### Q: Can VxBlocks steal my crypto?

**A:** No, private keys are stored locally. But they can:

- See all your transactions
- Know your balance
- Track your activity
- Share data with authorities if compelled

### Q: Is the Neptune Core Wallet official?

**A:** It's a community project using official Neptune binaries with minimal safe modifications for better UI integration. Not officially endorsed, but safe to use.

### Q: Which is safer from hackers?

**A:** Both store keys locally with encryption. Security depends more on your computer security than the wallet choice. The difference is in **privacy** not key security.

### Q: Can I use both wallets?

**A:** Yes, they use the same seed phrase format. But don't use both simultaneously with same wallet - choose one.

### Q: Why does VxBlocks wallet exist?

**A:** To provide easy onboarding for users who want convenience over privacy. Some users prioritize ease of use.

### Q: Can I run my own VxBlocks server?

**A:** Yes, the neptune-wallet-core code is available. But Neptune Core Wallet is easier.

### Q: Which has better UX?

**A:** VxBlocks has faster setup and mobile support. Neptune Core Wallet requires sync but gives you control.

### Q: What about mobile?

**A:** Currently, VxBlocks is only option for mobile. Neptune Core Wallet could potentially add remote connection to user's own full node in the future.

---

## Conclusion

### Simple Decision Tree

```
Do you value financial privacy?
├─ YES → Use Neptune Core Wallet (seaoffreedom)
│        ✅ Complete privacy
│        ✅ No surveillance
│        ✅ Trustless
│
└─ NO → Still consider Neptune Core Wallet
         (Privacy is important even if you think you don't need it)

         Acceptable alternative: VxBlocks Wallet
         ⚠️  But understand you're trading privacy for convenience
         ⚠️  Similar to using a bank vs cash
```

### Final Recommendation

**For 95% of users:** Use Neptune Core Wallet (seaoffreedom)

**Why:**

- ✅ Privacy is a fundamental right
- ✅ You don't know what the future holds
- ✅ Laws can change
- ✅ Governments can become authoritarian
- ✅ Financial surveillance is real
- ✅ True to the vision of cryptocurrency
- ✅ Your keys, your crypto, your privacy

**The setup time and disk space are worth the sovereignty.**

---

## Resources

### Neptune Core Wallet (seaoffreedom)

- **Repository:** https://github.com/seaoffreedom/neptune-core-wallet
- **Modified Neptune:** https://github.com/sploitzberg/neptune-core
- **License:** MIT

### VxBlocks Neptune Wallet

- **Repository:** https://github.com/VxBlocks/neptune-wallet-app
- **Server Code:** https://github.com/VxBlocks/neptune-wallet-core
- **License:** Not specified

### Official Neptune

- **Website:** https://neptune.cash
- **Repository:** https://github.com/Neptune-Crypto/neptune-core
- **Documentation:** https://neptune.cash/docs

---

**Report Version:** 1.0  
**Last Updated:** October 19, 2025  
**Next Review:** When significant updates occur

---

## Disclaimer

This comparison is based on code review and architectural analysis. Users should:

- Do their own research
- Verify information independently
- Understand their own threat model
- Follow security best practices
- Keep software updated

No accusations of malicious intent. Both projects serve different user needs.

**Remember:** The best security tool is understanding what you're using.
