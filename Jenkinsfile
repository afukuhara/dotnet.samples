pipeline {
  agent any
  stages {
    stage('Pull') {
      steps {
        git(url: 'https://github.com/afukuhara/dotnet.samples.git', branch: 'main')
      }
    }

    stage('Unit Test') {
      steps {
        dotnetTest(project: 'csharp\\unit-testing\\XUnit.TestProject\\XUnit.Project.csproj')
      }
    }

    stage('Build & Publish') {
      steps {
        dotnetPublish(project: 'csharp\\unit-testing\\XUnit.TestProject\\XUnit.Project.csproj')
        dotnetPublish(project: 'csharp\\unit-testing\\XUnit.TestProject\\XUnit.Project.csproj', outputDirectory: 'C:\\work\\dotnet-work', options: '-p:PublishSingleFile=true --self-contained true')
      }
    }

  }
}