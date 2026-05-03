![Sovereignbase Banner](https://img.shields.io/badge/Sovereignbase-user--owned%20backend%20architecture-000000?style=for-the-badge)

# Sovereignbase

**A backend architecture for building applications without becoming the custodian or canonical authority over user data.**

Sovereignbase treats every user-agent as an **Actor**: a cryptographic participant that owns and validates its own state.

Servers are **Base Stations**: service infrastructure for storage, relay, backup, synchronization, discovery, and cross-origin coordination. They support resources, but they do not become the source of truth.

The goal is simple:

**Build real applications without forcing developers to own the user’s identity, database, private state, or long-term data liability.**

---

<img src="https://github.com/sovereignbase/misc/blob/main/docs/neutral_diagram/digital-sovereignty-enabling_architecture_diagram.drawio.png" alt="Digital-Sovereignty-Enabling Architecture Diagram" />

## Core model

Sovereignbase is built around three primitives:

### Actor

A cryptographic user-agent.

An Actor owns keys, validates incoming state, authorizes delegation, signs claims, verifies other Actors, and decides what state it accepts.

Authority is not granted by the server.  
Authority is verified by the receiving Actor.

### Base Station

A standardized resource support server.

A Base Station can store, relay, back up, synchronize, route, index, and coordinate resources, but it does not become the application’s canonical database or backend authority.

The Base Station is infrastructure.  
The Actor is authority.

### Convergent Replicated Resource

A portable resource whose state can be replicated, synchronized, verified, and rendered by multiple clients.

A resource may be private, public, encrypted, publishable, cached, indexed, backed up, or shared. The important rule is that the resource remains portable and independently verifiable.

---

## What this means for developers

Sovereignbase is not just “privacy tech”.

It is a way to build applications where the developer does not need to become the legal, operational, or technical authority over user data.

Instead of building an app-owned canonical backend database, you build against user-owned resources:

- no app-owned canonical user database
- no hidden platform authority over user state
- no forced data custody as the default architecture
- no separate application-side schema as the only source of truth
- no provider lock-in as the basis of product retention

Developers still build products, interfaces, automations, workflows, indexes, services, payments, and integrations.

They just do not need to own the user’s existence to do it.

---

## What is being built

Sovereignbase is currently being specified and implemented from the bottom up.

The current work focuses on small, runtime-agnostic JS/TS packages and implementation-oriented specifications.

### Data and replication

- **Convergent Replicated List**
- **Convergent Replicated Map**
- **Convergent Replicated Set**
- **Convergent Replicated Text**
- **Schema CRDT**
- **Convergent Replicated Resource**

These form the replicated state layer for portable, convergent, application-usable resources.

### Cryptography and identifiers

- **cryptosuite**
- **hardware-bound**
- **bytecodec**
- **urn-anbs**

These provide byte handling, cryptographic identifiers, encryption, signatures, key agreement, hardware-bound local bootstrapping, and resource naming primitives.

### Browser and coordination primitives

- **peer2peer**
- **offline-kv-store**
- **qr**
- **base-station**

These support local-first state, WebRTC-style peer exchange, QR-based bootstrapping, offline persistence, and service-assisted coordination.

---

## What Sovereignbase is for

Sovereignbase fits systems where users, organizations, devices, or agents need to retain authority over their own state while still using modern application infrastructure.

Good fits:

- local-first applications
- collaborative editors
- private personal data layers
- organization-owned state
- encrypted resource storage
- portable identity and profile resources
- verifiable credentials and claims
- apps that need offline, sync, backup, and delegation
- services that want to reduce data custody and liability

Sovereignbase is not a replacement for every backend component.

Search engines, analytics systems, public indexes, AI workers, payment processors, compute services, and automation services can still exist. In Sovereignbase, they are modeled as explicit services or Actors with scoped access, not as hidden owners of user state.

---

## Privacy note

This architecture does not claim to eliminate surveillance.

It reduces the scope and value of surveillance by avoiding unnecessary plaintext custody, central identity ownership, and provider-controlled canonical state.

A Base Station may observe traffic patterns, metadata, timing, storage activity, and availability requests.

It should not need to own the plaintext resource, the user’s identity, or the authority to mutate state.

---

## Automation without custody

Automation is allowed.

Custody is not required.

If an automation service needs access to a resource, access should be:

- explicitly authorized by the Actor
- scoped to the required resource or operation
- time-bounded where possible
- revocable
- visible in the user interface
- auditable through signed or measurable activity

Delegation should not become dependence.

---

## What Sovereignbase refuses to be

Sovereignbase is not a platform that owns user identity.

It does not require a provider to define the truth.

It does not assume that a server is correct because it served the response.

It does not make provider shutdown an existential event for the user.

A provider may host, relay, back up, and coordinate.  
A user may leave, migrate, replicate, or use another provider.

Those two facts are meant to coexist.

---

## Why this matters

Most applications make the developer or company the unavoidable custodian of user data.

That creates operational burden, compliance risk, breach risk, migration pain, and user lock-in.

Sovereignbase takes a different position:

**Verify authority. Validate policy. Then accept state.**

The network can deliver claims.  
Actors decide whether those claims are valid.

---

## Current status

Early-stage.

The project is currently in recursive specification and implementation:

```text
specify -> implement -> test -> correct -> specify
````

The immediate priority is correctness of meaning, deterministic behavior, portable resource structure, and small usable libraries.

The initial implementation targets modern JavaScript environments: browsers, Node, Deno, Bun, workers, and edge runtimes.

The architecture is intended to outlive any specific hosting provider.

---

## Read more

* **[What Makes Sovereignbase Unique](https://github.com/sovereignbase/misc/blob/main/docs/WHY_SOVEREIGNBASE_IS_DIFFERENT.md)**
* **[Digital-Sovereignty-Enabling Architecture Overview](https://www.jortsupetterson.workers.dev/)**
* **[Rationalizing Why Digital-Sovereignty-Enabling Architecture Needs This Structure](https://github.com/sovereignbase/misc/blob/main/docs/neutral_diagram/rationale.md)**
* **[Long and Awkward Walkthrough on Digital-Sovereignty-Enabling System Architecture](https://www.youtube.com/watch?v=GIFVetIC8X0)**

---

<img src="https://github.com/sovereignbase/misc/blob/main/docs/TOP_LEVEL_LABELING.png" alt="Digital-Sovereignty-Enabling Architecture top-level labels" />

## Scalability note

The architecture scales horizontally by adding service providers.

It scales vertically by adding service clients, Actors, resources, relays, backups, indexes, and specialized services.

The model does not depend on one provider becoming the universal authority.

---

## Licensing

Everything produced by the Sovereignbase project is released under the **Apache License 2.0**, unless explicitly stated otherwise.

This includes code, packages, tooling, specifications, and images.

The intent is to keep the ecosystem usable in open-source and commercial environments.

---

## Invitation

Sovereignbase is not trying to build one app.

It is trying to make it practical to build many apps, clients, viewers, editors, platforms, services, and automations around shared user-owned resources.

Applications should compete on product quality, UX, reliability, and service.

Not on captivity.
