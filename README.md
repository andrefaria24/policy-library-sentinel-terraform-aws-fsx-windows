# Sentinel policies for Amazon FSx for Windows File Server

This repository provides Sentinel policies for Amazon FSx for Windows File Server to be used within either HCP Terraform or Terraform Enterprise.

## Policies

| Scope                              | Rule                                        | Description                                                                                | Enforcement level | URLs                                          |
|------------------------------------|---------------------------------------------|--------------------------------------------------------------------------------------------|-------------------|-----------------------------------------------|
| Amazon FSx for Windows File Server | deny-fsx-win-deletion                       | Prevents data-loss by denying the deletion of Amazon FSx for Windows File Server resources | hard-mandatory    | [doc](docs/policies/deny-fsx-win-deletion.md) | 