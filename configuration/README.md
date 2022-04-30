# Configuration

Every environments or deployment targets needs two files: main.tfvars and main.backend.tfvars.

* main.tfvars
  * contains envrionment specific and/or project variables
  * account_id ensures resources are deployed to the correct account
  * stage defines the DTAP environment

* main.backend.tfvars
  * partial configuration of terraform "backend"
  * specifies the terraform state file name that will be created in S3

Configurations can be created in several different ways:

## One Configuration

For simple projects where there is only one environment or deployment target.

|- configuration
    |-  main.tfvars
        main.backend.tfvars

## Single-tenant DTAP environments

Folder names are not fixed.

|- configuration
    |- dev
        |-  main.tfvars
            main.backend.tfvars
    |- tst
        |-  main.tfvars
            main.backend.tfvars
    |- acc
        |-  main.tfvars
            main.backend.tfvars
    |- prd
        |-  main.tfvars
            main.backend.tfvars

## Multi-tenant DTAP environments

|- configuration
    |- client_aaa
        |- dev
            |-  main.tfvars
                main.backend.tfvars
        |- tst
            |-  main.tfvars
                main.backend.tfvars
        |- acc
            |-  main.tfvars
                main.backend.tfvars
        |- prd
            |-  main.tfvars
                main.backend.tfvars
    |- client_bbb
        |- dev
            |-  main.tfvars
                main.backend.tfvars
        |- tst
            |-  main.tfvars
                main.backend.tfvars
        |- acc
            |-  main.tfvars
                main.backend.tfvars
        |- prd
            |-  main.tfvars
                main.backend.tfvars
