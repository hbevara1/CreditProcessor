pipeline {
   agent any
   stages {
      stage('build') {
         environment {
            version = bat (script : "type project.json|jq .projectVersion", returnStdout:true)
             }
            steps {
               echo ${env.version}
      }
   }
}
}   
