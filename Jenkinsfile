pipeline {
    agent any
        tools {
        maven 'maven'
        jdk 'java'
    } 
    stages {
        stage('Example clone') {
            steps {
                echo 'git clone'
                git 'https://github.com/rangareddy7/test1.git'
            }
        }
        stage('Example build') {
            steps {
                echo 'maven build'
                sh 'mvn clean'
                sh 'mvn package'
            }
        }
    }
}