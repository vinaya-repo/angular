pipeline {
    agent { label 'jenkins-slave'}

    environment {
        function_name = 'java-sample'
    }

    stages {
        stage('Build') {
            steps {
                echo 'Build'
                sh 'npm run build'
            }
        }

        stage('test') {
            steps {
                echo 'test'

                sh "npm run test"
            }
        }

        stage('Deploy') {
            steps {
                echo 'deploy'

                sh "npm run deploy"
            }
        }
    }
}