pipeline {
  agent {
    docker {
      image 'pivotalpa/angular-cli'
      args '-p 3000:3000'
    }

  }
  stages {
    
stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      environment {
        CI = 'true'
      }
      steps {
        sh 'ng test'
      }
    }

    stage('Deliver') {
      steps {
        sh './jenkins/scripts/deliver.sh'
        
      }
    }

  }
}
