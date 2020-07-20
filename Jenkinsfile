pipeline {
   agent any
   stages {
      stage('build') {
         environment {
            input = bat (script : "type project.json|jq .projectVersion", returnStdout:true)
             }
            steps {
            echo env.input
      }
   }
}
}   
