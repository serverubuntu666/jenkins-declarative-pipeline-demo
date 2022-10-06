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
            echo "testing phase..."
        }
        stage ('deploy') {
            echo "deploying phase..."
        }
    }

    post {
        success {
            echo "the build is successfull!!"
        }
    }
}