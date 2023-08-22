pipeline {
    agent any
    stages {
        stage('Checkout') {
            tools {
                dotnetsdk 'dotnet-sdk-7.0'
            }
            steps {
                checkout scm
            }
        }
        stage('Build Blazor App') {
            steps {
                script {
                    sh 'cd /D:\projects\GameStoreClient && dotnet publish -c Release -o publish_output'
                }
            }
        }
        // Add deployment stage here
    }
}
