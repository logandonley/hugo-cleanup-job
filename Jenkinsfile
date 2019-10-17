pipeline {
  agent any
  options { 
    buildDiscarder(logRotator(numToKeepStr: '2'))
    skipDefaultCheckout true
    preserveStashes(buildCount: 2)
  }
  triggers {
    eventTrigger jmespathQuery("(action == 'closed') && (pull_request.head.repo.full_name == `cloudbees-days/blog`)")
  }

  stages {
    stage('Test') {
      steps {
        echo "Hello!"
      }
    }
  }
}