pipeline {
   agent any

   stages {
      stage('build') {
          environment {
            version = bat (script : "type project.json|jq .projectVersion", returnStdout:true)
             //version = '5.0.1'
            }
         steps {
           //UiPathPack (outputPath: '${JENKINS_HOME}\\jobs\\${JOB_NAME}\\builds\\${env.version}', projectJsonPath: '${WORKSPACE}\\multi_branch_pipeline_master\\project.json', version: CustomVersion('${env.version}'))
            //UiPathPack (outputPath: '${JENKINS_HOME}\\jobs\\${JOB_NAME}\\builds\\${version}', projectJsonPath: '${WORKSPACE}', version: CustomVersion('${version}'))
            UiPathPack outputPath: '${WORKSPACE}\\Output', projectJsonPath: '${WORKSPACE}', version: CurrentVersion()
         }
      }
      stage('deploy') {
         steps {
           UiPathDeploy (credentialsId: 'dc9157d0-7a1e-48e9-900e-882bba45fe7e', orchestratorAddress: 'https://rpa.com:8443/', orchestratorTenant: 'Default', packagePath: '${JENKINS_HOME}\\jobs\\${JOB_NAME}\\builds\\${env.version}')
         }
      }
   }
}
