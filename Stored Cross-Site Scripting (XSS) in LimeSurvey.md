## Title
Stored Cross-Site Scripting (XSS) in LimeSurvey

## Summary
A stored cross-site scripting (XSS) vulnerability in LimeSurvey allows authenticated attackers to inject arbitrary JavaScript through insufficient input validation. Malicious payloads are stored on the server and executed when rendered in a victim’s browser.

## Affected Versions
- Limesurvey < 6.17.0 (build 260421) April 21, 2026

## Vulnerability Type
- Cross-Site Scripting (Stored XSS)

## Fixed Version
Limesurvey 6.17.0 (build 260421) April 21, 2026

## Affected Components
- Input handling and storage logic
- Rendering layer displaying stored user-controlled data

## Attack Vector
- Authenticated attacker submits crafted input containing JavaScript into a persistent application field  
- The payload is stored by the server without proper sanitization  
- When another user accesses the affected page, the stored payload is rendered and executed in their browser  

## Impact
- Execution of arbitrary JavaScript in victim’s browser  
- Session hijacking via cookie theft  
- Privilege escalation

## Fix
Upgrade LimeSurvey to version 6.17.0 or later.

## Reference
- [https://github.com/LimeSurvey/LimeSurvey/pull/4888](https://github.com/LimeSurvey/LimeSurvey/pull/4888)
