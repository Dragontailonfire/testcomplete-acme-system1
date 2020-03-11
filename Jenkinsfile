pipeline {
    agent {
        label 'testagent'
    }
    stages {
        stage('Build') {
            steps {
                // Get code from GitHub repository
                git credentialsId: '3de51411-75ec-4387-a1f6-a46d6f4a45c2', 
                url: 'https://github.com/Dragontailonfire/testcomplete-acme-system1.git/'
            }
        }
        stage('Test'){
            steps{
                testcompletetest actionOnErrors: 'MAKE_FAILED', 
                actionOnWarnings: 'MAKE_UNSTABLE', 
                generateMHT: true, 
                suite: 'TestComplete\\AcmeSystem1\\Acme_System1.pjs', 
                timeout: '120', 
                useTCService: true, 
                useTimeout: true, 
                userName: 'corp\\narayanan.kangath', 
                userPassword: 'N.ara..1'
            }
        }
    }
}

