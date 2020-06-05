node {
  stage('SCM') {
    git 'https://github.com/pcstaynor/angular-sonar-test.git'
  }
  stage('SonarQube analysis') {
    def scannerHome = tool 'sonarscanner';
    withSonarQubeEnv('SonarQube') { // If you have configured more than one global server connection, you can specify its name
              sh "${scannerHome}/sonar-scanner-4.3.0.2102-linux/bin/sonar-scanner"

    }
  }
}
