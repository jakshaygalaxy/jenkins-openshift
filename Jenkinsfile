node {
  stage('SCM') {
    checkout scm
  }
  stage('SonarQube Analysis') {
     withSonarQubeEnv(installationName: 'SonarQube', credentialsId: 'aef1ef4f-853f-464b-9430-6f25629a5314') {
      sh 'mvn clean package sonar:sonar'
    }
  }
}
