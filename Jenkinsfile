pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }

    stage('Teste') {
        steps {
            sh 'npm test'
        }
    }

    stage('Construindo o Docker') {
        steps {
            sh 'docker build -t devops .'
        }
    }

    stage('Iniciando o Docker') {
        steps { 
            sh 'docker-compose up -d'
        }
    }

    }
}