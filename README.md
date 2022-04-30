# ITC - Terraform Project Template

![CI workflow](https://github.com/indigo-tangerine/itc-tfm-project-template/actions/workflows/ci-pr.yml/badge.svg)
![CD workflow](https://github.com/indigo-tangerine/itc-tfm-project-template/actions/workflows/cd-pr.yml/badge.svg)

## Stuff that needs to be updated/changed

* Organization and repository names in lines 3 and 4 above. This ensures the badges display the correct values.
* configuration/main.backend.tfvars
  * Terraform state file name ("key" variable)
* configuration/main.tfvars
  * AWS Account ID ("aws_account_id" variable)
  * DTAP environment or deployment target ("stage" variable)
  * AWS Region ("aws_region" variable)
  * Client short name/code, if applicable ("client" variable)
* variables.tf
  * Project, application or service name ("service" variable)
  * Github organization name ("github_org" variable)
* backend.tf
  * Terraform state bucket name
  * Dynamodb state lock table name
* locals.tf
  * CICD automation role name ("cicd_automation_role_name" variable)
