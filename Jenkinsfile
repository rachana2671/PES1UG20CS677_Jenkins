pipeline {
    agent any
    
    stages {
        stage('Build') {
            steps {
                sh 'g++ -o program programm.cpp'
            }
        }
        stage('Test') {
            steps {
                sh './programm'
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
