pipeline {
    agent any

    stages {
        stage('stage in one agent') {
            agent {
                docker {
                    image 'ruby:2.5.1'
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
                    image 'ruby:2.5.1'
                }
            }
            steps {
                sh "git show"
            }
        }
    }
}
