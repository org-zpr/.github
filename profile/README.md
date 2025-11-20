# Welcome to ZPR

ZPR is building the future of secure, policy-driven networking infrastructure.

We maintain a suite of open-source tools to:
- Define zero-trust access policies in code
- Enforce them across cloud, hybrid, and on-prem networks
- Audit and reason about communication paths

## Overview

### Purpose

ZPR (Zero-trust Packet Routing) is a secure by construction network model that embeds fine-grained, identity-aware policy directly into packet handling. It moves away from the complexity and limitations of IP firewalls, NATs, and VLANs, offering instead a coherent, verifiable framework where access decisions are explicit, auditable, and topology-independent.

ZPR makes it possible to define *what* can communicate and *why*, using a common policy language applied uniformly across environments.

### Who It’s For

ZPR is built for teams with concrete security, compliance, or operational requirements:

- **Security architects** who need enforceable policy at the packet level.
- **Platform and infrastructure teams** managing dynamic, service-oriented networks.
- **Organizations in regulated industries** that need strong guarantees around who can access what, and under which conditions.
- **Tooling and systems developers** building platforms where security must be built in, not added later.

If your current stack involves layering multiple access controls without end-to-end visibility, ZPR is designed to simplify and unify that model.

### Architecture

ZPR is both a policy system and a runtime network overlay. The key components:

- **ZPL (Policy Language):** A declarative language for specifying roles, permissions, and conditions based on identity and context. Human-readable, type-safe, and expressive.
- **ZPRnet:** A mesh of cooperating nodes that enforce ZPL policies at the network level. Policy decisions are traceable and enforceable at every hop.
- **Visas:** Authenticated snippets of policy which bind packets to authenticated identities, explicitly granted permissions, and forwarding instructions. Each packet is cryptographically associated with the visa under which it is being forwarded by a label which replaces the traditional IP header.
- **Trusted Services:** Real-time attributes are fed into policy evalution by external identity sources (e.g., LDAP, cloud metadata services).
- **Visa Service:** Evaluates policy against live context to issue or revoke visas. Central to ZPR’s real-time enforcement model.
- **Adapters & Docks:** Bridges between the ZPR overlay and conventional IP systems. These handle encapsulation and translation at ingress/egress points.
- **Nodes:** Forwarders within the ZPRnet. Nodes enforce policy issued by the Visa Service.

ZPR is designed for environments where clarity and control are non-negotiable. All policy and enforcement decisions are distributed, verifiable, and transparent.

## Featured Projects
- [zpr-core](https://github.com/org-zpr/zpr-core): Core routing engine
- [zpl](https://github.com/org-zpr/zpr-compiler): Zero-trust Policy Language compiler

[Get in touch](mailto:info@zpr.org) and read more at [zpr.org](https://zpr.org)
