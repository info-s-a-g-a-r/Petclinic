pipeline {
    agent any
    
    tools{
        jdk 'jdk-17'
        maven 'maven3'
    }

    stages {
        stage('Git Checkout') {
            steps {
                git branch: 'feature-1', url: 'https://github.com/info-s-a-g-a-r/Petclinic.git'
            }
        }
        stage('Compile') {
            steps {
                 sh "mvn clean compile"
            }
        }
        stage('Package') {
            steps {
                 sh "mvn clean package -DskipTests=true"
            }
        }
        
    }
}
