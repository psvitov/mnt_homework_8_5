pipeline {
    agent {
        label 'centos'
    }

    stages {
        stage('Git clone') {
            steps {
                git branch: 'main', url: 'https://github.com/psvitov/mnt_homework_8_5.git'
            }
        }
        stage('Directory') {
            steps {
                dir('/opt/jenkins_agent/workspace/Pipeline-molecule/roles/vector-role') {
                sh 'molecule test'
                }
            }
        }
    }
}
