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
                echo "git work"
                // Add your git checkout commands here, e.g., checkout scm
            }
        }
         stage("build Application") {
            steps {
                sh "mvn clean package"
            }
        }
        stage("Test Application") {
            steps {
                sh "mvn test"
            }
        }
    }
}
