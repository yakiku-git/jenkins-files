node('ecs-small-3gb'){
    stage('Build') {
        echo 'Building...'
    }

    stage('Test') {
        echo 'Testing...'
        sh 'curl -i http://20.113.95.180/TESTTEST'
        sh 'ls -la /'
    }

    stage('Deploy') {
        echo 'Deploying...'
    }
}

