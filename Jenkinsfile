node('ecs-small-3gb'){
    stage('Build') {
        echo 'Building...'
    }

    stage('Test') {
        echo 'Testing...'
        sh 'python3 --version'
        sh 'which nc'
        sh 'ls -la ./'
        sh 'id && whoami'
    }

    stage('Deploy') {
        echo 'Deploying...'
    }
}

