pipeline {
    agent any

    stages {
        stage('Setup') {
            steps {
                echo 'Setting up virtual environment and installing dependencies...'
                bat '''
                  
                    pip install -r requirements.txt
                '''
            }
        }

        stage('Build') {
            steps {
                echo 'Running Python script...'
                bat '''
                    
                    python app.py
                '''
            }
        }
    }

    post {
        success {
            echo 'Pipeline executed successfully!'
        }
        failure {
            echo 'Something went wrong in one of the stages.'
        }
    }
}
