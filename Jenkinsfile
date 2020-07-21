pipeline {
   agent any

   stages {
      stage('Hello') {
          environment {
            //version = bat (script : "type project.json|jq .projectVersion", returnStdout:true)
             version = '1.0.1'
            }
         steps {
            UiPathPack (
          outputPath: "${JENKINS_HOME}\\jobs\\${JOB_NAME}\\builds\\${env.version}",
          projectJsonPath: "${WORKSPACE}",
          version: [$class: 'ManualVersionEntry', version: "${env.version}"]
        )
         }
      }
   }
}
