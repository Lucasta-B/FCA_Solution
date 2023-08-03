pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh "cd project1-python-flask"
                sh "sudo docker build -t localhost:8083/pythonapp:newest ./project1-python-flask/"
                sh "sudo docker image ls"
            }
            
        }
        
    }
}
