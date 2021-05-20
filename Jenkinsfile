pipeline {
 agent any
 stages {
  stage('Build') {
   steps {
    echo 'Building..'
	withMaven(maven: 'mvn_home') {
    		mvn clean package
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
