pipeline {
    agent any
    stages {
        stage('build') {
            steps {
                sh "mvn clean package"
            }
        }
        stage('test') {
            steps {
                sh "mvn test"
            }
			post{
				always{
					junit 'target/surefire-reports/*.xml'
				}
			}
        }
       
    }
}
