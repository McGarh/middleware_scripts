pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
            }
        }
	stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
	stage('Deploy') {
            steps {
                echo 'Deploy Step'
                sleep 10
            }
        }
	stage('Docker') {
            steps {
                echo 'Image step'
            }
        }
	    stage("create zip file") {
            steps {
                script{
                echo sh 'zip middlewareScript-$(date +%y%m%d-%H%M%S).zip *  --exclude Jenkinsfile README.md'
                }
            }
        }
    }
}
