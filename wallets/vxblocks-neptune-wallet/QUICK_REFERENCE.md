# Quick Reference: VxBlocks Neptune Wallet Security

## 🚨 Critical Issue Summary

**The VxBlocks Neptune Wallet routes ALL your blockchain activity through a third-party server at `nptwallet.vxb.ai`**

This means VxBlocks (and anyone with legal access to their servers) can see:

- ✅ Every transaction you send
- ✅ All amounts and recipients
- ✅ Your IP address and location
- ✅ When you use the wallet
- ✅ Your entire transaction history

---

## 📊 Quick Threat Assessment

| Question                         | Answer               | Risk        |
| -------------------------------- | -------------------- | ----------- |
| Can they steal my crypto?        | No - keys stay local | 🟢 Low      |
| Can they see my transactions?    | Yes - all of them    | 🔴 Critical |
| Can they identify me?            | Yes - via IP address | 🔴 Critical |
| Can law enforcement access data? | Yes - via subpoena   | 🔴 Critical |
| Can I self-host the server?      | Yes - it's possible  | 🟡 Medium   |
| Is this official Neptune?        | No - it's a fork     | 🟠 High     |

---

## 🎯 Quick Decision Guide

### ❌ DO NOT USE if you:

- Value financial privacy
- Are a journalist/activist/whistleblower
- Are in a high-risk jurisdiction
- Are politically active
- Handle large amounts
- Need anonymity

### ⚠️ MIGHT BE OKAY if you:

- Don't care about privacy
- Already use KYC exchanges
- Make small transactions only
- Trust VxBlocks completely
- Can self-host the server
- Are just testing/learning

---

## 🔍 What Law Enforcement Can See

### With Just a Subpoena (No Warrant):

- Complete transaction history
- Your IP address → Your location
- When you use the wallet
- Who you send money to
- All amounts involved

### With a Warrant:

- Real-time monitoring
- Live alerts when you transact
- Historical database dumps
- Network analysis (who else you interact with)

### With National Security Powers:

- Bulk collection of all users
- Modified updates targeting you
- Long-term silent surveillance
- Cross-reference with other databases

### With Server Seizure:

- Complete takeover
- Continued operation under FBI control
- Users unaware they're monitored
- Enhanced evidence collection

---

## 📋 Technical Evidence

### Default Server

```
Location: /neptune-wallet-app/src-tauri/src/config/mod.rs:150
Code: .unwrap_or("https://nptwallet.vxb.ai".to_string())
```

### Transaction Broadcast

```
Location: /neptune-wallet-app/src-tauri/src/rpc_client/mod.rs:148-175
Action: Posts full transaction to VxBlocks server
```

### Server-Side Logging

```
Location: /neptune-wallet-core/neptune-core/src/rest_server.rs:241
Code: info!("broadcasted insert tx: {}", tx.transaction.kernel.txid());
```

---

## 🛡️ Protection Options

### Option 1: Self-Host the Server (RECOMMENDED)

```bash
# Clone and run your own server
git clone https://github.com/VxBlocks/neptune-wallet-core -b wallet
cd neptune-wallet-core
cargo run --release -- --rest-port 9800

# Then configure wallet to use: http://localhost:9800
```

**Pros:**

- ✅ No third-party sees your transactions
- ✅ You control the data

**Cons:**

- ⚠️ You must maintain the server
- ⚠️ Still using unofficial Neptune fork

### Option 2: Use Official Neptune Tools

```bash
# Use official Neptune Core
git clone https://github.com/Neptune-Crypto/neptune-core
cd neptune-core
cargo run --release
```

**Pros:**

- ✅ Official codebase
- ✅ True P2P, no centralized gateway
- ✅ Maximum privacy

**Cons:**

- ⚠️ More technical setup
- ⚠️ Takes longer to sync
- ⚠️ Command-line interface

### Option 3: Use With Awareness

- Accept that transactions are monitored
- Use VPN/Tor (helps with IP privacy)
- Don't reuse addresses
- Minimize transaction amounts
- Know your privacy is compromised

---

## 🆚 Comparison Chart

| Feature                    | VxBlocks Wallet | Official Neptune     |
| -------------------------- | --------------- | -------------------- |
| **Ease of Use**            | ⭐⭐⭐⭐⭐ Easy | ⭐⭐ Technical       |
| **Privacy**                | ⭐ Poor         | ⭐⭐⭐⭐⭐ Excellent |
| **Trust Required**         | VxBlocks        | Cryptography only    |
| **Setup Time**             | 5 minutes       | 2+ hours             |
| **Surveillance Risk**      | 🔴 High         | 🟢 Low               |
| **Key Security**           | ✅ Good         | ✅ Good              |
| **Transaction Visibility** | 🔴 Centralized  | 🟢 Distributed       |
| **Update Source**          | VxBlocks GitHub | Official Neptune     |

---

## 💰 Privacy vs Convenience Trade-off

```
         High Privacy
              ↑
              |
    Official  |
    Neptune   |
              |
              |
Self-Hosted --|
 VxBlocks     |
              |
              |
  VxBlocks    |← YOU ARE HERE
  (Default)   |
              |
              └──────────────────→ High Convenience
```

---

## 🚩 Red Flags Found

1. **All traffic routes through third-party by default**
2. **No prominent privacy warnings**
3. **Unclear relationship to official Neptune**
4. **Vague git commit messages ("open source code")**
5. **Older version than official Neptune (0.3.0 vs 0.4.0)**
6. **Update mechanism points to VxBlocks GitHub**
7. **No transparency reports or data retention policy**
8. **README calls it "vxb neptune wallet" not "Neptune Wallet"**

---

## ✅ Things That Are OK

1. **Private keys stored locally** - VxBlocks never sees your keys
2. **Standard crypto libraries** - No custom/suspicious cryptography
3. **Transaction witnesses protected** - Secrets not leaked to server
4. **Can self-host** - Architecture supports running your own server
5. **No obvious malware** - Code appears legitimate
6. **Encryption works** - AES-256-GCM properly implemented

---

## 📚 Full Documentation

Three detailed reports created:

1. **SECURITY_ANALYSIS_REPORT.md** - Complete technical analysis
2. **LAW_ENFORCEMENT_CAPABILITIES.md** - Detailed surveillance scenarios
3. **QUICK_REFERENCE.md** - This document

---

## ⚖️ Bottom Line

**Is this malicious?**  
Probably not intentionally, but architecturally problematic.

**Is this private?**  
No. Financial privacy is completely compromised.

**Is this safe for my funds?**  
Probably yes - private keys stay local.

**Should I use it?**  
Only if you fully understand and accept that **every transaction you make will be visible to VxBlocks** (and anyone with legal access to their servers).

**Better alternatives?**

- Self-host the server component
- Use official Neptune Core
- Use hardware wallet with official tools

---

## 🆘 If You're Already Using It

### Assume:

- ✅ All past transactions are logged
- ✅ Your IP is associated with your wallet
- ✅ VxBlocks has a complete financial profile of you
- ✅ This data may be accessible to law enforcement

### Steps:

1. **Don't panic** - Your private keys are still safe
2. **Decide your risk level** - Are you a high-value target?
3. **Consider migration**:
   - Export your seed phrase
   - Set up self-hosted server OR official Neptune
   - Move funds to new addresses
4. **Improve opsec going forward**:
   - Use VPN/Tor
   - Don't reuse addresses
   - Vary transaction patterns

---

## 📞 Questions to Ask VxBlocks

If you want clarity, consider asking:

1. What transaction data do you log?
2. How long is data retained?
3. How many law enforcement requests have you received?
4. Do you have a warrant canary?
5. What is your relationship to official Neptune project?
6. Where are your servers located (jurisdiction)?
7. Do you encrypt stored transaction data?
8. Can you delete user data on request?

---

**Document Version:** 1.0  
**Last Updated:** October 19, 2025  
**Status:** Public

For detailed analysis, see: SECURITY_ANALYSIS_REPORT.md  
For LE scenarios, see: LAW_ENFORCEMENT_CAPABILITIES.md
