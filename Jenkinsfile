pipeline {
    agent any
    
    stages {
		stage("Build") {
			steps {
				echo "BUILD"	
			}
		}
		stage("Code Quality") {
			steps {
			 withSonarQubeEnv('LocalSonar') {
                sh 'mvn clean package sonar:sonar'
              }	
			}
		}
		stage("UAT") {
			steps {
				echo "UAT"	
			}
		}
		stage("Prod") {
			steps {
				echo "PROD"	
			}
		}
	}
}
