stage ('Scan and Build Jar File') {
            steps {
               withSonarQubeEnv(installationName: 'Sonar', credentialsId: 'Token for the Pet Clinic') {
                sh 'mvn clean package sonar:sonar'
                }
            }
        }