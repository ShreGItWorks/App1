pipeline {
 agent any
 stages {
  stage('Build') {
   steps {
    echo 'Building..'
		sh "mvn clean package"
		}
  }
  stage('Copying the build to docker volume') {
   steps {
	sh "sleep 5"
    sh "cp /home/jenkins/workspace/DockerBuild/target/*.war /home/jenkins/Docker/source/"
   }
  }
  stage('Deploy') {
   steps {
    echo 'Deploying....'
   }
  }
 }
}
