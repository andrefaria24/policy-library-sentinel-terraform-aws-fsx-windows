# Deny Amazon FSx for Windows File Server deletion

## Testing the policy

Changing the copy_tags_to_backups value from false to true within the following example resource will trigger resource deletion, causing the test to fail:

```terraform
resource "aws_fsx_windows_file_system" "example" {
  active_directory_id  = aws_directory_service_directory.bar.id
  kms_key_id           = aws_kms_key.a.arn
  storage_capacity     = 300
  subnet_ids           = [aws_subnet.foo.id]
  throughput_capacity  = 2048
  copy_tags_to_backups = false
}
```