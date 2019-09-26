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
            when (env.JOB_NAME.endsWith('cd') {
                steps {
                    sh './script/deploy'    
                }
            }
        }
    }
}
