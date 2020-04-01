pipeline {
    agent any

    stages {
         stage('Bitbucket checkout') {
            steps {
                echo 'Cloning..'
                sh 'pwd'
                sh 'echo $OSTYPE'
                sh 'git pull $REPO_NAME'
            }
        }
        stage('Build') {
            steps {
                echo 'Building..'
                dir('inpress') {
                    sh 'pwd'
                    sh './build.sh'
                }
            }
        }
        stage('Test') {
            steps {
                echo 'Testing..'
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying....'
            }
        }
    }
}
