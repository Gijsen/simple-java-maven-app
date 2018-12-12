pipeline {
    agent any
    tools {
       jdk 'jdk8'
       maven 'M3'
    }
    stages {
        stage('Prepare') {
          steps {
              sh 'mv avioport/* ./ -rf'
          }
        }

        stage('Validate') {
          steps {
            sh 'mvn validate'
          }
        }

        stage('Compile') {
          steps {
            sh 'mvn compile'
          }
        }

        stage('Test') {
          steps {
            sh 'mvn test'
          }
        }

        stage('Package') {
          steps {
            sh 'mvn package'
          }
        }

        stage('Verify') {
          steps {
            sh 'mvn verify'
          }
        }

        stage('Install') {
          steps {
            sh 'mvn install'
          }
        }

        stage('Clean') {
          steps {
            sh 'mvn clean'
          }
        }
    }
}
