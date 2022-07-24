pipeline {
     agent any
     stages{
          stage ('Scan and Build Jar File') {
               steps {
                    withSonarQubeEnv(installationName: 'JenkinsSonarServer', credentialsId: 'SonarToken2') {
                         sh 'mvn clean package sonar:sonar'
                    }
               }
          }
    }
}