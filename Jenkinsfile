pipeline {
  agent any
  tools {
    maven 'DHT_MVN'
    jdk 'DHT_SENSE'
  }
  stages {
    stage('checkout') {
      steps {
        git(url: 'https://github.com/malvikapatel/maven-samples', branch: 'master')
      }
    }

    stage('run') {
      steps {
        sh "${tool 'DHT_MVN'}/bin/mvn verify"
      }
    }

  }
}
