# Doppelganger – Advanced LSASS Dumper with PPL Bypass and Process Cloning

**Doppelganger** is a powerful LSASS dumping tool for red team operations. It bypasses Protected Process Light (PPL), clones `lsass.exe`, and performs a stealthy memory dump – encrypted and ready for offline extraction.

Unlike traditional tools, Doppelganger works on modern Windows with PPL enabled by:
- Using a BYOVD (Bring Your Own Vulnerable Driver) to disable PPL
- Cloning `lsass.exe` to evade direct memory access detection
- Dumping and XOR-obfuscating the clone to disk

Built in C, designed for stealth, and compatible with process hollowing frameworks like HollowReaper.

> Ideal for red teamers, malware developers, or researchers needing full LSASS dumps on hardened targets.

## Blogpost
- https://vari-sh.github.io/posts/doppelganger/
- https://labs.yarix.com/2025/06/doppelganger-an-advanced-lsass-dumper-with-process-cloning/

## Usage Flow
### Standalone
In order to use Doppelganger you must place `RTCore64.sys` in C:\Users\Public. Doppleganger can be used standalone or hollowed through HollowReaper.
```
.\Doppelganger.exe
```
