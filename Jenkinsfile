pipeline {
    agent any
    stages {
  //       stage('Clone repository') {
  //           steps {
  //               checkout([$class: 'GitSCM',
  //               branches: [[name: '*/main']],
  //               userRemteConfigs:[[url: 'https://github.com/PES2UG21CS235/PES2UG21CS235_Jenkins.git']]])
  //           }
  //       }
        stage('Build') {
            steps {
                build 'PES2UG21CS235-1'
                sh 'g++ main.cpp -o output'
            }
        }
        stage('Test') {
            steps {
                sh './output'
            }
        }
        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }
    post{
        failure{
            error 'Pipeline failed'
        }
    }
}