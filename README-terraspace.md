#  Terraspace
Version: v2.2.2

- This is a Terraspace project. It contains code to provision Cloud infrastructure built with [Terraform](https://www.terraform.io/) and the [Terraspace Framework](https://terraspace.cloud/).
- [Installing Terraspace](https://terraspace.cloud/docs/install/)
- **Modules** are reusable pieces of code. Generally, it contains non-business specific logic (same as in Terraform).
- **Stacks** are meant to be used to group together modules. Generally, this is where business-specific logic goes (equivalent to Terraform root modules).
- **Switch between environments** with `TS_ENV=stage` env var. `TS_ENV=dev terraspace up demo -y`  . This affects which `app/stacks/<stack>/tfvars/<environment>.tfvars` will be used.

## Commands
#### Initial commands
```
terraspace setup check

export AWS_REGION=<eg us-west-2>
export AWS_PROFILE=<eg default>
export TS_ENV=<eg stage>

terraspace new project <project name> --plugin aws
terraspace new project terraspace --plugin aws
cd <project name>

terraspace new stack main

# `terraform init` but for all stacks
terraspace all init


terraspace all up -y
terraspace all down -y

```

### Features
- Use[ advanced layering](https://terraspace.cloud/docs/layering/full-layering/#layering-modes-simple-namespace-provider) to deploy to different aws accounts or different cloud providers.

### Known problems
- Deleting `.tf` file does not delete it from the `.terraspace-cache` directory.

### Variables
- `terraspace/config/terraform/terraform.tfvars` This is one way to set a global  (for all stacks and environments) `.tfvars` file.
- `terraspace seed <stack>` to create new `<TS_ENV>.tfvars` file in `<stack>` stack.



# Repo convention
### Commit messages style
Use the same formatting for commit messages like [conventional commits](https://www.conventionalcommits.org/) suggests.
```txt

<type>[optional scope]: <description>

[optional body]

[optional footer(s)]

```
Following this convention, `standard-version` will be able generate `CHANGELOG.md`  automatically.
Conventional commits can be "enforced" with Husky. [Husky](https://typicode.github.io/husky/#/) is a tool for git hooks.
Do `npx husky install` to install **githooks** into this repo.
`.husky/commit-msg` enforces commit messages to follow [conventional commits](https://www.conventionalcommits.org/en/v1.0.0/).
In this repo `.commitlintrc.yaml` is for this purpose.
