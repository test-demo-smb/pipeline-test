pipeline {
    agent { label 'Node-1'}

    // agent {
    //     label 'jenkins_job'
    // }

    stages {

        stage('Build Parallel') {
            
            parallel {
                

                stage('Build-1') {

                    agent {label 'jenkins_job'}

                    steps {
                        sh 'sleep 5'
                        echo 'Build stage-1'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }

                stage('Build-2') {
                    //agent {label 'Node-1'}
                    steps {
                        sh 'sleep 5'
                        echo 'Build stage-2'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }

                stage('Build-3') {
                    //agent {label 'Node-2'}
                    agent {label 'jenkins_job'}
                    steps {
                        sh 'sleep 5'
                        echo 'Build stage-3'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }
            }
        }


        stage('Test Parallel') {

            parallel {

                stage('Test Chrome') {
                    //agent {label 'Node-1'}
                    agent {label 'jenkins_job'}
                    steps {
                        sh 'sleep 5'
                        echo 'Test Chrome'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }

                stage('Test Firefox') {
                    //agent {label 'Node-2'}
                    agent {label 'jenkins_job'}
                    steps {
                        sh 'sleep 5'
                        echo 'Test Firefox'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }
            }
        }




        stage('Deployment') {
            parallel {
                
                stage('Deploy Server 1') {
                    //agent {label 'Node-1'}
                    agent {label 'jenkins_job'}
                    steps {
                        sh 'sleep 5'
                        echo 'Deploy to Server 1'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }

                stage('Deploy Server 2') {
                    //agent {label 'Node-2'}
                    agent {label 'jenkins_job'}
                    steps {
                        sh 'sleep 5'
                        echo 'Deploy to Server 2'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }
                stage('Deploy Server 3') {
                    //agent {label 'master'}
                    agent {label 'jenkins_job'}
                    steps {
                        sh 'sleep 5'
                        echo 'Deploy to Server 3'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }
            }
        }
    
    
    }
}
