pipeline{
    agent {label 'ubuntu'}
    parameters{
        gitParameter(branchFilter: 'origin/(.*)',
        defaultValue: 'master',
        name: 'BRANCH',
        type: 'PT_BRANCH')
    }
    stages{
        stage('Checkout'){
            steps{
                checkout(branches: [[name: '**']], extensions: [], userRemoteConfigs: [[credentialsId: 'Diego-pgm', url: 'https://github.com/Diego-pgm/homepage.git']])
            }
        }
        stage('Clone'){
            steps{
                git branch: "${params.BRANCH}", url: 'https://github.com/Diego-pgm/homepage.git'
            }
        }
        stage('Move file'){
            steps{
                sh 'mv index.html /var/www/html/'
            }
        }
    }
}