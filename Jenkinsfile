pipeline {
    agent {
        label 'node-runner'
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
