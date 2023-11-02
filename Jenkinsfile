pipeline {
    agent any 
    tools {
         maven 'Maven'
         jdk 'Java'
    }
    stages {
       
        stage('Stage-2 : Clean') { 
            steps {
                sh 'mvn clean'
            }
        }
         stage('Stage-3 : Validate') { 
            steps {
                sh 'mvn validate'
            }
        }
         stage('Stage-4 : Compile') { 
            steps {
                sh 'mvn compile'
            }
        }
         stage('Stage-5 : Test') { 
            steps {
                sh 'mvn test'
            }
        } 
       stage('Stage-6 : Verify') { 
            steps {
                sh 'mvn verify'
            }
        }
          stage('Stage-7 : Package') { 
            steps {
                sh 'mvn package'
            }
        }
        stage('Stage-8 : install') { 
            steps {
                sh 'mvn install'
            }
        }
        stage('Stage-9 : JFrog') { 
            steps {
                sh 'mvn deploy'
            }
        }
    }
}
