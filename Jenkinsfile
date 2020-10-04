pipeline {
    agent any
    stages {
        stage('build') {
            steps  {
                sh 'python --version'
                sh 'echo "Hello World"'
                sh '''
                    echo "The cat sat on the mat"
                    ls -lah
                    whoami
                    pwd
                    uname -a
                '''
            }
        }
    }
}
