pipeline{
    agent any
    stages {
        stage('Install Dependencies') {
            steps {
                // Install any dependencies your Python test needs, like pip install <package>
                sh 'pip3 --version'
                sh 'pip3 install -r OnlineJudge_BE/deploy/requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                // Run your Python test script
                sh 'cd '
                sh 'python3.8 OnlineJudge_BE/manage.py test oj'
            }
        }
    }
    post {
        success {
            // Actions to take if the test succeeds
            echo 'Tests passed successfully!'
        }
        failure {
            // Actions to take if the test fails
            echo 'Tests failed!'
        }
    }
}