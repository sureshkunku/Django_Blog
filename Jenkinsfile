pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Check out your repository
                git branch: 'master', url: 'https://github.com/sureshkunku/Django_Blog.git'
            }
        }

        stage('Setup Virtual Environment') {
            steps {
                // Create and activate the virtual environment
                sh 'python3 -m venv venv'
                sh '. venv/bin/activate'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install project dependencies
                sh 'pip install -r requirements.txt'
            }
        }

        stage('Run Tests') {
            steps {
                // Run Django tests
                sh 'python manage.py test'
            }
        }

        stage('Build and Deploy') {
            steps {
                // Placeholder for deployment steps
                // For example, you can use Docker, AWS, etc.
                sh 'echo "Deploy your application here"'
            }
        }
    }

    post {
        always {
            // Deactivate the virtual environment
            sh 'deactivate'
        }
    }
}
