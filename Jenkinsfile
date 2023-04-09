pipeline {
    agent {
        node {
            label 'Node2'
        }
    }
    stages {
        stage('Clonar repositorio') {
            steps {
                git 'https://github.com/jhosep-lu/pruebas-jenkins.git'
            }
        }

        stage('Ejecutar Hola Mundo') {
            steps {
                script {
                    docker.image('docker/compose').withRun('-u root') {
                        sh 'docker-compose up hola-mundo'
                    }
                }
            }
        }
    }
}
