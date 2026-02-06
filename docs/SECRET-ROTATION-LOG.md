# Secret Rotation Audit Log

Track all secret rotations to ensure compliance with rotation policy.

## API Keys (90-day rotation)

| Secret | Last Rotated | Next Due | Status | Rotated By | Notes |
|--------|--------------|----------|--------|------------|-------|
| Anthropic API Key | 2026-02-05 | 2026-05-06 | ✅ Current | achim | Initial setup |
| GitHub API Token | - | 2026-05-06 | ⚠️ TODO | - | Need to rotate |
| Miniflux API Key | - | 2026-05-06 | ⚠️ TODO | - | Need to rotate |

## Network Credentials (6-month rotation)

| Secret | Last Rotated | Next Due | Status | Rotated By | Notes |
|--------|--------------|----------|--------|------------|-------|
| WiFi Eduroam Password | - | 2026-08-05 | ⚠️ TODO | - | Need to set rotation baseline |
| WiFi Home PSK | - | 2026-08-05 | ⚠️ TODO | - | Need to set rotation baseline |
| ProtonVPN Private Key | - | 2026-08-05 | ⚠️ TODO | - | Need to set rotation baseline |

## Standard Secrets (Yearly rotation)

| Secret | Last Rotated | Next Due | Status | Rotated By | Notes |
|--------|--------------|----------|--------|------------|-------|
| Hetzner VPS SSH Key | - | 2027-02-05 | ⚠️ TODO | - | Need to set rotation baseline |
| Posteo Email Password | - | 2027-02-05 | ⚠️ TODO | - | Need to set rotation baseline |

## Encryption Keys (Only on compromise)

| Secret | Created | Last Rotated | Status | Notes |
|--------|---------|--------------|--------|-------|
| Age Key | - | Never | ✅ Secure | Stored in `/var/lib/sops-nix/key.txt` |

---

## Rotation Template

When rotating a secret, add entry below:

**Date:** YYYY-MM-DD
**Secret:** [secret name]
**Rotated By:** [your name]
**Reason:** Scheduled / Compromised / Security Audit
**Old Value Hash:** [sha256 of old secret for verification]
**New Value Hash:** [sha256 of new secret]
**Services Restarted:** [list of affected services]
**Verification:** ✅ Passed / ❌ Failed
**Notes:** [any additional context]

---

## Legend

- ✅ Current - Within rotation window
- ⚠️ TODO - Needs rotation soon
- 🔴 OVERDUE - Past rotation deadline
- 🔒 Rotated - Recently rotated

---

**Last Updated:** 2026-02-05
