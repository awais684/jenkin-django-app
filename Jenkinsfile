@Library('sharedlib') _
pipeline {
    agent { label "myvm" }

    stages {
        stage('code') {
            steps {
                script{
                code('https://github.com/awais684/jenkin-django-app.git', 'master')
                }
            }
        }
        stage('build') {
            steps {
                script{
                build('jenkins-app', 'v1', 'awais684')
                }
            }
        }
        stage('push') {
            steps {
                script{
                push('jenkins-app', 'v1', 'awais684')
                }
            }
        }
        stage('deploy') {
            steps {
                script{
                deploy('jenkins-app', 'v1')
                }
            }
        }
    }
}
