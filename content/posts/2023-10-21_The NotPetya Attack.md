---
title: "The NotPetya Attack"
date: 2023-10-21
---

Today, I learnt about some of the technical details of the infamous NotPetya attack from 2017. It's fascinating to see how this malware combined various techniques for maximum disruption. Here's a brief rundown:

## Initial Infection
- **M.E.Doc Software**: Attackers compromised this Ukrainian tax software's update mechanism, making organizations unwittingly introduce malware when updating.

## Attack Techniques
- **MBR Overwriting**: Targeted the Master Boot Record (MBR) to prevent systems from booting up.
- **EternalBlue & EternalRomance**: NSA-linked exploits targeting the SMB protocol. Used for lateral movement.
- **Mimikatz**: Extracted plaintext passwords from RAM to aid lateral movement.
- **PsExec and WMIC**: Legitimate Windows tools used by NotPetya for executing commands on other machines.

## Deceptive Design
- **Fake Ransomware**: Presented a ransom note, but was mainly a wiper. Proper decryption was practically impossible.


