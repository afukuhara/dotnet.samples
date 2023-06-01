pipeline {
  agent any
  stages {
    stage('Pull') {
      steps {
        git(url: 'https://github.com/afukuhara/dotnet.samples.git', branch: 'main')
      }
    }

    stage('error') {
      steps {
        sh 'echo "hello world"'
      }
    }

  }
}