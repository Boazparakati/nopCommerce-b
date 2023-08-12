pipeline {
    agent { label 'NOP' }
    stages {
        stage ('VCS') {
            steps {
                git url: 'https://github.com/Boazparakati/nopCommerce-b.git',
                    branch: 'declarative'
            }
        }       
        stage ('Build') {
            steps {
                sh 'docker image build -t boazparakati/nop:3.0 .'
                sh 'docker image push boazparakati/nop:3.0' 
            }
        }  
    }
}
