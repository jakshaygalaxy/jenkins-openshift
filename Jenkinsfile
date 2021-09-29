node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
     withSonarQubeEnv(installationName: 'SonarQube Server', credentialsId: 'Sonarqube Server') {
      sh 'mvn clean package sonar:sonar'
    }
  }
}
