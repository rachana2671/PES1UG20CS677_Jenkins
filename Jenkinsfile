pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o program program.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './program'
            }
        }
        stage('Deploy') {
          steps {
              sh 'echo "Deployment completed successfully"'
          }
        }
    }
    
    post {
        failure {
            echo 'Pipeline failed!!'
        }
    }
}
