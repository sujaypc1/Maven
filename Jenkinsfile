pipeline {
  agent any

   stages {
         stage ('Compile Stage') {

               steps {
                  withMaven(maven : 'Maven_3.0.4') {
                        sh 'mvn clean complie'
                   echo 'Compiling...' 
                      }
                  }
             }
          stage ('Testing Stage') {

               steps {
                  withMaven(maven : 'Maven_3.0.4') {
                        sh 'mvn test'
                  echo 'Testing...'    
                      }
                  }
             }

            stage ('Deployment Stage') {

               steps {
                  withMaven(maven : 'Maven_3.0.4') {
                        sh 'mvn deploy'
                  echo 'Deploying...' 
                      }
                  }
              }
           }
        }