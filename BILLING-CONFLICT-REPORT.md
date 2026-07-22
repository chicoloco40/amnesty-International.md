# OFFICIAL DOCUMENTATION: SYSTEMIC INTERNATIONAL BILLING CONFLICT

**Filed By:** CL40 World LLC (US-registered multimedia enterprise)  
**Date:** 2026-07-22  
**Subject:** Cross-Border Payment Infrastructure Failure — GitHub Billing / PayPal US / CIH Bank (Morocco)  
**Status:** Formal Appeal for Administrative Override

---

## 1. EXECUTIVE SUMMARY

This document formally records a systemic billing conflict arising from incompatibilities between GitHub's subscription billing engine, a verified US-domiciled PayPal account, and Moroccan intermediary banking security protocols (specifically those enforced by CIH Bank). The conflict has resulted in unjust suspension of paid repository access and deployment capabilities for a legitimately operating US-registered entity.

---

## 2. PARTIES INVOLVED

| Party | Role | Jurisdiction |
|---|---|---|
| **GitHub, Inc.** | Subscription service provider (developer workspace, CI/CD, repository hosting) | United States |
| **PayPal US** | Primary digital payment processor; verified US-linked account | United States |
| **CIH Bank** | Moroccan intermediary banking network enforcing 3D Secure and geographic routing rules | Morocco |
| **CL40 World LLC** | Account holder; US citizen operating an international multimedia movement | United States |

---

## 3. BACKGROUND

CL40 World LLC maintains an active GitHub subscription at the **$29/month** tier to support international multimedia development projects. The account holder is a US citizen and the billing instrument is a **verified American PayPal account** with a documented history of successfully processing recurring GitHub subscription charges.

The account holder currently operates from Morocco, which introduces a geographic layer in the payment-routing chain, routed through local banking infrastructure — specifically CIH Bank's 3D Secure enforcement layer.

---

## 4. DESCRIPTION OF THE CONFLICT

### 4.1 Transaction Rejection Trigger

Automated security verification systems on the GitHub/PayPal billing pathway began rejecting the recurring $29/month subscription charge. Rejection codes point to:

- **Geographic routing restrictions**: Payment origin signals were flagged due to the physical location of the account holder (Morocco), despite the payment instrument being a verified US PayPal account.
- **3D Secure (3DS) Protocol Enforcement**: CIH Bank's intermediary network applied 3D Secure authentication requirements to outbound international transactions, creating an authentication loop that the PayPal-to-GitHub billing API handshake does not natively support.

### 4.2 Infrastructure Friction Chain

```
GitHub Billing Engine
        │
        ▼
  PayPal US API  ←── Verified US Account (historically successful)
        │
        ▼
  International Payment Routing Layer
        │
        ▼
  CIH Bank (Morocco) — 3D Secure Enforcement / Geographic Flag
        │
        ▼
  TRANSACTION REJECTED ← ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ ─ (Billing failure reported to GitHub)
```

### 4.3 Resulting Account Impact

As a direct consequence of this payment routing failure:

- GitHub repository access has been restricted or degraded.
- Deployment pipelines (GitHub Actions, CI/CD workflows) have been disabled.
- Paid-tier features essential to the CL40 World LLC multimedia development workflow are inaccessible.
- No fault lies with the PayPal account balance, standing, or the account holder's intent to pay.

---

## 5. TECHNICAL ANALYSIS

### 5.1 Why This Is a System-Level Conflict — Not a User Error

The PayPal account in question:
- Is **verified** and in good standing under US financial regulations.
- Has a **documented history** of successfully processing recurring GitHub charges.
- Holds **sufficient funds** to cover the $29/month subscription.

The rejection is not caused by insufficient funds, fraud, or account misuse. It is caused by a **mismatch between payment-layer security protocols**:

1. GitHub Billing expects a frictionless PayPal recurring charge authorization.
2. PayPal US initiates the charge through standard international rails.
3. CIH Bank's 3D Secure enforcement layer intercepts the routing signal and requires an additional cardholder authentication step that the automated GitHub–PayPal API pipeline cannot fulfill.
4. The authentication timeout or failure propagates back to GitHub as a generic payment failure.

### 5.2 Asymmetry of Impact

This technical failure disproportionately affects developers and digital entrepreneurs who:
- Are US-registered entities operating internationally.
- Use US-based digital wallets (PayPal, Stripe) as their primary billing instrument.
- Reside in or transit through countries with strict 3D Secure intermediary banking rules.

The affected party has no alternative recourse because:
- GitHub's billing system does not provide a manual override or exception pathway for verified prior-paying customers.
- PayPal does not expose granular 3DS bypass controls to end users.
- CIH Bank applies blanket 3DS policies to all outbound international digital-service payments above a threshold.

---

## 6. FORMAL APPEAL

### 6.1 Requested Actions from GitHub

1. **Administrative Payment Override**: Manually reinstate the $29/month subscription for the affected account for a period sufficient to allow the account holder to resolve the 3DS routing conflict at the banking level.
2. **Restore Repository Access**: Immediately lift any restrictions on repository visibility, collaboration permissions, and Actions/deployment quotas tied to the billing lapse.
3. **Flag Account for Billing Exception Review**: Mark the account for review under GitHub's cross-border payment exception policy, if such a policy exists, or escalate to establish one.
4. **Provide a Direct Payment Alternative**: Offer a one-time invoice or alternative payment method (e.g., GitHub Credits, wire transfer, or SWIFT-compatible billing option) to circumvent the PayPal–3DS incompatibility.

### 6.2 Requested Actions from PayPal US

1. **Issue a 3DS Exemption Flag** for recurring merchant charges to GitHub, Inc. (a pre-approved US merchant), consistent with PayPal's own recurring billing agreement terms.
2. **Provide Account Documentation** confirming the account's verified US status and transaction history to support any GitHub billing review process.

### 6.3 Requested Actions from CIH Bank

1. **Whitelist Recurring Digital Subscription Charges** originating from verified US PayPal accounts to established US SaaS providers.
2. **Provide Written Clarification** of the specific 3DS rule that triggered rejection of this transaction, to facilitate a formal dispute.

---

## 7. SUPPORTING CONTEXT

- **Entity Type**: US-registered LLC (CL40 World LLC) engaged in international multimedia production and digital distribution.
- **Payment Instrument**: Verified PayPal US account — not a Moroccan card or local bank account.
- **Subscription Tier**: GitHub $29/month (individual or organization paid tier).
- **Geographical Conflict**: Account holder's physical presence in Morocco creates routing signals that do not accurately represent the US-domiciled financial instrument being used.
- **Historical Precedent**: Prior billing cycles processed successfully, confirming the instrument's compatibility with GitHub's payment system before geographic security filters were tightened.

---

## 8. CONCLUSION

The billing failure described in this document is a **systemic infrastructure conflict** — not a reflection of the account holder's financial standing or intent. The intersection of GitHub's automated billing engine, PayPal's international routing rails, and CIH Bank's 3D Secure enforcement layer has created an unjust lock on cross-border development access for a legitimate US entity.

CL40 World LLC respectfully requests that GitHub, PayPal US, and CIH Bank coordinate an expedited resolution, restore full account access, and work toward permanent infrastructure accommodations for US-registered entities operating in regions with strict intermediary banking security protocols.

---

*This document was prepared by CL40 World LLC for submission to GitHub Support, PayPal Dispute Resolution, and CIH Bank Customer Relations as a formal record of the described billing conflict.*
