pipeline {
    agent { any }
    stages {
        stage('build') {
            steps {
                sh 'python hello1.py > ./Outputs/sim_outputs.txt.sim'
            }
        }
    }
}