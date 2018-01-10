pipeline {
  agent any

   stages {
         stage ('Compile Stage') {

               steps {
                  withMaven(maven : 'maven_3_5_0') {
                        sh 'mvn clean complie'
                   echo 'Compiling...' 
                      }
                  }
             }
          stage ('Testing Stage') {

               steps {
                  withMaven(maven : 'maven_3_5_0') {
                        sh 'mvn test'
                  echo 'Testing...'    
                      }
                  }
             }

            stage ('Deployment Stage') {

               steps {
                  withMaven(maven : 'maven_3_5_0') {
                        sh 'mvn deploy'
                  echo 'Deploying...' 
                      }
                  }
             }
   }
}
