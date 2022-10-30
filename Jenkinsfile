pipeline {
    agent any
    tools{
        maven 'Maven'
    }

    stages {
        stage('checkout') {
            steps {
                checkout scm
            }
        }
        stage('Build') {           
            steps {
                echo 'mvn install'
            }
        }
        stage('Unit testing') {
            steps {
                echo 'mvn test'
            }
        }
        stage('Sonar Analysis') {
            steps {
                withSonarQubeEnv('Test_Sonar'){
                echo 'mvn org.sonarsource.scanner.maven:sonar-maven-plugin:3.2:sonar'
                }
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
