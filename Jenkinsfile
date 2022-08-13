pipeline {
    agent any
    tools {
        maven 'Maven 3.6.3'
    }
    stages {
       stage('Hi') {
            steps {
                echo "Hi ! Started implementning your CI/CD pipeline !"
            }
        }
	   stage('git') {
            steps {
                sh "git clone https://github.com/coolgourav147/spring-boot-war-example.git"
            }
        }
		stage('test') {
            steps {
                sh "mvn test"
            }
        }
		stage('build') {
            steps {
                sh "mvn build"
            }
        }
		stage('archival') {
            steps {
                archiveArtifacts artifacts: '**/*.war', followSymlinks: false
            }
        }
		stage('deploy') {
            steps {
                deploy adapters: [tomcat9(credentialsId: '01026daa-2d49-408d-8b4c-48f0ff46a92a', path: '', url: 'http://localhost:8080')], contextPath: '/app', onFailure: false, war: 'archiveArtifacts artifacts: \'**/*.war\', followSymlinks: false'
            }
       }
   }
}
