
![ironcore banner](/images/github-ironcore-banner-dark.png)

# Welcome to IronCore Labs - Makers of Data Security for Cloud Applications 👋

IronCore Labs makes usable, searchable application-layer encryption that helps developers and security teams lock down their sensitive cloud and AI data while keeping it usable.

## The application-layer encryption platform


The [IronCore SaaS Shield platform](https://ironcorelabs.com/products/saas-shield/) helps encrypt and manage data, regardless of data store, taking care of all of the difficult concerns of security, scalability, key orchestration, and smokin' fast performance. Together with [Cloaked Search](https://ironcorelabs.com/products/cloaked-search/) and [Cloaked AI](https://ironcorelabs.com/products/cloaked-ai/), it keeps that data usable, findable, and secure **even from the servers and services that hold the data.**

For SaaS apps, supports per-tenant encryption and key management with options for BYOK/HYOK, real-time audit trails direct to customers, and more. It can connect to all of the major KMSes with per tenant keys. And no sensitive data flows through IronCore, ever.

<!-- ![platform diagram](/images/ironcore-platform.png) -->

## Groundbreaking AI data protection

[IronCore's Cloaked AI](https://ironcorelabs.com/products/cloaked-ai/) product uses property-preserving encryption that maintains the distance relationships between vectors while encrypting them, allowing organizations to perform nearest neighbor searches, clustering, and anomaly detection over encrypted AI data and to build models over encrypted embeddings that require a key to use. 

The encryption technique is based on the paper, "Approximate Distance-Comparison-Preserving Symmetric Encryption" by Georg Fuchsbauer, Riddhi Ghosal, Nathan Hauke & Adam O'Neill, and utilizes the scale and perturb algorithm, which randomly adds noise and redistributes vectors while preserving relative distances. Read more about the [security of AI embeddings](https://ironcorelabs.com/ai-encryption/).

[![Play: Cloaked AI Demo](https://img.youtube.com/vi/SjZPizj4SvE/0.jpg)](https://youtu.be/SjZPizj4SvE)

## Explainers

### Graphics and Text
* [Application-layer encryption explained](https://ironcorelabs.com/application-layer-encryption/)
* [Security of AI embeddings explained](https://ironcorelabs.com/ai-encryption/)
* [Security Risks with RAG Architectures explained](https://ironcorelabs.com/security-risks-rag/)
* [Customer Managed Keys (CMK/BYOK/HYOK) explained](https://ironcorelabs.com/cmk/)
* [Crypto-agility and post-quantum explained](https://ironcorelabs.com/crypto-agility-post-quantum/)
* [View all](https://ironcorelabs.com/resources/)

### Videos

* 📺 [Vector Encryption Mini Explainer - YouTube](https://youtu.be/ALUrSo1pQRM)
* 📺 [SaaS Shield Application-layer Encryption Demo - YouTube](https://www.youtube.com/watch?v=NLJFEGg3wtk)
* 📺 [IronCore Labs Complete Product Suite Overview - YouTube](https://www.youtube.com/watch?v=igMKN26HXXA)
* 📺 [DEF CON 32 - Attacks on GenAI data &amp; using vector encryption to stop them - Patrick Walsh, Bob Wall - YouTube](https://youtu.be/Lxg9YyFJ8s0)
* 📺 [RMISC 2024 - Exploitable Weaknesses in Gen AI Workflows: From RAG to Riches - YouTube](https://www.youtube.com/watch?v=Mrx-i5M-RfU)
* 📺 [Post-Quantum Cryptography Explained - YouTube](https://www.youtube.com/watch?v=h_m8MiwTdqA)
* [View all](https://www.youtube.com/@ironcorelabs/videos)

## Open source repos

We believe in transparency and we talk openly about our choice of algorithms and our implementations. Most of our source code is open source and we invite security and crypto researchers to check it out.

Note: the open source licenses are mostly AGPL so if you plan to use it in commercial or non-GPL software, you'll need an inexpensive commercial license.

### SaaS Shield

Our client libraries are open source and can be found in our per-language `tenant-security-client` repos: 

* [tenant-security-client-go ![Go](https://img.shields.io/badge/go-%2300ADD8.svg?style=flat&logo=go&logoColor=white)](https://github.com/IronCoreLabs/tenant-security-client-go)
* [tenant-security-client-java ![tenant-security-client-java Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=flat&logo=openjdk&logoColor=white)](https://github.com/IronCoreLabs/tenant-security-client-java)
* [tenant-security-client-nodejs ![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=flat&logo=typescript&logoColor=white)](https://github.com/IronCoreLabs/tenant-security-client-nodejs)
* [tenant-security-client-php ![PHP](https://img.shields.io/badge/php-%23777BB4.svg?style=flat&logo=php&logoColor=white)](https://github.com/IronCoreLabs/tenant-security-client-php)

We have a public [demo application](https://github.com/IronCoreLabs/saas-shield-demo-notes-app) showing SaaS Shield with our S3 Proxy, Cloaked AI and Cloaked Search.

### Cloaked AI

We're in the process of building out a single unified library that generates interfaces for various languages.  It has most of the functionality of the `tenant-security-clients` and also contains all of the Cloaked AI vector encryption functionality. 

That's all in our [ironcore-alloy](https://github.com/IronCoreLabs/ironcore-alloy) repo, which is written in Rust and is currently published to:

![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=flat&logo=openjdk&logoColor=white) ![Kotlin](https://img.shields.io/badge/kotlin-%237F52FF.svg?style=flat&logo=kotlin&logoColor=white) ![Python](https://img.shields.io/badge/python-3670A0?style=flat&logo=python&logoColor=ffdd54) ![Rust](https://img.shields.io/badge/rust-%23000000.svg?style=flat&logo=rust&logoColor=white)

### Cloaked Search

We have a public repo that lets anyone quickly get started using a docker container and test data: [Try Cloaked Search](https://github.com/IronCoreLabs/try-cloaked-search).

We also have public benchmarks and published approaches to performance testing: [Cloaked Search Perf](https://github.com/IronCoreLabs/cloaked-search-perf).

### Data Control Platform

The Data Control Platform (DCP) lets developers build access controls directly into their data, regardless of where it's stored. It is particularly good for end-to-end encryption use cases.

This platform uses a proxy re-encryption algorithm (we call it [transform encryption in our docs](https://ironcorelabs.com/docs/data-control-platform/concepts/transform-encryption/)) to encrypt to a public key, then delegate decryption rights to other public keys. DCP enables the ability to encrypt to a group key and have group administrator(s) add or remove members at any time, effectively granting and revoking access to data that's encrypted to the group's public key.

> The details can be found in the ACM paper [Cryptographically Enforced Orthogonal Access Control at Scale](https://dl.acm.org/authorize?N654085).

The key libraries are audited and we have extensive documentation.

* **Command line tools**
    * [ironhide](https://github.com/IronCoreLabs/ironhide) -- command line tool for encrypting files to groups or users; can be used by anyone
    * [ironoxide-cli](https://github.com/IronCoreLabs/ironoxide-cli) -- command line interface for IronOxide functions to create users, devices, and groups; used by developers and admins
* **High-level crypto libraries (these use recrypt)**
    * [ironoxide](https://github.com/IronCoreLabs/ironoxide) -- rust library for interacting with the proxy re-encryption service! [Rust](https://img.shields.io/badge/rust-%23000000.svg?style=flat&logo=rust&logoColor=white)
    * [ironoxide-swift](https://github.com/IronCoreLabs/ironoxide-swift) -- swift bindings for ironoxide for iOS ![Swift](https://img.shields.io/badge/swift-F54A2A?style=flat&logo=swift&logoColor=white)
    * [ironoxide-swig-bindings](https://github.com/IronCoreLabs/ironoxide-swig-bindings) --  bindings to ironoxide for  ![Java](https://img.shields.io/badge/java-%23ED8B00.svg?style=flat&logo=openjdk&logoColor=white),  ![C++](https://img.shields.io/badge/c++-%2300599C.svg?style=flat&logo=c%2B%2B&logoColor=white), and ![android](https://img.shields.io/badge/android-3DDC84?style=flat&logo=android&logoColor=white)
    * [ironoxide-scala](https://github.com/IronCoreLabs/ironoxide-scala) --  bindings to ironoxide for Scala ![Scala](https://img.shields.io/badge/scala-%23DC322F.svg?style=flat&logo=scala&logoColor=white)
    * [ironnode](https://github.com/IronCoreLabs/ironnode) -- node library for interacting with the proxy re-encryption service ![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=flat&logo=typescript&logoColor=white)
    * [ironweb](https://github.com/IronCoreLabs/ironweb) -- web browser library for interacting with the proxy re-encryption service ![TypeScript](https://img.shields.io/badge/typescript-%23007ACC.svg?style=flat&logo=typescript&logoColor=white)
* **Low-level crypto libraries**
    * [recrypt-rs](https://github.com/IronCoreLabs/recrypt-rs) -- proxy re-encryption / transform cryptography library in rust (audited, constant time)
    * [gridiron](https://github.com/IronCoreLabs/gridiron) -- constant time big number math library used by recrypt-rs
    * [recrypt](https://github.com/IronCoreLabs/recrypt) -- proxy re-encryption / transform cryptography library in scala (audited, not constant time)
    * [recrypt-wasm-binding](https://github.com/IronCoreLabs/recrypt-wasm-binding) -- build recrypt-rs for use in browsers
    * [recrypt-node-binding](https://github.com/IronCoreLabs/recrypt-node-binding) -- build recrypt-rs for use in node


### Other

* [phonetic-normalizer](https://github.com/IronCoreLabs/phonetic-normalizer) -- store latin-language words in pseudo-phonetic form
* [futurejs](https://github.com/IronCoreLabs/futurejs) -- promise-alternative library for asynchronous operations
* [cats-scalatest](https://github.com/IronCoreLabs/cats-scalatest) -- Scalatest bindings for Cats


## Community

IronCore Lab's community is a great way to contribute knowledge, learn, and otherwise participate in bringing better data security and privacy to apps.

* [Discord server](https://discord.gg/HMpce3NfQz) -- Get help, ask quick questions, show off your work, and get to know other IronCore Labs users.
* [Forums](https://github.com/IronCoreLabs/community/discussions) -- Post feature requests, report bugs, ask questions, and have in-depth discussions about privacy and security.


## About us

IronCore Labs is a pioneering force in data privacy with proven security for AI data, cloud data, and encrypted search.

Founded in 2015 and headquartered in Boulder, Colorado, the company focuses on making [application-layer encryption](https://ironcorelabs.com/application-layer-encryption/) a pattern that is adopted by everyone to improve the security of all of us.

