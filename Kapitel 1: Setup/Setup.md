# Chapter 1: Setup

## Prerequisite

 - Github.com or Github Enterprise Repository
 - Basic Knowlegde about BASH/CMD/SHELL
 - Things :)

## Starting Point

Github Actions or Workflows are an easy way of building, deploying or integrating projects based on the git repository it is executing on. This means that each starting point for an Action is the repository it is created on. As default the runners (executors) will be hosted and managed by github.com itself and every repository/organization gets Build minutes. Foreach repository and organization are free build minutes included from the pooled runners. This can be extended with paying by the minute. 

[Official Github Action Billing Documentation](https://docs.github.com/en/billing/managing-billing-for-github-actions/about-billing-for-github-actions)


## Runners

### Github-hosted runners

Standard runner for almost all use cases that don't need custom tools or are not in enterprise scenarios which got additional security requirements (only available on github.com).

 - OS: ubuntu, windows and macos (always latest version)
 - Hardware: 2core, 7GB RAM, 14 GB SSD
 - Installed Tools: [Long list of installed tools](https://github.com/actions/runner-images#software-and-image-support)


### Self-hosted runners

Self-hosted runner that is completly managed by you. All installation is done by you and handled. The registering of runners needs to be done manual (can be automated in image start in container setup [Docker Image](https://hub.docker.com/repository/docker/vexx662/github-action-runner-proxy)) on repository or organization level. This type of runner is the only option for the usage in github enterprise. For starting using a basic VM with preinstalling all nesecary tools is completly fine and can handle almost all use cases. Only in bigger use cases with many parallel long running executions scalling via container is advised!

 - OS: anything you want! (Linux highly advised!)
 - Hardware: use case specfic start with lowest possible (2 core, 4GB RAM)
 - Tools: everything you need! (python is advised to install on every runner)

Remarks:
 - Runner will grab all actions that are pending so high availability is no must!
 - Issues on VM level can cause problems that are not logged in github action
 - Network issues for accessing internal company resources can be challening
 - Handling of Updates and Security must be handled by yourself!

[Official Github Self Hosted Runner Documentation](https://docs.github.com/en/actions/hosting-your-own-runners/about-self-hosted-runners)

