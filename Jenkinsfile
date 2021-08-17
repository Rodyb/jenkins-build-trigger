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
        success {
            echo 'Run E2E Test pipeline!'
            build job: 'E2E_tests_pipeline', parameters: [string(name: 'MY_PARAM', value: 'value from Build pipeline')]
        }
    }

}