pipeline {
    agent any

    environment {
        GIT_REPO = "git@github.com:xxdhuehue/pipeline-sharing.git"
        GIT_BRANCH = "develop"
        NODE_VERSION = "22"
    }

    stages {
        stage('init') {
            steps {
                echo 'pull the latest code...'
                git url: 'git@github.com:xxdhuehue/pipeline-sharing.git', branch: 'develop'
            }
        }
        stage('install dependencies and bundle') {
            steps {
                echo 'install dependencies and bundle...'
                sh '''
                    pnpm install
                    pnpm run build
                '''
            }
        }
    }
}