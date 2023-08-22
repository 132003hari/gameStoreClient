pipeline {
    agent any
    stages {
        stage('Checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build Blazor App') {
            steps {
                script {
                    sh 'D:\projects\GameStoreClient && dotnet publish -c Release -o publish_output'
                }
            }
        }
        // Add deployment stage here
    }
}
