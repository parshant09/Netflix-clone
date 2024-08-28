pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                // Checkout code from GitHub
                git branch: 'main', url: 'https://github.com/adityaglobe/Netflix-clone.git'
            }
        }

        stage('Process JSON') {
            steps {
                script {
                    // Process or deploy the JSON file
                    def jsonFile = readFile 'path/to/your.json'
                    echo "JSON content: ${jsonFile}"
                    
                    // You can add any deployment steps here, e.g., copying to a server
                }
            }
        }
    }
}
