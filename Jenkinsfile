pipeline {
    agent any

    stages {
        stage('Build') {
            steps {
                echo 'Build'
            }
        }
        stage('Checkout') {
            steps {
                checkout([$class: 'GitSCM', branches: [[name: '*/main']], browser: [$class: 'GithubWeb', repoUrl: 'https://github.com/vickyg060/JenkinsDemo.git'], extensions: [[$class: 'CheckoutOption', timeout: 10]], userRemoteConfigs: [[credentialsId: '83602472-9efe-454e-971c-396813b4d722', url: 'https://github.com/vickyg060/JenkinsDemo.git']]])
            }
        }
        stage('Deploy') {
            steps {
                echo 'Deploying'
            }
        }
        stage('Release') {
            steps {
                echo 'Releasing'
            }
        }
    }
}
