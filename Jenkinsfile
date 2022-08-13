pipeline {
    agent any

    stages {
      stage('echo') {
            steps {
                echo 'Generating this pipeline directly from Github Jenkins File !'
            }
        }
		stage('Hello') {
            steps {
                echo 'Hello Deep'
                sh "date"
            }
        }
    }
}
