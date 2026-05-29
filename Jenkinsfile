pipeline {
    agent any

    // agent {
    //     label 'jenkins_job'
    // }

    stages {

        stage('Build Parallel') {
            agent {
                label 'Node-1'
            }

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



        stage('Test Parallel') {
            
            agent {
                label 'Node-2'
            }

            parallel {

                stage('Test Chrome') {
                    steps {
                        sh 'sleep 5'
                        echo 'Test Chrome'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }

                stage('Test Firefox') {
                    steps {
                        sh 'sleep 5'
                        echo 'Test Firefox'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }
            }
        }




        stage('Deployment') {
            agent {
                label 'master'
            }

            parallel {

                stage('Deploy Server 1') {
                    steps {
                        sh 'sleep 5'
                        echo 'Deploy to Server 1'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }

                stage('Deploy Server 2') {
                    steps {
                        sh 'sleep 5'
                        echo 'Deploy to Server 2'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }
            }
        }
    
    
    }
}
