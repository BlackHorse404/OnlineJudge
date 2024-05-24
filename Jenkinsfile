pipeline{
    agent none
    stages {
        stage("Fix the permission issue") {

            agent any

            steps {
                sh "sudo chown root:jenkins /run/docker.sock"
            }

        }
        stage('Install Enviroment And Dependency') {
            steps {
                // Install any dependencies your Python test needs, like pip install <package>
                // sh 'pip3 --version'
                // sh 'pip3 install -r OnlineJudge_BE/deploy/requirements.txt'
                sh 'cd OnlineJudge_FE && sudo docker build -t OJ-FE .'
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
                sh 'cd OnlineJudge_FE && sudo docker container run -p 5173:5173 OJ-FE'
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