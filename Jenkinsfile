pipeline {
    agent any
    stages {
        stage('---intoproj---') {
            steps {
                sh "cd /root/mvnproj/"
            }
        }

        stage('---clean---') {
            steps {
                sh "mvn clean"
            }
        }
        stage('--compile--') {
            steps {
                sh "mvn compile"
            }
        }
        stage('--test--') {
            steps {
                sh "mvn test"
            }
        }
        stage('--package--') {
            steps {
                sh "mvn package"
            }
        }
        stage('--deploy--') {
            steps {
                sh "cp /root/.jenkins/workspace/pipe-2/target/myproj.war /opt/apache-tomcat-8.5.35/webapps/"
            }
        }
    }
}
