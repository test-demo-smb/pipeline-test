pipeline {
    agent none

    // agent {
    //     label 'jenkins_job'
    // }

    stages {

        stage('Build Parallel') {
            
            parallel {
                

                stage('Build-1') {
                    agent { label 'Node-1'}

                    steps {
                        sh 'sleep 5'
                        echo 'Build stage-1'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }

                stage('Build-2') {

                    agent { label 'Node-2'}
                    steps {
                        sh 'sleep 5'
                        echo 'Build stage-2'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }

                stage('Build-3') {

                    agent { label 'master'}
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
