pipeline{
    agent {label 'ubuntu'}
    stages{
        stage('Checkout'){
            steps{
                checkout (branches: [[name: '**']], extensions: [], userRemoteConfigs: [[credentialsId: 'Diegopgm', url: 'https://github.com/Diego-pgm/homepage.git']])
            }
        }
        stage('Clone'){
            steps{
                git url: 'https://github.com/Diego-pgm/homepage.git'
                sh 'ls'
            }
        }
        stage('Move file'){
            steps{
                sh 'ls'
                sh 'mv index.html /var/www/html/'
            }
        }
    }
}