<!-- BEGIN_TF_DOCS -->

## Providers

| Name | Version |
|------|---------|
| <a name="provider_aws"></a> [aws](#provider\_aws) | n/a |
| <a name="provider_helm"></a> [helm](#provider\_helm) | n/a |
| <a name="provider_null"></a> [null](#provider\_null) | n/a |
## Inputs

| Name | Description | Type | Default | Required |
|------|-------------|------|---------|:--------:|
| <a name="input_eks_cluster_name"></a> [eks\_cluster\_name](#input\_eks\_cluster\_name) | The name of EKS cluster to get OIDC ARN and Name | `any` | n/a | yes |
| <a name="input_force_detach_policies"></a> [force\_detach\_policies](#input\_force\_detach\_policies) | Flag to force detachment of policies attached to the IAM role. | `string` | `false` | no |
| <a name="input_iam_role_path"></a> [iam\_role\_path](#input\_iam\_role\_path) | Path under which to create IAM role. | `string` | `"/"` | no |
| <a name="input_s3_kms_policy_arns"></a> [s3\_kms\_policy\_arns](#input\_s3\_kms\_policy\_arns) | List of IAM policies to attach IAM role | `list` | <pre>[<br>  "arn:aws:iam::aws:policy/AmazonS3FullAccess",<br>  "arn:aws:iam::aws:policy/AWSKeyManagementServicePowerUser"<br>]</pre> | no |
| <a name="input_vault_backend_bucket_kms_key"></a> [vault\_backend\_bucket\_kms\_key](#input\_vault\_backend\_bucket\_kms\_key) | The ID of the KMS key | `string` | `"alias/aws/s3"` | no |
| <a name="input_vault_backend_bucket_name"></a> [vault\_backend\_bucket\_name](#input\_vault\_backend\_bucket\_name) | The name of s3 bucket for backend | `any` | n/a | yes |
| <a name="input_vault_backend_bucket_region"></a> [vault\_backend\_bucket\_region](#input\_vault\_backend\_bucket\_region) | The region of the s3 bucket | `string` | `"us-east-1"` | no |
| <a name="input_vault_s3_kms_role_name"></a> [vault\_s3\_kms\_role\_name](#input\_vault\_s3\_kms\_role\_name) | Role used by the Vault as S3 backend | `string` | `"vault_s3_kms_role"` | no |
| <a name="input_vault_yml_file"></a> [vault\_yml\_file](#input\_vault\_yml\_file) | n/a | `any` | `null` | no |
## Resources

| Name | Type |
|------|------|
| [aws_iam_role.vault_s3_kms_role](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role) | resource |
| [aws_iam_role_policy_attachment.s3_kms](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/resources/iam_role_policy_attachment) | resource |
| [helm_release.vault](https://registry.terraform.io/providers/hashicorp/helm/latest/docs/resources/release) | resource |
| [null_resource.create_vault_yml](https://registry.terraform.io/providers/hashicorp/null/latest/docs/resources/resource) | resource |
| [aws_eks_cluster.cluster](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/eks_cluster) | data source |
| [aws_iam_policy_document.assume_role](https://registry.terraform.io/providers/hashicorp/aws/latest/docs/data-sources/iam_policy_document) | data source |
## Outputs

No outputs.
# 🚀 Built by opsZero!

<a href="https://opszero.com"><img src="https://opszero.com/wp-content/uploads/2024/07/opsZero_logo_svg.svg" width="300px"/></a>

Since 2016 [opsZero](https://opszero.com) has been providing Kubernetes
expertise to companies of all sizes on any Cloud. With a focus on AI and
Compliance we can say we seen it all whether SOC2, HIPAA, PCI-DSS, ITAR,
FedRAMP, CMMC we have you and your customers covered.

We provide support to organizations in the following ways:

- [Modernize or Migrate to Kubernetes](https://opszero.com/solutions/modernization/)
- [Cloud Infrastructure with Kubernetes on AWS, Azure, Google Cloud, or Bare Metal](https://opszero.com/solutions/cloud-infrastructure/)
- [Building AI and Data Pipelines on Kubernetes](https://opszero.com/solutions/ai/)
- [Optimizing Existing Kubernetes Workloads](https://opszero.com/solutions/optimized-workloads/)

We do this with a high-touch support model where you:

- Get access to us on Slack, Microsoft Teams or Email
- Get 24/7 coverage of your infrastructure
- Get an accelerated migration to Kubernetes

Please [schedule a call](https://calendly.com/opszero-llc/discovery) if you need support.

<br/><br/>

<div style="display: block">
  <img src="https://opszero.com/wp-content/uploads/2024/07/aws-advanced.png" width="150px" />
  <img src="https://opszero.com/wp-content/uploads/2024/07/AWS-public-sector.png" width="150px" />
  <img src="https://opszero.com/wp-content/uploads/2024/07/AWS-eks.png" width="150px" />
</div>
<!-- END_TF_DOCS -->