## Title
Conditional Remote Code Execution via Path Traversal in LimeSurvey

## Summary
A conditional remote code execution vulnerability in LimeSurvey allows authenticated attackers to exploit improper validation of plugin or question theme names during upload and installation. By using crafted metadata, attackers can perform path traversal and inject malicious Twig extensions, resulting in arbitrary code execution.

## Affected Versions
- Limesurvey < 6.17.0 (build 260421) April 21, 2026

## Vulnerability Type
- Remote Code Execution

## Fixed Version
Limesurvey 6.17.1+260427

## Affected Components
- Plugin / Question Theme upload & install
- `config.xml` parsing
- Path handling logic
- Twig extension loading

## Attack Vector
- Upload crafted plugin/theme package  
- Malicious name in `config.xml` (e.g. path traversal)  
- Files written to unintended location → executed via Twig  

## Impact
- Arbitrary code execution on server  
- Full system compromise (web context)  
- Persistent backdoor via plugin/theme  

## Fix
Upgrade LimeSurvey to version 6.17.1+260427 or later.

## Reference
- [https://github.com/LimeSurvey/LimeSurvey/pull/4900](https://github.com/LimeSurvey/LimeSurvey/pull/4900)
