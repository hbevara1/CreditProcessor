pipeline {
   agent any

   stages {
      stage('version') {
          environment {
            version = bat (script : "type project.json|jq .projectVersion", returnStdout:true)
             }
         steps {
            echo %env.version%
         }
      }
   }
}
