pipeline {
        agent any
        stages {
            stage('Compile stage') {
                steps {
                    withMaven(maven : 'Maven_3.0.4'){
                        bat "mvn clean compile"
                }
            }
        }

             stage('testing stage') {
                 steps {
                    withMaven(maven : 'Maven_3.0.4'){
                        bat "mvn test"
                }
            }
        }

              stage('deployment stage') {
                  steps {
                    withMaven(maven : 'Maven_3.0.4'){
                        bat "mvn deploy"
                }
            }
        }

      }

    }
