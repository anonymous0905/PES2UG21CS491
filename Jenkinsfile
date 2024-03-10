pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Compile the .cpp file
                    sh 'g++ -o hello hello.cpp'
                    echo 'Build completed.'
                }
            }
        }
        stage('Test') {
            steps {
                script {
                    // Print output of the .cpp file
                    sh './hello'
                    echo 'Test completed.'
                }
            }
        }
        stage('Deploy') {
            steps {
                // Add your deploy steps here
                echo 'Deploy stage.'
            }
        }
    }
    post {
        failure {
            echo 'Pipeline failed.'
        }
    }
}
