pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'Hello'
        git(credentialsId: 'f2f4098d-c065-443a-bbd8-4a67d2fca411', url: 'https://github.com/mskuratowski/DevOpsWorkshops.git', branch: 'master')
        dotnetRestore()
        dotnetBuild(configuration: 'Release')
        dotnetPublish(configuration: 'Release')
      }
    }

  }
}