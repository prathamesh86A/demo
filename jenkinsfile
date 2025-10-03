pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                git(
                    branch: 'main',
                    url: 'https://github.com/prathamesh86A/demo.git',
                    credentialsId: 'github-token'
                )
            }
        }
        stage('Install Dependencies') {
            steps {
                sh 'yarn'
            }
        }
        stage('Build') {
            steps {
                sh 'yarn run build'
            }
        }
    }
}
