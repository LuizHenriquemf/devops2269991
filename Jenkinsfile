pipeline {
    agent any


    stages {

        stage('Preparação do Ambiente') {
            steps {
                script {
                    // Instalar o Node.js e o npm
                    tool 'NodeJS'
                    echo 'node --version'
                    echo 'npm --version'
                }
            }
        }


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





