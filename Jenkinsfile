pipeline {
    agent any
    stages {
        stage('Build') { 
            steps {
                sh 'npm install' 
            }
        }
        stage('Test') {
            steps {
                sh './script/test'
            }
        }
        stage('Deploy') {
            when {
                branch 'master'
            }
            steps {
                sh './script/deploy'
            }
        }
    }
}
