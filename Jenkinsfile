pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh 'python hello1.py > ./Outputs/simulation_hello1.txt'
            }
        }
		stage('Phy Test 1') {
            steps {
                input message: "Configure Phy Layer 1 Instrument Test"
            }
        }
    }
	post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}