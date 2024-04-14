pipeline{
    agent any
    stages {
        stage('Install Dependencies') {
            steps {
                // Install any dependencies your Python test needs, like pip install <package>
                sh 'cd OnlineJudge_BE'
                sh 'pip3 install -r deploy/requirements.txt'
            }
        }
        stage('Run Tests') {
            steps {
                // Run your Python test script
                sh 'cd OnlineJudge_BE'
                sh 'python3.8 manage.py test oj'
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