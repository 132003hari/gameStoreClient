pipeline {
    agent any

    stages {
        stage('Checkout') {
            steps {
                script {
                    // Checkout the source code from the repository
                    checkout scm
                }
            }
        }

        stage('Build') {
            steps {
                script {
                    // Build the Blazor project
                    sh 'dotnet build Gamestore.client.sln'
                }
            }
        }

        stage('Publish') {
            steps {
                script {
                    // Publish the Blazor project
                    sh 'dotnet publish MyBlazorApp/MyBlazorApp.csproj -c Release -o publish'
                }
            }
        }
    }

    post {
        always {
            // Archive the published files
            archiveArtifacts artifacts: 'publish/**', allowEmptyArchive: true
        }
    }
}
