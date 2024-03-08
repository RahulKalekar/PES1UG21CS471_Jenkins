pipeline {
    agent any

    stages {
        stage('Clone repository') {
            steps {
                checkout([$class: 'GitSCM',
                          branches: [[name: '*/main']],
                          userRemoteConfigs: [[url: 'https://github.com/RahulKalekar/PES1UG21CS471_Jenkins']]])
            }
        }

        stage('Build') {
            steps {
                sh 'g++ main.cpp -o output'
            }
        }

        stage('Test') {
            steps {
                sh './outpu'
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'
            }
        }
    }

    post {
        failure {
            error 'Pipeline Failed'
        }
    }
}
