
      
pipeline {
    agent any

    triggers {
         pollSCM('* * * * *') // Polling Source Control
     }

     
 stages {
        stage('git clone') {
            steps {
                echo 'git cloning'
                git 'https://github.com/rangareddy7/test1.git'
            }
        }

        stage('Build'){
            steps {
                sh 'mvn clean package'
            }
            post {
                success {
                    echo 'Now Archiving...'
                    archiveArtifacts artifacts: '**/target/*.war'
                }
            }
        }

        stage ('Deployments'){
                stage ('Deploy to Staging'){
                    steps {
                        sh "scp -i /home/jenkins/tomcat-demo.pem **/target/*.war ec2-user@${params.tomcat_dev}:/var/lib/apache-tomcat-9.0.39/webapps"
                    }
                }
             }
    }
}
