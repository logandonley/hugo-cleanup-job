pipeline {
  agent any
  options { 
    buildDiscarder(logRotator(numToKeepStr: '2'))
    skipDefaultCheckout true
    preserveStashes(buildCount: 2)
  }
  triggers {
    eventTrigger jmespathQuery("action=='closed'")
  }

  stages {
    stage('Test') {
      steps {
        echo "Hello!"
      }
    }
  }
}