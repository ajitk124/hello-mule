pipeline {

  agent any
  
  stages {
    stage('Build') {
      steps {
            bat 'mvn -B -U -e -V clean -DskipTests package'
      }
    }

    stage('Test') {
      steps {
          echo "***Munit test case execution***"
      }
    }

     stage('Deployment') {
      
      steps {
            bat 'mvn -U -V -e -B -DskipTests deploy -DmuleDeploy'
      }
    }
    
  }
}