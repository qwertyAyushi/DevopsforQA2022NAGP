pipeline {
    agent any

    stages {
        stage('code checkout') {
            steps {
                echo 'Hello code checkout'
            }
        }
        stage('code build') {
            steps {
                echo 'Hello code build'
            }
        }
        stage('unit test') {
            steps {
                echo 'Hello unit test'
            }
        }
    }
    
    post{
        always{
            //Execute evry time
        }
        success{
            echo 'Hello success'
        }
    }
}
