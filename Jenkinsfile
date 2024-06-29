pipeline {
    agent {
        label 'node-runner'
    }
    options {
        jenkinsUrl('http://localhost:3000/')
    }
    stages {
        stage('Install Dependencies') {
            steps {
                script {
                    sh 'npm install'
                }
            }
        }
        stage('Build') {
            steps {
                script {
                    sh 'npm run build'
                }
            }
        }
        stage('Serve') {
            steps {
                script {
                    sh 'npm start -- --port 3004'
                }
            }
        }
    }
    post {
        always {
            echo 'Build and serve complete'
        }
    }
}
