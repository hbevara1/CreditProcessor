pipeline {
   agent any
   stages {
      stage('build') {
         environment {
      input = bat (script : "type project.json|jq .projectVersion", returnStdout:true)
        }
            steps {
               echo %env.input%
            //UiPathPack outputPath: '${JENKINS_HOME}\\jobs\\${JOB_NAME}\\builds\\${version}', projectJsonPath: '${WORKSPACE}', version: CustomVersion('${version}')
      }
   }
   stage('deploy') {
            steps {
               echo env.input
            //UiPathDeploy credentialsId: 'dc9157d0-7a1e-48e9-900e-882bba45fe7e', orchestratorAddress: 'https://rpa.com:8443/', orchestratorTenant: 'Default', packagePath: '${JENKINS_HOME}\\jobs\\${JOB_NAME}\\builds\\${version}'
      }
    }
  }
}   
