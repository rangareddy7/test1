pipeline {
    agent any
    tools {
        maven 'maven'
        jdk 'java'
    }
    stages {
        stage('git clone') {
            steps {
                echo 'git cloning'
                git 'https://github.com/rangareddy7/test.git'
            }
        }
        
         stage('build') {
            steps {
                sh 'mvn clean'
                sh 'mvn test'
                sh 'mvn install'
            }
        }
    }
}
