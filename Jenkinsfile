pipeline {
    agent any

    stages {

        stage('Checkout Code') {
            steps {
                // Pull code from GitHub repository
                git branch: 'main',
                    url: 'https://github.com/<your-username>/cicd-practice.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                // Install pytest
                sh 'pip install pytest'
            }
        }

        stage('Run Tests') {
            steps {
                // Execute unit tests
                sh 'python -m pytest'
            }
        }

        stage('Build Application') {
            steps {
                // Build step (artifact preparation)
                sh '''
                    echo "Building application..."
                    mkdir -p build
                    cp app.py build/
                '''
            }
        }

        stage('Deploy Application') {
            steps {
                // Deployment simulation
                sh '''
                    echo "Deploying application..."
                    echo "Deployment success"
                '''
            }
        }
    }
}
