pipeline {
    agent any
    environment {
        mvnHome = "C:\\apache-maven-3.8.6\\bin:$mvnHome"  
    }
    stages {
        stage ('SCM_Checkout') {
            steps {
               git url: 'https://github.com/mannepallyvinod/Multi_Branch.git' 
            }
        }
        stage ('Build') {
            steps {
               bat "mvn install"
            }
        }
        stage ("Deploy") {
            steps {
                bat "copy target\\Sample.war D:\\apache-tomcat-9.0.65\\webapps"
            }
        }
    }
}
