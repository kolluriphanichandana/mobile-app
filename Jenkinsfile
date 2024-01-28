pipeline {
    agent {
        label 'linux'
    }

    stages {
        stage('clean') {
            tools {
                maven 'maven_3.9.0'
            }
            steps {
                sh 'mvn --version'
                sh 'mvn clean'
            }
        }

        stage('compile') {
            tools {
                maven 'maven_3.9.0'
            }
            steps {
                sh 'mvn --version'
                sh 'mvn compile'
            }
        }

        stage('test') {
            tools {
                maven 'maven_3.9.0'
            }
            steps {
                sh 'mvn --version'
                sh 'mvn test'
            }
        }
    }

    post {
        always {
            echo 'This will always run.'
        }
        success {
            echo 'This will run only if the build succeeds.'
        }
        failure {
            echo 'This will run only if the build fails.'
        }
    }
}




