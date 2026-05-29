pipeline {
    agent 
    {
      label 'jenkins_job'
    }

    stages {
        stage('Build') {
            steps {
                sh 'sleep 5'
                echo "Biuls stage"
                sleep(time: 5, unit: 'SECONDS')
            }
        }

        stage('Deploy') {
            steps {
                sh 'sleep 5'
                echo "deplay stage"
                sleep(time: 5, unit: 'SECONDS')
            }
        }

        stage('Test') {
            steps {
                sh 'sleep 5'
                echo "test stage"
                sleep(time: 5, unit: 'SECONDS')
            }
        }
    }
}
