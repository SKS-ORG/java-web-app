node {
    stage ('checkout code') {
        git branch:'main', url:'https://github.com/SKS-ORG/java-web-app.git'
    }
    stage ('build code') {
        sh '/opt/maven/bin/mvn clean package'
    }
    stage ('deploy to tomcat') {
        deploy adapters:[tomcat9(url:'http://52.195.230.100:8080', credentialsId:'tomcatcred')], war:'**/*.war'
    }
}