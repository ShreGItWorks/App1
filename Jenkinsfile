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
    sh "cp /home/jenkins/workspace/DockerBuild/target/*.war ."
   }
  }
  stage('Deploy') {
   steps {
    echo 'Deploying....'
   }
  }
 }
}
