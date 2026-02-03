# 🚨 INCIDENT REPORT - Suspicious Privilege Escalation Detected

## 📋 Executive Summary
**Date:** 2026-02-03  
**Severity:** Medium  
**Status:** Investigated  
**Affected System:** wazuh-server (Agent 000)  
**Attack Technique:** T1548.003 - Sudo Abuse

## 🎯 Incident Timeline
| Time | Event | MITRE Technique |
|------|-------|-----------------|
| 13:36:22 | Successful sudo to ROOT executed | T1548.003 |
| 13:36:50 | Login session closed | - |
| 13:37:12 | Login session opened | T1078 |
| 13:37:12 | Successful sudo to ROOT executed | T1548.003 |

## 🔍 Wazuh Detection
**Alert Triggered:** Rule ID 5402 - "Successful sudo to ROOT executed"  
**MITRE Mapping:** T1548.003 (Privilege Escalation, Defense Evasion)

### Wazuh Dashboard Evidence:
![Privilege Escalation Alert](screenshots/wazuh-security-alerts.png)

## 🕵️ Investigation Findings
- **Source:** Local user on wazuh-server
- **Activity:** Multiple sudo root executions within 1 minute
- **Context:** Likely administrative maintenance (low suspicion)
- **Impact:** No unauthorized access detected

## 🛡️ Response Actions
1. **Review:** Checked user authorization (legitimate admin)
2. **Verify:** No unusual commands executed
3. **Document:** Incident logged for baseline understanding
4. **Monitor:** Continue watching for unusual sudo patterns

## 📊 MITRE ATT&CK Mapping
| Tactic | Technique | ID |
|--------|-----------|----|
| Privilege Escalation | Abuse Elevation Control Mechanism | T1548.003 |
| Defense Evasion | Abuse Elevation Control Mechanism | T1548.003 |

## 🎓 Lessons Learned
1. **Wazuh effectively detects** privilege escalation patterns
2. **MITRE ATT&CK integration** provides immediate context
3. **Baseline establishment** needed for normal admin activities
4. **Alert tuning** may reduce false positives for known admins

## 📈 Recommendations
1. Implement user behavior analytics for sudo usage
2. Create allow-list for authorized admin activities
3. Establish sudo usage baseline per user
4. Configure higher severity for sudo outside business hours

---
**Report Generated:** 2026-02-03  
**Investigator:** Renaldi  
**SOC Team:** Blue Team Alpha  
**Tools Used:** Wazuh SIEM, MITRE ATT&CK Framework
