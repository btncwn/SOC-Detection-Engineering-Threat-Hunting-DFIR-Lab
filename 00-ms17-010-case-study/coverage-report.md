# Detection Coverage Report – MS17-010 (EternalBlue) Emulation

**Last Updated:** 2026-06-07

## Executive Summary

**Overall Coverage: 66% (4 out of 6 phases detected)**

| Phase | MITRE TTP | Detection Status |
|-------|-----------|------------------|
| 1. Vulnerability Discovery | T1040 | ❌ NOT DETECTED |
| 2. SMB Enumeration | T1046 | ⚠️ LOGGED ONLY |
| 3. Exploit Execution | T1210 | ✅ DETECTED |
| 4. Reverse Shell / C2 | T1071 | ✅ DETECTED |
| 5. Lateral Movement | T1021.002 | ⚠️ LOGGED ONLY |
| 6. Persistence | T1053.005 | ✅ DETECTED |

## Gap Analysis

| Gap | Severity | Remediation |
|-----|----------|-------------|
| No SMB scan detection | High | Write Sigma rule for T1046 |
| No lateral movement alert | High | Write Sigma rule for T1021.002 |

## Lessons Learned

1. Parent-child process relationships are the strongest detection signal
2. Lateral movement is logged but not alerted
3. Manual detection is not enough – convert to Sigma rules
