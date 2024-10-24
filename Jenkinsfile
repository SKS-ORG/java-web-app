pipeline {
    agent { label 'jenkins-slave-node || jenkins-slave-node2' }
    stages {
        stage ('checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/SKS-ORG/java-web-app.git'
            }
        }
        stage ('build code') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }   
        }
    }
}