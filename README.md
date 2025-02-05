# Amazon FSx for Windows File Server Sentinel Policies for Terraform

This repository provides Sentinel policies for Amazon FSx for Windows File Server to be used within either HCP Terraform or Terraform Enterprise.

## Policies included

- Prevent data-loss by denying the deletion of Amazon FSx for Windows File Server resources ([docs](docs/policies/deny-fsx-win-deletion.md) | [code](policies/deny-fsx-win-deletion/deny-fsx-win-deletion.sentinel))
- Ensure high availability by creating Multi-AZ Amazon FSx for Windows File Server resources ([docs](docs/policies/ensure-multi-az-deployment.md) | [code](policies/ensure-multi-az-deployment/ensure-multi-az-deployment.sentinel))