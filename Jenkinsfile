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
                git 'https://your-repo-url.git'
            }
        }

        stage('Ejecutar Hola Mundo') {
            steps {
                sh 'docker-compose up hola-mundo'
            }
        }
    }
}
