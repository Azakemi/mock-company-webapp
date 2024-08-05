pipeline {
 pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                script {
                    // Run Gradle assemble to build the project
                    sh './gradlew assemble'
                }
            }
        }

        stage('Test') {
            steps {
                script {
                    // Run Gradle test to execute tests
                    sh './gradlew test'
                }
            }
        }
    }

    post {
        success {
            echo 'Build and Test stages succeeded!'
        }
        failure {
            echo 'Build or Test stage failed.'
        }
    }
}

}
