pipeline{
    agent any

    tools {
         maven 'maven3'
         jdk 'jdk'
    }

    stages{
        stage('checkout'){
            steps{
                checkout([$class: 'GitSCM', branches: [[name: '*/master']], extensions: [], userRemoteConfigs: [[credentialsId: 'github access', url: 'https://github.com/Vignesh-Balu/maven-sample.git']]])
            }
        }
        stage('build'){
            steps{
               bat 'mvn clean install'
            }
        }
    }
}
