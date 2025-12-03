A pipeline is a set of automated processes that build, test and deploy software, integrating workflows between development and operations teams to enable rapid, reliable software delivery.

It integrates various tools, processes and practices to achieve continuous integration, continuous delivery and continuous deployment [[CI & CD|CI/CD]]

- **Automation:** The core principle is to automate as many steps as possible to reduce manual effort and human error

### Stages of Pipelines
- **Build:** Compiling the code into an executable form
- **Test:** Running automated tests, such as unit, integration, and functional tests, to ensure quality and catch bugs early
- **Deploy:** Releasing the application to different environments, from staging to production

### Example using YAML
```YML
trigger:
- main

pool:
  vmImage: 'ubuntu-latest'

stages:
- stage: Build
  displayName: Build Project
  jobs:
  - job: BuildJob
    steps:
    - script: echo "Building the project..."
      displayName: 'Build Application'
    - task: DotNetCoreCLI@2
      inputs:
        command: 'build'
        projects: '**/*.csproj'
      displayName: 'dotnet build'
    - publish: $(Build.ArtifactStagingDirectory)
      artifact: drop
      displayName: 'Publish Build Artifact'

- stage: Deploy
  displayName: Deploy Application
  dependsOn: Build # This stage depends on the Build stage completing successfully
  jobs:
  - deployment: DeployJob
    environment: 'production' # Define the target environment
    strategy:
      runOnce:
        deploy:
          steps:
          - script: echo "Deploying to production..."
            displayName: 'Deploy to Production'
          - download: current
            artifact: drop
            displayName: 'Download Build Artifact'
          - script: echo "Deployed artifact contents:"
            displayName: 'Display Artifact Contents'
            # Add steps to actually deploy your application to a server or cloud service
```

