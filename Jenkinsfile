pipeline {
    stesshagent: {
            sh 'ssh -i var/jenkins_home/.ssh/id_rsa test1@192.168.1.25'
        }
    agent {
        docker {
            image 'node'
            args '-p 3000:3000'
        }
    }
    stages {
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
    }
}