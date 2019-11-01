pipeline {
    agent any

    stages {
        stage('stage in one agent') {
            steps {
                sh "git show"
                input "sigo?"
            }
        }

        stage('stage in other agent') {
            steps {
                sh "git show"
            }
        }
    }
}
