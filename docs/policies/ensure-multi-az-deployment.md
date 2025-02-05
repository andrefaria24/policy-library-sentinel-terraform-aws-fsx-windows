# Ensure Amazon FSx for Windows File Server resources are created with a Multi-AZ configuration

This policy is aimed at ensuring production FSx for Windows File Server deployments are created using the Multi-AZ option.

AWS recommends using Multi-AZ file systems for most production workloads. However, Single-AZ deployments can be a cost-efficient solution for non-production workloads as well. Please consult the [Amazon FSx for Windows File Server User Guide](https://docs.aws.amazon.com/fsx/latest/WindowsGuide/high-availability-multiAZ.html) to determine which file system deployment type is appropriate your use case.

## Testing the policy

Changing the deployment_type value from "MULTI_AZ_1" to "SINGLE_AZ_1" or "SINGLE_AZ_2" within the following example resource will prevent the creation of the file system, causing the test to fail:

```terraform
resource "aws_fsx_windows_file_system" "example" {
  active_directory_id  = aws_directory_service_directory.bar.id
  kms_key_id           = aws_kms_key.a.arn
  storage_capacity     = 300
  subnet_ids           = [aws_subnet.foo.id]
  throughput_capacity  = 2048
  copy_tags_to_backups = false
  deployment_type = "MULTI_AZ_1"
}
```