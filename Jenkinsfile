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
                    sh 'cd /path/to/your/blazor/app && dotnet build Jenkins-build.sln
                }
            }
        }
        // Add deployment stage here
    }
}
