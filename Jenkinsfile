node{
  checkout scm
 
  stage('Build'){
    def b = "jenkinsautobuild"
    sh "docker stop ${b} || true && docker rm ${b} || true"
    sh "docker build --tag ${b} ."
    sh "docker run -d -p 3333:3000 --name ${b} ${b}"
    
  }
}
