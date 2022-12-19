pipeline {
    agent any
    environment {
        path = "C:\\apache-maven-3.8.6\\bin:$path"    
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
    }
}
