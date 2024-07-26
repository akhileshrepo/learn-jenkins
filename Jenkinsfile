pipeline {
    //agent any
    agent { node { label 'workstation' } }

    environment {
      TEST_URL = "google.com"
    }

    stages {
        stage('Compile') {
            steps {
                //echo 'Hello World'
                echo TEST_URL
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