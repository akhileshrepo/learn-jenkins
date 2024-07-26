pipeline {
    //agent any
    agent { node { label 'workstation' } }

    environment {
      TEST_URL = "google.com"
      SSH = credentials("centos-ssh")
    }

    options {
            ansiColor('xterm')
    }

    stages {
        stage('Compile') {
            steps {
                //echo 'Hello World'
                echo TEST_URL
                echo SSH
                sh 'env'
                sh 'ansible -i 172.31.46.100, all -e ansible_user=${SSH_USR} -e ansible_password=${SSH_PSW} -m ping'
            }
        }
    }

    post {
        always {
            echo 'post'
            // send Email
            // Trigger some other Job
            // update Jira
        }
    }
}