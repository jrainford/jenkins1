pipeline {
    agent any
    stages {
        stage('build') {
            steps  {
                echo 'Building'
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
        stage('Test') {
            steps {
                echo 'Testing'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
    }
    post {
        always {
            echo 'One way or another, I have finished'
            deleteDir() /* clean up our workspace */
        }
        success {
            echo 'I succeeded!'
        }
        unstable {
            echo 'I am unstable :/'
        }
        failure {
            echo 'I failed :('
        }
        changed {
            echo 'Things were different before...'
        }
    }
}

