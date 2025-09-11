# Segmented Memory for R1CS

This repo contains our implementation of segmented memory as described in the [Coral paper](https://eprint.iacr.org/2025/1420.pdf).

We provide R1CS circuits, written in [arkworks](https://github.com/arkworks-rs), for several types of memory:
1. Our proposed segmented memory based on [Nebula](https://eprint.iacr.org/2024/1605.pdf) with segment-specific optimizations. It can be used with our [modified commitmit-carrying IVC version of Nova](https://github.com/jkwoods/Nova/tree/main).
2. A version of [Hekaton's memory construction](https://dl.acm.org/doi/pdf/10.1145/3658644.3690282?casa_token=PPpYVYkg0-wAAAAA:JOAcsNOzp071hfZpHEXRquOWhuMQq6NZMpBMKYcWGSO-7GF5S7s01zn_3XCaxYr5a90JY3v5KuAr), that needs our modified Nova.
3. Hash stack memory with the [Poseidon hash](https://www.usenix.org/system/files/sec21-grassi.pdf).
4. A version of the [nlookup protocol](https://eprint.iacr.org/2023/573.pdf) (that is, the nlookup verifier is made noninteractive and expressed as R1CS) that incorporates hybrid tables and projection optimizations as described [here](https://eprint.iacr.org/2023/1886.pdf).

It also contains code for converting between arkworks and [bellperson](https://github.com/filecoin-project/bellperson) (the circuit library used in Nova).
