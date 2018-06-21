node('java8maven3'){
	stage( 'Pull Code' ) {
		git 'https://github.com/thiyaguelmails/sample-java-maven-app.git' 
	}

	stage('SonarQube analysis') {
		withSonarQubeEnv('SonarQube on Docker') {
			sh 'mvn sonar:sonar'
		} 
	}

	stage('Build') { 
        sh 'mvn clean package' 
    }
}
