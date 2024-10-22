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
        stage('Deployment') {
			steps {
				deploy adapters: [ tomcat9(url: 'http://13.232.126.214:8080', credentialsId: 'Tomcat Cred')], war:'**/*.war'
			}
		}
    }
}
