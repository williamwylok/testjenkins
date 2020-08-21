#!groovy

node {
    
    env.myswitch = "one"
    
    stage('Shared') {
        echo 'Shared stage'

        checkout scm
    }

    echo "job name = ${env.JOB_NAME}"
    echo "myswitch = ${env.myswitch}"
 
    /*
    stage('Dedicated') {
        load 'Project1/Jenkinsfile'
    }
    */
    
    if ("${env.myswitch}" == 'one') {
        load 'Project1/Jenkinsfile'
    } else if ("${env.myswitch}" == 'two') {
        load 'Project2/Jenkinsfile'
    }
}
