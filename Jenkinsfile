pipeline {
    stages {
        stage('SSH connection') {
            steps {
                sh 'ssh -i var/jenkins_home/.ssh/id_rsa test1@192.168.1.25'
            }
        }
        agent {
            docker {
                image 'node'
                args '-p 3000:3000'
            }
        }
        stage('Build') {
            steps {
                sh 'npm install'
            }
        }
    }
}