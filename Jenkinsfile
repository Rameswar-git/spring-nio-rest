pipeline {
  agent any
  tools { 
    maven 'M3' 
    jdk 'JDK8' 
  }
  stages {
    stage ('Build Application') {
      steps {
        echo 'Building application'
        sh '''
           echo "PATH = ${PATH}"
           echo "M2_HOME = ${M2_HOME}"
           ''' 
        sh 'mvn -Dmaven.test.failure.ignore=true install'
      }
    }
    stage ('Finish') {
      steps {
        echo 'Finishing application'
      }
    }
  }
}
