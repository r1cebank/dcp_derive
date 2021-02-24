# DCP Key Derive Tool

Using NXP Data Co-Processor (DCP) to encrypt input with derived key

The unique OTPMK internal key is available only when Secure Boot (HAB) is enabled, otherwise a Non-volatile Test Key (NVTK), identical for each SoC, is used. The secure operation of the DCP and SNVS, in production deployments, should always be paired with Secure Boot activation.

The key derivation code is based on: https://github.com/f-secure-foundry/mxs-dcp

## Building

```
go build -ldflags "-s -w" -o dcp_derive dcp_derive.go
```
