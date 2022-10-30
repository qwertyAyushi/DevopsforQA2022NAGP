pipeline {
    agent any
    tools{
        maven 'Maven'
    }

    stages {
        stage('code checkout') {
            steps {
                echo 'Hello code checkout'
            }
        }
        stage('code build') {           
            steps {
                echo 'mvn clean'
            }
        }
        stage('unit test') {
            steps {
                echo 'mvn test'
            }
        }
    }
    
    post{
        always{
            echo 'Hello always'
        }
        success{
            echo 'Hello success'
        }
    }
}
