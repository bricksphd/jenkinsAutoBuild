pipeline {
  environment{
    c = "bobby"
  }
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo $c'
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
