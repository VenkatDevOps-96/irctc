pipeline {
    agent any
    environment {
        MAVEN_HOME = "/opt/maven"
        PATH = "$MAVEN_HOME/bin:$PATH"
    }
    stages {
        stage ('git clone') {
            steps {
                git url : 'https://github.com/VenkatDevOps-96/war-web-project.git', branch: 'master'
            }
        }
        stage ('Build') {
            steps {
                sh 'mvn clean package'
            }
        }
    }
}
