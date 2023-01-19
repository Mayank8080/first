pipeline {
  agent any
  stages {
    stage('testing') {
      steps {
        sh '''sh \'echo "hello"  > hello.txt\'
sh \'cp hello.txt sam.txt\'
sh \'cat sam.txt\'
sh \'cat hello.txt\'
sh\'cat sam.txt\''''
      }
    }

  }
}