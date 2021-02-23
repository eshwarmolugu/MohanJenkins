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
			 	withSonarQubeEnv('SonarQube_Local') {
					sh '/Users/eshwar.molugu/git/app-devops-jenkins/work/tools/hudson.plugins.sonar.SonarRunnerInstallation/sonarScanner/bin/sonar-scanner -Dproject.settings=/Users/eshwar.molugu/git/app-devops-jenkins/work/tools/hudson.plugins.sonar.SonarRunnerInstallation/sonarScanner/conf/sonar-scanner.properties'
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
