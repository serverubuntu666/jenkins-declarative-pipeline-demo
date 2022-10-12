pipeline {
    agent {
        label 'DEV'
    }
    // parameters {
    //     string (name:'NAME', description: 'whats your name?')
    //     text (name: 'DESC', description:'describe about the job details')
    //     booleanParam(name: 'SKIP_TEST', description: 'want to skip the running test')
    //     choice(name: 'BRANCH', description: 'choose branch', choices:['main', 'feature'])
    //     password(name: 'SONAR_SERVER_PWD', description: 'Enter Sonar password')
    // }
    environment {
        MY_CRED = credentials('jenkins')
    }
    stages {
        stage('run script') {
            steps {
                echo "hi"
                sh 'chmod +x simple.sh'
                sh 'simple.sh'
            }
        }
    }
    // stages {
    //     stage ('printing parameters') {
    //         steps {
    //             echo "Hello, ${params.NAME}"
    //             echo "Job details, ${params.DESC}"
    //             echo "Skip running test? ${params.SKIP_TEST}"
    //             echo "Branch choice, ${params.BRANCH}"
    //             echo "sonar password, ${params.SONAR_SERVER_PWD}"
    //         }
    //     }
    //     stage ('Load credentials') {
    //         steps {
    //             echo "username: ${MY_CRED_USR}"
    //             echo "password: ${MY_CRED_PSW}"
    //         }
    //     }
    // }
    // stages {
    //     stage('trycatchblock') {
    //         steps {
    //             script {
    //                 def apply = false
    //                 try {
    //                     input message: 'can you pls confirm the apply?', ok: 'ready to apply the config'
    //                     apply = true
    //                 } catch(err) {
    //                     apply = false
    //                     currentBuild.result = 'UNSTABLE'

    //                 }
    //                 if(apply) {
    //                     echo "build succesfull..."
    //                 }
    //             }
    //         }
    //     }
    // }
    // stages {
    //     stage('Build') {
    //         steps {
    //             echo "build phase..."
    //         }
    //     }
    //     stage ('test') {
    //         steps {
    //             echo "testing phase..."
    //         }
    //     }
    //     stage ('deploy') {
    //         steps {
    //             echo "deploying phase..."
    //         }
    //     }
    // }

    post {
        success {
            echo "the build is successfull!!"
        }
    }
}