pipeline {

    agent {
        node {
            label 'linux'
        }
    }

    stages
    {
        stage("checkout code")
        {
            steps{
                git 'https://github.com/MfumoMash/angularproj.git'
            }
        }

        stage("NPM install")
        {
            steps{
                script{
                    sh "npm install"
                }
            }
        }

        stage("Build")
        {
            steps{
                sh "npm run ng build"
            }
        }
    }

}