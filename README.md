# Isolated Cybersecurity Lab Environment

**Networkwalks Cybersecurity Course | Batch 84C | Week 1, Project 1**
**Author:** Joseph Wilson

## Summary

This project delivers a self-contained cybersecurity practice lab built on Oracle VirtualBox. It hosts one attacker machine and two target machines on a private network, isolated from the host and the local network, with a snapshot-based baseline for rapid recovery.

## Environment

| Component | Detail |
|---|---|
| Host | MacBook Air (macOS) |
| Virtualisation platform | Oracle VirtualBox |
| Network | NAT Network `NatNetwork1`, 10.0.0.0/24 |

## Virtual Machines

| Hostname | Role | Operating System | IP Address |
|---|---|---|---|
| Kali Linux | Attacker | Kali Linux | 10.0.0.2 |
| Windows 10 | Target | Windows 10 | 10.0.0.10 |
| Android | Target | Android 9 | 10.0.0.9 |

Kali Linux also has a second NAT adapter, which provides internet access for updates and tool installation while the lab network stays isolated.

## Method

1. Installed VirtualBox on the host.
2. Created the NAT Network `NatNetwork1` (10.0.0.0/24).
3. Deployed Kali Linux with two adapters: NatNetwork1 and NAT.
4. Deployed the Windows 10 and Android 9 targets on NatNetwork1.
5. Assigned the static IP addresses listed above.
6. Verified connectivity between all machines.
7. Captured a baseline snapshot of each machine.

## Results

- All three machines communicate over the private 10.0.0.0/24 network.
- Test traffic is contained within the lab.
- Each machine can be restored to a clean state from its snapshot.

## Evidence

Screenshots in this repository show the VM configurations, network settings, IP assignments and connectivity checks.

## Scope Note

Windows 11 was excluded from this phase. All testing is performed only on systems built and owned for this lab.
