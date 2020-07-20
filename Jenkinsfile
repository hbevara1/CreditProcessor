pipeline {
   agent any
   stages {
      stage('build') {
         environment {
            version = bat (script : "type project.json|jq .projectVersion", returnStdout:true)
            }
            steps {
               echo %env.version%
            //UiPathPack outputPath: '${JENKINS_HOME}\\jobs\\${JOB_NAME}\\builds\\${env.version}', projectJsonPath: '${WORKSPACE}', version: CustomVersion('${env.version}')
            }
     }
}   
