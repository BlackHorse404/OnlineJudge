pipeline{
    agent any
    stages {
        stage('Install Enviroment And Dependency') {
            steps {
                // Install any dependencies your Python test needs, like pip install <package>
                // sh 'pip3 --version'
                // sh 'pip3 install -r OnlineJudge_BE/deploy/requirements.txt'
                sh 'cd OnlineJudge_FE'
                sh 'ls'
                sh 'pwd && cd OnlineJudge_FE && docker build -t oj_fe .'
            }
        }
        // stage('Run Tests') {
        //     steps {
        //         // Run your Python test script
        //         // sh 'cd '
        //         // sh 'python3.8 OnlineJudge_BE/manage.py test oj'
        //     }
        // }
        stage('Run FE') {
            steps {
                // Run your Python test script
                sh 'cd OnlineJudge_FE'
                sh 'ls'
                sh 'docker images'
                sh 'cd OnlineJudge_FE && ls && docker container run -p 8899:5173 oj_fe'
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