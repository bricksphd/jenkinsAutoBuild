pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo $GIT_URL' 
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
