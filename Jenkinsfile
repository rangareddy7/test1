pipeline {
 agent any
    tools {
        maven 'maven'
        jdk 'java'
    } 
stages {
    stage('git clone') {
       steps {
         echo 'git clone'
         git 'https://github.com/rangareddy7/test1.git'
        }
      }  

      stage("build") {
         step{
             echo "maven build"
             sh 'mvn clean'
             sh 'mvn package'
           }
        }   
   }
}