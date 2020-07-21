pipeline {
   agent any

   stages {
      stage('Hello') {
          environment {
            //version = bat (script : "type project.json|jq .projectVersion", returnStdout:true)
             version = '1.0.1'
            }
         steps {
           UiPathPack (outputPath: '${JENKINS_HOME}\\jobs\\${JOB_NAME}\\builds\\${BUILD_NUMBER}', projectJsonPath: '${WORKSPACE}', version: CustomVersion('${BUILD_NUMBER}'))
         }
      }
   }
}
