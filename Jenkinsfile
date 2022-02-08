pipeline {
    agent any

    stages {
        stage('Clonar o repositorio') {
            steps {
                gir branch: 'main', url: 'https://github.com/rafaelmbarros/testes-api-cy.git'
            }
        }
        stage('Instalar dependencias') {
            steps {
                sh 'npm install'
            }
        }
        stage('Executar testes') {
            steps {
                sh 'NO_COLOR=1 npm run cy:run'
            }
        }
    }
}