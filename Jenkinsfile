pipeline {
    agent {
        label "deploy-machine"
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh '/bin/make build'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'chmod 777 bin/main'
                sh './bin/main'
            }
        }
        stage('Docker Image Build') {
            steps {
                echo '> Building the docker image ...'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
