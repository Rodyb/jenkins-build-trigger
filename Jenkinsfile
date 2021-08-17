pipeline {
    agent any
    stages {
        stage('Build') {
            steps {
                echo "Build step"
            }
        }

        stage('Test') {
            steps {
                echo "Test step"
            }
        }

        stage('Upload artifacts') {
            steps {
                echo "Upload artifacts step"
            }
        }
    }
    post {
        always {
            echo 'Run E2E Test pipeline!'
            build job: 'Pipeline-1/master", propagate: true, wait: true'
        }
    }
}