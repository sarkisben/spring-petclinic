node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Default Maven';
    withSonarQubeEnv() {
      sh "${mvn}/bin/mvn clean verify sonar:sonar -Dsonar.projectKey=PetClinic"
    }
  }
  stage('Build Jar File') {
    sh "./mvnw package"
	archiveArtifacts artifacts: '**/target/*.jar', fingerprint: true
	sh "java -jar target/*.jar"
  }
}