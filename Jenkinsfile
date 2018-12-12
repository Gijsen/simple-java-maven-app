pipeline {
    agent any
    tools {
       jdk 'jdk8'
       maven 'M3'
    }
    stages {
        stage('Initialize') {
          steps {
            sh '''
            echo "PATH = ${PATH}"
            echo "M2_HOME = ${M2_HOME}"
            '''


          }
        }

        stage('Install') {
          steps {
            sh 'mvn install'
          }
        }
    }
}
