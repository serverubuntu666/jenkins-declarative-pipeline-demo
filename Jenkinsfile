pipeline {
    agent {
        label 'DEV'
    }

    stages {
        stage('Build') {
            steps {
                echo "build phase..."
            }
        }
        stage ('test') {
            steps {
                echo "testing phase..."
            }
        }
        stage ('deploy') {
            steps {
                echo "deploying phase..."
            }
        }
    }

    post {
        success {
            echo "the build is successfull!!"
        }
    }
}