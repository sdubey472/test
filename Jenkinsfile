pipeline {
    agent any
            // environment {
            //     ANDROID_HOME='/home/ubuntu/android-sdk-linux'
            //     PATH='${PATH}'
            // }
    stages {
        stage('pull') {
            steps {
             sh 'pwd'
             sh 'rm -rf test'
             sh 'whoami'
            //  sh 'git clone http://sdubey472:sdubey123!@github.com/sdubey472/test.git'
            sh 'whoami'
            // sh 'sdkmanager'
            sh 'npm -v'
            sh 'whoami' 
            sh 'ionic'
            }
        }
        stage('build') {
            steps {
                sh 'pwd'
                sh 'ls -la'
                //sh 'BUILD_ID=dontKillMe' 
                //sh './deploymentScript.sh' 
            }
        }
        stage('push docker on registry') {
            steps {
                echo 'Deploying'
            }
        }
        stage('publish on play Store') {
            steps {
                echo 'Publish on PlayStore'
            }
        }        
        stage('publish on IOS Store') {
            steps {
                echo 'Publish on Apple Store'
            }
        }        
    }
    post {
        always {
            echo 'This will always run'
        }
        success {
            echo 'This will run only if successful'
        }
        failure {
            echo 'This will run only if failed'
        }
        unstable {
            echo 'This will run only if the run was marked as unstable'
        }
        changed {
            echo 'This will run only if the state of the Pipeline has changed'
            echo 'For example, if the Pipeline was previously failing but is now successful'
        }
    }
}
