pipeline {
    agent any

    stages {
        stage('stage in one agent') {
            agent {
                docker {
                    image 'obe-builder:1.3.0'
                }
            }
            steps {
                sh "git show"
                input "sigo?"
            }
        }

        stage('stage in other agent') {
            agent {
                docker {
                    image 'obe-builder:1.2.0'
                }
            }
            steps {
                sh "git show"
            }
        }
    }
}
