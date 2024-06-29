pipeline {
    agent {
        label 'node-runner'
    }
    options {
            jenkins {
                url 'http://localhost:3000/'
            }
    }
    stages {
        stage('Install Dependencies') {
            steps {
                sh 'npm install'
            }
        }
        stage('Build') {
            steps {
                sh 'npm run build'
            }
        }
        stage('Serve') {
            steps {
                sh 'npm start -- --port 3004'
            }
        }
    }
    post {
        always {
            echo 'Build and serve complete'
        }
    }
}
