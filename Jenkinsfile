pipeline {
    agent any

    environment {
        NODE_HOME = "/usr/local/bin/node"
        PATH = "${NODE_HOME}/bin:${env.PATH}"
    }

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub
                git branch: 'main', url: 'https://github.com/adityaglobe/Netflix-clone.git'
            }
        }

        stage('Install Dependencies') {
            steps {
                script {
                    // Install yarn if not already installed
                    sh 'npm install -g yarn'

                    // Install project dependencies
                    sh 'yarn install'
                }
            }
        }

        stage('Build Project') {
            steps {
                script {
                    // Build the project using Vite
                    sh 'yarn build'
                }
            }
        }

        stage('Process JSON') {
            steps {
                script {
                    // Example of reading a JSON file if required
                    def jsonFile = readFile 'path/to/your.json'
                    echo "JSON content: ${jsonFile}"
                    
                    // Additional processing steps can go here
                }
            }
        }

        stage('Deploy') {
            steps {
                script {
                    // Deployment steps
                    // You can add commands here to deploy the built project to your server
                }
            }
        }
    }
}
