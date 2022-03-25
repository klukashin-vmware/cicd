# Overall Infra Automation setup

1.1.	Artifacts

All artifacts are in GitEA repo: https://gitea.rogers.lab/klukashin/cicd

Concourse pipelines folder: https://gitea.rogers.lab/klukashin/cicd/src/branch/master/pipelines

Ansible playbooks folder: 
https://gitea.rogers.lab/klukashin/cicd/src/branch/master/ansible

Values.yaml for ECS folder:
https://gitea.rogers.lab/klukashin/cicd/src/branch/master/ECS_Values
https://gitea.rogers.lab/klukashin/cicd/src/branch/master/ECS_XXX_Values, where XXX is environment(QA1/2/3, DEV1/2/3)

Artifacts for Upgrade folder:
https://gitea.rogers.lab/klukashin/cicd/src/branch/master/Upgrade

1.2.	Pre-requisites


The following are pre-requisites to make it work:
1.	Concourse is installed on Jumphost. Concourse CLI(FLY) is installed
2.	Concourse pipelines are pushed to Concourse using Fly CLI 

1.3.	How it works

Concourse pipelines check out GitEA repo and run relevant Ansible Playbook. Ansible playbook calls relevant APIs(TCA, NSX-T, AVI, NetBox)
