#!groovy

node {
    stage('Shared') {
        echo 'Shared stage'

        checkout scm
    }

    if (env.JOB_NAME == 'Project1') {
        load 'Project1/Jenkinsfile'
    } else if (env.JOB_NAME == 'Project2') {
        load 'Project2/Jenkinsfile'
    }
}
