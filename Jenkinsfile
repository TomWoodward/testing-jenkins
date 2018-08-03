pipeline {
    agent any

    stages {
        stage('Test') {
            environment { 
                USER = credentials('0270f580-c17f-446e-a52d-3474d829cdc3') 
            }
            steps {
                sh "curl -X POST -d '{\"body\": \"hello\"}' -u $USER https://api.github.com/repos/TomWoodward/testing-jenkins/issues/$CHANGE_ID/comments"
            }
        }
    }
}
