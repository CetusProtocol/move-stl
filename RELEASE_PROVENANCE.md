# MoveSTL v6 source publication

Production sources and tests are copied from CetusProtocol/cetus-for-audit at `bf90ea71dce3786dfb3f32aace1f0b25b79ac347`, path `move-stl`. The production source files are unchanged from the supplied release commit `0faa42a9783a2cfe7d6e773abde6600c58ccb280`; subsequent changes record deployment metadata and release documentation.

Mainnet package v6: `0xab8e703f093e1d3efa04cca4494bd07ab926b2a189879fc9fe62f34532657464`.
Original package: `0xbe21a06129308e0495431d12286127897aff07a8ade3970495a4404d97f9eaaa`.
Upgrade transaction: `H1dRraMNowXZRQmSBSZRUKZkWDgm5pdSk8af3W5MBF9t`.

Changes include the optional u64 skip-list bitmap index and rejection of zero maximum levels for u64/u128 initialization. Publication metadata is retained from the release snapshot. Source verification is reproduced explicitly with the installed Sui 1.81.1 binary; this override is separate from the toolchain recorded by the original publisher.

```sh
sui client verify-source . --build-env mainnet --toolchain "$(command -v sui)"
sui move test --build-env mainnet --gas-limit 10000000000
```
