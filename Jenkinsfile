pipeline {
    agent any
    tools {
    maven '3.6.3',
	    java '1.8'
        }
stages {
	stage('Build') {
	steps {
	sh 'mvn -B -DskipTests clean package'
	}
}// End of Build
stage('Test') {
	steps {
		sh 'mvn test'
		junit 'target/surefire-reports/*.xml'
	}
}//end of test

}//End of Stages
}//end pipeline
