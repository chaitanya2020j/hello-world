pipeline {
  agent any
  stages {
    stages ('clone repo and clean it') {
      steps{
        sh "rm-rf my-app"
        sh "git clone https://github.com/ratnac37/hello-world"
        sh "mvn clean -f hello-world"
      }
    }
    stage('--test--') {
      steps{
        sh "mvn test"
      }
    }
    stage('--package--') {
      steps{
        sh "mvn package"
      }
    }
  }
}
