
pipeline {
    agent any
  //triggers {pollSCM('* * * * *')}
  stages {
    stage('Checkout') {
      steps {
        // Get some code from a GitHub repository
        git branch: "main", url: 'https://github.com/Benjaminjbonnet/ProjectTwoFrontEnd.git'
      }
    }
    
        stage('DockerBuild') {
      steps {
        sh ' docker build -t projecttwoviews:latest .'
      }
        }
         stage('DockerRun') {
      steps {
        sh 'docker run  -p 3000:3000 projecttwoviews'
      }
        }
  }
}