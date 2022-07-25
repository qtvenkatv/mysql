#!groovy
pipeline {
    agent node1
    stages {
        stage ('check out source') {
            steps {
                git url:'https://github.com/qtvenkatv/mysql.git', branch:'master'
            }         
        }
        stage (" move the directory") {
            steps {
                sh 'cd /springpet'
            }
        }
        stage ("creat the build using the image") {
            steps {
                sh 'docker build -t sps:latest .'
            }
        }
    }
}
