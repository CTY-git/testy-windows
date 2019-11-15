# [:] Using SourceClear via Azure DevOps

1. We'll [do this](azure-pipelines.yml) as the equivalent of [CI script](https://help.veracode.com/reader/hHHR3gv0wYc2WbCclECf_A/_p_RJqZHXQ4S5pkjSXCrzQ) for Powershell.
1. Add a [defined container action](docker/Dockerfile), which makes it easy to set up a build environment for your project, to a [container registry](https://docs.microsoft.com/en-us/azure/container-registry). You may have to customize the [Dockerfile](docker/Dockerfile) to install build dependencies.
1. Go to `Pipelines` > `Builds` > `Edit` > `Variables` and add a new secret with the name of `SRCCLR_API_TOKEN`. We'll use the name of the environment variable SourceClear expects for consistency.
1. [Declare the `SRCCLR_API_TOKEN` secret](azure-pipelines.yml). 
1. Run and enjoy!
