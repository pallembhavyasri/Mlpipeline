pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                // Checkout the SCM. For Multibranch Pipeline, this is automatic
                // but you can explicitly use: checkout scm
                echo "Code checked out from branch: ${env.BRANCH_NAME}"
            }
        }
        stage('Test Pipeline') {
            steps {
                // Replace this with your actual build/test commands
                sh """
                 echo "Running basic pipeline test for branch ${env.BRANCH_NAME}"
                 cat notes
                 """
            }
        }
        stage('Build Complete') {
            steps {
                echo "Build successfully completed for changes merged to ${env.BRANCH_NAME}!"
            }
        }
    }
}