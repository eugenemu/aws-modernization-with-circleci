---
title: "1.6 CircleCI: Setup Project"
chapter: true
weight: 20
---

In the previous section, you forked the [example project repository][1] in GitHub and now you will learn how to add that project to CircleCI. 

## Step 1 &mdash; Adding the project to CircleCI

1. Now go to your [CircleCI dashboard](https://circleci.com/vcs-authorize/). If you haven't signed up at this point, log in with your GitHub credentials.
1. ![CircleCI Login](/images/circleci-signup.png) 
1. On the left-hand side, click the Projects section and you will land here:
1. ![CircleCI Projects Dashboard](/images/circleci-project-dashboard.png)
1. Click **Set Up Project** next to the name of your new project.
1. This opens the **New Project Set Up** page, select the **Skip this step** option.
1. ![Skip Config](/images/skip-config.png)
1. Click **Use Existing Config** button
1. Click **Start Building** button

Congratulations! You have just triggered your first pipeline build on CircleCI. The example project has the default config.yml file with the default pipeline definition which will trigger the first build in your new project. In future modules, you will replace the entire contents of this file as you make progress in this workshop.

## Step 2 &mdash; Configure project environment variables

Before you start building your pipeline, you must create project environment variables that will provide the integration access to the services you previously registered for. All of the Access and API tokens you previous generated will now be assigned to new project environment variables that will serve as values in your config syntax.

Now you will create new project environment variables in CircleCI using the key and tokens you previously created.

On your CircleCI dashboard, navigate to `Project Settings > Environment Variables` in the CircleCI control panel and add these keys and values in their respective fields:

```bash
Name: AWS_ACCESS_KEY_ID 
Value: Your AWS IAM Accounts Access Key ID

Name: AWS_SECRET_ACCESS_KEY 
Value: Your AWS IAM Accounts Secret Access Key

Name: DOCKER_LOGIN 
Value: Your Docker Hub User login

Name: DOCKER_PASSWORD
Value: Your Docker Hub Access Token

Name: SNYK_TOKEN 
Value: Your Snyk Access Token

Name:   TERRAFORM_TOKEN 
Value: Your Terraform Cloud API Token
```

After entering all of the environment variables listed above, your environment variables dialog should look similar to the image below.

![Add Env Variable](/images/add-env-var.png)

Click the **X** in the top right corner to return to the pipeline dashboard.

Your project is now setup in CircleCI and now you can start building a new pipeline for your project.

<!-- URL Links index -->
[1]: https://github.com/aws-samples/aws-modernization-with-circleci
[2]: https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh
[3]: https://docs.github.com/en/github/authenticating-to-github/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account