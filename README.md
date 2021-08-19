# cloudiac-pulumi
Pulumi based Infrastructure as Code
[![Open in Gitpod](https://gitpod.io/button/open-in-gitpod.svg)](https://gitpod.io/#https://github.com/netresearch-cloudiac/cloudiac-pulumi)

## install pulumi
Install Pulumi on Linux by running the installation script:

```shell
curl -fsSL https://get.pulumi.com | sh
```

This will install the pulumi CLI to ~/.pulumi/bin and add it to your path. When it can’t automatically add pulumi to your path, you will be prompted to add it manually (you can it by below shell command)

```shell
export PATH=$PATH:~/.pulumi/bin
```

# Azure setup

## Azure login and set default subscription
```shell
$az login
The default web browser has been opened at https://login.microsoftonline.com/common/oauth2/authorize. Please continue the login in the web browser. If no web browser is available or if the web browser fails to open, use device code flow with `az login --use-device-code`.

$az account list

Pick out the <id> from the list and run:

$az account set --subscription=<id>
```

## Setup programatic access in Azure
- setup service principle on azure
- alloow contributor role for the service principle

## Setup ENV variables 

```shell
export ARM_CLIENT_ID="WWWWWWWW-WWWW-WWWW-WWWW-WWWWWWWWWWWW"
export ARM_CLIENT_SECRET="XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX"
export ARM_TENANT_ID="YYYYYYYY-YYYY-YYYY-YYYY-YYYYYYYYYYYY"
export ARM_SUBSCRIPTION_ID="ZZZZZZZZ-ZZZZ-ZZZZ-ZZZZ-ZZZZZZZZZZZZ"
```

## Create a new project
Now that you have set up your environment by installing Pulumi, installing your preferred language runtime, and configuring your Azure credentials, let’s create your first Pulumi program.
```shell
$mkdir quickstart && cd quickstart 
$pulumi new azure-python
```

## Deploy the stack
```shell
pulumi up
```

## remove the stack
```shell
pulumi destroy
```



