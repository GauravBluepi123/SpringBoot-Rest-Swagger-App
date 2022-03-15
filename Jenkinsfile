pipeline{
    
    agent any
    
    tools{
        maven 'Maven3'
    }
    
    stages{
        stage('Checkout'){
            steps{
            sh 'pwd'
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '1', url: 'https://github.com/GauravBluepi123/SpringBoot-Rest-Swagger-App']]])
            }
        }
        stage('Build'){
            steps{
            sh 'pwd'
            sh 'mvn clean install -f pom.xml'
            }
        }
    }
}
