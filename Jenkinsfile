pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Building the project...'
                bat 'mvn clean package' // Use 'sh' for Unix/Linux
            }
        }

        stage('Test') {
            steps {
                echo 'Running tests...'
                // Add your test command here
            }
        }

        stage('Archive Artifacts') {
            steps {
                archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
                // Adjust the path according to your project's structure
            }
        }
    }
}
