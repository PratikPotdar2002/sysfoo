pipeline {
    agent any
    tools{
      maven 'Maven 3.9.6'
    }
      
    stages {
        stage("Build") {
            steps {
              echo 'Compiling app..'
              sh 'mvn compile'   
            }
        }
        stage("Test") {
            steps {
                echo 'Running unit test..'
                sh 'mvn clean test'
            }
        }
        stage("Package") {
            steps {
                echo 'packaging the app..'
                sh 'mvn package -DskipTests'
            }
        }
    }
    post {
        always {
            echo 'This pipeline is completed..'
        }
    }
}
