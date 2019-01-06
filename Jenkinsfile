pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo $GIT_URL' 
            }
        }
        stage('Test') { 
            steps {
                sh 'echo test' 
            }
        }
        stage('Deploy') { 
            steps {
                sh 'echo deploy' 
            }
        }
    }
}
