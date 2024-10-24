pipeline {
    agent {
        node {
            label 'jenkins-slave-node'
        }
    }
    stages {
        stage ('checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/SKS-ORG/java-web-app.git'
            }
        }
    }
}