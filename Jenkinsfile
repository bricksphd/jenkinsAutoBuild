pipeline {
  environment{
    CC = """${sh(
                returnStdout: true,
                script: 'echo $GIT_URL'
            )}""" 
    
  }
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh "e=${env.GIT_URL}"
                sh 'echo $CC'
                sh 'd=${c##*/}'
                sh 'echo $d'
                sh 'b=`echo `'
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
                sh 'b=${GIT_URL##*/}'
                echo 'b'
                echo '$b'
                sh 'docker stop $b || true && docker rm $b || true'
                sh 'docker build --tag $b .'
                sh 'docker run -d -p 3333:3000 --name $b -e "PASSWORD=adminadmin" $b' 
            }
        }
    }
}
