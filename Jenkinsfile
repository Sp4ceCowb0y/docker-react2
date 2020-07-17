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
		sh 'docker build -t rfiguerasdegea/nginx_react_frontend -f Dockerfile.dev .'
            }
        }

        stage('Test') {
            steps {
                sh 'echo test'
		sh 'docker run rfiguerasdegea/nginx_react_frontend npm run test -- --coverage'
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

