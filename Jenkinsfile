pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                echo 'Building Portfolio Website (HTML/CSS)'
            }
        }

        stage('Deploy') {
            steps {
                echo 'Deploying Website'
                // If on Windows machine (College Lab), comment Linux commands
                // Copy files inside workspace to a folder
                
                bat '''
                if not exist C:\\PortfolioDeploy mkdir C:\\PortfolioDeploy
                xcopy /s /y * C:\\PortfolioDeploy
                '''
            }
        }
    }
}
