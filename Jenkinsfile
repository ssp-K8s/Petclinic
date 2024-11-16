pipeline {
    agent any
    
    tools{
        jdk 'jdk-17'
        maven 'maven3'
        }

    stages {
        stage('git checkout') {
            steps {
                git branch: 'feature-1', url: 'https://github.com/ssp-K8s/Petclinic.git'
            }
        }
        stage('maven compile') {
            steps {
                sh 'mvn compile'
            }
        }
        stage('maven pkg') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
