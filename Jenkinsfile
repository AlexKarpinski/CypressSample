pipeline {
    agent any

    stages {
        stage('build') {
            steps {
                bat 'npm install'
            }
        }
        stage('parallel') {
            parallel {
                // start several test jobs in parallel, and they all
                // will use Cypress Dashboard to load balance any found spec files
                stage('Run tests in parallel A') {
                    steps {
                        bat 'npx cypress run --record --key 71bee1fb-3850-4ef5-af96-34296456abbf --parallel'
                    }
                }
                stage('Run tests in parallel B') {
                    steps {
                        bat 'npx cypress run --record --key 71bee1fb-3850-4ef5-af96-34296456abbf --parallel'
                    }
                }           
            }
        }
    }
}
