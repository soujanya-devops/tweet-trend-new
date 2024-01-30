pipeline {
    agent {
        node {
            label 'maven'
        }
    }
environment {
    PATH = "/opt/apache-maven-3.9.6/bin:$PATH"
}

    stages {
        stage('build') {
            steps {
                sh 'mvn clean deploy'
            }
        }
<<<<<<< HEAD
stage('SonarQube analysis') {
=======
    stage('SonarQube analysis') {
>>>>>>> be404b8b57ce7991a0187b3da19c02d0d37fb01b
    environment {
      scannerHome = tool 'valaxy-sonar-scanner'
    }
    steps{
    withSonarQubeEnv('valaxy-sonarqube-server') { // If you have configured more than one global server connection, you can specify its name
      sh "${scannerHome}/bin/valaxy-sonar-scanner"
    }
    }
  }
}
}
