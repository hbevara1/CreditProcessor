pipeline {
   agent any

   stages {
      stage('Hello') {
          environment {
            version = bat (script : "type project.json|jq .projectVersion", returnStdout:true)
            }
         steps {
            echo '%env.version%'
         }
      }
   }
}
