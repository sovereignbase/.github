![sovereignbase Banner](https://img.shields.io/badge/Sovereignbase-digital--sovereignty--enabling%20pwa%20architecture-000000?style=for-the-badge)

**Treat every user-agent as an Actor in a distributed system (a cryptographic authority over its own state), supported by servers as Base Stations (standardized resource support servers run by service providers, used for storage, relay, backup, and cross-origin coordination), and let state emerge from convergent replicated verifiable data over interoperable resources, independent of network location or service operators.**

---

<img src="https://github.com/sovereignbase/z-base/blob/main/docs/neutral_diagram/digital-sovereignty-enabling_architecture_diagram.drawio.png" alt="Digital-Sovereignty-Enabling Architecture Diagram" />

**PRIVACY NOTE:** This architecture does not attempt to eliminate surveillance.  
It limits the **scope** and **value** of surveillance.

**Read more**
- **[What Makes Sovereignbase Unique](https://github.com/sovereignbase/z-base/blob/main/docs/WHY_SOVEREIGNBASE_IS_DIFFERENT.md)**
- **[Digital-Sovereignty-Enabling Architecture Overview](https://www.jortsupetterson.workers.dev/)**
- **[Rationalizing Why Digital-Sovereignty-Enabling Architecture Needs This Structure](https://github.com/sovereignbase/z-base/blob/main/docs/neutral_diagram/rationale.md)**
- **[Long and Awkward Walkthrough on Digital-Sovereignty-Enabling System Architecture](https://www.youtube.com/watch?v=GIFVetIC8X0)**

<img src="https://github.com/sovereignbase/z-base/blob/main/docs/TOP_LEVEL_LABELING.png" alt="Digital-Sovereignty-Enabling Architecture top-level labels" />

**SCALABILITY NOTE:** The diagram scales both horizontally and vertically.  
Horizontally: add as many **Service Providers** as needed.  
Vertically: add as many **Service Clients** as needed.

---

## What Sovereignbase is building

### 1) Interoperable resources (not “apps”)

Sovereignbase is about **portable resources**: media, documents, identities, credentials, objects—and anything else that can be expressed as a shared, verifiable model.

The point is not “a decentralized app”.  
The point is **a decentralized _resource format + semantics_**, so many competing clients can render, edit, and verify the same thing.

Think:
- a video format + many players
- a document format + many editors
- a shared object model + many viewers

Clients compete on UX.  
Formats guarantee portability and interoperability.

### 2) Real-time coordination across origins

Resources should sync in real time, offline-first, peer-to-peer when possible, and service-assisted when needed.

The service layer is not “the truth”.  
It’s routing, relays, indexing, hosting, availability, backups, and coordination.

**Authority stays with the Actor.**

### 3) Private *and* public resources

Sovereignbase is designed to support both:
- **private resources** (E2EE, local-first, selective disclosure, peer verification)
- **public resources** (publishable, cacheable, replicable, indexable, without turning platforms into identity owners)

### 4) Automation as a service model (not a custody model)

Automation is real. But “automation” must not imply “the platform owns your state”.

If automation needs access:
- it must be explicitly authorized by the Actor
- scoped to a narrow purpose and dataset
- time-bounded
- auditable and measurable in the UI
- revocable without collapsing your existence

Delegation without dependence.

---

## What Sovereignbase refuses to be

Sovereignbase does not:
- own your identity
- define your reality
- grant authority for your intentions
- require that a provider is “trusted” to be correct

Sovereignbase does:
- host resources you control (as a service, not as a throne)
- store and relay encrypted envelopes without needing plaintext
- enable peers to verify claims locally
- keep resources portable so provider shutdown is a business event, not an existential event

A provider has no inherent right to own your data or identity.  
A provider has no inherent obligation to host you forever.

Those statements do not conflict when the system is portable.

---

## Who this is for

### End users
- privacy without surveillance economics
- local-first state
- real exit: migrate without begging

### Service providers
- lower liability: operate infrastructure without handling sensitive user data
- better competition: users can migrate from a competitor without normalization headaches
- predictable costs: store/relay envelopes, not dossiers

### Platform builders
- build services, not prisons
- competition shifts to experience, not captivity

### Developers (and vibe coders)
- no surprise backend database work
- small, deterministic APIs
- sync + events patterns that map to real apps

---

## Where it fits (and where it doesn’t)

Fits:
- user/organization state layers
- collaborative and personal resources
- anything needing offline + sync + verification
- systems where the user must remain the authority

Doesn’t fit (by itself):
- unattended automation that must mutate state without user authorization
- systems that require third-party plaintext by default
- purely public discovery/search as the primary feature (use a purpose-built index)

Sovereignbase is a foundation. You can add specialized services without re-centralizing authority.

---

## Building blocks

Sovereignbase is being built from the bottom up as two layers that evolve together:

### 1) JS runtime-agnostic libraries + implementation-agnostic specs
We start by writing **JS runtime-agnostic JS/TS libraries** alongside **implementation-agnostic specifications**.

The specs focus on execution-level structure:
- data ontologies and semantics
- topologies and coordination models
- object handling, processing, and verification rules
- deterministic behavior and portability constraints

The goal is that multiple independent implementations can exist without divergence in meaning.

### 2) Pragmatic infrastructure first, then expand
For transport and storage we start with what is already widely deployable:
- **Browser APIs**
- **Cloudflare** (as an initial service substrate)

Then we expand to additional runtimes, environments, and platforms as the model stabilizes:
- wider JS runtime support
- native and Wasm support
- other providers and deployment targets

The priority is correctness of meaning and verification first; the hosting substrate is replaceable.

---

## Licensing

Everything produced by the Sovereignbase project is released under the **Apache License 2.0**.

This includes:
- Code
- Images
- Tooling
- Packages
- Specifications

The goal is to keep the ecosystem fully open and usable in both open-source and commercial environments.

---

## The invitation

Sovereignbase is not trying to build *the* app.  
It’s trying to make it obvious how to build **many** apps—viewers, editors, platforms, and services—around shared resources without reintroducing captivity.

If the web is going to serve people first, it needs to serve developers first: enabling competition on UX/UI **without** becoming data custodians, through simple, familiar APIs.

That’s the bet.

---

## Status

Early-stage, recursive specify<->implement iteration.

If you like CRDTs, portable formats, verifiable claims, E2EE, real-time coordination, and sovereignty-by-design... welcome!
