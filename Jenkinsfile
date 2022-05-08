pipeline {
  agent {
    docker {
      image 'node:6-alpine'
      args '-p 3000:3000'
    }

  }
  stages {
    stage('install') {
      steps {
      nodejs(nodeJSInstallationName: 'NodeJS')
         { 
      sh 'npm install'
         }  
      }
  }
    

     stage('Test') {
       steps  {
         sh 'chmod u+x  ./jenkins/scripts/test.sh'
          sh './jenkins/scripts/test.sh'
     }
    }

  
    stage('Deploy') {
      steps {
        sh './jenkins/scripts/deliver.sh'
        
      }
    }
    }
  }