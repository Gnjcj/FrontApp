pipeline {
  agent {
    docker {
      image 'houssemdocker/angular-app'
      args '-p 3000:3000'
    }

  }
  stages {
    

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
