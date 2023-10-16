# UCAN Promise Specification v1.0.0-rc. 1

## Editors

- [Brooklyn Zelenka], [Fission]
- [Irakli Gozalishvili], [DAG House]

## Authors

- [Brooklyn Zelenka], [Fission]
- [Irakli Gozalishvili], [DAG House]
- [Zeeshan Lakhani], [Fission]

## Depends On

- [DAG-CBOR]
- [DID]
- [UCAN Invocation]

## Language

The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED", "NOT RECOMMENDED", "MAY", and "OPTIONAL" in this document are to be interpreted as described in [BCP 14] when, and only when, they appear in all capitals, as shown here.

# 0 Abstract

This specification describes a mechanism for extending UCAN [Invocation]s with distributed [promise pipeline]s.

# 1 Introduction

## 1.1 Motivation

# 2 Format

| Tag           | Type    | Description |
|---------------|---------|-------------|
| `await/*`     | `&Task` |             |
| `await/ok`    | `&Task` |             |
| `await/error` | `&Task` |             |

# 3 Resolution

# 4 Prior Art

[ucanto RPC] from [DAG House] is a production system that uses UCAN as the basis for an RPC layer.

The [Capability Transport Protocol (CapTP)] is one of the most influential object-capability systems, and forms the basis for much of the rest of the items on this list.

The Object Capability Network ([OCapN]) protocol extends [CapTP] with a generalized networking layer. It has implementations from the [Spritely Institute] and [Agoric]. At time of writing, it is in the process of being standardized.

[Electronic Rights Transfer Protocol (ERTP)] builds on top of [CapTP] concepts for blockchain & digital asset use cases.

[Cap 'n Proto RPC] is an influential RPC framework based on concepts from [CapTP].

# 5 Acknowledgements

Many thanks to [Mark Miller] for his [trail blazing work][erights] on [capability systems].

Many thanks to [Luke Marsen] and [Simon Worthington] for their feedback on invocation model from their work on [Bacalhau] and [IPVM].

Thanks to [Marc-Antoine Parent] for his discussions of the distinction between declarations and directives both in and out of a UCAN context.

Many thanks to [Quinn Wilton] for her discussion of speech acts, the dangers of signing canonicalized data, and ergonomics.

Thanks to [Blaine Cook] for sharing their experiences with OAuth 1, irreversible design decisions, and advocating for keeping the spec simple-but-evolvable.

Thanks to [Philipp Krüger] for the enthusiastic feedback on the overall design and encoding.

Thanks to [Christine Lemmer-Webber] for the many conversations about capability systems and the programming models that they enable.

Thanks to [Rod Vagg] for the clarifications on IPLD Schema implicits and the general IPLD worldview

<!-- Footnotes -->

[^js-num]: JavaScript has a single numeric type ([`Number`][JS Number]) for both integers and floats. This representation is defined as a [IEEE-754] double-precision floating point number, which has a 53-bit significand.
 
<!-- Internal Links -->

[Arguments]: #312-arguments
[Command]: #311-command
[Execution Proxy]: #41112-proxy-execution
[Executor]: #212-executor
[Invocation Payload]: #331-invocation-payload
[Invocation Signature]: #331-invocation-envelope
[Invocation]: #33-invocation
[Invoker]: #211-invoker
[Nonce]: #314-nonce
[Receipt Payload]: #411-receipt-payload
[Receipt]: #42-receipt
[Response]: #4-response
[Result]: #41-result
[Subject]: #313-subject
[Task]: #32-task
[enqueue]: #4111-enqueue
[lazy-vs-eager]: #112-lazy-vs-eager-evaluation

<!-- External Links -->

[Ability]: https://github.com/ucan-wg/delegation#33-abilities
[Agoric]: https://agoric.com/
[BCP 14]: https://www.rfc-editor.org/info/bcp14
[Bacalhau]: https://www.bacalhau.org/
[Blaine Cook]: https://github.com/blaine
[Brooklyn Zelenka]: https://github.com/expede/
[CapTP]: https://capnproto.org/rpc.html#specification
[Christine Lemmer-Webber]: https://github.com/cwebber
[DAG House]: https://dag.house
[DAG-CBOR]: https://ipld.io/specs/codecs/dag-cbor/spec/
[DID]: https://www.w3.org/TR/did-core/
[Delegation]: https://github.com/ucan-wg/delegation
[E-lang Mailing List, 2000 Oct 18]: http://wiki.erights.org/wiki/Capability-based_Active_Invocation_Certificates
[Electronic Rights Transfer Protocol (ERTP)]: https://docs.agoric.com/guides/ertp/
[Fission]: https://fission.codes/
[Haskell]: https://en.wikipedia.org/wiki/Haskell
[IPVM]: https://github.com/ipvm-wg
[Irakli Gozalishvili]: https://github.com/Gozala
[JS Number]: https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Number
[Luke Marsen]: https://github.com/lukemarsden
[Marc-Antoine Parent]: https://github.com/maparent
[Mark Miller]: https://github.com/erights
[OCapN]: https://github.com/ocapn/
[Philipp Krüger]: https://github.com/matheus23/
[Quinn Wilton]: https://github.com/QuinnWilton
[Robust Composition]: http://www.erights.org/talks/thesis/markm-thesis.pdf
[Rod Vagg]: https://github.com/rvagg/
[Simon Worthington]: https://github.com/simonwo
[Spritely Institute]: https://spritely.institute/news/introducing-a-distributed-debugger-for-goblins-with-time-travel.html
[UCAN Ability]: https://github.com/ucan-wg/delegation/#23-ability
[UCAN Delegation]: https://github.com/ucan-wg/delegation/
[UCAN Promise]: https://github.com/ucan-wg/promise/
[URI]: https://en.wikipedia.org/wiki/Uniform_Resource_Identifier
[Zeeshan Lakhani]: https://github.com/zeeshanlakhani
[`data`]: https://en.wikipedia.org/wiki/Data_URI_scheme
[`ipfs`]: https://docs.ipfs.tech/how-to/address-ipfs-on-web/#native-urls
[`magnet`]: https://en.wikipedia.org/wiki/Magnet_URI_scheme
[capability systems]: https://en.wikipedia.org/wiki/Capability-based_security
[distributed promise pipelines]: http://erights.org/elib/distrib/pipeline.html
[eRights]: https:/erights.org
[erights]: https://erights.org
[ucanto RPC]: https://github.com/web3-storage/ucanto
