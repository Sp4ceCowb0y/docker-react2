pipeline {

    agent any

    stages {

        stage('Clone repository') {
	    steps {
                checkout scm
            }
        }

        stage('Build') {
            steps {
                sh '''
                    echo build

                    '''
                docker build -t rfiguerasdegea/nginx_react_frontend .
            }
        }

        stage('Test') {
            steps {
                sh 'echo test'
            }
        }

        stage('Push') {
            steps {
                sh 'echo push'
            }
        }

        stage('Deploy') {
            steps {
                sh 'echo deploy'
            }
        }
    }
}

