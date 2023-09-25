pipeline{
    agent {label 'ubuntu'}
    stages{
        stage('Checkout'){
            steps{
                checkout scmGit(branches: [[name: '**']], extensions: [], userRemoteConfigs: [[credentialsId: 'Diegopgm', url: 'https://github.com/Diego-pgm/homepage.git']])
            }
        }
        stage('Clone'){
            steps{
                git url: 'https://github.com/Diego-pgm/homepage.git'
            }
        }
        stage('Move file'){
            steps{
                sh 'mv index.html /var/www/html/'
            }
        }
    }
}