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
                sh "ls -1 | wc -l"
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
                sh "ls -1 | wc -l"
                sh "git show"
            }
        }
    }
}
