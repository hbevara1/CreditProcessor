pipeline {
   agent any

   stages {
      stage('Hello') {
          environment {
            version = bat (script : "type project.json|jq .projectVersion", returnStdout:true)
            }
         steps {
           UiPathPack (outputPath: '${JENKINS_HOME}\\jobs\\${JOB_NAME}\\builds\\${env.version}', projectJsonPath: '${WORKSPACE}', version: CustomVersion('${env.version}'))
         }
      }
   }
}
