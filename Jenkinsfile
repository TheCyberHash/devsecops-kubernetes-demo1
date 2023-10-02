pipeline {
  agent any

  stages {
      stage('Build Artifact- Maven  ') {
            steps {
              sh "mvn clean package -DskipTests=true"
              archiveArtifacts artifacts: 'target/*.jar', allowEmptyArchive: True  
            }
        }   

    stage('Unit Test') {
            steps {
              sh "mvn test"  
            }
        }   
    }
}
