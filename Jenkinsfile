pipeline {
    agent any
    stages {
        stage('Checkout Code') {
            steps {
                git branch: 'master', url: 'https://github.com/Mahadtkxel/python-project-blueprint.git'
            }
        }
        stage('Sonarqube Code Analysis') {
            environment {
                scannerHome = tool name: 'sonarqube'
            }
            steps {
                script {
                    withSonarQubeEnv('sonarqube') {
                        sh """
                            ${scannerHome}/bin/sonar-scanner \
                                -Dsonar.projectKey=tkxelassigment1 \
                                -Dsonar.projectName=tkxelassigment1 \
                                -Dsonar.sources=.
                        """
                    }
                }
            }
        }

        stage("Building Docker Image") {
            steps {
                script {
                    sh "docker build -t tkxelassingment_1 -f dev.Dockerfile ."
                }
             }
        }
    }
}