pipeline {
    agent any

    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'main',
                    url: 'https://github.com/roopkumarmolleti233/jenkins-pipeline-demo.git'
            }
        }

        stage('Build') {
            steps {
                echo 'Build stage running...'
            }
        }

        stage('Test') {
            steps {
                echo 'Test stage running...'
            }
        }

        stage('Run Script') {
            steps {
                sh 'chmod +x app.sh && ./app.sh'
            }
        }
    }

    post {
        success {
            echo 'Pipeline completed successfully!'
        }
        failure {
            echo 'Pipeline failed!'
        }
    }
}
