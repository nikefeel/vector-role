pipeline {
    agent {
     label 'vector'
    }
    stages {
        stage('Download repository from GitHub') {
            steps {
                    git branch: 'main', credentialsId: 'github', url: 'git@github.com:nikefeel/vector-role.git'
            }
        }
        stage ('Molecule test') {
            steps {
                sh 'molecule test'
            }
        }
    }
}