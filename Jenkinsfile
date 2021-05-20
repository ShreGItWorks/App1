pipeline {
 agent any
 stages {
  stage('Build') {
   steps {
    echo 'Building..'
        withMaven(maven: 'mvn_home') {
                 clean package
          }
		}
  }
  stage('Test') {
   steps {
    echo 'Testing..'
   }
  }
  stage('Deploy') {
   steps {
    echo 'Deploying....'
   }
  }
 }
}

