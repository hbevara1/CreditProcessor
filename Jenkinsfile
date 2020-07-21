pipeline {
   agent any

   stages {
      stage('build') {
         when {
                branch 'master'
            }
         steps {
            UiPathPack (outputPath: 'Output', projectJsonPath: 'project.json', version: CurrentVersion())
         }
      }
      stage('deploy') {
         when {
                branch 'dev'
            }
         steps {
           echo "the barnch is dev"
         }
      }
   }
}
