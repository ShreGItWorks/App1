pipeline {
 agent any
 stages {
  stage('Build') {
   steps {
    echo 'Building..'
   sshPublisher(publishers: [sshPublisherDesc(configName: 'Docker1', transfers: [sshTransfer(cleanRemote: false, excludes: '', execCommand: '', execTimeout: 120000, flatten: false, makeEmptyDirs: false, noDefaultExcludes: false, patternSeparator: '[, ]+', remoteDirectory: 'cd /appl/', remoteDirectorySDF: false, removePrefix: '', sourceFiles: 'target/*.war')], usePromotionTimestamp: false, useWorkspaceInPromotion: false, verbose: false)])

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
