pipeline {
  agent any
  stages {
    stage ('Clone application repository') {
      steps {
        sh 'printenv'
        git "${env.TARGET_APPLICATION_REPO_URL}"
      }
    }
    stage ('Print README.md from application repository') {
      steps {
        script {
          def fileContent = readFile 'README.md'
          echo(fileContent)
        }
      }
    }
  }
}
