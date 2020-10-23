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
                git 
            }
        }
        
         stage('build') {
            steps {
                sh 'mvn --vn'
            }
        }
    }
}
