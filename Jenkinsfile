pipeline {
    agent {
        docker {
            image 'docker/compose'
            args '-u root'
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
                sh 'docker-compose up hola-mundo'
            }
        }
    }
}
