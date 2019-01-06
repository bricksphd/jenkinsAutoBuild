pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'a=$GIT_URL'
                sh 'b=${a##*/}'
                sh 'echo b' 
                sh 'yarn'
            }
        }
        stage('Test') { 
            steps {
                sh 'ls' 
            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo deploy' 
            }
        }
    }
}
