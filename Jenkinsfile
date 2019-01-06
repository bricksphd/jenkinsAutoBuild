pipeline {
    agent any 
    stages {
        stage('Build') { 
            steps {
                sh 'echo ${GIT_URL##*/}'
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
                sh 'docker stop ${GIT_URL##*/} || true && docker rm ${GIT_URL##*/} || true'
                sh 'docker build --tag ${GIT_URL##*/} .'
                sh 'docker run -d -p 3333:3000 --name ${GIT_URL##*/} -e "PASSWORD=adminadmin" ${GIT_URL##*/}' 
            }
        }
    }
}
