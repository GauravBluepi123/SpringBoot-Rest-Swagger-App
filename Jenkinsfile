pipeline{
    
    agent any
    
    tools{
        maven 'Maven3'
    }
    
    stages{
        stage('Checkout'){
            steps{
            checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: '1', url: 'https://github.com/GauravBluepi123/HelloWorld']]])
            }
        }
        stage('Build'){
            steps{
            sh 'mvn clean install -f HelloWorld/blob/master/Hello.java'
            }
        }
    }
}
