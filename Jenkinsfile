pipeline {
    agent any

    stages {
      stage('echo') {
            steps {
                echo 'Generating this pipeline directly from Github Jenkins File !'
            }
        }
        stage('scm') {
            steps {
                echo 'Hello Deep'
            }
        }
		stage('shell') {
            steps {
                echo 'Hello Deep'
                sh "date"
            }
        }
    }
}
