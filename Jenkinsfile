// Powered by Infostretch 

timestamps {

node () {

	stage ('walmart-dev - Checkout') {
 	 checkout([$class: 'GitSCM', branches: [[name: '*/development']], doGenerateSubmoduleConfigurations: false, extensions: [], submoduleCfg: [], userRemoteConfigs: [[credentialsId: '5bccd71d-0f78-4915-b77d-ff9f84457ded', url: 'https://github.com/Prajwal3007/maven-web-application.git']]]) 
	}
	stage ('walmart-dev - Build') {
 			// Maven build step
	withMaven(maven: 'maven3.8.5') { 
 			if(isUnix()) {
 				sh "mvn clean package " 
			} else { 
 				bat "mvn clean package " 
			} 
 		} 
	}
}
}