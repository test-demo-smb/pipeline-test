pipeline {
    agent none

    // agent {
    //     label 'jenkins_job'
    // }

    stages {

        stage('Build Parallel') {
            agent Node-1

            parallel {

                stage('Build-1') {
                    steps {
                        sh 'sleep 5'
                        echo 'Build stage-1'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }

                stage('Build-2') {
                    steps {
                        sh 'sleep 5'
                        echo 'Build stage-2'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }

                stage('Build-3') {
                    steps {
                        sh 'sleep 5'
                        echo 'Build stage-3'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }
            }
        }

    }
}
