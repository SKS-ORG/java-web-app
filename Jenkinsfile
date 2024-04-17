pipeline {
    agent {
        node {
            label 'jenkins-slave-node1'
        }
    }
    stages {
        stage ('checkoutcode') {
            steps{
                git branch: 'main' , url: 'https://github.com/SKS-ORG/java-web-app.git'
            }
        }
        stage ('buildcode'){
            steps{
                sh '/opt/maven/bin/mvn clean package'
            }
        }
        
    }
}
