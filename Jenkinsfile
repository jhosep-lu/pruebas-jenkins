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
            agent {
                docker {
                    image 'docker/compose'
                    args '-u root'
                }
            }
            steps {
                sh 'docker-compose up hola-mundo'
            }
        }
    }
}
