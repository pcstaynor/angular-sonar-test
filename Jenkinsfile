node {
  stage('SCM') {
    git 'https://github.com/pcstaynor/angular-sonar-test.git'
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'sonarscanner';
    withSonarQubeEnv('sonarscanner') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/sonar-scanner"
    }
  }
}
