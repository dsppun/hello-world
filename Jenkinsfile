pipeline {
    agent {
        label "dinesh-e2e-machine"
    }

    stages {
        stage('Build') {
            steps {
                echo 'Building..'
                sh 'go build main.go'
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
                sh 'chmod 777 main'
                sh './main'
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
