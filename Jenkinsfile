pipeline {
    agent any

   
        stage('parallel') {
            parallel {
                // start several test jobs in parallel, and they all
                // will use Cypress Dashboard to load balance any found spec files
                stage('Run tests in parallel A') {
                    steps {
                        bat 'npx cypress run --record --key d359f2ab-8828-480a-9bd0-150fd7951f15 --parallel'
                    
                }             
            }
        }
    }
}

