pipeline {
   agent any

   stages {
      stage('build') {
         steps {
            UiPathPack (outputPath: 'Output', projectJsonPath: 'project.json', version: CurrentVersion())
            UiPathDeploy (credentials: UserPass('dc9157d0-7a1e-48e9-900e-882bba45fe7e'), environments: 'dev', folderName: 'Default', orchestratorAddress: 'https://rpa.com:8443/', orchestratorTenant: 'Default', packagePath: 'output')
         }
      }
   }
}
