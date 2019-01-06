pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'a=`echo $GIT_URL`'
                sh 'a=hello'
                sh 'echo $a'
                sh 'b=`echo ${a##*/}`'
                sh 'echo $b' 
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
                sh 'echo $b' 
            }
        }
    }
}
