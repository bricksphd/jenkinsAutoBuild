pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo $BUILD_NUMBER' 
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
