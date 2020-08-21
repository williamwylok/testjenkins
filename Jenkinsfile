#!groovy

node {
    
    environment {
        myswitch = "one"
    }
    stage('Shared') {
        echo 'Shared stage'

        checkout scm
    }

    echo "job name = ${env.JOB_NAME}"

    if ("${env.myswitch}" == 'one') {
        load 'Project1/Jenkinsfile'
    } else if ("${env.myswitch}" == 'two') {
        load 'Project2/Jenkinsfile'
    }
}
