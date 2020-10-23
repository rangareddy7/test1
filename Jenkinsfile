pipeline {
agent any
    tools {
            maven 'maven'
            jdk 'java'
        } 
stages {
    stage("gitclone") {
       steps {
        echo 'git clone'
        git 'https://github.com/rangareddy7/test.git'
        }
    } 
    stage("mavenbuild") {
         step {      
             echo 'maven build'
             sh 'mvn clean'
             sh 'mvn compile'
             sh 'mvn test'
             sh 'mvn package'
             sh 'mvn install'
           }
        }   
   }
}
