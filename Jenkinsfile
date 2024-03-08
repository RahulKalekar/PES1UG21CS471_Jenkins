pipeline {
    agent any

    stages {
        
       

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
