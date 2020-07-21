pipeline {
   agent any
   stages {
      stage('build') {
         environment {
            //version = bat (script : "type project.json|jq .projectVersion", returnStdout:true)
             //version = '5.0.1'
            input = '${WORKSPACE}'
            }
            steps {
           // UiPathPack outputPath: '${JENKINS_HOME}\\jobs\\${JOB_NAME}\\builds\\${version}', projectJsonPath: '${WORKSPACE}', version: CustomVersion('${version}')
               echo "the workspace is ...${input}"
      }
   }
   
}
}   
