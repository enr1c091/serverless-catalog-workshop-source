---
title: "Create a Workspace"
chapter: false
weight: 14
---

{{% notice warning %}}
The Cloud9 workspace should be built by an IAM user with Administrator privileges,
not the root account user. Please ensure you are logged in as an IAM user, not the root
account user.
{{% /notice %}}

{{% notice tip %}}
Ad blockers, javascript disablers, and tracking blockers should be disabled for
the cloud9 domain, or connecting to the workspace might be impacted.
Cloud9 requires third-party-cookies. You can whitelist the [specific domains]( https://docs.aws.amazon.com/cloud9/latest/user-guide/troubleshooting.html#troubleshooting-env-loading).
{{% /notice %}}

### Launch Cloud9 in your closest region:
{{< tabs name="Region" >}}
{{{< tab name="N. Virginia" include="us-east-1.en.md" />}}
{{{< tab name="Oregon" include="us-west-2.en.md" />}}
{{{< tab name="Ireland" include="eu-west-1.en.md" />}}
{{{< tab name="Ohio" include="us-east-2.en.md" />}}
{{{< tab name="Singapore" include="ap-southeast-1.en.md" />}}
{{< /tabs >}}

- Select **Create environment**
- Name it **serverless-catalog-workshop**, click Next.
- Choose **"t3.small"** for instance type, take all default values and click **Create environment**
- When it comes up, customize the environment by closing the **welcome tab**
and **lower work area**, and opening a new **terminal** tab in the main work area:
![c9before](/images/c9before.png)

- Your workspace should now look like this:
![c9after](/images/c9after.png)

- If you like this theme, you can choose it yourself by selecting **View / Themes / Solarized / Solarized Dark**
in the Cloud9 workspace menu.

#### Install jq
```
sudo yum -y install jq 
```