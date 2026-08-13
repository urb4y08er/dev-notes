# Terraform State Management Notes

- Always use remote state (S3 + DynamoDB lock) for team projects.
- For personal experiments, local state is fine, but keep it out of git.
- Use `terraform plan -out` to review changes before apply.
- Tag resources with `terraform:managed` for easy cleanup.
- Remember: state file contains secrets — never commit it.

Quick command:
```bash
terraform state list
```

TODO: Document our module registry setup.