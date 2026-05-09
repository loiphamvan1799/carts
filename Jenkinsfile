pipeline {
  agent any
  stages {
    stage('build') {
      steps {
        echo 'this is the first job'
        sh 'mvn compile '
        sleep 4
      }
    }

    stage('test') {
      steps {
        echo 'this is the second job'
        sh 'mvn clean test'
        sleep 9
      }
    }

    stage('package') {
      steps {
        echo 'this is the third job'
        sh 'mvn package -DskipTests'
        archiveArtifacts '**/target/*.jar'
      }
    }

  }
  tools {
    maven 'Maven 3.9.15'
  }
  post {
    always {
      echo 'this pipeline has completed...'
    }

  }
}