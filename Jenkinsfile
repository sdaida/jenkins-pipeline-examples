// https://jenkins.io/doc/book/pipeline/syntax/#when
pipeline {

    agent any

     parameters {
        string(name: 'DEPLOYER', defaultValue: 'Mr Jenkins', description: 'Who are you?')
        choice(name: 'DEPLOY_TO', choices: 'development\nproduction', description: 'Deploy to ...')
     }

    stages {
        stage('Build') { 
            steps { 
                sh 'printenv'
                echo 'Building ...'
            }
        }
        stage('Test'){
            steps {
                echo 'Testing ...'
            }
        }
        stage('Deploy to Prod') {
            when { environment name: 'DEPLOY_TO', value: 'production' }
            steps {
                // sh 'make publish'
                echo 'Deploying ...'
            }
        }
    }
}