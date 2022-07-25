#!groovy
pipeline {
    agent { label 'JDK11' } 
    stages {
        stage ('check out source') {
            steps {
                git url:'https://github.com/qtvenkatv/mysql.git', branch:'master'
            }         
        }
        stage ("creat the build using the image") {
            steps {
                sh 'sudo docker build -t sps:latest .'
            }
        }
    }
}
