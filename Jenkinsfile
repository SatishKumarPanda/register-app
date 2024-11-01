pipeline {
    agent {
        label 'Test'
    }
    tools {
        jdk 'jdk17'
        maven 'maven3'
    }
    stages {
        stage("Git Checkout") {
            steps {
                echo "Checking out code from Git"
                checkout scm // Uncomment and adjust as necessary for your repo
            }
        }
        stage("Build Application") {
            steps {
                sh "mvn clean package"
            }
        }
        stage("Test Application") {
            steps {
                sh "mvn test"
            }
        }
        stage("SonarQube Scanner") {
            steps {
                script {
                   withSonarQubeEnv(credentialsId: 'jenkins-sonarqube-token') {
                        sh "mvn sonar:sonar"
                    }
                }
            }
        }
        stage("Cleanup Workspace") {
            steps {
                cleanWs()
            }
        }
    }
}
