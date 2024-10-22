pipeline {
    agent any
    
    stages {
        stage('checkout code') {
            steps {
                git branch: 'main', url: 'https://github.com/SKS-ORG/java-web-app.git'
            }
        }
        stage('build code') {
            steps {
                sh '/opt/maven/bin/mvn clean package'
            }
        }
        stage('Deployment'){
			steps{
				deploy adapters: [ tomcat9(url: 'http://13.235.51.163:8080/', credentialsId: 'tomcatcred')], war:'target/*.war'
			}
		}
    }
}
