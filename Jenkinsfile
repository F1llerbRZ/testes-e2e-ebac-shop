pipeline {
    agent any

    stages {
        stage('Clonar repositorio') {
            steps {
                git branch: 'main', url: 'https://github.com/FillerbRZ/testes-e2e-ebac-shop.git'
            }
        }
        stage('Instalar dependencias') {
            steps {
                sh 'npm install'
            }
        }
        stage('Executar servidor') {
            steps {
               sh 'npm start' 
            }
        }
        stage('Executar testes') {
            steps {
               sh 'npx cypress run'
            }
        }
    }
}
