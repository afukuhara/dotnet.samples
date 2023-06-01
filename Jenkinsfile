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
        dotnetTest(project: 'csharp\\unit-testing\\XUnit.TestProject\\XUnit.Project.csproj')
      }
    }

  }
}