pipeline {
    agent any
            stages {
                stage("Install dependencies") {
                    steps {
                        sh "npm install"
                    
                

                stage("Build") {
                    steps {
                        sh "ng run build"
                    }
                }

                stage("Lint") {
                    steps {
                        sh "ng lint"
                    }
                }

                stage("Unit tests") {
                    steps {
                        sh "ng test"
                    }
                }

                stage("End-to-end tests") {
                    steps {
                        sh "npm run e2e"
                    }
                }
                
            }
        }

       
    }
}
