pipeline {
    agent any
    stages {
        // stage('Checkout Code') {
        //     steps {
        //         git branch: 'master', url: 'https://github.com/Mahadtkxel/python-project-blueprint.git'
        //     }
        // }
        // stage('Code Analysis') {
        //     environment {
        //         scannerHome = tool name: 'sonarqube'
        //     }
        //     steps {
        //         script {
        //             withSonarQubeEnv('sonarqube') {
        //                 sh """
        //                     ${scannerHome}/bin/sonar-scanner \
        //                         -Dsonar.projectKey=tkxelassigmenttest \
        //                         -Dsonar.projectName=tkxelassigmenttest \
        //                         -Dsonar.sources=.
        //                 """
        //             }
        //         }
        //     }
        // }

        stage("Building Docker Image") {
            steps {
                script {
                    sh "docker --version"
                }
             }
        }
    }
}