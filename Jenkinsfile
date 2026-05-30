pipeline {
    agent any
    parameters {
         string defaultValue: 'TEST', description: 'environment to deplay the Apllication', name: 'ENV', trim: true
               
    }

    environment{
        NAME='Bharath'
        NAME1="$name"
        DEPLOY_ENV="$defaultValue"

    }


    // agent {
    //     label 'jenkins_job'
    // }

    stages {

        stage('Build Parallel') {
            
            parallel {
                

                stage('Build-1') {

                    agent {label 'master'}

                    steps {
                        
                        echo "$NAME"
                        
                        echo "deplay to ${params.ENV}"
                        sh '''
                        
                        sleep 5
                        echo $NAME
                        exit 0

                        echo $NAME1
                        echo $NAME1
                        echo $NAME1
                        echo $NAME1
                        echo $NAME1
                        echo $NAME1
                        echo $NAME1

                        echo $DEPLOY_ENV
                        echo $DEPLOY_ENV
                        echo $DEPLOY_ENV
                        echo $DEPLOY_ENV
                        echo $DEPLOY_ENV
                        echo $DEPLOY_ENV
                        echo $DEPLOY_ENV


                        echo "deplay to $ENV"
                        //echo "code is from $ENV"

                        '''
                       
                        echo 'Build stage-1'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }

                stage('Build-2') {
                    agent {label 'Node-1'}
                    steps {
                        sh 'sleep 5'
                        echo 'Build stage-2'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }

                stage('Build-3') {
                    agent {label 'Node-1'}
                    steps {
                        sh 'sleep 5'
                        echo 'Build stage-3'
                        sleep(time: 5, unit: 'SECONDS')
                    }
                }
            }
        }


        stage('Test Parallel') {
            environment{
                NAME='Bhavani'

            }

            parallel {

                stage('Test Chrome') {
                    agent {label 'Node-2'}
                    steps {

                        echo "$NAME"
                        sh '''
                            sleep 5
                            echo $NAME

                        '''
                    }
                }

                stage('Test Firefox') {
                    agent {label 'Node-2'}
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
