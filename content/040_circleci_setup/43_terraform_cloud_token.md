---
title: "1.2 Terraform Cloud: Create API Token"
chapter: true
weight: 14
---

## Terraform Cloud

Terraform Cloud is an application that helps teams use Terraform together. It manages Terraform runs in a consistent and reliable environment, and includes easy access to shared state and secret data, access controls for approving changes to infrastructure, a private registry for sharing Terraform modules, detailed policy controls for governing the contents of Terraform configurations, and more.

You will be using Terraform Cloud to store the [Terraform state][1] of the infrastructures your pipeline will provision and deploy using Terraform in future modules.


## Create Terraform Cloud Access Token

1. Create a [Terraform Cloud][4] account
1. Create a new [Terraform Cloud organization][7]
1. Create two new [Terraform Cloud workspace][8] named:
    - **app-aws-circleci**
    - **ecr-aws-circleci**
1. Click the **CLI-driven workflow** option for both spaces
1. In the workspace, click **app-aws-circleci** > **Settings** > **General** then enable [local execution mode][18]
1. In the workspace, click **ecr-aws-circleci** > **Settings** > **General** then enable [local execution mode][18]
1. Go to the [User Settings section][16] in the Terraform Cloud Dashboard
1. In the User Settings section, Create a new [Terraform API token][17] then copy and paste the token in a secure location for later use.

{{% notice warning %}}
Your Terraform Cloud API token must be protected and not shared with unauthorized parties to prevent exposure and unauthorized access.
{{% /notice %}}

Great, you have created and safely stored your newly created Terraform Cloud API Token, Now, we can create AWS access keys and secrets.

<!-- URL Links index -->
[1]: https://www.terraform.io/docs/language/state/index.html
[4]: https://app.terraform.io/signup/account
[7]: https://learn.hashicorp.com/terraform/cloud-getting-started/signup#create-your-organization
[8]: https://learn.hashicorp.com/terraform/cloud-getting-started/create-workspace
[16]: https://www.terraform.io/docs/cloud/users-teams-organizations/users.html#user-settings
[17]: https://www.terraform.io/docs/cloud/users-teams-organizations/users.html#api-tokens
[18]: https://www.terraform.io/docs/cloud/workspaces/settings.html#execution-mode