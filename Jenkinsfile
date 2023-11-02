node {
   def mvnHome
  stage('Prepare') {
      git url: 'https://github.com/bhavaniharika1/CodeToDeployToJenkins.git', branch: 'main'
      mvnHome = tool 'Maven'
   }
   stage ('SonarQube') {
      sh "'${mvnHome}/bin/mvn' clean verify sonar:sonar"
  }
  stage ('Clean') {
      sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore clean"
  }
  stage ('Validate') {
      sh "'${mvnHome}/bin/mvn' -Dmaven.test.failure.ignore validate"
  }
  stage ('Compile') {
      sh "'${mvnHome}/bin/mvn' compile"
  }
  stage ('Test') {
      sh "'${mvnHome}/bin/mvn' test"
  }
  stage ('Package') {
      sh "'${mvnHome}/bin/mvn' package"
  }
  stage ('Verify') {
      sh "'${mvnHome}/bin/mvn'  verify"
  }
  stage ('Install') {
      sh "'${mvnHome}/bin/mvn' install"
  }

}
