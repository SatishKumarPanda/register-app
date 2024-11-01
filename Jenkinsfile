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
        stage("Cleanup Workspace") {
            steps {
                cleanWs()
            }
        }
    }
}
