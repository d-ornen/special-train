pipeline {
  agent any
    stages{
      stage('Build'){
        checkout scm
        echo "building"
        sh "sudo docker buildx build --platform linux/amd64 -t just4lulz/flaskapp:v1 --push ."
      }
      stage('Test'){
        echo "testing"
        echo "no tests defined"
      }
      stage('Deploy'){
        echo "deploying"
        sh  "kubectl set image deployment/flaskapp flaskapp=just4lulz/flaskapp:v1"

      }
    }
}
