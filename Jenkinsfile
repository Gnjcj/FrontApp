
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
         sh ' ng test '
          
     }
    }

  
    stage('Deploy') {
      steps {
        sh 'ng serve '
        
      }
    }
    }
 
