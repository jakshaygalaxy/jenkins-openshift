node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
    def mvn = tool 'Default Maven';
     withSonarQubeEnv(installationName: 'SonarQube Server', credentialsId: 'Sonarqube Server') {
      sh "${mvn}/bin/mvn clean verify sonar:sonar"
    }
  }
}
