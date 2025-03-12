pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    sh 'g++ -o output main.cpp'  // Compiling C++ file
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    sh './nonexistent'  // Running compiled C++ program
                }
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying application...'
            }
        }
    }

    post {
        failure {
            echo 'Pipeline failed'
        }
    }
}
